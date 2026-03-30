# Pricelist

The Pricelist object includes key pricing details such as sales and purchase prices, enabling vendors and operations to effectively manage and apply different price points for product items. This is essential for aligning pricing strategies with market and internal financial objectives.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="144">Field Name</th><th width="208">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The business identifier of the price list.</p><p>Example: PRC-1234-5678-9012</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>The resource URI of the price list.</p><p>Example: /v1/price-lists/PRC-1234-5678-9012</p></td></tr><tr><td><code>currency</code></td><td>string</td><td><p>The ISO code for the currency.</p><p>Example: EUR</p></td></tr><tr><td><code>precision</code></td><td>integer</td><td><p>Precision of the pricelist as decimal places.</p><p>Example: 3</p></td></tr><tr><td><code>notes</code></td><td>string</td><td><p>The notes about the price list.</p><p>Example: This is the primary price list for the EU region.</p></td></tr><tr><td><code>externalIds</code></td><td>object (<a href="../../common-api-objects/externalids.md"><code>externalIds</code></a>)</td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "vendor": "op-322-322",
}
</code></pre></td></tr><tr><td><code>statistics</code></td><td>object (<a href="./#priceliststatistics"><code>priceListStatistics</code></a>)</td><td>The system calculated metrics about the price list.</td></tr><tr><td><code>product</code></td><td>object</td><td>The <a href="../product/"><code>product</code></a>that the pricelist belongs to.</td></tr><tr><td><code>vendor</code></td><td>object</td><td>The vendor <a href="../../accounts-api/account/">account</a> of the price list. The field is visible only to SoftwareOne Operations.</td></tr><tr><td><code>audit</code></td><td>object</td><td><p>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "created": { 
    "at": "2023-12-14T17:28:57Z", 
    "by": {
      "id": "UR-1234-1234-1234",
      "name": "John Smith",
      "icon": "/static/users/UR-1234-1234-1234.icon.svg"
    }
}
</code></pre></td></tr></tbody></table>

## Pricelist Statistics object <a href="#priceliststatistics" id="priceliststatistics"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="239">Field Name</th><th width="144">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>sellers</code></td><td>integer</td><td><p>The number of sellers that are using this price list.</p><p>Example: 10</p></td></tr><tr><td><code>listings</code></td><td>integer</td><td><p>The number of listings that are using this price list.</p><p>Example: 12</p></td></tr><tr><td><code>priceListitems</code></td><td>integer</td><td><p>The total number of price list Items on the price list.</p><p>Example: 23</p></td></tr><tr><td><code>purchasePriceItems</code></td><td>integer</td><td><p>The number of Items with a populated purchase price.</p><p>Example: 10</p></td></tr><tr><td><code>purchasePriceCompleteness</code></td><td>integer</td><td><p>The percentage of Items with a populated purchase price.</p><p>Example: 0.4347826</p></td></tr></tbody></table>

## Example response

{% code lineNumbers="true" %}
```json
{
  "id": "PRC-1234-5678-9012",
  "currency": "EUR",
  "precision": 3,
  "notes": "This is the primary Price List for the EU region",
  "statistics": {
    "sellers": 10,
    "listings": 12,
    "items": 23,
    "purchasePriceItems": 10,
    "purchasePriceCompleteness": 0.4347826
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
