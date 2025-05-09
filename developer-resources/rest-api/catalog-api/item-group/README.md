---
hidden: true
---

# Item Group

## Item Group object

The `ItemGroup` object represents a group of items.

<table><thead><tr><th width="199">Field</th><th width="185">Type</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p>Platform generated ID. </p><p></p><p>Example: "IGR-6790-8304-0001"</p></td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td><p>Relative reference to object on API (always <code>/products/{product-id}/item-groups/{id}</code>). </p><p></p><p>Example: "/products/PRD-6790-8304/item-groups/IGR-6790-8304-0001"</p></td></tr><tr><td><strong><code>name</code></strong></td><td>string</td><td><p>Name of the group. </p><p></p><p>Example: "Items"</p></td></tr><tr><td><strong><code>label</code></strong></td><td>string</td><td><p>Label displayed in the wizard steps selector. </p><p></p><p>Example: "Select items"</p></td></tr><tr><td><strong><code>description</code></strong></td><td>string</td><td><p>Description of the group. </p><p></p><p>Example: "&#x3C;p>&#x3C;span>Your purchase of Microsoft 365 Online Services comes with SoftwareOne’s best-in-class Digital Workplace Essentials service offering includes. &#x3C;/span>&#x3C;/p>&#x3C;p>&#x3C;br>&#x3C;/p>&#x3C;p>&#x3C;span>In addition to this offering, you can add SoftwareOne’s backup service to your purchase. For more information on this service, click &#x3C;/span>&#x3C;a href="www.google.pl" >&#x3C;span >here&#x3C;/span>&#x3C;/a>&#x3C;span>.&#x3C;/span>&#x3C;/p>"</p></td></tr><tr><td><strong><code>displayOrder</code></strong></td><td>integer</td><td><p>Defines the display order of the group. </p><p></p><p>Example: "100"</p></td></tr><tr><td><strong><code>default</code></strong></td><td>boolean</td><td><p>Marks the default item group. </p><p></p><p>Example: "true"</p></td></tr><tr><td><strong><code>multiple</code></strong></td><td>boolean</td><td><p>Allows multiple selection of items. </p><p></p><p>Example: "false"</p></td></tr><tr><td><strong><code>required</code></strong></td><td>boolean</td><td><p>Requires selection of item in the group. </p><p></p><p>Example: "true"</p></td></tr><tr><td><strong><code>itemCount</code></strong></td><td>integer</td><td><p>The number of items in the group. </p><p></p><p>Example: "5"</p></td></tr><tr><td><strong><code>product</code></strong></td><td><a href="../product/">Product</a></td><td>Reference to <a href="../product/">Product </a>object. </td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="ITEM OBJECT GROUP" %}
```json
{
    "id": "IGR-6790-8304-0001",
    "name": "Items",
    "label": "Select items",
    "description": "<p><span>Your purchase of Microsoft 365 Online Services comes with SoftwareOne’s best-in-class Digital Workplace Essentials service offering includes. </span></p><p><br></p><p><span>In addition to this offering, you can add SoftwareOne’s backup service to your purchase. For more information on this service, click </span><a href="www.google.pl" ><span >here</span></a><span>.</span></p>",
    "displayOrder": 100,
    "default": true,
    "multipleChoice": false,
    "required": true,
    "product": {
        "id": "PRD-6790-8304-0171"
    }
}
```
{% endtab %}
{% endtabs %}
