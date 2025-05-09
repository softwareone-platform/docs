# Media

The Media object enables vendors to add, view, or delete media from the product object. This object contains the following properties:

<table><thead><tr><th width="158">Field</th><th width="158">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td> Identifier for the Media object.</td></tr><tr><td>name</td><td>string</td><td><p>The name of the media object. </p><p></p><p>Example: Office 365 Product Image</p></td></tr><tr><td>description</td><td>string</td><td><p>The description of the media object. </p><p></p><p>Example: An image of Office 365, which is available to purchase within the Microsoft 365 Online Services product</p></td></tr><tr><td>type</td><td>string</td><td>The type of the media object.</td></tr><tr><td>url</td><td>string</td><td><p>The URI to access the media object. </p><p></p><p>Example: https://address.to.media.file.pl/abcde.png</p></td></tr><tr><td>displayOrder</td><td>integer</td><td><p>Media object order on the list. </p><p></p><p>Example: 100</p></td></tr><tr><td>status</td><td>string</td><td>Draft or Published.</td></tr><tr><td>product</td><td>Product Object</td><td><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>audit</td><td>Audit Object</td><td><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
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
