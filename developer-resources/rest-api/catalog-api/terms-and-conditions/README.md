# Terms

The Terms object represents terms as a collection of uploaded PDF or DOCX documents or links to externally hosted documents as an element of a product.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="172">Field</th><th width="147">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The identifier for the terms.</td></tr><tr><td><code>name</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>The name for the terms.</td></tr><tr><td><code>description</code></td><td>string, core</td><td>A description of the terms.</td></tr><tr><td><code>displayOrder</code></td><td>integer, core</td><td>The display order for the terms.</td></tr><tr><td><code>status</code></td><td>string, core</td><td>The status of the terms. </td></tr><tr><td><code>product</code></td><td>object</td><td>Represents the <a href="../product/"><code>product</code></a> to which the item is assigned.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Example

{% code title="TERMS OBJECT" overflow="wrap" %}
```json
{
  "id": "TCS-3159-1891-0980-8679",  
  "name": "Microsoft 365 Terms of Service",
  "description": "Description of Microsoft 365 Terms of Service",
  "displayOrder": 100,
  "state": "Draft",
  "product": {
    "id": "PRD-6822-9898-4256",
    "href": "/products/PRD-6822-9898-4256",
    "name": "Microsoft 365 online services for commercial"
  },
  "audit": {
    "created": {
      "at": "2024-01-16T21:30:13.1046031",
      "by": {
        "id": "USR-0000-0001"
      }
    },
    "updated": null
  }
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
