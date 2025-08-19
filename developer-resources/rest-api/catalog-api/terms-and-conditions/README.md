# Terms

The Terms and Conditions object represents terms as a collection of uploaded PDF or DOCX documents or links to externally hosted documents as an element of a product. The object contains the following properties:

<table><thead><tr><th width="133">Field</th><th width="138">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The identifier for the terms.</p><p>Example: TCS-1234-1234-1234</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>A relative reference to the terms. </p><p>Example:</p><pre class="language-json"><code class="lang-json">/products/PRD-6822-9898-4256/terms-and-conditions/TCS-3159-1891-0980-8679
</code></pre></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name for the terms.</p><p>Example: Terms of Service</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>A description of the terms.</p><p>Example: Terms of Service description</p></td></tr><tr><td>displayOrder</td><td><code>integer</code></td><td><p>The display order for the terms.</p><p>Example: 10</p></td></tr><tr><td>status</td><td><code>string</code></td><td><p>The status of the terms. </p><p>Example: Draft</p></td></tr><tr><td>product</td><td><a href="../product/"><code>product</code></a></td><td>The product to which the item is assigned.</td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the Audit object. </td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="TERMS OBJECT" %}
{% code lineNumbers="true" %}
```json
{
  "id": "TCS-3159-1891-0980-8679",
  "name": "Microsoft 365 Terms of Service",
  "description": "Description of Microsoft 365 Terms of Service",
  "displayOrder": 100,
  "state": "Draft",
  "product": {
    "id": "PRD-6822-9898-4256",
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
{% endcode %}
{% endtab %}
{% endtabs %}
