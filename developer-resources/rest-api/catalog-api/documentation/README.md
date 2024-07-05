# Documentation

## Documentation object

The `Document` object provides the ability to upload product documentation (via an online link or file upload) to the product object.

<table><thead><tr><th width="239">Field</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td> </td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td> </td></tr><tr><td><strong><code>name</code></strong></td><td>string</td><td><p>The name of the document object. </p><p></p><p>Example: "Guide to establishing a reseller relationship"</p></td></tr><tr><td><strong><code>description</code></strong></td><td>string</td><td><p>The description of the document object. </p><p></p><p>Example: "Learn what happens when you establish a reseller relationship with SoftwareOne"</p></td></tr><tr><td><strong><code>type</code></strong></td><td>string</td><td>The type of the document object/</td></tr><tr><td><strong><code>url</code></strong></td><td>string</td><td><p>The URI to access document object. </p><p></p><p>Example: "Polish"</p></td></tr><tr><td><strong><code>language.name</code></strong></td><td>string</td><td> Example: "pl-pl"</td></tr><tr><td><strong><code>language.code</code></strong></td><td>string</td><td> Example: "Guide to establishing a reseller relationship"</td></tr><tr><td><strong><code>status</code></strong></td><td>string</td><td>Draft, Published, or Deleted.</td></tr><tr><td><strong><code>product</code></strong></td><td><a href="../product/">Product</a></td><td><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111",
    "href": "/catalog/products/PRD-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td><strong><code>audit</code></strong></td><td>Audit Object</td><td><p> Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="DOCUMENT OBJECT" %}
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
      code: "pl-pl"
    },
    "state": "Draft",
    "product": {
      "id": "PRD-1111-1111-1111",
      "href": "/catalog/products/PRD-1111-1111-1111",
      "name": "Microsoft Office 365 NCE",
      "icon": "/static/PRD-1111-1111-1111/logo.png"
     },
    "audit": {
     "created": { "at": "...", "by": { } },
     "updated": { "at": "...", "by": { } }
   }
  }
```
{% endtab %}
{% endtabs %}
