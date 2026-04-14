# Price

The `Price` object is a sub-object that represents sales and purchase prices, markup, margin, and other relevant financial data. The visibility of the Price object is determined by the context in which it is included. However, certain fields are always hidden from specific users. For example, clients cannot see purchase prices.&#x20;

<table><thead><tr><th width="145">Field Name</th><th width="139">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>PPxY</code></td><td>decimal</td><td>The yearly purchase price.</td></tr><tr><td><code>PPxM</code></td><td>decimal</td><td>The monthly purchase price.</td></tr><tr><td><code>PPx1</code></td><td>decimal</td><td>The one-time purchase price.</td></tr><tr><td><code>unitPP</code></td><td>decimal</td><td>The purchase price per unit in base object terms.</td></tr><tr><td><code>SPxY</code></td><td>decimal</td><td>The yearly sales price.</td></tr><tr><td><code>SPxM</code></td><td>decimal</td><td>The monthly sales price.</td></tr><tr><td><code>SPx1</code></td><td>decimal</td><td>The one-time sales price.</td></tr><tr><td><code>unitSP</code></td><td>decimal</td><td>The sales price per unit in base object terms.</td></tr><tr><td><code>markup</code></td><td>decimal</td><td>The markup for the base object, in percent (7.2%)</td></tr><tr><td><code>margin</code></td><td>decimal</td><td>The margin for base object, in percent (5.1%)</td></tr><tr><td><code>defaultMarkup</code></td><td>decimal</td><td>The default markup for base object (subscriptions only), in percent</td></tr><tr><td><code>currency</code></td><td>string</td><td>The currency of the price.</td></tr></tbody></table>

### Example

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
