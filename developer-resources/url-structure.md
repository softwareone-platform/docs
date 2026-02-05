---
description: Learn how to map between Portal URLs and API endpoints for Marketplace Platform objects.
---

# URL Structure

The Marketplace Platform provides two main entry points for interacting with your data:

* **Portal (Web UI)**: `https://portal.platform.softwareone.com/`
* **API**: `https://api.platform.softwareone.com/public/v1/`

While both the Portal and API operate on the same underlying objects, their URL structures differ slightly due to usability requirements. This article explains how to map between Portal URLs and API endpoints, which is useful when you need to:

* Generate deep links to specific objects in the Portal
* Determine which API endpoint to call based on a Portal URL
* Build integrations that navigate between UI and API resources
* Enable LLM agents to translate between human-readable links and API calls

## Object ID prefixes

Every object in the Marketplace Platform has a unique identifier with a prefix that indicates the object type. Use these prefixes to quickly identify what kind of object you are working with:

### Accounts

| Prefix | Object Type | Example |
|--------|-------------|---------|
| `ACC-` | Account | `ACC-1234-5678` |
| `BUY-` | Buyer | `BUY-5171-6994` |
| `SEL-` | Seller | `SEL-6685-4945` |
| `LCE-` | Licensee | `LCE-8499-1473-5603` |
| `USR-` | User | `USR-3758-7092` |
| `UGR-` | User Group | `UGR-0601-5102` |
| `TKN-` | API Token | `TKN-9299-7556` |

### Commerce

| Prefix | Object Type | Example |
|--------|-------------|---------|
| `AGR-` | Agreement | `AGR-8784-9237-0931` |
| `AST-` | Asset | `AST-3258-2228-4345` |
| `ORD-` | Order | `ORD-8108-0372-6265` |
| `SUB-` | Subscription | `SUB-9892-4074-5613` |
| `REQ-` | Request | `REQ-5375-9599` |

### Billing

| Prefix | Object Type | Example |
|--------|-------------|---------|
| `SOM-` | Statement | `SOM-6005-1054-1535-5364` |
| `INV-` | Invoice | `INV-2078-0901-9457-5058` |
| `CRD-` | Credit Memo | `CRD-8280-7533-0235-8348` |

### Catalog

| Prefix | Object Type | Example |
|--------|-------------|---------|
| `PRD-` | Product | `PRD-4471-6929` |
| `ITM-` | Item | `ITM-3386-3348-1368` |
| `LST-` | Listing | `LST-7264-0230` |
| `AUT-` | Authorization | `AUT-6222-9718` |
| `PRC-` | Price List | `PRC-3386-3348-0003` |

### Program

| Prefix | Object Type | Example |
|--------|-------------|---------|
| `PRG-` | Program | `PRG-0742-8320` |
| `CER-` | Certificate | `CER-1104-3765-0381` |
| `ENR-` | Enrollment | `ENR-9988-8127-1981` |

### Notifications

| Prefix | Object Type | Example |
|--------|-------------|---------|
| `WBH-` | Webhook | `WBH-0700-8876` |

## URL mapping reference

The following tables show how Portal URLs map to API endpoints for each category of objects.

### Accounts objects

| Object | Portal URL | API Endpoint |
|--------|-----------|--------------|
| **Buyers List** | `/accounts/buyers` | `GET /accounts/buyers` |
| **Buyer Details** | `/accounts/buyers/{id}` | `GET /accounts/buyers/{id}` |
| **Licensees List** | `/accounts/licensees` | `GET /accounts/licensees` |
| **Licensee Details** | `/accounts/licensees/{id}` | `GET /accounts/licensees/{id}` |
| **Users List** | `/accounts/users` | `GET /accounts/users` |
| **User Details** | `/accounts/users/{id}` | `GET /accounts/users/{id}` |
| **User Groups List** | `/accounts/groups` | `GET /accounts/user-groups` |
| **User Group Details** | `/accounts/groups/{id}` | `GET /accounts/user-groups/{id}` |
| **API Tokens List** | `/settings/tokens` | `GET /accounts/api-tokens` |
| **API Token Details** | `/settings/tokens/{id}` | `GET /accounts/api-tokens/{id}` |

