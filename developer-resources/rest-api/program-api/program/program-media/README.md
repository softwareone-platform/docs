# Program Media

The Program Media object allows vendors to add, view, or delete media from the object.

{% include "../../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="152">Field</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>(Read-only) The business identifier of the <code>media</code> object. </td></tr><tr><td>name</td><td>string</td><td>(Read-only) The name of the <code>media</code> object. </td></tr><tr><td>description</td><td>string</td><td>A description of the <code>media</code> object. </td></tr><tr><td>type</td><td>string</td><td>The type of the <code>media</code> object. </td></tr><tr><td>displayOrder</td><td>integer</td><td>The display order of the <code>media</code> object.</td></tr><tr><td>status</td><td>string</td><td><p>The status of the document object. Allowed values are: </p><ul><li><code>Draft</code></li><li><code>Published</code></li><li><code>Unpublished</code></li><li><code>Deleted</code></li></ul></td></tr><tr><td>program</td><td>object</td><td>Represents the <a href="../"><code>program</code></a> to which the media belongs.</td></tr><tr><td>audit</td><td>object</td><td>Represents the <a href="../../../../api-usage-and-reference/common-api-objects/audit.md"><code>a</code>udit</a> object.</td></tr></tbody></table>

## Example

{% code title="THE PROGRAM MEDIA OBJECT" overflow="wrap" lineNumbers="true" %}
```json
 {
    "id": "MED-1234-1234",
    "href": "v1/catalog/programs/media/MED-1234-1234",
    "name": "Microsoft AI Cloud Partner",
    "description": "Build a solid foundation with the support of workplace specialists who take the time to understand your unique business needs.",
    "type": "Image",
    "url": "https://address.to.media.file.pl/abcde.png",
    "displayOrder": 100,
    "state": "Draft",
    "program": {
        "id": "PRG-1111-1111",
        "href": "/catalog/programs/PRG-1111-1111",
        "name": "Microsoft Office 365 NCE",
        "icon": "/static/PRG-1111-1111/logo.png"
    },
    "audit": {
     "created": { "at": "...", "by": { } },
     "updated": { "at": "...", "by": { } }
   }
  }
```
{% endcode %}
