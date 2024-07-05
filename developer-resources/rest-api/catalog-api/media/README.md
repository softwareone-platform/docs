# Media

## Media object

The Media object enables vendors to add, view, or delete media from the product object.

<table><thead><tr><th width="197">Field</th><th width="158">Type</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td> </td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td> </td></tr><tr><td><strong><code>name</code></strong></td><td>string</td><td><p>The name of the media object. </p><p></p><p>Example: "Office 365 Product Image"</p></td></tr><tr><td><strong><code>description</code></strong></td><td>string</td><td><p>The description of the media object. </p><p></p><p>Example: "An image of Office 365 which is available to purchase within the Microsoft 365 Online Services product"</p></td></tr><tr><td><strong><code>type</code></strong></td><td>string</td><td>The type of the media object.</td></tr><tr><td><strong><code>url</code></strong></td><td>string</td><td><p>The URI to access media object. </p><p></p><p>Example: "https://address.to.media.file.pl/abcde.png"</p></td></tr><tr><td><strong><code>displayOrder</code></strong></td><td>integer</td><td><p>Media object order on list. </p><p></p><p>Example: "100"</p></td></tr><tr><td><strong><code>status</code></strong></td><td>string</td><td>Draft or Published.</td></tr><tr><td><strong><code>product</code></strong></td><td>Product Object</td><td><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "href": "/catalog/products/PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td><strong><code>audit</code></strong></td><td>Audit Object</td><td><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="MEDIA OBJECT" %}
```json
 {
    "id": "MED-1234-1234",
    "href": "v1/catalog-management/media/MED-1234-1234",
    "name": "Office 365 Product Image",
    "description": "An image of Office 365 which is available to purchase within the Microsoft 365 Online Services product",
    "type": "Image",
    "url": "https://address.to.media.file.pl/abcde.png",
    "displayOrder": 100,
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
