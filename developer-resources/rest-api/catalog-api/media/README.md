# Media

The Media object enables vendors to add, view, or delete media from the product object.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="158">Field Name</th><th width="134">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>The identifier for the media.</td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the media.</p><p>Example: Office 365 Product Image</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the media.</p><p>Example: An image of Office 365, available to purchase within the Microsoft 365 Online Services product.</p></td></tr><tr><td><code>type</code></td><td>string</td><td>The type of the media.</td></tr><tr><td><code>url</code></td><td>string</td><td><p>The URI to access the media.</p><p>Example: https://address.to.media.file.pl/abcde.png</p></td></tr><tr><td><code>displayOrder</code></td><td>integer</td><td><p>The object's order in the list.</p><p>Example: 100</p></td></tr><tr><td><code>status</code></td><td>string</td><td><p>The status of the media. </p><p>Example: Published.</p></td></tr><tr><td><code>product</code></td><td>object</td><td><p>A reference to the <a href="../product/"><code>product</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
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
    "id": "MED-1234-1234",
    "href": "v1/catalog-management/media/MED-1234-1234",
    "name": "Office 365 Product Image",
    "description": "An image of Office 365, which is available to purchase within the Microsoft 365 Online Services product",
    "type": "Image",
    "url": "https://address.to.media.file.pl/abcde.png",
    "displayOrder": 100,
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
