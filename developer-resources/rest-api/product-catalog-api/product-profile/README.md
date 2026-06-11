# Product Profile

The Product Profile object represents a product in the public catalog.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="174">Field</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>The identifier of the product profile. </td></tr><tr><td><code>externalId</code></td><td>string</td><td>The identifier within an external system. </td></tr><tr><td><code>name</code></td><td>string, core</td><td>A user-friendly name of the product profile.</td></tr><tr><td><code>icon</code></td><td>string</td><td>The icon to be shown in grids and information cards.</td></tr><tr><td><code>shortDescription</code></td><td>string</td><td>A short description of the product. </td></tr><tr><td><code>longDescription</code></td><td>string</td><td>A long description of the product.</td></tr><tr><td><code>featured</code></td><td>bool</td><td>Indicates whether this product should be featured on the UI. </td></tr><tr><td><code>website</code></td><td>string</td><td>A URL to the vendor’s website.</td></tr><tr><td><code>linkedin</code></td><td>string</td><td>A URL to the vendor’s LinkedIn page.</td></tr><tr><td><code>facebook</code></td><td>string</td><td>A URL to the vendor’s Facebook page.</td></tr><tr><td><code>youtube</code></td><td>string</td><td>A URL to the vendor’s Facebook page.</td></tr><tr><td><code>xProfile</code></td><td>string</td><td>A URL to the vendor’s X page.</td></tr><tr><td><code>categories</code></td><td>object</td><td><p>Represents the <a href="../../notifications-api/categories/"><code>category</code></a> that owns this object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "categories": [
    {
      "id": "CAT-1671-3887",
      "name": "Development",
      "revision": 1,
      "status": "Published"
    }
  ]
}
</code></pre></td></tr><tr><td><code>industries</code></td><td>object</td><td><p>Represents the <a href="../industry/"><code>industry</code></a> that owns this object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "industries": [
    {
      "id": "IND-8249-7679",
      "name": "Development",
      "revision": 1,
      "status": "Published"
    }
  ]
}
</code></pre></td></tr><tr><td><code>segments</code></td><td>object</td><td><p>Represents the <a href="../segment/"><code>segment</code></a> that owns this object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">"segments": [
  {
            "id": "SEG-1671-3887",
            "name": "Development",
            "revision": 1,
            "status": "Published"
        }
</code></pre></td></tr><tr><td><code>vendorProfiles</code></td><td>object</td><td><p>Represents the <a href="../vendor-profile/"><code>vendorProfile</code></a> that owns this object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "vendorProfiles": [
    {
      "id": "VNP-1671-3887",
      "icon": "/v1/public-catalog/vendor-profiles/VNP-1671-3887/icon",
      "name": "Microsoft",
      "status": "Draft"
    }
  ]
}
</code></pre></td></tr><tr><td><code>platformProducts</code></td><td>object</td><td>Indicates <a href="../../catalog-api/product/"><code>products</code></a> that have been linked to this profile. </td></tr><tr><td><code>status</code></td><td>string</td><td>Indicates whether the product is <code>draft</code>, <code>published</code>, <code>unpublished</code>, or <code>deleted</code>.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>revision</code></td><td>integer, core</td><td>The entity's revision number. </td></tr></tbody></table>

## Example

{% code title="PRODUCT PROFILE OBJECT" lineNumbers="true" %}
```json
{
  "id": "PRP-1671-3887",
  "externalId": "arK9uX45",
  "name": "Office",
  "vendorProfile": {
    "id": "VNP-1671-3887",
    "icon": "/v1/public-catalog/vendor-profiles/VNP-1671-3887/icon",
    "name": "Microsoft"
  },
  "shortDescription": "Enterprise productivity suite",
  "longDescription": "Enterprise productivity suites are cloud-based software packages designed to streamline communication.",
  "website": "https://www.microsoft.com/office",
  "linkedin": "https://www.linkedin.com/microsoft-office",
  "facebook": "https://www.facebook.com/microsoft-office",
  "xProfile": "https://www.x.com/microsoft-office",
  "youtube": "https://www.youtube.com/microsoft-office",
  "termsLink": "https://info.here",
  "featured": false,
  "categories": [],
  "industries": [],
  "segments": [],
  "vendorProfiles": [],
  "platformProducts": [
    {
      "id": "PRD-0049-1332",
      "name": "Microsoft Office",
      "icon": "/v1/catalog/products/PRD-0049-1332/icon",
      "revision": 2,
      "externalIds": {
        "operations": "123"
      },
      "status": "Published"
    }
  ],
  "status": "Published",
  "icon": "/v1/public-catalog/product-profiles/PRP-1671-3887/icon",
  "revision": 2,
  "audit": {
    "created": {
      "at": "2024-04-08T06:30:05.807Z",
      "by": {
        "id": "USR-2172-2499",
        "revision": 1,
        "name": "John User"
      }
    },
    "updated": {
      "at": "2024-05-16T09:17:36.406Z",
      "by": {
        "id": "TKN-3836-7769",
        "revision": 2,
        "name": "My token"
      }
    },
    "deleted": {
      "at": "2024-05-17T09:17:36.406Z",
      "by": {
        "id": "TKN-3836-7769",
        "revision": 3,
        "name": "My token"
      }
    }
  }
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
