# Single Line Text Options Object

The “Single-line text” parameter is the usual input field supported with the standard constraints which are optional by default. The value type is `string`.

<table><thead><tr><th width="186">Field</th><th width="155">Type</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td><code>string</code></td><td><p>Label of a widget. </p><p>Example: Segment</p></td></tr><tr><td>placeholderText</td><td><code>string</code></td><td><p>Provides default text within the control when no selection is not made. </p><p>Example: Commercial</p></td></tr><tr><td>hintText</td><td><code>string</code></td><td><p>Provides help text describing what value is expected in control. </p><p>Example: Define segment value</p></td></tr><tr><td>defaultValue</td><td><code>string</code></td><td><p>(optional) Default value. </p><p>Example: Commercial</p></td></tr><tr><td>minChar</td><td><code>int</code></td><td>(optional) Defines minimum length of characters. Example: 3</td></tr><tr><td>maxChar</td><td><code>int</code></td><td>(optional) Defines maximum length of characters. Example: 100</td></tr><tr><td>pattern</td><td><code>string</code></td><td><p>(optional) RegEx pattern to be validated against provided value. </p><p>Example: \w+00</p></td></tr></tbody></table>

### Example

{% tabs %}
{% tab title="SINGLE LINE TEXT OPTIONS OBJECT" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
  "name": "Segment",
  "placeholderText": "Specify segment",
  "hintText": "Commercial",
  "minChar": 10,
  "maxChar": 20,
  "pattern": "[A-Za-z]*"
  "defaultValue": "def"
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

### Value Example <a href="#value-example" id="value-example"></a>

{% code lineNumbers="true" %}
```json
"Medical Segment"
```
{% endcode %}
