# Vendor Profile

The Vendor Profile object represents a vendor in the public catalog.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="156">Field Name</th><th width="169">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The identifier of the vendor profile. </p><p>Example: VNP-1671-3887</p></td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>The identifier within an external system.</p><p>Example: arK9uX45</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>A user-friendly name of the vendor profile.</p><p>Example: Microsoft</p></td></tr><tr><td><code>icon</code></td><td>string</td><td><p>Icon to be shown on grids and info cards.</p><p>Example: /v1/public-catalog/vendor-profiles/VNP-1671-3887/icon</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the vendor.</p><p>Example: Sells Enterprise</p></td></tr><tr><td><code>featured</code></td><td>bool</td><td><p>Indicates if this product should be featured on the user interface.</p><p>Example: False</p></td></tr><tr><td><code>website</code></td><td>string</td><td><p>A URL to the vendor’s website.</p><p>Example: www.microsoft.com</p></td></tr><tr><td><code>linkedin</code></td><td>string</td><td><p>A URL to the vendor’s LinkedIn page.</p><p>Example: www.linkedin.com/microsoft</p></td></tr><tr><td><code>facebook</code></td><td>string</td><td><p>A URL to the vendor’s Facebook page.</p><p>Example: www.facebook.com/microsoft</p></td></tr><tr><td><code>youtube</code></td><td>string</td><td><p>A URL to the vendor’s YouTube page.</p><p>Example: www.youtube.com/microsoft</p></td></tr><tr><td><code>xProfile</code></td><td>string</td><td><p>A URL to the vendor’s X page.</p><p>Example: www.x.com/microsoft</p></td></tr><tr><td><code>owner</code></td><td>object</td><td><p>The vendor <a href="../../accounts-api/account/"><code>account</code></a> that owns this vendor profile, if applicable. The value is  <code>null</code> for unclaimed profiles.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "ACC-6881-3912",
    "name": "Microsoft",
    "icon": "/v1/accounts/accounts/ACC-6881-3912/icon",
    "revision": 1,
    "type": "Vendor",
    "status": "Enabled"
}
</code></pre></td></tr><tr><td><code>products</code></td><td>object (<a href="../product-profile/"><code>productProfile</code></a>)</td><td><p> Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "PRP-1671-3887",
    "name": "Office",
    "icon": "/v1/public-catalog/product-profiles/PRP-1671-3887/icon",
    "revision": 2
  }
]
</code></pre></td></tr><tr><td><code>categories</code></td><td>object</td><td><p>Reference to the <a href="../category/"><code>categor</code>y</a> that owns this object </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json"> "categories": [
        {
            "id": "CAT-1671-3887",
            "name": "Development",
            "revision": 1,
            "status": "Published"
        }
    ]
</code></pre></td></tr><tr><td><code>status</code></td><td>string</td><td>Indicates whether the item is <code>draft</code>, <code>published</code>, <code>unpublished</code>, or <code>deleted</code>. </td></tr><tr><td><code>audit</code></td><td>object</td><td><p>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
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
      "revision": 1,
      "name": "My token"
    },
  "deleted": {
    "at": "2024-05-17T09:17:36.406Z",
    "by": {
      "id": "TKN-3836-7769",
      "revision": 1,
      "name": "My token"
    }
  }
}
</code></pre></td></tr><tr><td><code>revision</code></td><td>integer</td><td><p>The revision number of the entity.</p><p>Example: 3</p></td></tr></tbody></table>

## Example response <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
{
  "id": "VNP-1671-3887",
  "externalId": "arK9uX45", --??
  "name": "Microsoft",
  "icon": "/v1/public-catalog/vendor-profiles/VNP-1671-3887/icon",
  "description": "Provides enterprise software",
  "website": "www.microsoft.com",
  "linkedin": "www.linkedin.com/microsoft",
  "facebook": "www.facebook.com/microsoft",
  "xProfile": "www.x.com/microsoft",
  "youtube": "www.youtube.com/microsoft",
  "featured": false,
  "categories": [],
  "status": "Published",
  "revision": 2,
  "owner": {
    "id": "ACC-6881-3912",
    "name": "Microsoft",
    "icon": "/v1/accounts/accounts/ACC-6881-3912/icon",
    "revision": 1,
    "type": "Vendor",
    "status": "Enabled"
  },
  "products": [
    {
      "id": "PRP-1671-3887",
      "name": "Office",
      "icon": "/v1/public-catalog/product-profiles/PRP-1671-3887/icon",
      "revision": 2
    }
  ],
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
        "revision": 1,
        "name": "My token"
      },
    "deleted": {
      "at": "2024-05-17T09:17:36.406Z",
      "by": {
        "id": "TKN-3836-7769",
        "revision": 1,
        "name": "My token"
      }
    }
  }
}
```
{% endcode %}

