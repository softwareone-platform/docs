# Multi-Line Text Options Object

The “Multi-line text” parameter controls text area form when a larger textual value must be captured. The value type is `string`.

<table><thead><tr><th width="169">Field</th><th width="112">Type</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td><code>string</code></td><td><p>Label of a widget. </p><p>Example: Description</p></td></tr><tr><td>placeholderText</td><td><code>string</code></td><td><p>Provides default text within the control when no selection is not made. </p><p>Example: Product extended information</p></td></tr><tr><td>hintText</td><td><code>string</code></td><td><p>Provides help text describing what value is expected in control. </p><p>Example: Add product data</p></td></tr><tr><td>defaultValue</td><td><code>string</code></td><td><p>(optional) Default value. </p><p>Example: Expensive product</p></td></tr><tr><td>minChar</td><td><code>int</code></td><td><p>(optional) Defines minimum length of characters. </p><p>Example: 3</p></td></tr><tr><td>maxChar</td><td><code>int</code></td><td>(optional) Defines maximum length of characters. Example: 100</td></tr></tbody></table>

### Example

{% tabs %}
{% tab title="MULTI LINE TEXT OPTIONS OBJECT" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
  "name": "description",
  "placeholderText": "product description",
  "hintText": "add product data",
  "minChar": 10,
  "maxChar": 20
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

### Value Example <a href="#value-example" id="value-example"></a>

{% code lineNumbers="true" %}
```json
"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.\nDuis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur."
```
{% endcode %}
