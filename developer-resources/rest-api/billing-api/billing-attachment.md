# Billing Attachment

The `billingAttachment` object provides the ability to upload attachments to billing objects. This object inherits from the abstract `fileBase` object.

{% include "../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="141">Field Name</th><th width="204">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>A primary identifier for the billing attachment. Example: JOA-1234-1234</td></tr><tr><td><code>type</code></td><td>string</td><td><p>The type of attachment.</p><p>Example: File</p></td></tr></tbody></table>

### Example

{% code lineNumbers="true" %}
```json
{
  "id": "JOA-1234-1234",
  "name": "29 Nov 2024 #1 - journal data",
  "type": "Input",
  "contentType": "text/csv",
  "description" : "Journal charges for Microsoft 365",
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
