# Program Document

The Program Document object allows you to upload program documentation using an online link or file upload to the Program object.&#x20;

{% include "../../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="172">Field</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The business identifier of the <code>document</code> object.</td></tr><tr><td><code>name</code></td><td>string</td><td>The name of the <code>document</code> object. </td></tr><tr><td><code>description</code></td><td>string</td><td>The description of the <code>document</code> object. </td></tr><tr><td><code>type</code></td><td>string</td><td>The type of the <code>document</code> object. </td></tr><tr><td><code>url</code></td><td>string</td><td>The URI to access the <code>document</code> object. </td></tr><tr><td><code>language</code></td><td>string</td><td>The document's language. </td></tr><tr><td><code>status</code></td><td>string</td><td>Represents the status of the <code>document</code> object. </td></tr><tr><td><code>program</code></td><td>object</td><td>Represents the <a href="../"><code>program</code></a> to which the document belongs.</td></tr><tr><td><code>audit</code></td><td>object</td><td>Represents the <a href="../../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Example

{% code title="THE PROGRAM DOCUMENT OBJECT" overflow="wrap" lineNumbers="true" %}
```json
 {
    "id": "PDM-1234-5678-0001",    
    "name": "Guide to establishing a reseller relationship",
    "description": "Learn what happens when you establish a reseller relationship with SoftwareOne",
    "type": "File",
    "url": "https://address.to.media.file.pl/abcde.docx",
    "language": "pl-pl",
    "state": "Draft",
    "program": {
      "id": "PRG-1234-5678",    
      "name": "Microsoft AI Cloud Partner",
      "icon": "/static/PRG-1234-1234/logo.png"
     },
    "audit": {
     "created": { "at": "...", "by": { } },
     "updated": { "at": "...", "by": { } }
   }
  }
```
{% endcode %}
