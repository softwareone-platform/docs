---
description: >-
  Learn how to map between Portal URLs and API endpoints for Marketplace
  Platform objects.
---

# URL structure

The Marketplace Platform provides two main entry points for interacting with your data:

* **Portal (Web UI)** – `https://portal.platform.softwareone.com/`
* **API** – `https://api.platform.softwareone.com/public/v1/`

While both the Portal and API operate on the same underlying objects, their URL structures differ slightly due to usability requirements. This topic explains how you can map between portal URLs and API endpoints to:

* Generate deep links to specific objects in the portal.
* Determine which API endpoint to call based on a portal URL.
* Build integrations that navigate between UI and API resources.
* Enable LLM agents to translate between human-readable links and API calls.

### API endpoint

The base endpoint for the Marketplace Platform API is:

```http
https://api.platform.softwareone.com/public
```

&#x20;All API requests start from that base URL. For example, if you have an endpoint like:

```http
/v1/accounts/buyers
```

The fully qualified URL that you need to use is:

```http
https://api.platform.softwareone.com/public/v1/accounts/buyers
```

Use this base endpoint with specific API paths to access the resources and services provided by the Marketplace Platform.

### Object ID prefixes

Every object in the Marketplace Platform has a unique identifier with a prefix that indicates the object type. For details on all such objects, see [Business objects & API collection reference](business-objects-and-api-collections.md).

### URL mapping reference

The following tables show how Portal URLs map to API endpoints for each category of objects.

### Accounts objects

<table><thead><tr><th width="139">Object</th><th width="362">Portal URL</th><th>API Endpoint</th></tr></thead><tbody><tr><td>Buyers List</td><td><code>/administration/settings/buyers</code></td><td><code>GET /accounts/buyers</code></td></tr><tr><td>Buyer Details</td><td><code>/administration/settings/buyers/{id}</code></td><td><code>GET /accounts/buyers/{id}</code></td></tr><tr><td>Sellers List</td><td><code>/administration/settings/sellers</code></td><td><code>GET /accounts/sellers</code></td></tr><tr><td>Seller Details</td><td><code>/administration/settings/sellers/{id}</code></td><td><code>GET /accounts/sellers/{id}</code></td></tr><tr><td>Licensees List</td><td><code>/administration/settings/licensees</code></td><td><code>GET /accounts/licensees</code></td></tr><tr><td>Licensee Details</td><td><code>/administration/settings/licensees/{id}</code></td><td><code>GET /accounts/licensees/{id}</code></td></tr><tr><td>Users List</td><td><code>/administration/settings/users</code></td><td><code>GET /accounts/users</code></td></tr><tr><td>User Details</td><td><code>/administration/settings/users/{id}</code></td><td><code>GET /accounts/users/{id}</code></td></tr><tr><td>User Groups List</td><td><code>/administration/settings/groups</code></td><td><code>GET /accounts/user-groups</code></td></tr><tr><td>User Group Details</td><td><code>/administration/settings/groups/{id}</code></td><td><code>GET /accounts/user-groups/{id}</code></td></tr><tr><td>API Tokens List</td><td><code>/administration/settings/api-tokens</code></td><td><code>GET /accounts/api-tokens</code></td></tr><tr><td>API Token Details</td><td><code>/administration/settings/api-tokens/{id}</code></td><td><code>GET /accounts/api-tokens/{id}</code></td></tr></tbody></table>

{% hint style="info" %}
All account-related objects in the Portal are accessed via the `/administration/settings/` path. The Portal uses `groups` , while the API uses `user-groups`.
{% endhint %}

### Commerce objects

<table><thead><tr><th width="180">Object</th><th>Portal URL</th><th>API Endpoint</th></tr></thead><tbody><tr><td>Agreements List</td><td><code>/commerce/agreements</code></td><td><code>GET /commerce/agreements</code></td></tr><tr><td>Agreement Details</td><td><code>/commerce/agreements/{id}</code></td><td><code>GET /commerce/agreements/{id}</code></td></tr><tr><td>Assets List</td><td><code>/commerce/assets</code></td><td><code>GET /commerce/assets</code></td></tr><tr><td>Asset Details</td><td><code>/commerce/assets/{id}</code></td><td><code>GET /commerce/assets/{id}</code></td></tr><tr><td>Entitlements List</td><td><code>/commerce/entitlements</code></td><td><code>GET /commerce/lines</code></td></tr><tr><td>Entitlement Details</td><td><code>/catalog/items/{id}</code></td><td><code>GET /catalog/items/{id}</code></td></tr><tr><td>Orders List</td><td><code>/commerce/orders</code></td><td><code>GET /commerce/orders</code></td></tr><tr><td>Order Details</td><td><code>/commerce/orders/{id}</code></td><td><code>GET /commerce/orders/{id}</code></td></tr><tr><td>Subscriptions List</td><td><code>/commerce/subscriptions</code></td><td><code>GET /commerce/subscriptions</code></td></tr><tr><td>Subscription Details</td><td><code>/commerce/subscriptions/{id}</code></td><td><code>GET /commerce/subscriptions/{id}</code></td></tr><tr><td>Requests List</td><td><code>/commerce/requests</code></td><td><code>GET /commerce/requests</code></td></tr><tr><td>Request Details</td><td><code>/commerce/requests/{id}</code></td><td><code>GET /commerce/requests/{id}</code></td></tr></tbody></table>

