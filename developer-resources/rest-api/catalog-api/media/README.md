# Media

The Media object enables vendors to add, view, or delete media from the product object. This object contains the following properties:

<table><thead><tr><th width="158">Field</th><th width="134">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td>The identifier for the Media object.</td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the Media object.</p><p>Example: Office 365 Product Image</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>A description of the Media object.</p><p>Example: An image of Office 365, available to purchase within the Microsoft 365 Online Services product.</p></td></tr><tr><td>type</td><td><code>string</code></td><td>The type of the Media object.</td></tr><tr><td>url</td><td><code>string</code></td><td><p>The URI to access the media object.</p><p>Example: https://address.to.media.file.pl/abcde.png</p></td></tr><tr><td>displayOrder</td><td><code>integer</code></td><td><p>The object's order in the list.</p><p>Example: 100</p></td></tr><tr><td>status</td><td><code>string</code></td><td><p>The status of the media. </p><p>Example: Published.</p></td></tr><tr><td>product</td><td><a href="../product/"><code>product</code></a></td><td><p>A reference to the Product object.</p><p>Example:</p><pre class="language-json"><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td><p>A reference to the Audit object.</p><p>Example:</p><pre class="language-json"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="MEDIA OBJECT" %}
{% code lineNumbers="true" %}
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
{% endcode %}
{% endtab %}
{% endtabs %}
