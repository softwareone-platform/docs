# Program Terms

The Program Terms object represents terms in the form of uploaded PDF or DOCX documents, as well as links to documents hosted externally. This object contains the following attributes:

<table><thead><tr><th width="152">Field</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The business identifier of the terms. </p><p>Example: TCS-0001-0001</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>The resource URI of the terms. </p><p>Example: /programs/PRG-6822-9898-4256/terms/TCS-3159-1891-0980-8679</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the terms. </p><p>Example: Terms of Service</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>The description of the terms. </p><p>Example: Terms of Service description.</p></td></tr><tr><td>displayOrder</td><td><code>integer</code></td><td><p>The display order of the terms. </p><p>Example: 100</p></td></tr><tr><td>status</td><td><code>string</code></td><td>The status of the terms. The possible values are <code>Draft</code>, <code>Published</code>, <code>Unpublished</code>, or <code>Published</code>.</td></tr><tr><td>program</td><td><a href="../"><code>program</code></a></td><td>The program to which the term item belongs.</td></tr><tr><td>audit</td><td><code>audit</code></td><td>A reference to the Audit object.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="TERMS OBJECT" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "TCS-3159-1891-0980-8679",
  "href": "/programs/PRG-6822-9898-4256/terms/TCS-3159-1891-0980-8679",
  "name": "Microsoft 365 Terms of Service",
  "description": "Description of Microsoft 365 Terms of Service",
  "displayOrder": 100,
  "state": "Draft",
  "program": {
    "id": "PRG-6822-9898-4256",
    "href": "/programs/PRG-6822-9898-4256",
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
{% endtab %}
{% endtabs %}
