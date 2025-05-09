# Terms & Conditions

The Terms object represents terms as a collection of uploaded PDF or DOCX documents or links to externally hosted documents as an element of a product. The object contains the following properties:

<table><thead><tr><th width="133">Field</th><th width="247">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Identifier for the terms. </p><p></p><p>Example: TCS-1234-1234-1234</p></td></tr><tr><td>href</td><td>string</td><td><p>Relative reference to terms to product (/products/{productid}/terms-and-conditions/{termsAndConditionsId} </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">/products/PRD-6822-9898-4256/terms-and-conditions/TCS-3159-1891-0980-8679
</code></pre></td></tr><tr><td>name</td><td>string</td><td><p>Terms name </p><p></p><p>Example: Terms of Service</p></td></tr><tr><td>description</td><td>string</td><td><p>Terms description </p><p></p><p>Example: Terms of Service description</p></td></tr><tr><td>displayOrder</td><td>integer</td><td><p>Terms display order </p><p></p><p>Example: 10</p></td></tr><tr><td>status</td><td><a href="./">Terms &#x26; Conditions States</a></td><td><p>Terms status.</p><p></p><p>Example: draft</p></td></tr><tr><td>product</td><td><a href="../product/">Product</a></td><td>Product to which item is assigned.</td></tr><tr><td>audit</td><td>AuditObject</td><td><p>Audit events: created, updated.  </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="TERMS OBJECT" %}
```json
{
  "id": "TCS-3159-1891-0980-8679",
  "href": "/products/PRD-6822-9898-4256/terms-and-conditions/TCS-3159-1891-0980-8679",
  "name": "Microsoft 365 Terms of Service",
  "description": "Description of Microsoft 365 Terms of Service",
  "displayOrder": 100,
  "state": "Draft",
  "product": {
    "id": "PRD-6822-9898-4256",
    "href": "/products/PRD-6822-9898-4256",
    "name": "Microsoft 365 online services for commercial"
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
{% endtab %}
{% endtabs %}

## TermsVariant <a href="#termsvariant" id="termsvariant"></a>

The `TermsVariant` object represents terms variant as an uploaded PDF or DOCX document or a link to an externally hosted document as an element of terms for a product.

| Field                    | Type                 | Description                                                                                                                                                                                                                                                                                                                                   |
| ------------------------ | -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`id`**                 | string               | <p>Terms Variant identifier.  </p><p></p><p>Example: "TCS-1234-1234-1234-1234"</p>                                                                                                                                                                                                                                                            |
| **`href`**               | string               | <p>Relative reference to the terms item to terms to product (always products/{productId}/terms/{tcid}/terms-item/{termsAndConditionsItemId}) </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">/products/PRD-1234-1234/terms/tcs-1234-1234-1234/terms-item/tcs-1234-1234-1234-1234
</code></pre> |
| **`type`**               | Online or File       | <p>Terms Item type. </p><p></p><p>Example: "Online"</p>                                                                                                                                                                                                                                                                                       |
| **`name`**               | string               | <p>Terms Variant name. </p><p></p><p>Example: "TCS-1234-1234-1234-1234"</p>                                                                                                                                                                                                                                                                   |
| **`description`**        | string               | <p>Terms Variant description. </p><p></p><p>Example: "Terms of Service description in English"</p>                                                                                                                                                                                                                                            |
| **`assetUrl`**           | string               | <p>URL of the terms item uploaded document or or online document/resource. </p><p></p><p>Example: "https://www.test.com/terms-of-service"</p>                                                                                                                                                                                                 |
| **`languageCode`**       | string               | <p>Terms Item 2-digit language code. </p><p></p><p>Example: "en"</p>                                                                                                                                                                                                                                                                          |
| **`status`**             | status               | <p>Terms Item status: Draft</p><p>Pending, Published, Unpublished.</p><p></p><p>Example: "Draft"</p>                                                                                                                                                                                                                                          |
| **`termsAndConditions`** | Terms and conditions | Terms to which item is assigned.                                                                                                                                                                                                                                                                                                              |
| **`audit`**              | AuditObject          | <p>Audit events: created, updated. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre>                                                                                                          |

## Example

{% tabs %}
{% tab title="TERMS VARIANT OBJECT" %}
```json
{
  "id": "TCS-1234-1234-1234-1234",
  "href": "/products/PRD-1234-1234/terms/tcs-1234-1234-1234/terms-item/tcs-1234-1234-1234-1234",
  "name": "Terms and Conditions Variant - EN",
  "description": "Terms and Conditions Variant in English",
  "type": "Online",
  "assetUrl": "https://www.microsoft.com",
  "languageCode": "en",
  "state": "Draft",
  "termsAndConditions": {
    "id": "TCS-1234-1234-1234",
    "href": "/products/PRD-1234-1234/terms/tcs-1234-1234-1234",
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
{% endtab %}
{% endtabs %}
