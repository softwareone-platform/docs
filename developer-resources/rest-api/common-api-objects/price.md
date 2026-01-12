# Price

The `Price` object is a sub-object that represents sales and purchase prices, markup, margin, and other relevant financial data. The visibility of the Price object is determined by the context in which it is included. However, certain fields are always hidden from specific users. For example, clients cannot see purchase prices.&#x20;

<table><thead><tr><th width="145">Field</th><th width="139">Type</th><th></th></tr></thead><tbody><tr><td>PPxY</td><td><code>decimal</code></td><td>The yearly purchase price.</td></tr><tr><td>PPxM</td><td><code>decimal</code></td><td>The monthly purchase price.</td></tr><tr><td>PPx1</td><td><code>decimal</code></td><td>The one-time purchase price.</td></tr><tr><td>unitPP</td><td><code>decimal</code></td><td>The purchase price per unit in base object terms.</td></tr><tr><td>SPxY</td><td><code>decimal</code></td><td>The yearly sales price.</td></tr><tr><td>SPxM</td><td><code>decimal</code></td><td>The monthly sales price.</td></tr><tr><td>SPx1</td><td><code>decimal</code></td><td>The one-time sales price.</td></tr><tr><td>unitSP</td><td><code>decimal</code></td><td>The sales price per unit in base object terms.</td></tr><tr><td>markup</td><td><code>decimal</code></td><td>The markup for the base object, in percent (7.2%)</td></tr><tr><td>margin</td><td><code>decimal</code></td><td>The margin for base object, in percent (5.1%)</td></tr><tr><td>defaultMarkup</td><td><code>decimal</code></td><td>The default markup for base object (subscriptions only), in percent</td></tr><tr><td>currency</td><td><code>string</code></td><td>The currency of the price.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="PRICE OBJECT" %}
{% code lineNumbers="true" %}
```json
{
    "PPxY": 150,
    "PPxM": 12.50,
    "PPx1": 290,
    "SPxY": 165,
    "SPxM": 13.75,
    "SPx1": 300,
    "markup": 10,
    "margin": 9,
    "currency": "USD"
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
