# Document

The Document object provides the ability to upload extension documentation (via an online link or file upload) to the extension object.

<table><thead><tr><th width="165">Field</th><th width="154">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>The ID of the document object. </td></tr><tr><td><code>name</code></td><td>string</td><td>The name of the document object. </td></tr><tr><td><code>description</code></td><td>string</td><td>The description of the document object. </td></tr><tr><td><code>type</code></td><td>string</td><td>The type of the document object.</td></tr><tr><td><code>url</code></td><td>string</td><td>The URI to access the document object. </td></tr><tr><td><code>language</code></td><td>string</td><td>The language of the document object. </td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the document object. Allowed values: <code>draft</code>, <code>published</code>, or <code>unpublished</code>. </td></tr><tr><td><code>extension</code></td><td>object</td><td>Represents the <a href="../extension/"><code>extension</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% code title="DOCUMENT OBJECT" overflow="wrap" lineNumbers="true" %}
```json
 {
    "id": "EDM-1234-5678-0001",    
    "name": "Guide to establishing a reseller relationship",
    "description": "Learn what happens when you establish a reseller relationship with SoftwareOne",
    "type": "File",
    "url": "https://address.to.media.file.pl/abcde.docx",
    "language": "pl-pl",
    "status": "Draft",
    "extension": {
      "id": "EXT-1234-5678",    
      "name": "Microsoft AI Cloud Partner",
      "icon": "/static/EXT-1234-5678/logo.png"
     },
    "audit": {
     "created": { "at": "...", "by": { } },
     "updated": { "at": "...", "by": { } }
   }
  }
```
{% endcode %}