{% hint style="info" %}
The **Entitlements** page in the platform shows commerce lines, and selecting an entitlement opens the catalog item details page.
{% endhint %}

### Billing objects

<table><thead><tr><th width="204">Object</th><th width="253">Portal URL</th><th>API Endpoint</th></tr></thead><tbody><tr><td>Statements List</td><td><code>/billing/statements</code></td><td><code>GET /billing/statements</code></td></tr><tr><td>Statement Details</td><td><code>/billing/statements/{id}</code></td><td><code>GET /billing/statements/{id}</code></td></tr><tr><td>Invoices List</td><td><code>/billing/invoices</code></td><td><code>GET /billing/invoices</code></td></tr><tr><td>Invoice Details</td><td><code>/billing/invoices/{id}</code></td><td><code>GET /billing/invoices/{id}</code></td></tr><tr><td>Credit Memos List</td><td><code>/billing/credit-memos</code></td><td><code>GET /billing/credit-memos</code></td></tr><tr><td>Credit Memo Details</td><td><code>/billing/credit-memos/{id}</code></td><td><code>GET /billing/credit-memos/{id}</code></td></tr></tbody></table>

### Catalog objects

<table><thead><tr><th width="196">Object</th><th width="250">Portal URL</th><th>API Endpoint</th></tr></thead><tbody><tr><td>Products List</td><td><code>/catalog/products</code></td><td><code>GET /catalog/products</code></td></tr><tr><td>Product Details</td><td><code>/catalog/products/{id}</code></td><td><code>GET /catalog/products/{id}</code></td></tr><tr><td>Items List</td><td><code>/catalog/items</code></td><td><code>GET /catalog/items</code></td></tr><tr><td>Item Details</td><td><code>/catalog/items/{id}</code></td><td><code>GET /catalog/items/{id}</code></td></tr><tr><td>Price Lists</td><td><code>/catalog/price-lists</code></td><td><code>GET /catalog/price-lists</code></td></tr><tr><td>Price List Details</td><td><code>/catalog/price-lists/{id}</code></td><td><code>GET /catalog/price-lists/{id}</code></td></tr><tr><td>Listings</td><td>API only</td><td><code>GET /catalog/listings</code></td></tr><tr><td>Listing Details</td><td>API only</td><td><code>GET /catalog/listings/{id}</code></td></tr><tr><td>Authorizations</td><td>API only</td><td><code>GET /catalog/authorizations</code></td></tr><tr><td>Authorization Details</td><td>API only</td><td><code>GET /catalog/authorizations/{id}</code></td></tr></tbody></table>

{% hint style="info" %}
Listings and Authorizations are available through the API, but don't have dedicated Portal pages. They are typically accessed programmatically for integration purposes.
{% endhint %}

### Program objects

<table><thead><tr><th width="187">Object</th><th width="264">Portal URL</th><th>API Endpoint</th></tr></thead><tbody><tr><td>Programs List</td><td><code>/program/programs</code></td><td><code>GET /program/programs</code></td></tr><tr><td>Program Details</td><td><code>/program/programs/{id}</code></td><td><code>GET /program/programs/{id}</code></td></tr><tr><td>Certificates List</td><td><code>/program/certificates</code></td><td><code>GET /program/certificates</code></td></tr><tr><td>Certificate Details</td><td><code>/program/certificates/{id}</code></td><td><code>GET /program/certificates/{id}</code></td></tr><tr><td>Enrollments List</td><td><code>/program/enrollments</code></td><td><code>GET /program/enrollments</code></td></tr><tr><td>Enrollment Details</td><td><code>/program/enrollments/{id}</code></td><td><code>GET /program/enrollments/{id}</code></td></tr></tbody></table>

### Notifications objects (API only)

The notifications module is primarily accessed through the API for webhook management and programmatic notification handling.

<table><thead><tr><th width="174">Object</th><th width="159">Portal URL</th><th>API Endpoint</th></tr></thead><tbody><tr><td>Webhooks</td><td>API only</td><td><code>GET /notifications/webhooks</code></td></tr><tr><td>Webhook Details</td><td>API only</td><td><code>GET /notifications/webhooks/{id}</code></td></tr><tr><td>Messages</td><td>API only</td><td><code>GET /notifications/messages</code></td></tr><tr><td>Message Details</td><td>API only</td><td><code>GET /notifications/messages/{id}</code></td></tr><tr><td>Contacts</td><td>API only</td><td><code>GET /notifications/contacts</code></td></tr><tr><td>Subscribers</td><td>API only</td><td><code>GET /notifications/subscribers</code></td></tr></tbody></table>

### URL patterns

#### Portal URL pattern

```
https://portal.platform.softwareone.com/{module}/{resource}/{id}
```

Where:

