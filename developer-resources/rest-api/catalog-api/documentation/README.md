# Documents

The Document object provides the ability to upload product documentation (via an online link or file upload) to the product object.

<table><thead><tr><th width="185">Field</th><th width="135">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td>The identifier for the object.</td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the Document object.</p><p>Example: Guide to establishing a reseller relationship</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>A description of the Document object.</p><p>Example: Learn what happens when you establish a reseller relationship with SoftwareOne</p></td></tr><tr><td>type</td><td><code>string</code></td><td>The type of the Document object.</td></tr><tr><td>url</td><td><code>string</code></td><td>The URI to access the Document object.</td></tr><tr><td>language.name</td><td><code>string</code></td><td><p>The name of the language.</p><p>Example: Polish</p></td></tr><tr><td>language.code</td><td><code>string</code></td><td><p>The ISO code of the language.</p><p>Example: pl-pl</p></td></tr><tr><td>status</td><td><code>string</code></td><td><p>The status of the document. </p><p>Example: Draft, Published, or Deleted.</p></td></tr><tr><td>product</td><td><a href="../product/"><code>product</code></a></td><td><p>A reference to the Product object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td><p>A reference to the Audit object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="DOCUMENT OBJECT" %}
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
      code: "pl-pl"
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
{% endtab %}
{% endtabs %}
