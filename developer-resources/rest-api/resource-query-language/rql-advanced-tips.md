---
description: Advanced RQL patterns, pitfalls, and best practices from real-world API usage.
---

# RQL Advanced Tips

This page expands on the [Resource Query Language](../resource-query-language.md) with patterns and pitfalls learned from building integrations against the Marketplace Platform REST API. Use it when you need to write correct, efficient RQL and avoid common errors.

## Discover fields before writing RQL

RQL filter and sort expressions only work with fields that exist on the resource. The API returns errors (for example, 'Unknown expression group' or 400 Bad Request) if you use a field name that does not exist or is not exposed for filtering.

### What to do

* Use the resource schema (OpenAPI or your API documentation) to see the exact property names and types for each resource.
* Do not invent field names. For example, there is no generic `subscriptionsCount` field on agreements; the number of subscriptions is not a filterable RQL field. To get '_agreements with more than N subscriptions_' you must either:
  * Query the child resource (for example, subscriptions) and filter by parent (for example, `agreement.id`).
  * Fetch agreements with `select=+id,+name,+subscriptions.id,+subscriptions.name` and compute or filter in your application.

### Summary

| Mistake                                       | Correct approach                                                                                                    |
| --------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `gt(subscriptionsCount,5)` on agreements      | Query subscriptions filtered by `agreement.id`, or fetch agreements with `+subscriptions` and count/filter in code. |
| Filtering by a field you assume exists        | Check the resource schema first; use only documented fields.                                                        |
| `order=created` when the field is under audit | Use `audit.created.at` and include `select=audit` (see below).                                                      |

## How RQL is sent (query string, not a parameter)

A very common source of 400 errors is sending RQL as a single query parameter.

### Wrong

```http
GET /public/v1/catalog/products?rql=eq(status,Published)
```

Many clients send this when given a params object like `{ "rql": "eq(status,Published)" }`. The API typically responds with 400 Bad Request or 'Invalid equals shortcut expression' because it does not treat `rql` as a parameter whose value is the expression.

### Correct

Append the RQL expression as the query string (or as the first part of it):

```http
GET /public/v1/catalog/products?eq(status,Published)
```

When you have both RQL and other parameters (like, `limit`, `offset`), combine them with `&`:

```http
GET /public/v1/catalog/products?eq(status,Published)&limit=20&offset=0
```

So in code: build the URL so that the RQL string is the first query segment; then append `&limit=...&offset=...` (and `&select=...`, `&order=...`) as needed. Do not put the whole RQL inside a single `rql=` parameter.

### Do not mix parameters inside the RQL string

**Wrong:** `rql="ilike(name,*Microsoft*) limit=20"` or `rql="eq(status,Active)&order=-created"` — `limit` and `order` are not part of RQL; they are separate query parameters.

**Correct:** Send RQL as the filter only (example, `ilike(name,*Microsoft*)` or `eq(status,Active)`), and pass `limit`, `offset`, `select`, and `order` as separate parameters. The final URL will combine them: `?eq(status,Active)&limit=20&order=-audit.created.at`.

## IDs and special characters in RQL values

ID values (such as, `ACC-1234-5678`, `PRD-xxx`, `BUY-xxx`, `USR-xxx`) must be in double quotes in RQL. Example: `eq(client.id,"ACC-4402-5918")`, `eq(buyer.id,"BUY-1234-5678")`. Unquoted IDs can return zero results.

Special characters (spaces, `&`, `?`) in string values must be enclosed in double or single quotes: `eq(firstName,"Buzz !!!")`.

To use a literal asterisk inside an `ilike` pattern, escape it: `ilike(name,"The\**")`.

## Audit fields and the select parameter

Date and audit metadata (created, updated) live under the audit object. The API behavior is:

Filtering or sorting by audit fields (such as `audit.created.at`, `audit.updated.at`) only works if the audit data is in scope for the response. That means you must include `audit` in the `select` parameter when you filter or sort by it.

If you omit `select=audit` (or equivalent), the API may ignore the filter or return 400.

### Examples

Filter by creation date:

