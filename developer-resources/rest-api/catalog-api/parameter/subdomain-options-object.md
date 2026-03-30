# Subdomain Options Object

The “Subdomain” parameter provides a convenient way for Vendor to ensure data quality.

<table><thead><tr><th width="178">Field</th><th width="125">Type</th><th width="395">Description</th></tr></thead><tbody><tr><td>name</td><td><code>string</code></td><td><p>The label of the widget. </p><p>Example: Your domain</p></td></tr><tr><td>placeholderText</td><td><code>string</code></td><td><p>Provides default text within the control when no input is available. </p><p>Example: Enter your subdomain</p></td></tr><tr><td>domainSuffix</td><td><code>string</code></td><td>Provides a domain part of a subdomain address. Example: <code>onmicrosoft.com</code></td></tr><tr><td>hintText</td><td><code>string</code></td><td>Provides help text describing what value is expected in control. Example: Specify your desired subdomain</td></tr></tbody></table>

### Example <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
{
  "name": "Your domain",
  "placeholderText": "subdomain",
  "hintText": "Specify your desired subdomain",
  "domainSuffix": "onmicrosoft.com"
}
```
{% endcode %}
