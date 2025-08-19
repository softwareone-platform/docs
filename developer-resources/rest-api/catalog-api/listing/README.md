# Listings

The Listing object represents a business entity that aligns a product with a specific SoftwareOne seller. It is defined by an authorization and an assigned price list. Listings are essential for managing the visibility and availability of products across different markets and for overseeing their lifecycle in an efficient and scalable way.&#x20;

The Listings object contains the following attributes:

<table><thead><tr><th width="153">Field</th><th width="199">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td>The primary identifier for the listing.</td></tr><tr><td>product</td><td><a href="../product/"><code>product</code></a></td><td>A reference to the Product object.</td></tr><tr><td>authorization</td><td><a href="../authorization/"><code>authorization</code></a></td><td>A reference to the Authorization object.</td></tr><tr><td>seller</td><td><a href="../../accounts-api/seller/"><code>seller</code></a></td><td>A reference to the Seller object.</td></tr><tr><td>priceList</td><td><a href="../pricelists/"><code>pricelist</code></a></td><td>A reference to the PriceList object.</td></tr><tr><td>primary</td><td><code>boolean</code></td><td>If the product has more associated listings with the same seller, the <code>primary</code> flag indicates the listing used in the purchase wizard.</td></tr><tr><td>notes</td><td><code>string</code></td><td>The user notes about the Listing.</td></tr><tr><td>statistics</td><td><a href="./#listingstatistics"><code>listingStatistics</code></a></td><td>The system calculated metrics about the listing.</td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the Audit object.</td></tr></tbody></table>

## Listing Statistics <a href="#listingstatistics" id="listingstatistics"></a>

<table><thead><tr><th width="158">Field</th><th width="192">Type</th><th>Description</th></tr></thead><tbody><tr><td>subscriptions</td><td><code>integer</code></td><td><p>The number of associated subscriptions. </p><p>Example: 10</p></td></tr><tr><td>agreements</td><td><code>integer</code></td><td><p>The number of associated agreements. </p><p>Example: 5</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="LISTING OBJECT" %}
{% code overflow="wrap" lineNumbers="true" %}
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
{% endtab %}
{% endtabs %}
