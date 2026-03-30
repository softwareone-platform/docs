# Data Object Options Object

Data object parameters is used for programmatic operations to express complex data object structures.&#x20;

<table><thead><tr><th width="157">Field</th><th width="231">Type</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td><code>string</code></td><td>The label of the widget.</td></tr><tr><td>hintText</td><td><code>string</code></td><td>Provides help text describing what value is expected in control.</td></tr><tr><td>defaultValue</td><td><code>string</code></td><td>Default value.</td></tr><tr><td>objectType</td><td> <code>JSON</code> or <code>XML</code></td><td>The type of the input object.</td></tr></tbody></table>

### Example <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
{
  "name": "Seller address",
  "hintText": "Provide seller address",
  "defaultValue": "Seller",
  "objectType": "JSON"
}
```
{% endcode %}

### Value Example <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
{
  "auth": {
    "token": "the token",
    "signature": "the signature"
  },
  "URI": "https://example.com"
}
```
{% endcode %}
