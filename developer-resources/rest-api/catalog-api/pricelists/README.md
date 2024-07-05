# Pricelists

## Pricelist object

The `Pricelist` object includes key pricing details such as sales and purchase prices, enabling vendors and operations to effectively manage and apply different price points for product items. This tool is essential for aligning pricing strategies with market and internal financial objectives.

| Field             | Type                | Description                                                                                                                                                                                                                                                                                                                                |
| ----------------- | ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **`id`**          | string              | <p>The business identifier of the Price List. </p><p></p><p>Example: "PRC-1234-5678-9012"</p>                                                                                                                                                                                                                                              |
| **`href`**        | string              | <p>The resource URI of the Price List. </p><p></p><p>Example: "/v1/price-lists/PRC-1234-5678-9012"</p>                                                                                                                                                                                                                                     |
| **`currency`**    | string              | <p>Currency as ISO code. </p><p></p><p>Example: "EUR"</p>                                                                                                                                                                                                                                                                                  |
| **`precision`**   | integer             | <p>Precision of the Price List as number of decimal places. </p><p></p><p>Example: "3"</p>                                                                                                                                                                                                                                                 |
| **`notes`**       | string              | <p>Any user notes about the Price List. </p><p></p><p>Example: "This is the primary Price List for the EU region"</p>                                                                                                                                                                                                                      |
| **`externalIds`** | ExternalIds         | <p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "vendor": "op-322-322",
}
</code></pre>                                                                                                                                                                                                            |
| **`statistics`**  | PriceListStatistics | System calculated metrics about the Price List                                                                                                                                                                                                                                                                                             |
| **`product`**     | Product             | The Product that the Price List belongs to.                                                                                                                                                                                                                                                                                                |
| **`vendor`**      | Account             | The Vendor that the Price List belongs to. Field is visible only for OPS                                                                                                                                                                                                                                                                   |
| **`audit`**       | Audit               | <p>Audit events for the object.</p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { 
    "at": "2023-12-14T17:28:57Z", 
    "by": {
      "id": "UR-1234-1234-1234",
      "name": "John Smith",
      "icon": "/static/users/UR-1234-1234-1234.icon.svg"
    }
}
</code></pre> |

## PriceListStatistics <a href="#priceliststatistics" id="priceliststatistics"></a>

| Field                           | Type    | Description                                                                                        |
| ------------------------------- | ------- | -------------------------------------------------------------------------------------------------- |
| **`sellers`**                   | integer | <p>The number of Sellers that are using this Price List. </p><p></p><p>Example: "10"</p>           |
| **`listings`**                  | integer | <p>The number of Listings that are using this Price List. </p><p></p><p>Example: "12"</p>          |
| **`priceListitems`**            | integer | <p>The total number of pice list Items on the Price List. </p><p></p><p>Example: "23"</p>          |
| **`purchasePriceItems`**        | integer | <p>The number of Items with a populated purchase price. </p><p></p><p>Example: "10"</p>            |
| **`purchasePriceCompleteness`** | decimal | <p>The percentage of Items with a populated purchase price. </p><p></p><p>Example: "0.4347826"</p> |

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
