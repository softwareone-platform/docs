# Price List Item

The Pricelist Item object represents pricing information for a particular Product Item.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="197">Field</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The business identifier of the price list Item. </td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the pricelist item. Allowed values: <code>draft</code> or  <code>private</code> (can be used in subscription, but not for sale), or <code>forSale</code> (available for assignment on a subscription and sale).</td></tr><tr><td><code>description</code></td><td>string</td><td>A description of the price list item.</td></tr><tr><td><code>reasonForChange</code></td><td>string</td><td>OPS‑only field indicating the reason for a change. </td></tr><tr><td><code>info</code></td><td>object</td><td>Represents the <a href="./#priceinfo-object"><code>PriceInfo</code></a> object, , which enables or disables the display of price information and its associated text.</td></tr><tr><td><code>unitLP</code></td><td>decimal</td><td>The unit list price of the product item, also known as the Manufacturer's Suggested Retail Price. Only SoftwareOne operations or vendors can edit the field. Clients can see the field in the Marketplace, but cannot edit it. </td></tr><tr><td><code>unitPP</code></td><td>decimal</td><td>The unit purchase price of the product item. Only SoftwareOne operations or vendors can see the field. </td></tr><tr><td><code>markup</code></td><td>decimal</td><td>The markup that has been applied to the item price. Optional on request: if omitted, the price list default markup is used. Only SoftwareOne Operations can view the field. </td></tr><tr><td><code>margin</code></td><td>decimal</td><td>(Read-only) The margin of the item price, calculated from the purchase price and the markup. Only SoftwareOne operations can view the field.  </td></tr><tr><td><code>unitSP</code></td><td>decimal</td><td>(Read-only) The unit sales price of the product item, calculated from the purchase price and the markup. Only SoftwareOne operations and clients can view the field.  </td></tr><tr><td><code>PPx1</code></td><td>decimal</td><td>(Read-only) The purchase price. Only SoftwareOne operations and vendors can view the field. </td></tr><tr><td><code>PPxM</code></td><td>decimal</td><td>(Read-only) The purchase price per month. Only SoftwareOne operations and vendors can view the field. </td></tr><tr><td><code>PPxY</code></td><td>decimal</td><td>(Read-only) The purchase price per year. Only SoftwareOne operations and vendors can view the field. </td></tr><tr><td><code>SPx1</code></td><td>decimal</td><td>(Read-only) The sales price. Only SoftwareOne operations and clients can view the field. </td></tr><tr><td><code>SPxM</code></td><td>decimal</td><td>(Read-only) The sales price value per month. Only SoftwareOne operations and clients can view the field. </td></tr><tr><td><code>SPxY</code></td><td>decimal</td><td>(Read-only) The sales price per year. Only SoftwareOne operations and clients can view the field. </td></tr><tr><td><code>LPx1</code></td><td>decimal</td><td>(Read-only) The estimated list price value per. Only SoftwareOne Operations and Clients can view the field. </td></tr><tr><td><code>LPxM</code></td><td>decimal</td><td>(Read-only) The estimated list price per month. Only SoftwareOne operations and clients can view the field.</td></tr><tr><td><code>LPxY</code></td><td>decimal</td><td>(Read-only) The estimated list price per year. Only SoftwareOne operations and clients can view the field. </td></tr><tr><td><code>priceList</code></td><td>object</td><td>(Read-only) Represents the <a href="../pricelists/"><code>priceList</code></a> that this item belongs to.</td></tr><tr><td><code>item</code></td><td>object</td><td>(Read-only) Represents the <a href="../items/"><code>item</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Price Info object

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="172">Field</th><th width="125">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>visible</code></td><td>boolean</td><td></td></tr><tr><td><code>description</code></td><td>string</td><td>Appears as the title on the request wizard.</td></tr></tbody></table>

## Example

{% code title="PRICE LIST ITEM OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "PRI-1234-5678-9012-0001",
  "status": "ForSale",
  "description": "Sample description",
  "reasonForChange": "Example Reason For Change",
  "priceInfo": {
    "enabled": "true",
    "description": "This is the description as to why the item costs this much."
  },
  "unitLP": 39.95,
  "unitPP": 19.95,
  "markup": 0.5013,
  "margin": 0.3339,
  "unitSP": 29.95,
  "PPx1": 3.00,
  "PPxM": 19.95,
  "PPxY": 239.40,
  "PPx3Y": 718.20,
  "SPx1": 3.45,
  "SPxM": 29.95,
  "SPxY": 359.40,
  "SPx3Y": 1078.2,
  "LPx1": 1.15,
  "LPxM": 10.55,
  "LPxY": 150.05,
  "LPx3Y": 450.15,
  "priceList": {
    "id": "PRC-1234-5678-9012"
  },
  "item": {
    "id": "ITM-1234-5678-0001"
  }
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
