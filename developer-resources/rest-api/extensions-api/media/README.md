# Media

The Media Object enables vendors to add, view, or delete media from the extension object.

<table data-search="false"><thead><tr><th width="139">Field</th><th width="143">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The ID of the media object. </td></tr><tr><td><code>href</code></td><td>string</td><td>(Read-only) The resource URI of the media object.  </td></tr><tr><td><code>name</code></td><td>string</td><td>The name of the media object. </td></tr><tr><td><code>description</code></td><td>string</td><td>A description of the media object. </td></tr><tr><td><code>type</code></td><td>string</td><td>The type of the media object. </td></tr><tr><td><code>url</code></td><td>string</td><td>The URI to access the media object. </td></tr><tr><td><code>displayOrder</code></td><td>integer</td><td>The display order of the media object in the list. </td></tr><tr><td><code>status</code></td><td>enum</td><td><p>The status of the media object. Allowed values are:</p><ul><li><code>Draft</code></li><li><code>Published</code></li><li><code>Unpublished</code></li><li><code>Deleted</code></li></ul></td></tr><tr><td><code>extension</code></td><td>object</td><td>Represents the <a href="../extension/"><code>extension</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% code title="MEDIA OBJECT" overflow="wrap" lineNumbers="true" %}
```json
  {
    "id": "EMD-0001-0001",
    "href": "v1/extensions/EXT-1111-1111/media/EMD-0001-0001",
    "name": "Microsoft AI Cloud Partner",
    "description": "Build a solid foundation with the support of workplace specialists who take the time to understand your unique business needs.",
    "type": "Image",
    "url": "https://address.to.media.file.pl/abcde.png",
    "displayOrder": 100,
    "status": "Draft",
    "extension": {
        "id": "EXT-1111-1111",
        "href": "/extensions/EXT-1111-1111",
        "name": "Microsoft Office 365 NCE",
        "icon": "/static/EXT-1111-1111-1111/logo.png"
    },
    "audit": {
     "created": { "at": "...", "by": { } },
     "updated": { "at": "...", "by": { } }
   }
  }
```
{% endcode %}
