# Listing

The Listing object represents a business entity that aligns a product with a specific SoftwareOne seller. It's defined by an authorization and an assigned price list.&#x20;

Listings are essential for managing the visibility and availability of products across markets.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-search="false"><thead><tr><th width="184">Field</th><th width="139">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The primary identifier for the listing.</td></tr><tr><td><code>product</code></td><td>object</td><td>(Read-only) Represents the <a href="../product/"><code>product</code></a> object.</td></tr><tr><td><code>eligibility</code></td><td>object, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>Represents the <a href="./#listingeligibility-object"><code>Listing Eligibility</code></a> object, which defines the eligibility status.</td></tr><tr><td><code>authorization</code></td><td>object</td><td>(Read-only) Represents the <a href="../authorization/"><code>authorization</code></a> object.</td></tr><tr><td><code>vendor</code></td><td></td><td>The vendor that the listing belongs to.</td></tr><tr><td><code>seller</code></td><td>object</td><td>(Read-only) Represents the <a href="../../accounts-api/seller/"><code>seller</code></a> object.</td></tr><tr><td><code>priceList</code></td><td>object</td><td>Represents the <a href="../pricelists/"><code>pricelist</code></a> object.</td></tr><tr><td><code>primary</code></td><td>boolean</td><td>Indicates the listing used in the purchase wizard. If the product has multiple associated listings from the same seller, the <code>primary</code> flag identifies which one is selected.</td></tr><tr><td><code>notes</code></td><td>string</td><td>(Optional) The user notes about the listing.</td></tr><tr><td><code>statistics</code></td><td>object</td><td>(Read-only) Represents the <a href="./#listingstatistics"><code>Listing Statistics</code></a> object, containing system-calculated metrics about the listing.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Listing Statistics object <a href="#listingstatistics" id="listingstatistics"></a>

<table><thead><tr><th width="158">Field</th><th width="139">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>subscriptions</code></td><td>integer</td><td>(Read-only) Number of associated subscriptions. </td></tr><tr><td><code>agreements</code></td><td>integer</td><td>(Read-only) Number of associated agreements. </td></tr></tbody></table>

## Listing Eligibility object

<table><thead><tr><th width="158">Field</th><th width="152">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>client</code></td><td>integer</td><td>Indicates direct client.</td></tr><tr><td><code>partner</code></td><td>integer</td><td>Indicates indirect client, also called partners.</td></tr></tbody></table>

## Example

{% code title="LISTING OBJECT" lineNumbers="true" %}
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
  "notes": "This is the primary Listing for the EU region.",
   "eligibility": {
    "client": true,
    "partner": true
  },
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
