# Price List

The Price List object includes key pricing details such as sales and purchase prices, enabling vendors and operations to effectively manage and apply different price points for product items. This is essential for aligning pricing strategies with market and internal financial objectives.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="144">Field</th><th width="160">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The business identifier of the price list.</td></tr><tr><td><code>currency</code></td><td>string, core</td><td>The ISO code for the currency.</td></tr><tr><td><code>precision</code></td><td>integer</td><td>Precision of the pricelist as decimal places.</td></tr><tr><td><code>notes</code></td><td>string</td><td>The notes about the price list.</td></tr><tr><td><code>externalIds</code></td><td>object </td><td>Represents the <a href="../../../api-usage-and-reference/common-api-objects/externalids.md"><code>externalIds</code></a> object.</td></tr><tr><td><code>statistics</code></td><td>object</td><td>(Read-only) Represents the <a href="./#priceliststatistics"><code>priceListStatistics</code></a> object, which contains the system-calculated metrics about the price list.</td></tr><tr><td><code>product</code></td><td>object</td><td>(Read-only) Represents the <a href="../product/"><code>product</code></a> that the pricelist belongs to.</td></tr><tr><td><code>vendor</code></td><td>object</td><td>(Read-only) Represents the vendor <a href="../../accounts-api/account/">account</a> of the price list. The field is visible only to SoftwareOne Operations.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Pricelist Statistics object <a href="#priceliststatistics" id="priceliststatistics"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="243">Field</th><th width="125">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>sellers</code></td><td>integer</td><td>(Read-only) Number of sellers that are using this price list.</td></tr><tr><td><code>listings</code></td><td>integer</td><td>(Read-only) Number of listings that are using this price list.</td></tr><tr><td><code>priceListitems</code></td><td>integer</td><td>(Read-only) Total number of price list Items on the price list.</td></tr><tr><td><code>purchasePriceItems</code></td><td>integer</td><td>(Read-only) Number of Items with a populated purchase price.</td></tr><tr><td><code>purchasePriceCompleteness</code></td><td>integer</td><td>(Read-only) Percentage of Items with a populated purchase price.</td></tr></tbody></table>

## Example

{% code title="PRICE LIST OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "PRC-1234-5678-9012", 
  "currency": "EUR",
  "precision": 3,
  "defaultMarkup": 0.0869,
  "notes": "This is the primary Price List for the EU region",
  "statistics": {
    "sellers": 10,
    "listings": 12,
    "items": 23,
    "purchasePriceItems": 10,
    "purchasePriceCompleteness": 0.4347826,
    "salesPriceItems": 16,
    "salesPriceCompleteness": 0.6956521,
    "averageMarkup": 0.5405,
    "averageMargin": 0.4465
  },
  "product": {
    "id": "PRD-1234-5678"
  },
  "vendor": {
    "id": "ACC-1671-0642"
  }
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
