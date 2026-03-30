# Listing

The Listing object represents a business entity that aligns a product with a specific SoftwareOne seller. It is defined by an authorization and an assigned price list. Listings are essential for managing the visibility and availability of products across different markets and for overseeing their lifecycle in an efficient and scalable way.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="153">Field Name</th><th width="199">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>The primary identifier for the listing.</td></tr><tr><td><code>product</code></td><td>object</td><td>A reference to the <a href="../product/"><code>product</code></a> object.</td></tr><tr><td><code>authorization</code></td><td>object</td><td>A reference to the <a href="../authorization/"><code>authorization</code></a> object.</td></tr><tr><td><code>seller</code></td><td>object</td><td>A reference to the <a href="../../accounts-api/seller/"><code>seller</code></a> object.</td></tr><tr><td><code>priceList</code></td><td>object</td><td>A reference to the <a href="../pricelists/"><code>pricelist</code></a> object.</td></tr><tr><td><code>primary</code></td><td>boolean</td><td>If the product has more associated listings with the same seller, the <code>primary</code> flag indicates the listing used in the purchase wizard.</td></tr><tr><td><code>notes</code></td><td>string</td><td>The user notes about the listing.</td></tr><tr><td><code>statistics</code></td><td>object (<a href="./#listingstatistics">listingStatistics</a>)</td><td>The system calculated metrics about the listing.</td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Listing Statistics object <a href="#listingstatistics" id="listingstatistics"></a>

<table><thead><tr><th width="158">Field Name</th><th width="192">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>subscriptions</code></td><td>integer</td><td><p>The number of associated subscriptions. </p><p>Example: 10</p></td></tr><tr><td><code>agreements</code></td><td>integer</td><td><p>The number of associated agreements. </p><p>Example: 5</p></td></tr></tbody></table>

## Example response

{% code lineNumbers="true" %}
```json
{
  "id": "LST-1234-4678",  
  "product": {
    "id": "PRD-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111/logo.png"
  },
  "authorization": {
    "id": "AUT-1234-4567",   
    "name": "Salesforce Enterprise License"
  }, 
  "seller": {
    "id": "SEL-1234-45678",   
    "name": "SoftwareOne, Inc."
  },
  "priceList": {
    "id": "PRC-1234-5678-1234"   
  },
  "primary": true,
  "notes": "This is the primary Listing for the EU.",
  "statistics": {
    "subscriptions": 10,
    "agreements": 5
  },
  "audit": {
    "created": { "at": "...", "by": { } },
    "updated": { "at": "...", "by": { } }
  },
}
```
{% endcode %}
