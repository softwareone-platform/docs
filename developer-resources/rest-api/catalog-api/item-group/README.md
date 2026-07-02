# Item Group

The ItemGroup object represents a group of items.

<table data-search="false"><thead><tr><th width="187">Field</th><th width="164">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The ID of the item group. </td></tr><tr><td><code>name</code></td><td>string, core</td><td>The name of the group.</td></tr><tr><td><code>label</code></td><td>string</td><td>The label that is displayed in the wizard steps selector.</td></tr><tr><td><code>description</code></td><td>string</td><td>A description of the group.</td></tr><tr><td><code>displayOrder</code></td><td>integer</td><td>Defines the display order of the group.</td></tr><tr><td><code>default</code></td><td>boolean</td><td>Marks the default item group.</td></tr><tr><td><code>multiple</code></td><td>boolean</td><td>Allows multiple selection of items.</td></tr><tr><td><code>required</code></td><td>boolean</td><td>Requires the selection of an item in the group.</td></tr><tr><td><code>itemCount</code></td><td>integer</td><td>(Read-only) Number of items in the group.</td></tr><tr><td><code>product</code></td><td>object</td><td>Represents the <a href="../product/"><code>product</code> </a>object.</td></tr></tbody></table>

## Example

{% code title="ITEM GROUP OBJECT" overflow="wrap" lineNumbers="true" %}
```json
	{
	    "id": "IGR-6790-8304-0001",
	    "name": "Items",
	    "label": "Select items",
	    "description": "<p><span>Your purchase of Microsoft 365 Online Services comes with SoftwareOne’s best-in-class Digital Workplace Essentials service offering.",
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
