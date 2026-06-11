# Journal Attachment

The Journal Attachment object allows users to upload attachments to billing objects through an online link or file upload. It inherits from the abstract File base object.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="134">Field</th><th width="144">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>URL</code></td><td>string</td><td>The external link to the attachment.</td></tr><tr><td><code>id</code></td><td>string</td><td>The primary identifier for the billing attachment.</td></tr><tr><td><code>type</code></td><td>string</td><td>The type of billing attachment.</td></tr></tbody></table>

## Example

{% code title="JOURNAL ATTACHMENT OBJECT" lineNumbers="true" %}
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
