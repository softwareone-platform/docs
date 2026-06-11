# Variant

The Terms Variant object represents terms variant as an uploaded PDF or DOCX document or a link to an externally hosted document as an element of the terms for an extension.

<table><thead><tr><th width="158">Field</th><th width="136">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>The business identifier of the Terms Variant.</td></tr><tr><td><code>href</code></td><td>string</td><td>The resource URI of the Terms Variant.</td></tr><tr><td><code>type</code></td><td>string</td><td>Terms item type.</td></tr><tr><td><code>name</code></td><td>string</td><td>Terms Variant name. </td></tr><tr><td><code>description</code></td><td>string</td><td>Terms Variant description. </td></tr><tr><td><code>assetUrl</code></td><td>string</td><td>The URL of the terms item uploaded document or online document/resource. </td></tr><tr><td><code>languageCode</code></td><td>string</td><td>The terms Item 2-digit language code from the <a href="https://en.wikipedia.org/wiki/List_of_ISO_639_language_codes">List of ISO 639 language codes</a> and data format for language. Where type is <code>online</code>, the languageCode <code>null</code> is displayed as  <code>multiple</code> on the UI. </td></tr><tr><td><code>status</code></td><td>string</td><td>Terms Item status. </td></tr><tr><td><code>terms</code></td><td>object </td><td>The <a href="./#terms-object"><code>terms</code></a> object to which the variant belongs.</td></tr><tr><td><code>audit</code></td><td>object</td><td>Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% code title="VARIANT OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "ETV-1234-1234-1234-1234",
  "href": "/extensions/EXT-1234-1234/terms/ETC-1234-1234-1234/variants/ETV-1234-1234-1234-1234",
  "name": "Terms and Conditions Variant - EN",
  "description": "Terms and Conditions Variant in English",
  "type": "Online",
  "assetUrl": "https://www.microsoft.com",
  "languageCode": "en",
  "status": "Draft",
  "termsAndConditions": {
    "id": "ETC-1234-1234-1234",
    "href": "/extensions/EXT-1234-1234/terms/ETC-1234-1234-1234",
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