```http
GET /public/v1/commerce/orders?select=audit&and(gt(audit.created.at,"2024-12-01T00:00:00.000Z"),lt(audit.created.at,"2025-12-01T00:00:00.000Z"))&limit=20
```

Sort by most recently updated:

```http
GET /public/v1/commerce/orders?select=+id,+name,audit&order=-audit.updated.at&limit=10
```

### Date format

Dates must be UTC with 3-digit millisecond precision: `YYYY-MM-DDTHH:mm:ss.sssZ` (for example, `2026-01-31T23:00:00.000Z`). Prefer the full timestamp for precise filters; date-only (`YYYY-MM-DD`) may not behave as expected when comparing timestamps.&#x20;

Other formats may not filter or sort correctly.

## Efficient counting with `limit=0`

To get only the total count of resources matching a filter (such as, _how many subscriptions does this agreement have?_):

1. Call the child resource endpoint (for example, subscriptions).
2. Apply the filter (for example, by agreement ID via RQL or a direct filter like `agreement.id=AGR-XXX` if supported).
3. Set `limit=0`.
4. Read the count from `$meta.pagination.total`.

The response will have an empty `data` array but the correct total. This avoids transferring full payloads when you only need the number.

Example:

```http
GET /public/v1/commerce/subscriptions?eq(agreement.id,AGR-1234-5678)&limit=0
```

Response:

```json
{
  "$meta": {
    "pagination": {
      "total": 42,
      "limit": 0,
      "offset": 0
    }
  },
  "data": []
}
```

## Select: additive, subtractive, and omitted fields

### Additive select (`+field`)

* `select=+id,+name,+status` - Include only these fields in addition to the default set. Use this to keep payloads small when you know what you need.
* Many resources omit large or sensitive fields by default. The response includes `$meta.omitted` listing properties that were not returned (for example, `["lines", "parameters", "subscriptions"]`). To include one of them, add it with `select=+field` (for exampple, `select=+lines,+parameters`).

### Subtractive select (`-field`)

**`select=-metadata`** - Exclude a field.&#x20;

Some integrations use `select=-*,+id,+name,+field` (exclude all, then add back only what is needed). Not all endpoints support the subtractive form; if you get 400, retry with additive only (for example, `select=+id,+name,+field`).

### Nested collections

* **`+subscriptions`** - Return the full nested representation of the collection.
* `+subscriptions.id,+subscriptions.name` - Return only `id` and `name` for each nested item. Prefer this when you only need to list or count related items; it keeps responses smaller.

### Commonly omitted fields

Many resources omit certain fields by default for performance.&#x20;

They are listed in `$meta.omitted` in the response. Common examples: lines (order line items), parameters, subscriptions, assets, termsAndConditions, certificates, audit.&#x20;

To include them, use `select=+field` (for example, `select=+lines,+parameters`).

## Limit and pagination

* **Default limit** - If you omit `limit`, the API may apply a large default (like, 1000). For most use cases, set an explicit limit (such as, 20–50) to avoid oversized responses and timeouts.
* **Maximum** - The platform caps `limit` (often at 100). Values above the cap are treated as the cap.
* **Count-only** - Use `limit=0` to get only `$meta.pagination.total` (see above).
* **Pagination** - Use `limit` and `offset` (or the equivalent page-based parameters if documented) to page through results.

## Combining count and list in one request

When you need both the total count and a list of items, use a single request with a reasonable limit (for example, 20–50):

* `$meta.pagination.total` gives the total count.
* `data` gives the first page of items.

Avoid running a second request with `limit=0` just to get the count if the first request already returns the total in metadata.

## Order in the query string

Sort order is specified as part of the query string, not as a separate body or header:

* Ascending - `order=+property` or `order=+audit.created.at`
* Descending - `order=-property` or `order=-audit.updated.at`

Example:

```http
GET /public/v1/catalog/products?order=-audit.created.at&limit=10
```

