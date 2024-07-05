# Documents

## Document object

The `Document` object provides the ability to upload product documentation (via an online link or file upload) to the product object.

| Field               | Type            | Description                                                                                                                                                                                                                                                               |
| ------------------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`id`**            | string          |                                                                                                                                                                                                                                                                           |
| **`href`**          | string          |                                                                                                                                                                                                                                                                           |
| **`name`**          | string          | <p>The name of the document object. </p><p></p><p>Example: "Guide to establishing a reseller relationship"</p>                                                                                                                                                            |
| **`description`**   | string          | <p>The description of the document object. </p><p></p><p>Example: "Learn what happens when you establish a reseller relationship with SoftwareOne"</p>                                                                                                                    |
| **`type`**          | string          | The type of the document object/                                                                                                                                                                                                                                          |
| **`url`**           | string          | <p>The URI to access document object. </p><p></p><p>Example: "Polish"</p>                                                                                                                                                                                                |
| **`language.name`** | string          |  Example: "pl-pl"                                                                                                                                                                                                                                                         |
| **`language.code`** | string          |  Example: "Guide to establishing a reseller relationship"                                                                                                                                                                                                                 |
| **`status`**        | string          | Draft, Published, or Deleted.                                                                                                                                                                                                                                             |
| **`product`**       | Product Object  | <p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111",
    "href": "/catalog/products/PRD-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre> |
| **`audit`**         | Audit Object    | <p> Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre>                                                                                   |

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
