# Program Terms Variants

The Terms Variant Object represents a terms variant as an uploaded PDF or DOCX document, or a link to an externally hosted document, as an element of the terms for a program.

This object contains the following attributes:

<table><thead><tr><th width="152">Field</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The business identifier of the terms variant. </p><p>Example: TCS-0001-0001</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>The resource URI of the terms variant. </p><p>Example: /programs/PRG-1234-1234/terms/TCS-1234-1234-1234/variants/TCV-1234-1234-1234-1234</p></td></tr><tr><td>type</td><td><code>string</code></td><td>Terms Item type. The possible values are <code>Online</code> or <code>File</code>.</td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the term's variant. </p><p>Example: Terms of Service - EN</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>The description of the term's variant. </p><p>Example: Terms of Service in English.</p></td></tr><tr><td>assetUrl</td><td><code>string</code></td><td><p>The URL of the terms item uploaded document or online document/resource. </p><p>Example: /programs/PRG-1234-1234/terms/TCS-1234-1234-1234/variants/TCV-1234-1234-1234-1234</p></td></tr><tr><td>languageCode</td><td><code>string</code></td><td><p>A 2-digit language code from the list of language codes in ISO 639 and its corresponding data format. When the type is Online, <code>null</code> will appear as <strong>multiple</strong> on the UI.</p><p>Example: 100</p></td></tr><tr><td>status</td><td><code>string</code></td><td>The status of the terms variant. The possible values are <code>Draft</code>, <code>Published</code>, <code>Unpublished</code>, or <code>Published</code>.</td></tr><tr><td>program</td><td><a href="../"><code>program</code></a></td><td>The program to which the variant belongs.</td></tr><tr><td>audit</td><td><a href="../../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the Audit object. </td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="PROGRAM TERMS VARIANT OBJECT" %}
{% code overflow="wrap" lineNumbers="true" %}
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
{% endtab %}
{% endtabs %}
