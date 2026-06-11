# Terms

The `Terms` object represents the billing terms for a subscription within the Marketplace. This object contains the following fields:

<table><thead><tr><th width="140">Field Name</th><th width="122">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>model</code></td><td>string</td><td>The billing model for the subscription. Allowed values are <code>one-time</code>, <code>usage</code>, <code>quantity</code>.</td></tr><tr><td><code>period</code></td><td>string</td><td><p>The billing period applicable to the subscription. Allowed values are:</p><ul><li><code>1m</code> - indicates monthly billing.</li><li><code>1y</code> - indicates annual billing.</li><li><code>one-time</code> - indicates a one-time purchase.</li></ul></td></tr><tr><td><code>commitment</code></td><td>string</td><td><p>The commitment or renewal period for the subscription.</p><ul><li>&#x3C;N>m - N months commitment</li><li>&#x3C;N>y - N years commitment</li></ul></td></tr></tbody></table>

### Example

{% code lineNumbers="true" %}
```json
{
  "model": "quantity",
  "period": "1m",
  "commitment": "1y"
}
```
{% endcode %}
