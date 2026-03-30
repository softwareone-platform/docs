# Media

The Media Object enables Vendors to add, view delete media to the extension object.

<table><thead><tr><th width="139">Field Name</th><th width="143">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The ID of the media object. </p><p>Example: EMD-0001-0001</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>The resource URI of the media object.  </p><p>Example: /extensions/EXT-1111-1111/media/EMD-0001-0001</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the media object. </p><p>Example: Microsoft AI Cloud Partner</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the media object. </p><p>Example: Build a solid foundation with the support of workplace specialists who take the time to understand your unique business needs.</p></td></tr><tr><td><code>type</code></td><td>string</td><td>The type of the media object. </td></tr><tr><td><code>url</code></td><td>string</td><td><p>The URI to access the media object. </p><p>Example: https://address.to.media.file.pl/abcde.png</p></td></tr><tr><td><code>displayOrder</code></td><td>integer</td><td><p>The display order of the media object in the list. </p><p>Example: 100</p></td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the media object. Allowed values: <code>draft</code>, <code>published</code>, <code>unpublished</code>, or <code>deleted</code>. </td></tr><tr><td><code>extension</code></td><td>object</td><td><p>A reference to the <a href="../extension/"><code>extension</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "EXT-1111-1111",
    "href": "/extensions/EXT-1111-1111-1111",
    "name": "Microsoft AI Cloud Partner",
    "icon": "/static/EXT-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td> A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

### Example response <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
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
