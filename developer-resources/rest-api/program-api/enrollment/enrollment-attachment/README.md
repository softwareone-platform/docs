# Enrollment Attachment

The `enrollmentAttachment` object provides the ability to upload an enrollment attachment (via file upload or license key) to the enrollment object.

{% include "../../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="180">Field Name</th><th width="152">Data Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The primary identifier of the attachment. </p><p>Example: ATT-0001-0001-0001-001</p></td></tr><tr><td>href</td><td><code>string</code></td><td> A reference to attachment within the API. </td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the <code>attachment</code> object.  </p><p>Example: Guide to establishing a reseller relationship</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>The description of the <code>attachment</code> object. </p><p>Example: Learn what happens when you establish a reseller relationship with SoftwareOne</p></td></tr><tr><td>type</td><td><code>string</code></td><td><p>The type of the <code>attachment</code> object. </p><p>Example: File</p></td></tr><tr><td>reference</td><td><code>string</code></td><td><p>The URI to access the <code>attachment</code> object. </p><p>Example: microsoft-agreement-certification.pdf</p></td></tr><tr><td>order</td><td><code>order</code></td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "ORD-5542-1187-3130-0991",
    "href": "/commerce/orders/ORD-5542-1187-3130-0991"
}
</code></pre></td></tr><tr><td>audit</td><td><a href="../../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the <code>audit</code> object. </td></tr></tbody></table>

### Example

{% code lineNumbers="true" %}
```json
{
    "id": "ATT-0001-0001-0001-0001",
    "href": "v1/catalog/enrollment/attachment/ATT-0001-0001-0001-0001",
    "name": "Guide to establishing a reseller relationship",
    "description": "Learn what happens when you establish a reseller relationship with SoftwareOne",
    "type": "File",
    "reference": "microsoft-agreement-certification.pdf",
    "order": {
        "id": "ORD-5542-1187-3130-0991",
        "href": "/commerce/orders/ORD-5542-1187-3130-0991"
    },
    "audit": {
     "created": { "at": "...", "by": { } },
     "updated": { "at": "...", "by": { } }
   }
  }
```
{% endcode %}
