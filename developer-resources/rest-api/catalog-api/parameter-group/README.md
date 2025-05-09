# Parameter Group

The Parameter Group object contains the following properties:

<table><thead><tr><th width="197">Field</th><th width="123">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>The identifier for the parameter group. </p><p></p><p>Example: PGR-6790-8304-0001</p></td></tr><tr><td>href</td><td>string</td><td><p>Relative reference to the object in the API. </p><p></p><p>Example: /products/PRD-6790-8304-0171/parameter-groups/PGR-6790-8304-0001</p></td></tr><tr><td>name</td><td>string</td><td><p>Name of the group. </p><p></p><p>Example: Parameters</p></td></tr><tr><td>label</td><td>string</td><td><p>Label displayed in the wizard steps selector. </p><p></p><p>Example: Create agreement</p></td></tr><tr><td>description</td><td>string</td><td><p>Description of the group. </p><p></p><p>Example: When creating a new agreement with SoftwareOne, you can establish a new Microsoft account or connect your existing account.</p></td></tr><tr><td>displayOrder</td><td>integer</td><td><p>Defines the display order. </p><p></p><p>Example: 100</p></td></tr><tr><td>default</td><td>boolean</td><td><p>Marks the default item group. </p><p></p><p>Example: true</p></td></tr><tr><td>parameterCount</td><td>integer</td><td><p>Number of parameters in the group. </p><p></p><p>Example: 5</p></td></tr><tr><td>product</td><td><a href="../product/">Product</a></td><td>Reference to the <a href="../product/">Product </a>object. </td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="PARAMETER GROUP OBJECT" %}
{% code overflow="wrap" %}
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
{% endtab %}
{% endtabs %}
