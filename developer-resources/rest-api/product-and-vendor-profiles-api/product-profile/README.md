# Product Profile

The Product Profile object represents a product in the public catalog.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="165">Field Name</th><th width="146">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The identifier of the product profile. </p><p>Example: PRP-1671-3887</p></td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>The identifier within an external system. </p><p>Example: arK9uX45</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>A user-friendly name of the product profile.</p><p>Example: Microsoft</p></td></tr><tr><td><code>icon</code></td><td>string</td><td>The icon to be shown in grids and information cards. Example: /v1/public-catalog/product-profiles/PRP-1671-3887/icon</td></tr><tr><td><code>shortDescription</code></td><td>string</td><td><p>A short description of the product. </p><p>Example: Enterprise productivity suite</p></td></tr><tr><td><code>longDescription</code></td><td>string</td><td><p>A long description of the product.</p><p>Example: Enterprise productivity suites are cloud-based software packages designed to streamline communication.</p></td></tr><tr><td><code>featured</code></td><td>bool</td><td><p>Indicates whether this product should be featured on the UI. </p><p>Example: False</p></td></tr><tr><td><code>website</code></td><td>string</td><td><p>A URL to the vendor’s website.</p><p>Example: www.microsoft.com</p></td></tr><tr><td><code>linkedin</code></td><td>string</td><td><p>A URL to the vendor’s LinkedIn page.</p><p>Example: www.linkedin.com/microsoft-office</p></td></tr><tr><td><code>facebook</code></td><td>string</td><td><p>A URL to the vendor’s Facebook page.</p><p>Example: www.facebook.com/microsoft-office</p></td></tr><tr><td><code>youtube</code></td><td>string</td><td><p>A URL to the vendor’s Facebook page.</p><p>Example: www.youtube.com/micromicrosoft-officesoft</p></td></tr><tr><td><code>xProfile</code></td><td>string</td><td><p>A URL to the vendor’s X page.</p><p>Example: www.x/microsoft-office</p></td></tr><tr><td><code>categories</code></td><td>object</td><td><p>A reference to the <a href="../../notifications-api/categories/"><code>category</code></a> that owns this object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json"> "categories": [
        {
            "id": "CAT-1671-3887",
            "name": "Development",
            "revision": 1,
            "status": "Published"
        }
    ]
</code></pre></td></tr><tr><td><code>industries</code></td><td>object</td><td><p>A reference to the <a href="../industry/"><code>industry</code></a> that owns this object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">"industries": [
  {
            "id": "IND-8249-7679",
            "name": "Development",
            "revision": 1,
            "status": "Published"
        }
</code></pre></td></tr><tr><td><code>segments</code></td><td>object</td><td><p>A reference to the <a href="../segment/"><code>segment</code></a> that owns this object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">"segments": [
  {
            "id": "SEG-1671-3887",
            "name": "Development",
            "revision": 1,
            "status": "Published"
        }
</code></pre></td></tr><tr><td><code>vendorProfiles</code></td><td>object</td><td><p>Reference to the <a href="../vendor-profile/"><code>vendorProfile</code></a> that owns this object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">"vendorProfiles": [{
    "id": "VNP-1671-3887",
    "icon": "/v1/public-catalog/vendor-profiles/VNP-1671-3887/icon"
    "name": "Microsoft",

     "status": "Draft"
  }]
</code></pre></td></tr><tr><td><code>platformProducts</code></td><td>object</td><td><p>Indicates <a href="../../catalog-api/product/"><code>products</code></a> that have been linked to this profile. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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
]
</code></pre></td></tr><tr><td><code>status</code></td><td>string</td><td>Indicates whether the product is <code>draft</code>, <code>published</code>, <code>unpublished</code> , or <code>deleted</code>.</td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>revision</code></td><td>integer</td><td><p>The entity's revision number. </p><p>Example: 3</p></td></tr></tbody></table>

## Example response <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
{
  "id": "PRP-1671-3887",
  "externalId": "arK9uX45",
  "name": "Office",
  "vendorProfile": {
    "id": "VNP-1671-3887",
    "icon": "/v1/public-catalog/vendor-profiles/VNP-1671-3887/icon"
    "name": "Microsoft"
  }
  "shortDescription": "Enterprise productivity suite",
  "longDescription": "Enterprise productivity suites are cloud-based software packages designed to streamline communication.",
  "website": "www.microsoft.com/office",
  "linkedin": "www.linkedin.com/microsoft-office",
  "facebook": "www.facebook.com/microsoft-office",
  "xProfile": "www.x.com/microsoft-office",
  "youtube": "www.youtube.com/microsoft-office",
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
