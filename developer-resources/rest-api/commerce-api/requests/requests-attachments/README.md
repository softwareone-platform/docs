# Requests Attachments

The Attachment object inherits from the abstract File base object.

<table><thead><tr><th width="234">Field</th><th width="100">Type</th><th>Description</th></tr></thead><tbody><tr><td>inlineAttachmentContent</td><td><code>string</code></td><td><p>Inline attachment content. For example, in the case of type <code>LicenseKey</code>, this field is populated with a license key string.</p><p>Example: DFE25-GQ943-GH992-KL235-PY037</p></td></tr><tr><td>id</td><td><code>string</code></td><td><p>Primary attachment identifier using the 'ATT' prefix.</p><p>Example: ATT-1234-1234-1234</p></td></tr><tr><td>classification</td><td><code>string</code></td><td><p>File or license key.</p><p>Example: File</p></td></tr><tr><td>status</td><td><code>string</code></td><td>Status of the attachment. Possible values include <code>Published</code> or <code>Deleted</code>.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="REQUEST ATTACHMENT OBJECT" %}
```json
{
  "id": "ATT-1234-1234-1234",
  "name": "Some order attachment",
  "classification": "Text",
  "contentType": "application/x-iso9660-image",
  "size": 123,
  "description": "Some order attachment description",
  "filename": "SomeOrderAttachment.txt",
  "inlineAttachmentContent": null,
  "audit": {
    "created": {
      "at": "2023-01-01T22:00:00Z",
      "by": { ... }
    }
  }
}
```
{% endtab %}
{% endtabs %}
