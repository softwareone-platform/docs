# Media

## Media object

The `Media` object enables vendors to add, view, or delete media from the `product` object.

| Field              | Type           | Description                                                                                                                                                                                                                                                                         |
| ------------------ | -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`id`**           | string         |                                                                                                                                                                                                                                                                                     |
| **`href`**         | string         |                                                                                                                                                                                                                                                                                     |
| **`name`**         | string         | <p>The name of the media object. </p><p></p><p>Example: "Office 365 Product Image"</p>                                                                                                                                                                                              |
| **`description`**  | string         | <p>The description of the media object. </p><p></p><p>Example: "An image of Office 365 which is available to purchase within the Microsoft 365 Online Services product"</p>                                                                                                         |
| **`type`**         | string         | The type of the media object.                                                                                                                                                                                                                                                       |
| **`url`**          | string         | <p>The URI to access media object. </p><p></p><p>Example: "https://address.to.media.file.pl/abcde.png"</p>                                                                                                                                                                          |
| **`displayOrder`** | integer        | <p>Media object order on list. </p><p></p><p>Example: "100"</p>                                                                                                                                                                                                                     |
| **`status`**       | string         | Draft or Published.                                                                                                                                                                                                                                                                 |
| **`product`**      | Product Object | <p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "href": "/catalog/products/PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre> |
| **`audit`**        | Audit Object   | <p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre>                                                                                              |

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
