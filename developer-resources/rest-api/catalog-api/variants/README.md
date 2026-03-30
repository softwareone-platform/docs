# Terms Variant

The Terms Variant object represents a variant as an uploaded PDF or DOCX document or a link to an externally hosted document as an element of terms for a product.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="185">Field Name</th><th width="131">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>A unique identifier for the terms variant.</p><p>Example: TCS-1234-1234-1234-1234</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">/products/PRD-1234-1234/terms/tcs-1234-1234-1234/terms-item/tcs-1234-1234-1234-1234
</code></pre></td></tr><tr><td><code>type</code></td><td>string</td><td><p>The type of terms variant.</p><p>Example: Online</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>A name for the terms variant.</p><p>Example: TCS-1234-1234-1234-1234</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the terms variant.</p><p>Example: Terms of Service description in English</p></td></tr><tr><td><code>assetUrl</code></td><td>string</td><td><p>The URL of the uploaded document or online document/resource.</p><p>Example: https://www.test.com/terms-of-service</p></td></tr><tr><td><code>languageCode</code></td><td>string</td><td><p>The 2-digit language code for the terms item.</p><p>Example: en</p></td></tr><tr><td><code>status</code></td><td>string</td><td><p>The status of the terms.</p><p>Example: Draft</p></td></tr><tr><td><code>termsAndConditions</code></td><td>string</td><td>The terms to which the item has been assigned.</td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Example response

```json
{
  "id": "TCS-1234-1234-1234-1234",
  "name": "Terms and Conditions Variant - EN",
  "description": "Terms and Conditions Variant in English",
  "type": "Online",
  "assetUrl": "https://www.microsoft.com",
  "languageCode": "en",
  "state": "Draft",
  "termsAndConditions": {
    "id": "TCS-1234-1234-1234",
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
