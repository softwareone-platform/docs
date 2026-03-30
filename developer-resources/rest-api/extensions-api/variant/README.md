# Variant

The Terms Variant object represents terms variant as an uploaded PDF or DOCX document or a link to an externally hosted document as an element of the terms for an extension.

<table><thead><tr><th width="158">Field Name</th><th width="187">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>The business identifier of the Terms Variant. Example: ETV-1234-1234-1234-1234</td></tr><tr><td><code>href</code></td><td>string</td><td>The resource URI of the Terms Variant. Example: <code>/extensions/EXT-1234-1234/terms/ETC-1234-1234-1234/variants/ETV-1234-1234-1234-1234</code></td></tr><tr><td><code>type</code></td><td>string</td><td><p>Terms item type. </p><p>Example: Online</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>Terms Variant name. </p><p>Example: Terms of Service - En</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>Terms Variant description. </p><p>Example: Terms of Service description in English</p></td></tr><tr><td><code>assetUrl</code></td><td>string</td><td><p>The URL of the terms item uploaded document or online document/resource. </p><p>Example: https://www.test.com/terms-of-service</p></td></tr><tr><td><code>languageCode</code></td><td>string</td><td><p>The terms Item 2-digit language code from the <a href="https://en.wikipedia.org/wiki/List_of_ISO_639_language_codes">List of ISO 639 language codes</a> and data format for language. Where type is <code>online</code>, the languageCode <code>null</code> is displayed as  <code>multiple</code> on the UI. </p><p>Example: en-GB</p></td></tr><tr><td><code>status</code></td><td>string</td><td><p>Terms Item status. </p><p>Example: Draft</p></td></tr><tr><td><code>terms</code></td><td>object </td><td>The <a href="./#terms-object"><code>terms</code></a> object to which the variant belongs.</td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

### Example response

{% code lineNumbers="true" %}
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
