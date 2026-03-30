# Item Group

The `ItemGroup` object represents a group of items.

<table><thead><tr><th width="199">Field Name</th><th width="185">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The ID of the item group. </p><p>Example: "IGR-6790-8304-0001"</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>A relative reference to object on API (always <code>/products/{product-id}/item-groups/{id}</code>)</p><p>Example: "/products/PRD-6790-8304/item-groups/IGR-6790-8304-0001"</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the group.</p><p>Example: Items</p></td></tr><tr><td><code>label</code></td><td>string</td><td><p>The label displayed in the wizard steps selector.</p><p>Example: Select items</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the group.</p><p>Example: "<code>&#x3C;p>&#x3C;span>Your purchase of Microsoft 365 Online Services comes with SoftwareOne’s best-in-class Digital Workplace Essentials service offering includes. &#x3C;/span>&#x3C;/p>&#x3C;p>&#x3C;br>&#x3C;/p>&#x3C;p>&#x3C;span>In addition to this offering, you can add SoftwareOne’s backup service to your purchase. For more information on this service, click &#x3C;/span>&#x3C;a href="www.google.pl" >&#x3C;span >here&#x3C;/span>&#x3C;/a>&#x3C;span>.&#x3C;/span>&#x3C;/p></code>"</p></td></tr><tr><td><code>displayOrder</code></td><td>integer</td><td><p>Defines the display order of the group.</p><p>Example: 100</p></td></tr><tr><td><code>default</code></td><td>boolean</td><td><p>Marks the default item group.</p><p>Example: true</p></td></tr><tr><td><code>multiple</code></td><td>boolean</td><td><p>Allows multiple selection of items.</p><p>Example: false</p></td></tr><tr><td><code>required</code></td><td>boolean</td><td><p>Requires selection of item in the group.</p><p>Example: true</p></td></tr><tr><td><code>itemCount</code></td><td>integer</td><td><p>The number of items in the group.</p><p>Example: 5</p></td></tr><tr><td><code>product</code></td><td>object</td><td>A reference to the <a href="../product/"><code>product</code> </a>object.</td></tr></tbody></table>

## Example response

{% code lineNumbers="true" %}
```json
{
    "id": "IGR-6790-8304-0001",
    "name": "Items",
    "label": "Select items",
    "description": "<p><span>Your purchase of Microsoft 365 Online Services comes with SoftwareOne’s best-in-class Digital Workplace Essentials service offering includes.",
    "displayOrder": 100,
    "default": true,
    "multipleChoice": false,
    "required": true,
    "product": {
        "id": "PRD-6790-8304-0171"
    }
}
```
{% endcode %}
