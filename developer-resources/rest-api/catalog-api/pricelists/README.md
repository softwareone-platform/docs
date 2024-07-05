# Pricelists

## Pricelist object

The `Pricelist` object includes key pricing details such as sales and purchase prices, enabling vendors and operations to effectively manage and apply different price points for product items. This tool is essential for aligning pricing strategies with market and internal financial objectives.

<table><thead><tr><th width="214">Field</th><th width="204">Type</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p>The business identifier of the Price List. </p><p></p><p>Example: "PRC-1234-5678-9012"</p></td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td><p>The resource URI of the Price List. </p><p></p><p>Example: "/v1/price-lists/PRC-1234-5678-9012"</p></td></tr><tr><td><strong><code>currency</code></strong></td><td>string</td><td><p>Currency as ISO code. </p><p></p><p>Example: "EUR"</p></td></tr><tr><td><strong><code>precision</code></strong></td><td>integer</td><td><p>Precision of the Price List as number of decimal places. </p><p></p><p>Example: "3"</p></td></tr><tr><td><strong><code>notes</code></strong></td><td>string</td><td><p>Any user notes about the Price List. </p><p></p><p>Example: "This is the primary Price List for the EU region"</p></td></tr><tr><td><strong><code>externalIds</code></strong></td><td>ExternalIds</td><td><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "vendor": "op-322-322",
}
</code></pre></td></tr><tr><td><strong><code>statistics</code></strong></td><td>PriceListStatistics</td><td>System calculated metrics about the Price List</td></tr><tr><td><strong><code>product</code></strong></td><td>Product</td><td>The Product that the Price List belongs to.</td></tr><tr><td><strong><code>vendor</code></strong></td><td>Account</td><td>The Vendor that the Price List belongs to. The field is visible only for OPS</td></tr><tr><td><strong><code>audit</code></strong></td><td>Audit</td><td><p>Audit events for the object.</p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
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

<table><thead><tr><th width="321">Field</th><th width="144">Type</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>sellers</code></strong></td><td>integer</td><td><p>The number of Sellers that are using this Price List. </p><p></p><p>Example: "10"</p></td></tr><tr><td><strong><code>listings</code></strong></td><td>integer</td><td><p>The number of Listings that are using this Price List. </p><p></p><p>Example: "12"</p></td></tr><tr><td><strong><code>priceListitems</code></strong></td><td>integer</td><td><p>The total number of pice list Items on the Price List. </p><p></p><p>Example: "23"</p></td></tr><tr><td><strong><code>purchasePriceItems</code></strong></td><td>integer</td><td><p>The number of Items with a populated purchase price. </p><p></p><p>Example: "10"</p></td></tr><tr><td><strong><code>purchasePriceCompleteness</code></strong></td><td>decimal</td><td><p>The percentage of Items with a populated purchase price. </p><p></p><p>Example: "0.4347826"</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="PRICE LIST OBJECT" %}
```json
{
  "id": "PRC-1234-5678-9012",
  "href": "/v1/price-lists/PRC-1234-5678-9012",
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
{% endtab %}
{% endtabs %}
