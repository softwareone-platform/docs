---
description: Learn about Resource Query Language and how to use it.
---

# Resource Query Language

Resource Query Language (RQL) is a query language used by the Marketplace Platform in its REST API. It's used for querying and manipulating resources in the Marketplace Platform's [REST API](./).&#x20;

With RQL, you can filter, sort, paginate, and project data. It's simple to use but flexible enough to handle complex scenarios.

## Using RQL&#x20;

RQL consists of a set of operators that can be classified into three main categories:

* **Comparison operators** - These operators perform comparisons like equals, greater than, and so on.
* **Logical operators** - These operators combine multiple conditions.
* **Algorithmic operators** - These operators handle functionalities, like sorting and pagination.

Operators are formatted as `operator(arg1,arg2,...)`. Complex expressions can be created by nesting these operators.

## Practical examples

Let's say you want to list all users with a specific domain. Implementing filtering is essential, and this is where RQL comes in.

### **Basic filtering**

To display all users with the first name 'Buzz, your `GET` request will look like this:

```http
GET /v1/accounts/users?firstName=Buzz
```

The same expression can be written as:&#x20;

```http
GET /v1/accounts/users?eq(firstName,Buzz)
```

### Sorting

To sort users based on their first name, your `GET` request will look like this:

```http
GET /v1/accounts/users?order=firstName
```

To sort in the opposite direction, the '-' operator can be used:

```http
GET /v1/accounts/users?order=-firstName
```

### Pagination

To paginate your results with a limit of 10 users and to retrieve the third page (offset 20):

```http
GET /v1/accounts/users?limit=10&offset=20
```

* The first parameter `limit=10` expresses the number of users to return
* The second parameter `offset=20` offsets the starting position in the result set. The first 20 users will be skipped.

### Projection

To request specific fields, such as `firstName`, `lastName`, and `email` to be included, the `select=+` operator can be used:

```http
GET /v1/accounts/users?select=+firstName,+lastName,+email
```

To request certain fields to be excluded, the `select=-` operator can be used:

```http
GET /v1/accounts/users?select=-firstName,-lastName,-email
```

### Search

To search for all users with the first name starting from 'Bu', the following query can be used:

```http
GET /v1/accounts/users?ilike(firstName,Bu*)
```

the operator `ilike` performs a case-insensitive search.

### Combining operators

Logical operators can be used to combine multiple operators. For example, to filter users with first name 'Buzz' and last name 'Astral':

```http
GET /v1/accounts/users?and(eq(firstName,Buzz),eq(lastName,Astral))
```

In simple cases, a combined expression can also be written in the following form:

```http
GET /v1/accounts/users?firstName=Buzz&lastName=Astral
```

## Operators

