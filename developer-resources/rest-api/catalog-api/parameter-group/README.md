# Parameter Groups

The Parameter Group object contains the following properties:

<table><thead><tr><th width="169">Field</th><th width="123">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The identifier for the parameter group.</p><p>Example: PGR-6790-8304-0001</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>Relative reference to the object in the API.</p><p>Example: /products/PRD-6790-8304-0171/parameter-groups/PGR-6790-8304-0001</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the group.</p><p>Example: Parameters</p></td></tr><tr><td>label</td><td><code>string</code></td><td><p>The label displayed in the wizard steps selector.</p><p>Example: Create agreement</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>A description of the group.</p><p>Example: When creating a new agreement with SoftwareOne, you can establish a new Microsoft account or connect your existing account.</p></td></tr><tr><td>displayOrder</td><td><code>integer</code></td><td><p>Defines the display order.</p><p>Example: 100</p></td></tr><tr><td>default</td><td><code>boolean</code></td><td><p>Marks the default item group.</p><p>Example: true</p></td></tr><tr><td>parameterCount</td><td><code>integer</code></td><td><p>Number of parameters in the group.</p><p>Example: 5</p></td></tr><tr><td>product</td><td><a href="../product/"><code>product</code></a></td><td>Reference to the Product object.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="PARAMETER GROUP OBJECT" %}
{% code overflow="wrap" lineNumbers="true" %}
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
