# Media

The Media object enables vendors to add, view, or delete media from the product object.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="158">Field</th><th width="134">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The identifier for the media.</td></tr><tr><td><code>name</code></td><td>string</td><td>The name of the media.</td></tr><tr><td><code>description</code></td><td>string</td><td>A description of the media.</td></tr><tr><td><code>type</code></td><td>string</td><td>The type of the media.</td></tr><tr><td><code>url</code></td><td>string</td><td>The URI to access the media.</td></tr><tr><td><code>displayOrder</code></td><td>integer</td><td>The object's order in the list.</td></tr><tr><td><code>status</code></td><td>string</td><td>The status of the media. </td></tr><tr><td><code>product</code></td><td>object</td><td>Represents the <a href="../product/"><code>product</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Example

{% code title="MEDIA OBJECT" overflow="wrap" lineNumbers="true" %}
```json
  {
    "id": "MED-1234-1234",   
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
