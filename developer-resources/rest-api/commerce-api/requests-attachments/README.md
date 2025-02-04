# Requests Attachments

## Attachment object

The definition represents an Attachment object in Marketplace. This Attachment object inherits from the abstract File base object.

## Fields <a href="#fields" id="fields"></a>

<table><thead><tr><th>Field</th><th width="100">Type</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>inlineAttachmentContent</code></strong></td><td>string</td><td><p>Inline attachment content. For example, in the case of type <code>LicenseKey</code>, this field is populated with a license key string. </p><p></p><p>Example: "DFE25-GQ943-GH992-KL235-PY037"</p></td></tr></tbody></table>

## Specific field behavior <a href="#specific-field-behaviour" id="specific-field-behaviour"></a>

<table><thead><tr><th width="170">Field</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><p>Primary attachment identifier using the prefix “ATT”. </p><p></p><p>Example: "ATT-1234-1234-1234"</p></td></tr><tr><td>classification</td><td><p>File or License Key </p><p></p><p>Example: "File"</p></td></tr><tr><td>status</td><td><p>Attachment status. Can be Published or Deleted. </p><p></p><p>Example: "Published"</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="REQUEST ATTACHMENTS OBJECT" %}
```json
{
  "id": "ATT-1234-1234-1234",
  "name": "Some order attachment",
  "href": "/commerce/orders/ORD-2119-4550/attachment/ATT-1234-1234-1234",
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
