# Variant

The Variant object represents a variant as an uploaded PDF or DOCX document or a link to an externally hosted document as an element of terms for a product.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-search="false"><thead><tr><th width="205">Field</th><th width="146">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) A unique identifier for the terms variant.</td></tr><tr><td><code>type</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>The type of terms variant.</td></tr><tr><td><code>name</code></td><td>string, core</td><td>A name for the terms variant.</td></tr><tr><td><code>description</code></td><td>string, core</td><td>A description of the terms variant.</td></tr><tr><td><code>assetUrl</code></td><td>string, core</td><td>The URL of the uploaded document or online document/resource.</td></tr><tr><td><code>languageCode</code></td><td>string, core</td><td>The 2-digit language code for the terms item.</td></tr><tr><td><code>status</code></td><td>string, core</td><td>The status of the terms.</td></tr><tr><td><code>termsAndConditions</code></td><td>string</td><td>The terms to which the item has been assigned.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Example

{% code title="VARIANT OBJECT" overflow="wrap" lineNumbers="true" %}
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
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
