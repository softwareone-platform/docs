# Program Document

The Program Document object provides the ability to upload program documentation using an online link or file upload to the Program object. This object contains the following attributes:

<table><thead><tr><th width="152">Field</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The business identifier of the Document object</p><p>Example: PDM-1234-5678-0001</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the document object. </p><p>Example: Guide to establishing a reseller relationship</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>The description of the document object. </p><p>Example: Learn what happens when you establish a reseller relationship with SoftwareOne</p></td></tr><tr><td>type</td><td><code>string</code></td><td><p>The type of the document object. </p><p>Example: Online</p></td></tr><tr><td>url</td><td><code>string</code></td><td><p>The URI to access the document object. </p><p>Example: https://address.to.media.file.pl/abcde.docx</p></td></tr><tr><td>language</td><td><code>string</code></td><td><p>The document's language. </p><p>Example: pl-pl</p></td></tr><tr><td>status</td><td><code>string</code></td><td><p>Status of the document object. </p><p>Example: Draft</p></td></tr><tr><td>program</td><td><a href="../"><code>program</code></a></td><td><p>The program to which the document belongs.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
    "id": "PRG-1234-5678",    
    "name": "Microsoft AI Cloud Partner",
    "icon": "/static/PRG-1234-1234/logo.png"
}
</code></pre></td></tr><tr><td>audit</td><td><code>audit</code></td><td><p>The audit information object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="PROGRAM DOCUMENT OBJECT" %}
{% code overflow="wrap" lineNumbers="true" %}
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
{% endtab %}
{% endtabs %}
