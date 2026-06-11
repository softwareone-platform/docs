# Document

The Document object lets you upload product documentation (via an online link or file upload) to the product object.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="199">Field</th><th width="142">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The identifier for the object.</td></tr><tr><td><code>name</code></td><td>string</td><td>The name of the document.</td></tr><tr><td><code>description</code></td><td>string</td><td>A description of the document.</td></tr><tr><td><code>type</code></td><td>string</td><td>The type of the document.</td></tr><tr><td><code>url</code></td><td>string</td><td>The URI to access the document.</td></tr><tr><td><code>language.name</code></td><td>string</td><td>The name of the language.</td></tr><tr><td><code>language.code</code></td><td>string</td><td>The ISO code of the language.</td></tr><tr><td><code>status</code></td><td>string</td><td>The status of the document. </td></tr><tr><td><code>product</code></td><td>object</td><td>Represents the <a href="../product/"><code>product</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Example

{% code title="DOCUMENT OBJECT" overflow="wrap" lineNumbers="true" %}
```json
 {
    "id": "DOC-1234-1234",
    "href": "v1/catalog-management/media/DOC-1234-1234",
    "name": "Guide to establishing a reseller relationship",
    "description": "Learn what happens when you establish a reseller relationship with SoftwareOne",
    "type": "File",
    "url": "https://address.to.media.file.pl/abcde.docx",
    "language": {
      name: "Polish",
      code: "pl-pl",
    },
    "state": "Draft",
    "product": {
      "id": "PRD-1111-1111-1111",
      "name": "Microsoft Office 365 NCE",
      "icon": "/static/PRD-1111-1111-1111/logo.png"
     },
    "audit": {
     "created": { "at": "...", "by": { } },
     "updated": { "at": "...", "by": { } }
   }
  }
```
{% endcode %}
