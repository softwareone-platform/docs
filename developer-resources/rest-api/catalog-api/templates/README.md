# Template

The Template object provides functionality for templates to be made and automatically delivered once a set of rules based on type is met. This enables the client to know what is happening with their order and if anything is needed of them.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="120">Field</th><th width="129">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The template's ID.</td></tr><tr><td><code>name</code></td><td>string</td><td>The name of the template.</td></tr><tr><td><code>type</code></td><td>string</td><td>The type of template.</td></tr><tr><td><code>content</code></td><td>string</td><td>The content of the template.</td></tr><tr><td><code>default</code></td><td>boolean</td><td><ul><li>Each product has 4 defaults automatically generated upon product creation (against each status).</li><li>Each template automatically created has a default system message that the client account will need to update.</li><li>The default cannot be deleted, but non-default can be deleted.</li></ul></td></tr><tr><td><code>product</code></td><td>object</td><td>Represents the <a href="../product/"><code>product</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Example

{% code title="TEMPLATE OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "TPL-1234-5678-0001",
  "name": "Thank you for your interest",
  "type": "RequestProcessing",
  "content": "We are delighted that you have contacted us at SoftwareOne. Your interest in Microsoft 365 Online Services product is greatly valued, and we are here to provide all the support you need. Our dedicated team is actively working on your query, and we are committed to responding within 24 hours. \n Thank you!!!",
  "isDefault": true,
  "product": {
    "id": "PRD-1234-5678-0001"
  },
  "externalIds": {
    "vendor": "op-322-322",
  }
}
```
{% endcode %}
