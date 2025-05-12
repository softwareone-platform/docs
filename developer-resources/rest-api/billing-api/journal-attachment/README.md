# Journal Attachment

The Journal Attachment object allows users to upload attachments to billing objects through an online link or file upload. This object inherits from the abstract File base object.

<table><thead><tr><th width="134">Field</th><th width="206">Type</th><th>Description</th></tr></thead><tbody><tr><td>URL</td><td><code>string</code></td><td><p>The external link to the attachment.</p><p>Example: https://address.to.journal.file.com/file.xlsx</p></td></tr><tr><td>id</td><td><code>string</code></td><td><p>The primary identifier for the billing attachment.</p><p>Example: BIA-1234-1234</p></td></tr><tr><td>type</td><td><code>string</code></td><td><p>The type of billing attachment.</p><p>Example: File</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="JOURNAL ATTACHMENT" %}
{% code lineNumbers="true" %}
```json
{
  "id": "BIA-1234-1234",
  "name": "29 Nov 2024 #1 - journal data",
  "href": "/billing/journals/BJO-1234-5678/attachments/BIA-1234-1234",
  "type": "File",
  "contentType": "text/csv",
  "description": "Journal charges for Microsoft 365",
  "filename": "charges.csv",
  "audit": {
    "created": {
      "at": "2024-12-02T17:00:00Z",
      "by": { ... }
    }
  }
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
