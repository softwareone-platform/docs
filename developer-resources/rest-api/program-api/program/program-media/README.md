# Program Media

The Program Media object allows vendors to add, view, or delete media from the object. This object contains the following attributes:

<table><thead><tr><th width="152">Field</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The business identifier of the Media object. </p><p>Example: MED-0001-0001</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the Media object. </p><p>Example: Microsoft AI Cloud Partner</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>The description of the Media object. </p><p>Example: Build a solid foundation with the support of workplace specialists who take the time to understand your unique business needs.</p></td></tr><tr><td>type</td><td><code>string</code></td><td><p>The type of the Media object. </p><p>Example: Online</p></td></tr><tr><td>displayOrder</td><td><code>integer</code></td><td><p>The display order of the Media object.</p><p>Example: 100</p></td></tr><tr><td>status</td><td><code>string</code></td><td><p>The status of the document object. </p><p>The possible values are <code>Draft</code>, <code>Published</code>, <code>Unpublished</code>, or <code>Deleted</code>.</p></td></tr><tr><td>program</td><td><a href="../"><code>program</code></a></td><td><p>The program to which the media belongs.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
    "id": "PRG-1111-1111",
    "href": "/catalog/programs/PRG-1111-1111",
    "name": "Microsoft AI Cloud Partner",
    "icon": "/static/PRG-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>audit</td><td><code>audit</code></td><td>A reference to the Audit object. </td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="PROGRAM MEDIA" %}
{% code overflow="wrap" lineNumbers="true" %}
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
{% endtab %}
{% endtabs %}
