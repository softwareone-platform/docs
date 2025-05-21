# Terms

The Terms object represents billing terms for subscriptions.

<table><thead><tr><th width="140">Field</th><th width="122">Type</th><th>Description</th></tr></thead><tbody><tr><td>period</td><td><code>string</code></td><td><p>The billing period for the subscription.</p><ul><li>1m - monthly billing</li><li>1y - annual billing</li><li>one-time - one time purchase</li></ul></td></tr><tr><td>commitment</td><td><code>string</code></td><td><p>The commitment period (renewal period) for the subscription.</p><ul><li>&#x3C;N>m - N months commitment</li><li>&#x3C;N>y - N years commitment</li></ul></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="TERMS OBJECT" %}
{% code lineNumbers="true" %}
```json
{
  "period": "1m",
  "commitment": "1y"
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
