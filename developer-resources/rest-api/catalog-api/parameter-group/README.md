# Parameter Group

The Parameter Group object contains the following properties:

<table><thead><tr><th width="185">Field</th><th width="147">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The identifier for the parameter group.</td></tr><tr><td><code>name</code></td><td>string, core</td><td>The name of the group.</td></tr><tr><td><code>label</code></td><td>string</td><td>The label displayed in the wizard steps selector.</td></tr><tr><td><code>description</code></td><td>string</td><td>A description of the group.</td></tr><tr><td><code>displayOrder</code></td><td>integer</td><td>Defines the display order.</td></tr><tr><td><code>default</code></td><td>boolean</td><td>Marks the default item group.</td></tr><tr><td><code>parameterCount</code></td><td>integer</td><td>(Read-only)Number of parameters in the group.</td></tr><tr><td><code>product</code></td><td>object</td><td>Represents the <a href="../product/"><code>product</code></a> object.</td></tr></tbody></table>

## Example

{% code title="PARAMETER GROUP OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
    "id": "PGR-6790-8304-0001",   
    "title": "Parameters",
    "label": "Create agreement",
    "description": "When creating a new agreement with SoftwareOne, you have the option to establish a new Microsoft account or connect it to an existing account you already hold with Microsoft.",
    "displayOrder": 100,
    "default": true,
    "product": {
        "id": "PRD-6790-8304-0171"
    }
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
