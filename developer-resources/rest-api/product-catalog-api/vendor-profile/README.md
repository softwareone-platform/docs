# Vendor Profile

The Vendor Profile object represents a vendor in the public catalog.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="156">Field</th><th width="156">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The identifier of the vendor profile. </td></tr><tr><td><code>externalId</code></td><td>string</td><td>The identifier within an external system.</td></tr><tr><td><code>name</code></td><td>string, core</td><td>A user-friendly name of the vendor profile.</td></tr><tr><td><code>icon</code></td><td>string</td><td>Icon to be shown on grids and info cards.</td></tr><tr><td><code>description</code></td><td>string</td><td>A description of the vendor.</td></tr><tr><td><code>featured</code></td><td>bool</td><td>Indicates if this product should be featured on the user interface.</td></tr><tr><td><code>website</code></td><td>string</td><td>A URL to the vendor’s website.</td></tr><tr><td><code>linkedin</code></td><td>string</td><td>A URL to the vendor’s LinkedIn page.</td></tr><tr><td><code>facebook</code></td><td>string</td><td>A URL to the vendor’s Facebook page.</td></tr><tr><td><code>youtube</code></td><td>string</td><td>A URL to the vendor’s YouTube page.</td></tr><tr><td><code>xProfile</code></td><td>string</td><td>A URL to the vendor’s X page.</td></tr><tr><td><code>owner</code></td><td>object</td><td>The vendor <a href="../../accounts-api/account/"><code>account</code></a> that owns this vendor profile, if applicable. The value is  <code>null</code> for unclaimed profiles.</td></tr><tr><td><code>products</code></td><td>object</td><td>Represents the <a href="../product-profile/"><code>productProfile</code></a> object.</td></tr><tr><td><code>categories</code></td><td>object</td><td>Represents the <a href="../category/"><code>category</code></a> that owns this object </td></tr><tr><td><code>status</code></td><td>string, core</td><td>Indicates whether the item is <code>draft</code>, <code>published</code>, <code>unpublished</code>, or <code>deleted</code>. </td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>revision</code></td><td>integer, core</td><td>The revision number of the entity.</td></tr></tbody></table>

## Example

{% code title="VENDOR PROFILE OBJECT" lineNumbers="true" %}
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
