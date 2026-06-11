# Billing Attachment

The Billing Attachment object is used to upload attachments to billing objects. It inherits from the abstract `fileBase` object.

{% include "../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="141">Field</th><th width="140">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>A primary identifier for the billing attachment.</td></tr><tr><td><code>type</code></td><td>string</td><td>The type of attachment.</td></tr></tbody></table>

## Example

{% code title="BILLING ATTACHMENT OBJECT" lineNumbers="true" %}
```json
{
  "id": "JOA-1234-1234",
  "name": "29 Nov 2024 #1 - journal data",
  "type": "File",
  "contentType": "text/csv",
  "description": "Journal charges for Microsoft 365",
  "filename": "charges.csv",
  "audit": {
    "created": {
      "at": "2024-12-02T17:00:00Z",
      "by": { }
    }
  }
}
```
{% endcode %}