{% hint style="info" %}
The Portal uses `/accounts/groups` while the API uses `/accounts/user-groups`. API tokens are accessed via the Settings section in the Portal.
{% endhint %}

### Commerce objects

| Object | Portal URL | API Endpoint |
|--------|-----------|--------------|
| **Agreements List** | `/commerce/agreements` | `GET /commerce/agreements` |
| **Agreement Details** | `/commerce/agreements/{id}` | `GET /commerce/agreements/{id}` |
| **Assets List** | `/commerce/assets` | `GET /commerce/assets` |
| **Asset Details** | `/commerce/assets/{id}` | `GET /commerce/assets/{id}` |
| **Entitlements List** | `/commerce/entitlements` | `GET /commerce/lines` |
| **Entitlement Details** | `/catalog/items/{id}` | `GET /catalog/items/{id}` |
| **Orders List** | `/commerce/orders` | `GET /commerce/orders` |
| **Order Details** | `/commerce/orders/{id}` | `GET /commerce/orders/{id}` |
| **Subscriptions List** | `/commerce/subscriptions` | `GET /commerce/subscriptions` |
| **Subscription Details** | `/commerce/subscriptions/{id}` | `GET /commerce/subscriptions/{id}` |
| **Requests List** | `/commerce/requests` | `GET /commerce/requests` |
| **Request Details** | `/commerce/requests/{id}` | `GET /commerce/requests/{id}` |

{% hint style="info" %}
The Entitlements page in the Portal shows commerce lines, and clicking on an entitlement opens the catalog item details page.
{% endhint %}

### Billing objects

| Object | Portal URL | API Endpoint |
|--------|-----------|--------------|
| **Statements List** | `/billing/statements` | `GET /billing/statements` |
| **Statement Details** | `/billing/statements/{id}` | `GET /billing/statements/{id}` |
| **Invoices List** | `/billing/invoices` | `GET /billing/invoices` |
| **Invoice Details** | `/billing/invoices/{id}` | `GET /billing/invoices/{id}` |
| **Credit Memos List** | `/billing/credit-memos` | `GET /billing/credit-memos` |
| **Credit Memo Details** | `/billing/credit-memos/{id}` | `GET /billing/credit-memos/{id}` |

### Catalog objects

| Object | Portal URL | API Endpoint |
|--------|-----------|--------------|
| **Products List** | `/catalog/products` | `GET /catalog/products` |
| **Product Details** | `/catalog/products/{id}` | `GET /catalog/products/{id}` |
| **Items List** | `/catalog/items` | `GET /catalog/items` |
| **Item Details** | `/catalog/items/{id}` | `GET /catalog/items/{id}` |
| **Listings** | API only | `GET /catalog/listings` |
| **Listing Details** | API only | `GET /catalog/listings/{id}` |
| **Authorizations** | API only | `GET /catalog/authorizations` |
| **Authorization Details** | API only | `GET /catalog/authorizations/{id}` |
| **Price Lists** | API only | `GET /catalog/price-lists` |
| **Price List Details** | API only | `GET /catalog/price-lists/{id}` |

{% hint style="info" %}
Listings, Authorizations, and Price Lists are available through the API but do not have dedicated Portal pages. They are typically accessed programmatically for integration purposes.
{% endhint %}

### Program objects

| Object | Portal URL | API Endpoint |
|--------|-----------|--------------|
| **Programs List** | `/program/programs` | `GET /program/programs` |
| **Program Details** | `/program/programs/{id}` | `GET /program/programs/{id}` |
| **Certificates List** | `/program/certificates` | `GET /program/certificates` |
| **Certificate Details** | `/program/certificates/{id}` | `GET /program/certificates/{id}` |
| **Enrollments List** | `/program/enrollments` | `GET /program/enrollments` |
| **Enrollment Details** | `/program/enrollments/{id}` | `GET /program/enrollments/{id}` |

