# Terms

The Terms object represents terms as a collection of uploaded PDF or DOCX documents or links to externally hosted documents as an element of an extension.

<table><thead><tr><th width="161">Field Name</th><th width="135">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The business identifier of the terms. </p><p>Example: ETC-1234-1234-1234 </p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>The resource URI of the terms. </p><p>Example: <code>/extensions/EXT-6822-9898-4256/terms/ETC-1234-1234-1234</code></p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the terms. </p><p>Example: Terms of Service</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the terms. </p><p>Example: Terms of Service description</p></td></tr><tr><td><code>displayOrder</code></td><td>integer</td><td><p>The display order of the terms. </p><p>Example: 100</p></td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the terms object. Allowed values:  <code>draft</code>, <code>published</code>, <code>unpublished</code>, or <code>deleted</code>.  </td></tr><tr><td><code>extension</code></td><td>object</td><td>The <a href="../extension/"><code>extension</code></a> to which the terms item belongs.</td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

### Example response <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
  {
  "id": "ETC-1234-1234-1234",
  "href": "/extensions/EXT-6822-9898-4256/terms/ETC-1234-1234-1234",
  "name": "Microsoft 365 Terms of Service",
  "description": "Description of Microsoft 365 Terms of Service",
  "displayOrder": 100,
  "state": "Draft",
  "extension": {
    "id": "EXT-6822-9898-4256",
    "href": "/extensions/EXT-6822-9898-4256",
    "name": "Microsoft AI Cloud Partner"
  },
  "audit": {
    "created": {
      "at": "2024-01-16T21:30:13.1046031",
      "by": {
        "id": "USR-0000-0001"
      }
    },
    "updated": null
  }
}
```
{% endcode %}
