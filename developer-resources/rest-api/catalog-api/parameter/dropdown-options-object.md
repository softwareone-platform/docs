# Dropdown Options Object

The “Dropdown” parameter is another “choice” type parameter but confined to a single form element.

<table><thead><tr><th width="173">Field</th><th width="176">Type</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td><code>string</code></td><td><p>Label of the widget. </p><p>Example: Segment</p></td></tr><tr><td>hintText</td><td><code>string</code></td><td><p>Provides help text describing what value is expected in control. </p><p>Example: Define segment value</p></td></tr><tr><td>placeholderText</td><td><code>string</code></td><td><p>(optional) Provides default text within the control when no selection is not made. </p><p>Example: Commercial</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>(optional) Provides description for the drop down component. </p><p>Example: Define segment value</p></td></tr><tr><td>optionsList</td><td><code>selectionOption</code></td><td><p>Effectively a data source for the parameter options</p><p>component provides drag and drop functionality to determine the ordering of options. </p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "label": "Microsoft Office 365",
    "value": "MsOffice365"
  },
  {
    "label": "Dynamics 365",
    "value": "Dynam365"
  },
  {
    "label": "Windows 11"
    "value": "Win11x64"
  }
]
</code></pre></td></tr><tr><td>defaultValue</td><td><code>string</code></td><td><p>(optional) used to mark default selection if needed (one selection only). </p><p>Example: Win11x64</p></td></tr></tbody></table>

### Example <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
{
  "name": "Which service you are interested in?",
  "hintText": "Select one value",
  "description": "Select interested service",
  "placeholderText": "Select your choice"
  "optionsList": [
    {
      "label": "Microsoft Office 365",
      "value": "MsOffice365"
    },
    {
      "label": "Dynamics 365",
      "value": "Dynam365"
    },
    {
      "label": "Windows 11"
      "value": "Win11x64"
    }
  ],
  "defaultValue": "Dynam365"
}
```
{% endcode %}
