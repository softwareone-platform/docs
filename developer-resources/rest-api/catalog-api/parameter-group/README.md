# Parameter Group

## Parameter Group object

<table><thead><tr><th width="200">Field</th><th width="187">Type</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p>Platform </p><p>generated ID. </p><p></p><p>Example: "PGR-6790-8304-0001"</p></td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td><p>Relative reference to object on API (always <code>/products/{product-id}/parameter-groups/{id}</code>). </p><p></p><p>Example: "/products/PRD-6790-8304-0171/parameter-groups/PGR-6790-8304-0001"</p></td></tr><tr><td><strong><code>name</code></strong></td><td>string</td><td><p>Name of the group. </p><p></p><p>Example: "Parameters"</p></td></tr><tr><td><strong><code>label</code></strong></td><td>string</td><td><p>Label displayed in the wizard steps selector. </p><p></p><p>Example: "Create agreement"</p></td></tr><tr><td><strong><code>description</code></strong></td><td>string</td><td><p>Description of the group. </p><p></p><p>Example: "When creating a new agreement with SoftwareOne, you have the option to establish a new Microsoft account or connect it to an existing account you already hold with Microsoft."</p></td></tr><tr><td><strong><code>displayOrder</code></strong></td><td>integer</td><td><p>Defines the display order. </p><p></p><p>Example: "100"</p></td></tr><tr><td><strong><code>default</code></strong></td><td>boolean</td><td><p>Marks the default item group. </p><p></p><p>Example: "true"</p></td></tr><tr><td><strong><code>parameterCount</code></strong></td><td>integer</td><td><p>The number of parameters in the group. </p><p></p><p>Example: "5"</p></td></tr><tr><td><strong><code>product</code></strong></td><td><a href="../product/">Product</a></td><td>Reference to <a href="../product/">Product </a>object. </td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="PARAMETER GROUP OBJECT" %}
```json
{
    "id": "PGR-6790-8304-0001",
    "href": "/products/PRD-6790-8304/parameter-groups/PGR-6790-8304-0001",
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
{% endtab %}
{% endtabs %}
