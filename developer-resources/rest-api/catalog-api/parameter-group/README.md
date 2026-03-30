# Parameter Group

The Parameter Group object contains the following properties:

<table><thead><tr><th width="169">Field Name</th><th width="123">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The identifier for the parameter group.</p><p>Example: PGR-6790-8304-0001</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>A relative reference to the object in the API.</p><p>Example: /products/PRD-6790-8304-0171/parameter-groups/PGR-6790-8304-0001</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the group.</p><p>Example: Parameters</p></td></tr><tr><td><code>label</code></td><td>string</td><td><p>The label displayed in the wizard steps selector.</p><p>Example: Create agreement</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the group.</p><p>Example: When creating a new agreement with SoftwareOne, you can establish a new Microsoft account or connect your existing account.</p></td></tr><tr><td><code>displayOrder</code></td><td>integer</td><td><p>Defines the display order.</p><p>Example: 100</p></td></tr><tr><td><code>default</code></td><td>boolean</td><td><p>Marks the default item group.</p><p>Example: true</p></td></tr><tr><td><code>parameterCount</code></td><td>integer</td><td><p>Number of parameters in the group.</p><p>Example: 5</p></td></tr><tr><td><code>product</code></td><td>object</td><td>Reference to the <a href="../product/"><code>product</code></a> object.</td></tr></tbody></table>

## Example response

{% code lineNumbers="true" %}
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
