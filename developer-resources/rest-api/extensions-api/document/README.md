# Document

The `document` object provides the ability to upload extension documentation (via an online link or file upload) to the extension object.

<table><thead><tr><th width="165">Field Name</th><th width="154">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p> The ID of the document object. </p><p>Example: EDM-1234-5678-0001</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the document object. </p><p>Example: Guide to establishing a reseller relationship</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>The description of the document object. </p><p>Example: Learn what happens when you establish a reseller relationship with SoftwareOne</p></td></tr><tr><td><code>type</code></td><td>string</td><td>The type of the document object.</td></tr><tr><td><code>url</code></td><td>string</td><td><p>The URI to access the document object. </p><p>Example: https://address.to.media.file.pl/abcde.docx</p></td></tr><tr><td><code>language</code></td><td>string</td><td><p>The language of the document object. </p><p>Example: pl-PL</p></td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the document object. Allowed values: <code>draft</code>, <code>published</code>, or <code>unpublished</code>. </td></tr><tr><td><code>extension</code></td><td>object</td><td><p>A reference to the <a href="../extension/"><code>extension</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "EXT-1234-5678",    
    "name": "Microsoft AI Cloud Partner",
    "icon": "/static/EXT-1234-5678/logo.png"
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

### Example response <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
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
