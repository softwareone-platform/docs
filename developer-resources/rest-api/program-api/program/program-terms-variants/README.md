# Program Terms Variant

The Terms Variant Object represents a terms variant as an uploaded PDF or DOCX document, or a link to an externally hosted document, as an element of the terms for a program.

This object contains the following attributes:

<table><thead><tr><th width="152">Field</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The business identifier of the terms variant. </td></tr><tr><td><code>href</code></td><td>string</td><td>(Read-only) The resource URI of the terms variant. </td></tr><tr><td><code>type</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>Terms Item type. The possible values are <code>Online</code> or <code>File</code>.</td></tr><tr><td><code>name</code></td><td>string, core</td><td>The name of the term's variant. </td></tr><tr><td><code>description</code></td><td>string, core</td><td>The description of the term's variant. </td></tr><tr><td><code>assetUrl</code></td><td>string, core</td><td>The URL of the terms item uploaded document or online document/resource. </td></tr><tr><td><code>languageCode</code></td><td>string, core</td><td>A 2-digit language code from the list of language codes in ISO 639 and its corresponding data format. When the type is Online, <code>null</code> will appear as <strong>multiple</strong> on the UI.</td></tr><tr><td><code>status</code></td><td>string, core</td><td><p>The status of the terms variant. Allowed values are:</p><ul><li><code>Draft</code></li><li><code>Published</code></li><li><code>Unpublished</code></li><li><code>Published</code></li></ul></td></tr><tr><td><code>program</code></td><td>object</td><td>Represents the <a href="../"><code>program</code></a> to which the term item belongs.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../../api-usage-and-reference/common-api-objects/audit.md">audit</a> object.</td></tr></tbody></table>

## Example

{% code title="THE PROGRAM TERMS VARIANT OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "TCS-1234-1234-1234-1234",
  "href": "/programs/PRG-1234-1234/terms/TCS-1234-1234-1234/variants/TCV-1234-1234-1234-1234",
  "name": "Terms and Conditions Variant - EN",
  "description": "Terms and Conditions Variant in English",
  "type": "Online",
  "assetUrl": "https://www.microsoft.com",
  "languageCode": "en",
  "state": "Draft",
  "termsAndConditions": {
    "id": "TCS-1234-1234-1234",
    "href": "/programs/PRG-1234-1234/terms/TCS-1234-1234-1234",
    "name": "Microsoft 365 Terms of Service"
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
