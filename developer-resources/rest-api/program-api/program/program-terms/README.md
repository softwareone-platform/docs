# Program Terms

The Program Terms object represents terms in the form of uploaded PDF or DOCX documents, as well as links to documents hosted externally.&#x20;

{% include "../../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="151">Field</th><th width="161">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The business identifier of the terms. </td></tr><tr><td><code>href</code></td><td>string</td><td>(Read-only) The resource URI of the terms. </td></tr><tr><td><code>name</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>The name of the terms. </td></tr><tr><td><code>description</code></td><td>string, core</td><td>A description of the terms. </td></tr><tr><td><code>displayOrder</code></td><td>integer, core</td><td>The display order of the terms. </td></tr><tr><td><code>status</code></td><td>string, core</td><td><p>The status of the terms. Allowed values are:</p><ul><li><code>Draft</code></li><li><code>Published</code></li><li><code>Unpublished</code></li><li><code>Published</code></li></ul></td></tr><tr><td><code>program</code></td><td>object</td><td>Represents the <a href="../"><code>program</code></a> to which the term item belongs.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../../api-usage-and-reference/common-api-objects/audit.md">audit</a> object.</td></tr></tbody></table>

## Example

{% code title="THE PROGRAM TERMS OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "TCS-3159-1891-0980-8679",
  "href": "/programs/PRG-6822-9898-4256/terms/TCS-3159-1891-0980-8679",
  "name": "Microsoft 365 Terms of Service",
  "description": "Description of Microsoft 365 Terms of Service",
  "displayOrder": 100,
  "state": "Draft",
  "program": {
    "id": "PRG-6822-9898-4256",
    "href": "/programs/PRG-6822-9898-4256",
    "name": "Microsoft AI Cloud Partner"
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