<table><thead><tr><th width="341">Function</th><th>Description</th></tr></thead><tbody><tr><td><strong>or</strong> (&#x3C;condition1>, &#x3C;condition2>, ...)</td><td>Returns records that satisfy at least one of the specified conditions.</td></tr><tr><td><strong>and</strong> (&#x3C;condition1>, &#x3C;condition2>, ...)</td><td>Returns records that satisfy all of the specified conditions.</td></tr><tr><td><strong>not</strong> (&#x3C;condition>)</td><td>Returns records that do not satisfy the specified condition.</td></tr><tr><td><strong>empty</strong> ( )</td><td>Constant that is used to represent an empty string. Example: /users?firstName=empty()</td></tr><tr><td><strong>null</strong> ( )</td><td>Constant that is used to represent an unassigned ("null") value. Example: /users?firstName=null()</td></tr><tr><td><strong>order</strong> = +&#x3C;property1>,-&#x3C;property2>, ...</td><td>Sorts the returned records by <code>&#x3C;property></code>. <code>+</code> represents the ascending order, while <code>-</code> represents the descending order.</td></tr><tr><td><strong>select</strong> = +&#x3C;property1>, -&#x3C;property2>, ...</td><td>Used to add and remove certain objects from the representation.</td></tr><tr><td><strong>offset</strong> = &#x3C;value></td><td>Offsets the starting position in the resulting set.</td></tr><tr><td><strong>limit</strong> = &#x3C;value></td><td>Limits the number of returned records by the specified value.</td></tr><tr><td><strong>eq</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> exactly matches the <code>&#x3C;value></code>.</td></tr><tr><td><strong>ne</strong>  (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> does not match the <code>&#x3C;value></code>.</td></tr><tr><td><strong>gt</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> is greater than the <code>&#x3C;value></code>.</td></tr><tr><td><strong>ge</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> is greater or equal to the <code>&#x3C;value></code>.</td></tr><tr><td><strong>lt</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> is less than the <code>&#x3C;value></code>.</td></tr><tr><td><strong>le</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> is less than or equal to the <code>&#x3C;value></code>.</td></tr><tr><td><strong>ilike</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> contains <code>&#x3C;value></code> as a substring, the comparison is case-insensitive.</td></tr><tr><td><strong>in</strong> (&#x3C;property>,(&#x3C;value1>,&#x3C;value2>,...))</td><td>Filters records where <code>&#x3C;property></code> matches any of the listed <code>&#x3C;value>s</code>.</td></tr><tr><td><strong>out</strong> (&#x3C;property>,(&#x3C;value1>,&#x3C;value2>,...))</td><td>Filters records where <code>&#x3C;property></code> matches none of the listed <code>&#x3C;value>s</code>.</td></tr><tr><td><strong>any</strong> (&#x3C;collection>, &#x3C;condition>)</td><td>Filters records by applying <code>&#x3C;condition></code> to the nested <code>&#x3C;collection></code> .</td></tr><tr><td><strong>all</strong> (&#x3C;collection>, &#x3C;condition>)</td><td>Filters records by applying <code>&#x3C;condition></code> to the nested <code>&#x3C;collection></code> .</td></tr></tbody></table>

## Advanced use cases <a href="#markdown-header-more-information" id="markdown-header-more-information"></a>

### Special characters in values

To pass special characters (like, &^$?) or whitespaces as values to RQL operators, enclose them in either double quotes (") or single quotes (') as shown in the following example:

```http
GET /v1/accounts/users?firstName="Buzz !!!"
```

If you need to include a quotation mark within the value, you can do so by enclosing it with a different type of quotation mark, as shown in the following example:

```http
GET /v1/accounts/users?firstName="Buzz with the ' Quote"
```

Allowing you to pass these special symbols as values.

### The asterisk Character and the ilike operator

The asterisk (\*) character has a special meaning in the `ilike` operator, matching zero or more characters in its place from the parameter value. For example, the "\*dog" pattern will match strings like "big dog" and "dog," but it will not match "big dog!" because of the exclamation mark.

If you need to use the asterisk (\*) character itself in the pattern, you can escape it as '\*', as shown in the following example:

```http
GET /v1/accounts/users?ilike(firstName,"The\**")
```

The ilike operator in this case will be searching for the literal value “The\*” at the beginning of the firstName property.

## Best practices (quick reference)

Before writing RQL, keep these in mind:

| Topic | Recommendation |
|-------|-----------------|
| **Field names** | RQL filter and sort fields must exist on the resource. Do not invent field names (e.g. `subscriptionsCount`). Use the resource schema or API documentation to see exact field names and types. |
| **Dates** | Use UTC with 3-digit millisecond precision: `YYYY-MM-DDTHH:mm:ss.sssZ` (e.g. `2026-01-31T23:00:00.000Z`). |
| **Audit fields** | When filtering or sorting by `audit.created.at`, `audit.updated.at`, etc., you **must** include `audit` in the `select` parameter (e.g. `select=audit` or `select=+id,+name,audit`). The API will not filter by fields that are not selected. |
| **Counting** | Use `limit=0` to get only the count: the response has an empty `data` array and the total in `$meta.pagination.total`. |
| **Limit** | Prefer a reasonable limit (e.g. 20–50) for list queries. Maximum is 100 (values above 100 are capped). For count-only, use `limit=0`. |
| **Select** | Use `select=+id,+name,+field` to include only needed fields (smaller payloads). To include omitted fields (see `$meta.omitted`), use `select=+field`. For nested collections, `+subscriptions.id,+subscriptions.name` returns only id and name per item; `+subscriptions` returns the full nested representation. |
| **Order in URL** | Order is part of the query string: `?order=-audit.created.at&limit=10`. Do not send RQL as a single query parameter (see below). |
| **RQL vs parameters** | Do not put `limit` or `order` inside the RQL string. RQL is only the filter expression; `limit`, `offset`, `select`, and `order` are separate query parameters. |
| **IDs in RQL** | When filtering by ID fields (e.g. `client.id`, `buyer.id`, `agreement.id`), use **double-quoted** values: `eq(client.id,"ACC-1234-5678")`. Unquoted IDs can return no results. |

For more detail and advanced patterns, see [RQL advanced tips](rql-advanced-tips.md).

## Integration guide and best practices

This section documents key findings and best practices for interacting with the SoftwareOne Platform API, derived from real-world integration and debugging experience.

### 1. Authentication
The API supports standard Bearer token authentication.
- **Header**: `Authorization: Bearer <token>`

### 2. Querying and RQL (Resource Query Language)
One of the most critical findings is how RQL filters must be passed to the API.

#### The Findings
- **DO NOT** pass RQL as a query parameter value (e.g., `?rql=and(...)`). This often results in `400 Bad Request` or "Invalid equals shortcut expression".
- **DO** append the RQL string directly to the URL query string.

#### Syntax Pattern
**Incorrect:**
```http
GET /resource?rql=and(eq(status,Active),ilike(name,*Microsoft*))
```

**Correct:**
```http
GET /resource?and(eq(status,Active),ilike(name,*Microsoft*))
```

#### Combining with Standard Parameters
You can mix RQL with standard parameters like `limit` and `offset`.
```http
GET /resource?and(eq(status,Active))&limit=100&offset=0
```

### 3. Efficient Resource Counting
To get the count of related resources (e.g., "How many subscriptions does this agreement have?") without fetching all the data:

1.  **Query the Child Resource**: Target the specific resource endpoint (e.g., `/commerce/subscriptions`).
2.  **Filter by Parent ID**: Use a direct filter parameter if available, or RQL.
    *   *Finding*: The API often accepts direct property filters like `?agreement.id=AGR-XXX`.
3.  **Minimize Payload**: Set `limit=0`.
    *   *Finding*: `limit=0` is fully supported and recommended. It returns an empty `data` array but includes the correct count in `$meta.pagination.total`.
4.  **Read Metadata**: Extract the count from the response metadata.

**Example Request:**
```http
GET /commerce/subscriptions?agreement.id=AGR-1234-5678&limit=0
```

**Response Structure:**
```json
{
  "$meta": {
    "pagination": {
      "total": 42,  <-- The value you want
      "limit": 0,
      "offset": 0
    }
  },
  "data": [] 
}
```
*Note: Using `limit=0` is the most efficient way to get counts as it minimizes data transfer.*

### 4. Handling Large Datasets (JSONL & Redirects)
When requesting large datasets (e.g., full collections), the API might respond with a `302 Redirect` to a file download URL (often for `application/jsonl` format).
- **Finding**: Clients must handle redirects and potentially download from a secondary URL (e.g., AWS S3).
- **Header**: `Accept: application/jsonl` is often used for these bulk operations.

### 5. Advanced RQL Patterns

#### Date Filtering
You can filter by date ranges using ISO 8601 strings.

> [!IMPORTANT]
> **API Date Requirement**: Dates must be in **UTC** and include **3-digit millisecond precision** (e.g., `YYYY-MM-DDTHH:mm:ss.sssZ`).

```http
GET /billing/invoices?select=audit&and(gt(audit.created.at,"2024-12-01T08:00:00.000Z"),lt(audit.created.at,"2026-01-01T08:00:00.000Z"))
```

#### Nested Collection Filtering with `any()`
The `any()` operator is powerful for filtering based on properties of nested objects (e.g., finding users in a specific group).
```http
GET /accounts/account-users?any(groups,id=UGR-1234-5678)
```

### 6. Response Metadata
Be aware of metadata fields that affect data processing.
- **`$meta.pagination.total`**: The total number of records matching the query (useful when `limit=0`).
- **`$meta.omitted`**: A list of properties excluded from the response payload for security or performance reasons (e.g., `["credits"]`).

### 7. Date Fields & Projection
Date fields like `created` and `updated` are typically nested within the `audit` object.
- **Finding**: To filter by these dates OR see them in the response, you **MUST explicitly select** the `audit` object. The API will not filter by fields that are not selected/visible in the response context.
- **Example**: `?select=audit&and(gt(audit.created.at,"2024-01-01..."))`

### 8. Terminology & Identity Resolution

In the API, **Buyer** and **Client** have distinct meanings and ID formats:

*   **Buyer**: Represents a legal entity in the platform.
    *   **ID Format**: `BUY-xxxx-xxx`
    *   *Note*: This is the core entity for billing and legal purposes.
*   **Client**: Represents one or multiple Buyers activated in the self-service part of the platform (Client Portal).
    *   **ID Format**: `ACC-1234-5678`

When filtering by Client (ACC- IDs), use **`client.id`** in RQL on resources that expose it (e.g. `commerce.orders`, `commerce.agreements`): `eq(client.id,"ACC-1234-5678")`. When filtering by Buyer (BUY- IDs), use **`buyer.id`**. Check the resource schema to see which relationship field exists.

## Further resources <a href="#further-resources" id="further-resources"></a>

For a C# reference implementation of RQL for .NET applications, see the GitHub repository at [https://github.com/softwareone-platform/mpt-rql-net](https://github.com/softwareone-platform/mpt-rql-net).