If you filter or sort by an audit field, include `select=audit` (see [IDs and special characters in RQL values](rql-advanced-tips.md#ids-and-special-characters-in-rql-values)).

## Common RQL patterns (reference)

<table><thead><tr><th width="264">Need</th><th>Example</th></tr></thead><tbody><tr><td>Exact match</td><td><code>eq(status,Active)</code></td></tr><tr><td>Case-insensitive search</td><td><code>ilike(name,*Microsoft*)</code></td></tr><tr><td>Greater / less than</td><td><code>gt(price.SPxM,100)</code>, <code>lt(endDate,2026-12-31T23:59:59.999Z)</code></td></tr><tr><td>Multiple conditions</td><td><code>and(eq(status,Active),ilike(name,*Corp*))</code></td></tr><tr><td>Either condition</td><td><code>or(eq(type,A),eq(type,B))</code></td></tr><tr><td>In list</td><td><code>in(status,(Active,Updating))</code></td></tr><tr><td>Nested collection</td><td><code>any(groups,id=UGR-1234-5678)</code></td></tr><tr><td>Date range</td><td><code>and(gt(audit.created.at,"2024-01-01T00:00:00.000Z"),lt(audit.created.at,"2025-01-01T00:00:00.000Z"))</code></td></tr></tbody></table>

Always use field names that exist on the resource (see section 1).

## Terminology and identity (Buyer, Client)

In the API, Buyer and Client have distinct meanings and ID formats:

* **Buyer** - Legal entity; ID format `BUY-xxxx-xxx`. Core for billing and legal.
* **Client** - One or more Buyers in the Client Portal; ID format `ACC-xxxx-xxxx`.

**Filtering by Client or Buyer:** To filter by Client (ACC- IDs), use `client.id` in RQL on resources that expose it (for example, `commerce.orders`, `commerce.agreements`): `eq(client.id,"ACC-1234-5678")`. To filter by Buyer (BUY- IDs), use `buyer.id`: `eq(buyer.id,"BUY-1234-5678")`. Check the resource schema to see which relationship field exists (`client.id`, `buyer.id`, etc.).

Many resources also expose `externalIds` (vendor, client, operations), identifiers from actors outside the marketplace. Use them to filter by external references (for example, `eq(externalIds.vendor,"Microsoft-account-123")` or `eq(externalIds.client,"my-order-ref")`) when the resource schema includes these fields. See [External IDs](../common-api-objects/externalids.md) for semantics and typical usage.

## Price fields in RQL

Price objects typically expose SPxM / SPxY (sales/sell price) and currency. Include currency when stating amounts. See [Price](../common-api-objects/price.md) for full field semantics and visibility rules.

## Subscription and commitment fields (commerce.subscriptions)

For "expiring", "renewal", or "commitment end" questions, key fields are: `commitmentDate` (ISO 8601 UTC), `terms.commitment` (for example,  `1y`, `1m`), `terms.period` (billing period), and `autoRenew` (boolean).&#x20;

Filter by `commitmentDate` in RQL for date ranges; include `select=+commitmentDate,+autoRenew,+terms` (or `+terms.commitment`) when you need to interpret renewal vs expiry in the response.

## Path parameters (by-id endpoints)

Some resources have endpoints that require path parameters (for example, get product by id: `/catalog/products/{id}`).&#x20;

RQL applies to list endpoints; when you need a single item by ID, use the appropriate by-id endpoint and supply the path parameter (e.g. `id=PRD-1234-5678`). The resource schema or API docs will indicate when path parameters are required.

## 400 Bad Request or "Unknown expression"

If the API returns 400 or "Unknown expression" (or "Unknown expression group"):

1. Re-check the resource schema - The field path you used may not exist or may be nested differently (e.g. `seller.country` vs `seller.address.country`).
2. Quote ID values - use `eq(client.id,"ACC-1234-5678")` not `eq(client.id,ACC-1234-5678)`.
3. Include `select=audit` when filtering or sorting by `audit.created.at` or `audit.updated.at`.
4. Use full UTC date format - `YYYY-MM-DDTHH:mm:ss.sssZ`.

## Further resources

* [Resource Query Language](../resource-query-language.md) - Core operators and syntax.
* [.NET RQL reference](https://github.com/softwareone-platform/mpt-rql-net) - C# implementation reference.
