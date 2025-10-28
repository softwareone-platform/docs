# Pricelists

The Pricelist object includes key pricing details such as sales and purchase prices, enabling vendors and operations to effectively manage and apply different price points for product items. This is essential for aligning pricing strategies with market and internal financial objectives.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="144">Field</th><th width="193">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The business identifier of the price list.</p><p>Example: PRC-1234-5678-9012</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>The resource URI of the price list.</p><p>Example: /v1/price-lists/PRC-1234-5678-9012</p></td></tr><tr><td>currency</td><td><code>string</code></td><td><p>The ISO code for the currency.</p><p>Example: EUR</p></td></tr><tr><td>precision</td><td><code>integer</code></td><td><p>Precision of the pricelist as decimal places.</p><p>Example: 3</p></td></tr><tr><td>notes</td><td><code>string</code></td><td><p>The notes about the price list.</p><p>Example: This is the primary price list for the EU region.</p></td></tr><tr><td>externalIds</td><td><a href="../../common-api-objects/externalids.md"><code>externalIds</code></a></td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "vendor": "op-322-322",
}
</code></pre></td></tr><tr><td>statistics</td><td><code>priceListStatistics</code></td><td>The system calculated metrics about the price list.</td></tr><tr><td>product</td><td><a href="../product/"><code>product</code></a></td><td>The product that the pricelist belongs to.</td></tr><tr><td>vendor</td><td><a href="../../accounts-api/account/">account</a></td><td>The vendor of the price list. The field is visible only to SoftwareOne Operations.</td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td><p>A reference to the Audit object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "created": { 
    "at": "2023-12-14T17:28:57Z", 
    "by": {
      "id": "UR-1234-1234-1234",
      "name": "John Smith",
      "icon": "/static/users/UR-1234-1234-1234.icon.svg"
    }
}
</code></pre></td></tr></tbody></table>

## PriceListStatistics <a href="#priceliststatistics" id="priceliststatistics"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="239">Field</th><th width="123">Type</th><th>Description</th></tr></thead><tbody><tr><td>sellers</td><td><code>integer</code></td><td><p>The number of Sellers that are using this Price List.</p><p>Example: 10</p></td></tr><tr><td>listings</td><td><code>integer</code></td><td><p>The number of Listings that are using this Price List.</p><p>Example: 12</p></td></tr><tr><td>priceListitems</td><td><code>integer</code></td><td><p>The total number of pricelist Items on the Price List.</p><p>Example: 23</p></td></tr><tr><td>purchasePriceItems</td><td><code>integer</code></td><td><p>The number of Items with a populated purchase price.</p><p>Example: 10</p></td></tr><tr><td>purchasePriceCompleteness</td><td><code>integer</code></td><td><p>The percentage of Items with a populated purchase price.</p><p>Example: 0.4347826</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="PRICE LIST OBJECT" %}
{% code overflow="wrap" lineNumbers="true" %}
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
{% endtab %}
{% endtabs %}
