# Terms

The `Terms` object represents the billing terms for a subscription within the Marketplace. This object contains the following fields:

<table><thead><tr><th width="140">Field</th><th width="122">Type</th><th>Description</th></tr></thead><tbody><tr><td>model</td><td><code>string</code></td><td>The billing model for the subscription. Possible values include <code>one-time</code>, <code>usage</code>, and <code>quantity</code>.</td></tr><tr><td>period</td><td><code>string</code></td><td><p>The billing period applicable to the subscription. Possible values include <code>1m</code>, <code>1y</code>, or <code>one-time</code>.</p><ul><li>1m - indicates monthly billing.</li><li>1y - indicates annual billing.</li><li>one-time - indicates a one-time purchase.</li></ul></td></tr><tr><td>commitment</td><td><code>string</code></td><td><p>The commitment or renewal period for the subscription.</p><ul><li>&#x3C;N>m - N months commitment</li><li>&#x3C;N>y - N years commitment</li></ul></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="TERMS OBJECT" %}
{% code lineNumbers="true" %}
```json
{
  "model": "quantity",
  "period": "1m",
  "commitment": "1y"
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
