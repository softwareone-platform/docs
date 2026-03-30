# Checkbox Options Object

The “Checkbox” parameter represents a checkbox control (multi-choice) on the form. It is usually used when a user needs or wants to select multiple objects. All options are required to be present on the screen at the same time, if this is not required better option is to use the “Dropdown” parameter.

The value type is `object`.

<table><thead><tr><th width="137">Field</th><th width="167">Type</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td><code>string</code></td><td><p>Label of a widget. </p><p>Example: Segment</p></td></tr><tr><td>hintText</td><td><code>string</code></td><td><p>Provides help text describing what value is expected in control. </p><p>Example: Define segment value</p></td></tr><tr><td>optionsList</td><td><code>selectionOption</code></td><td><p>Effectively a data source for the parameter options</p><p>component provides drag and drop functionality to determine the ordering of options. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "label": "None",
    "value": "none"
  },
  {
    "label": "Seller address",
    "value": "sellerAddress"
  },
  {
    "label": "Buyer address",
    "value": "buyerAddress"
  }
]
</code></pre></td></tr><tr><td>defaultValue</td><td><code>string</code></td><td><p>(optional) Used to mark default selection if needed (supports multi-selection). </p><p>Example: [“sellerAddress”]</p></td></tr></tbody></table>

### Example <a href="#options-example" id="options-example"></a>

{% code lineNumbers="true" %}
```json
{
  "name": "Select items",
  "hintText": "Pick all the items you want",
  "optionsList": [
    {
      "label": "Microsoft Office 365",
      "value": "ms_office_365"
    },
    {
      "label": "Microsoft Dynamycs",
      "value": "dynamics"
    },
    {
      "label": "Other Products",
      "value": "products"
    }
  ]
}
```
{% endcode %}

### Value Fields <a href="#value-fields" id="value-fields"></a>

<table><thead><tr><th width="132">Field</th><th width="165">Type</th><th>Description</th><th data-hidden></th></tr></thead><tbody><tr><td>[]</td><td>string</td><td><p>List of selected checkbox values. </p><p>Example: my val3</p></td><td>my val3</td></tr></tbody></table>

### Example <a href="#options-example" id="options-example"></a>

{% code lineNumbers="true" %}
```json
[
  "dynamics",
  "products"
]
```
{% endcode %}