### Notifications objects (API only)

The notifications module is primarily accessed through the API for webhook management and programmatic notification handling.

| Object | Portal URL | API Endpoint |
|--------|-----------|--------------|
| **Webhooks** | API only | `GET /notifications/webhooks` |
| **Webhook Details** | API only | `GET /notifications/webhooks/{id}` |
| **Messages** | API only | `GET /notifications/messages` |
| **Message Details** | API only | `GET /notifications/messages/{id}` |
| **Contacts** | API only | `GET /notifications/contacts` |
| **Subscribers** | API only | `GET /notifications/subscribers` |

### Sellers objects (API only)

Sellers are organizational entities that represent SoftwareOne regional operations.

| Object | Portal URL | API Endpoint |
|--------|-----------|--------------|
| **Sellers List** | API only | `GET /accounts/sellers` |
| **Seller Details** | API only | `GET /accounts/sellers/{id}` |

## URL patterns

### Portal URL pattern

```
https://portal.platform.softwareone.com/{module}/{resource}/{id}
```

Where:
* `{module}` is one of: `accounts`, `commerce`, `billing`, `catalog`, `program`, `settings`
* `{resource}` is the plural resource name (for example, `agreements`, `orders`, `invoices`)
* `{id}` is the object identifier (optional, only for detail pages)

### API URL pattern

```
https://api.platform.softwareone.com/public/v1/{module}/{resource}/{id}
```

The API follows the same structure, with `/public/v1/` added after the base domain.

### Module mapping between Portal and API

| Portal Module | API Module | Notes |
|---------------|------------|-------|
| `accounts` | `accounts` | User groups use different paths |
| `commerce` | `commerce` | Direct mapping |
| `billing` | `billing` | Direct mapping |
| `catalog` | `catalog` | Direct mapping |
| `program` | `program` | Direct mapping |
| `settings` | `accounts` | API tokens are under accounts in API |
| N/A | `notifications` | API only |
| N/A | `audit` | API only |
| N/A | `spotlight` | API only |

## Usage examples

### Generating a Portal link from an API response

When you retrieve an object from the API, you can construct a Portal link using the object's `id`:

```python
# Python example
def get_portal_url(api_response, resource_type):
    base_url = "https://portal.platform.softwareone.com"
    object_id = api_response["id"]
    
    # Map resource types to Portal paths
    resource_paths = {
        # Accounts
        "buyer": "accounts/buyers",
        "licensee": "accounts/licensees",
        "user": "accounts/users",
        "user-group": "accounts/groups",
        "api-token": "settings/tokens",
        # Commerce
        "agreement": "commerce/agreements",
        "order": "commerce/orders",
        "subscription": "commerce/subscriptions",
        "asset": "commerce/assets",
        "request": "commerce/requests",
        # Billing
        "statement": "billing/statements",
        "invoice": "billing/invoices",
        "credit-memo": "billing/credit-memos",
        # Catalog
        "product": "catalog/products",
        "item": "catalog/items",
        # Program
        "program": "program/programs",
        "certificate": "program/certificates",
        "enrollment": "program/enrollments",
    }
    
    path = resource_paths.get(resource_type)
    if path is None:
        return None  # API-only resource
    return f"{base_url}/{path}/{object_id}"

# Example usage
order = {"id": "ORD-8108-0372-6265", "status": "Completed"}
portal_link = get_portal_url(order, "order")
# Returns: https://portal.platform.softwareone.com/commerce/orders/ORD-8108-0372-6265
```

### Determining the API endpoint from a Portal URL

When you have a Portal URL and need to call the corresponding API:

