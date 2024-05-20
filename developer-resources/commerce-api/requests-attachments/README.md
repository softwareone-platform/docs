# Requests Attachments

## Attachment object

The definition represents an Attachment object in Marketplace. This Attachment object inherits from the abstract File base object.

## Fields <a href="#fields" id="fields"></a>

| Field                         | Type   | Description                                                                                                                                                                                       |
| ----------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`inlineAttachmentContent`** | string | <p>Inline attachment content. For example, in the case of type LicenseKey, this field is actually populated with a license key string. </p><p></p><p>Example: "DFE25-GQ943-GH992-KL235-PY037"</p> |

## Specific field behavior <a href="#specific-field-behaviour" id="specific-field-behaviour"></a>

| Field          | Description                                                                                              |
| -------------- | -------------------------------------------------------------------------------------------------------- |
| id             | <p>Primary attachment identifier using the prefix “ATT”. </p><p></p><p>Example: "ATT-1234-1234-1234"</p> |
| classification | <p>File or License Key </p><p></p><p>Example: "File"</p>                                                 |
| status         | <p>Attachment status. Can be Published or Deleted. </p><p></p><p>Example: "Published"</p>                |

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
