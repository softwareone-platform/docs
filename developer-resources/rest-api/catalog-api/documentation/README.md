# Document

The Document object provides the ability to upload product documentation (via an online link or file upload) to the product object.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="185">Field Name</th><th width="131">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>The identifier for the object.</td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the document.</p><p>Example: Guide to establishing a reseller relationship</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the document.</p><p>Example: Learn what happens when you establish a reseller relationship with SoftwareOne</p></td></tr><tr><td><code>type</code></td><td>string</td><td>The type of the document.</td></tr><tr><td><code>url</code></td><td>string</td><td>The URI to access the document.</td></tr><tr><td><code>language.name</code></td><td>string</td><td><p>The name of the language.</p><p>Example: Polish</p></td></tr><tr><td><code>language.code</code></td><td>string</td><td><p>The ISO code of the language.</p><p>Example: pl-pl</p></td></tr><tr><td><code>status</code></td><td>string</td><td><p>The status of the document. </p><p>Example: Draft</p></td></tr><tr><td><code>product</code></td><td>object</td><td><p>A reference to the <a href="../product/"><code>product</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td><p>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Example response

{% code lineNumbers="true" %}
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