```python
# Python example
from urllib.parse import urlparse

def get_api_endpoint(portal_url):
    base_api = "https://api.platform.softwareone.com/public/v1"
    
    parsed = urlparse(portal_url)
    path = parsed.path.strip("/")
    
    # Skip 'home' as it has no API equivalent
    if path == "home":
        return None
    
    return f"{base_api}/{path}"

# Example usage
portal_url = "https://portal.platform.softwareone.com/commerce/orders/ORD-8108-0372-6265"
api_endpoint = get_api_endpoint(portal_url)
# Returns: https://api.platform.softwareone.com/public/v1/commerce/orders/ORD-8108-0372-6265
```

### Extracting the object type from an ID

You can determine the object type from the ID prefix:

```python
# Python example
def get_object_type(object_id):
    prefix_map = {
        # Accounts
        "ACC": "account",
        "BUY": "buyer",
        "SEL": "seller",
        "LCE": "licensee",
        "USR": "user",
        "UGR": "user-group",
        "TKN": "api-token",
        # Commerce
        "AGR": "agreement",
        "AST": "asset",
        "ORD": "order",
        "SUB": "subscription",
        "REQ": "request",
        # Billing
        "SOM": "statement",
        "INV": "invoice",
        "CRD": "credit-memo",
        # Catalog
        "PRD": "product",
        "ITM": "item",
        "LST": "listing",
        "AUT": "authorization",
        "PRC": "price-list",
        # Program
        "PRG": "program",
        "CER": "certificate",
        "ENR": "enrollment",
        # Notifications
        "WBH": "webhook",
    }
    
    prefix = object_id.split("-")[0]
    return prefix_map.get(prefix, "unknown")

# Example usage
object_type = get_object_type("ORD-8108-0372-6265")
# Returns: "order"
```

## Notes for LLM agents

When working with Marketplace Platform URLs, follow these guidelines:

1. **ID Recognition**: Object IDs always follow the pattern `{PREFIX}-{segments}` where the prefix is 3 letters (for example, `AGR`, `ORD`, `SUB`). Extract the prefix to determine the object type.

2. **URL Translation**: To convert a Portal URL to an API endpoint:
   * Replace `portal.platform.softwareone.com` with `api.platform.softwareone.com/public/v1`
   * Keep the path unchanged (for example, `/commerce/orders/{id}`)

3. **API to Portal**: To convert an API endpoint to a Portal URL:
   * Replace `api.platform.softwareone.com/public/v1` with `portal.platform.softwareone.com`
   * Keep the path unchanged

4. **Special Cases**:
   * The Portal home page (`/home`) has no API equivalent
   * Entitlement details pages redirect to `/catalog/items/{id}`
   * Portal uses `/accounts/groups` but API uses `/accounts/user-groups`
   * API tokens are at `/settings/tokens` in Portal but `/accounts/api-tokens` in API
   * The API requires authentication via Bearer token

5. **Module Detection**: The first path segment after the base URL indicates the module:
   * `accounts` = Buyers, Licensees, Users, User Groups, API Tokens, Sellers
   * `commerce` = Agreements, Assets, Orders, Subscriptions, Requests, Entitlements
   * `billing` = Statements, Invoices, Credit Memos
   * `catalog` = Products, Items, Listings, Authorizations, Price Lists
   * `program` = Programs, Certificates, Enrollments
   * `notifications` = Webhooks, Messages, Contacts, Subscribers (API only)

6. **API-Only Resources**: Some resources are only accessible via API and have no Portal equivalent:
   * Sellers (`SEL-`)
   * Listings (`LST-`)
   * Authorizations (`AUT-`)
   * Price Lists (`PRC-`)
   * Webhooks (`WBH-`)
   * Notification Messages, Contacts, Subscribers

## Related topics

{% content-ref url="rest-api/" %}
[rest-api](rest-api/)
{% endcontent-ref %}

{% content-ref url="rest-api/resource-query-language.md" %}
[resource-query-language.md](rest-api/resource-query-language.md)
{% endcontent-ref %}
