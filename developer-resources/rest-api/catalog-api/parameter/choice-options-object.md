# Choice Options Object

The “Choice” parameter represents either a radio button control (single choice) on the form. It is used when one selection must be made only. If multiple selections can or need to be made the better option is to use the “Checkbox” parameter.

The value type is `string`.

<table><thead><tr><th width="163"></th><th width="177"></th><th></th></tr></thead><tbody><tr><td>name</td><td><code>string</code></td><td><p>Label of the widget. </p><p>Example: Which service you are interested in?</p></td></tr><tr><td>hintText</td><td><code>string</code></td><td><p>Provides help text describing what value is expected in control. </p><p>Example: Select one value</p></td></tr><tr><td>optionsList</td><td><code>selectionOption</code></td><td><p>Effectively a data source for the parameter options</p><p>component provides drag and drop functionality to determine the ordering of options. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "label": "Microsoft Office 365",
    "description": "Office 365 product",
    "value": "MsOffice365"
  },
  {
    "label": "Dynamics 365",
    "value": "Dynam365"
  },
  {
    "label": "Windows 11"
    "description": "Latest Windows 11",
    "value": "Win11x64"
  }
]
</code></pre></td></tr><tr><td>defaultValue</td><td><code>string</code></td><td><p>Used to mark default selection if needed (one selection only). </p><p>Example: Win11x64</p></td></tr></tbody></table>

### Example <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
{
  "name": "Which service you are interested in?",
  "hintText": "Select one value",
  "optionsList": [
    {
      "label": "Microsoft Office 365",
      "description": "Office 365 product",
      "value": "MsOffice365"
    },
    {
      "label": "Dynamics 365",
      "value": "Dynam365"
    },
    {
      "label": "Windows 11",
      "description": "Latest Windows 11",
      "value": "Win11x64"
    }
  ],
  "defaultValue": "Dynam365"
}
```
{% endcode %}

### Value Example <a href="#value-example" id="value-example"></a>

{% code lineNumbers="true" %}
```json
"Dynam365"
```
{% endcode %}