* `{module}` is one of: `administration/settings`, `commerce`, `billing`, `catalog`, `program`
* `{resource}` is the plural resource name (for example, `agreements`, `orders`, `invoices`)
* `{id}` is the object identifier (optional, only for detail pages)

#### API URL pattern

```
https://api.platform.softwareone.com/public/v1/{module}/{resource}/{id}
```

The API follows the same structure, with `/public/v1/` added after the base domain.

#### Module mapping between Portal and API

<table><thead><tr><th width="249">Portal Module</th><th width="190">API Module</th><th>Notes</th></tr></thead><tbody><tr><td><code>administration/settings</code></td><td><code>accounts</code></td><td>Buyers, Sellers, Licensees, Users, Groups, API Tokens</td></tr><tr><td><code>commerce</code></td><td><code>commerce</code></td><td>Direct mapping</td></tr><tr><td><code>billing</code></td><td><code>billing</code></td><td>Direct mapping</td></tr><tr><td><code>catalog</code></td><td><code>catalog</code></td><td>Direct mapping</td></tr><tr><td><code>program</code></td><td><code>program</code></td><td>Direct mapping</td></tr><tr><td>N/A</td><td><code>notifications</code></td><td>API only</td></tr><tr><td>N/A</td><td><code>audit</code></td><td>API only</td></tr><tr><td>N/A</td><td><code>spotlight</code></td><td>API only</td></tr></tbody></table>

### Usage examples

#### Generating a Portal link from an API response

When you retrieve an object from the API, you can construct a Portal link using the object's `id`:

{% code lineNumbers="true" %}
```python
# Python example
def get_portal_url(api_response, resource_type):
    base_url = "https://portal.platform.softwareone.com"
    object_id = api_response["id"]
    
    # Map resource types to Portal paths
    resource_paths = {
        # Accounts (under administration/settings)
        "buyer": "administration/settings/buyers",
        "seller": "administration/settings/sellers",
        "licensee": "administration/settings/licensees",
        "user": "administration/settings/users",
        "user-group": "administration/settings/groups",
        "api-token": "administration/settings/api-tokens",
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
        "price-list": "catalog/price-lists",
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
{% endcode %}

#### Determining the API endpoint from a Portal URL

When you have a Portal URL and need to call the corresponding API:

{% code lineNumbers="true" %}
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
{% endcode %}

#### Extracting the object type from an ID

You can determine the object type from the ID prefix:

{% code lineNumbers="true" %}
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
{% endcode %}

### Notes for LLM agents

When working with Marketplace Platform URLs, follow these guidelines:

1. **Use the correct portal URL** - Always use `https://portal.platform.softwareone.com/` for Portal links. The legacy URL `https://portal.softwareone.com/` is kept for backwards compatibility only and should not be used for new requests. Always route new links to `portal.platform.softwareone.com`.
2. **ID recognition** - Object IDs always follow the pattern `{PREFIX}-{segments}` where the prefix is 3 letters (for example, `AGR`, `ORD`, `SUB`). Extract the prefix to determine the object type.
3. **URL translation** - To convert a Portal URL to an API endpoint:
   * Replace `portal.platform.softwareone.com` with `api.platform.softwareone.com/public/v1`
   * Keep the path unchanged (for example, `/commerce/orders/{id}`)
4. **API to portal** - To convert an API endpoint to a Portal URL:
   * Replace `api.platform.softwareone.com/public/v1` with `portal.platform.softwareone.com`
   * Keep the path unchanged
5. **Special cases** -
   * The Portal home page (`/home`) has no API equivalent
   * Entitlement details pages redirect to `/catalog/items/{id}`
   * Portal uses `/administration/settings/groups` but API uses `/accounts/user-groups`
   * All accounts-related objects are under `/administration/settings/` in Portal but `/accounts/` in API
   * The API requires authentication via a Bearer token
6. **Module detection** - The first path segment after the base URL indicates the module:
   * Portal `administration/settings` = API `accounts` (Buyers, Sellers, Licensees, Users, User Groups, API Tokens)
   * `commerce` = Agreements, Assets, Orders, Subscriptions, Requests, Entitlements
   * `billing` = Statements, Invoices, Credit Memos
   * `catalog` = Products, Items, Price Lists, Listings, Authorizations
   * `program` = Programs, Certificates, Enrollments
   * `notifications` = Webhooks, Messages, Contacts, Subscribers (API only)
7. **API-only resources** - Some resources are only accessible via API and have no Portal equivalent:
   * Listings (`LST-`)
   * Authorizations (`AUT-`)
   * Webhooks (`WBH-`)
   * Notification Messages, Contacts, Subscribers
8. **Legacy URL handling** - If you encounter URLs using `portal.softwareone.com`, rewrite them to use `portal.platform.softwareone.com` before processing or generating links.

### Related topics

{% content-ref url="/broken/pages/c48wsZ6OnZim0prmKKFx" %}
[Broken link](/broken/pages/c48wsZ6OnZim0prmKKFx)
{% endcontent-ref %}

{% content-ref url="resource-query-language/" %}
[resource-query-language](resource-query-language/)
{% endcontent-ref %}
