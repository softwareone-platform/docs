# Journal Attachment

The Journal Attachment object allows users to upload attachments to billing objects through an online link or file upload. This object inherits from the abstract File base object.

<table><thead><tr><th width="131">Field</th><th width="189">Type</th><th>Description</th></tr></thead><tbody><tr><td>url</td><td>string</td><td><p>External attachment link. </p><p></p><p>Example: https://address.to.journal.file.com/file.xlsx</p></td></tr><tr><td>id</td><td>string</td><td><p>Primary identifier for the billing attachment. </p><p></p><p>Example: BIA-1234-1234</p></td></tr><tr><td>type</td><td>string</td><td><p>The type of billing attachment. </p><p></p><p>Example: File</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="JOURNAL ATTACHMENT" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "BIA-1234-1234",
  "name": "29 Nov 2024 #1 - journal data",
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
