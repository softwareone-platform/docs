# Category

The Category object represents a software category or sub-category. It is used to classify software in the Public Catalog.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="179">Field Name</th><th width="166">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>An identifier for the category.</p><p>Example: CAT-1671-3887</p></td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>Identifier in the external system.</p><p>Example: arK9uX45</p></td></tr><tr><td><code>parentCategory</code></td><td>category</td><td><p>A reference to the parent <a href="../../extensions-api/category/">category</a>. If <code>null</code>, then this is a top-level category. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "CAT-1670-0003",
  "name": "Productivity"
}
</code></pre></td></tr><tr><td><code>name</code></td><td>string</td><td><p>A user-friendly name of the category.</p><p>Example: Development</p></td></tr><tr><td><code>icon</code></td><td>string</td><td><p>Icon to be shown on grids and info cards </p><p>Example: /v1/public-catalog/product-profiles/PRP-1671-3887/icon</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A short description of the category </p><p>Example: Software development tools</p></td></tr><tr><td><code>longDescription</code></td><td>string</td><td><p>A long description of the category </p><p>Example: Tools used to build and test software</p></td></tr><tr><td><code>featured</code></td><td>bool</td><td><p>Indicates whether this product should be featured on the UI. </p><p>Example: false</p></td></tr><tr><td><code>status</code></td><td>string</td><td>Indicates the status of the category. Allowed values: <code>draft</code>, <code>published</code>, <code>unpublished</code>, or <code>deleted</code>.</td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>revision</code></td><td>integer</td><td><p>The entity's revision number.</p><p>Example: 3</p></td></tr></tbody></table>

## Example response <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
{
  "id": "CAT-1671-3887",
  "externalId": "arK9uX45", -- ??
  "name": "Development",
  "parentCategory": {
    "id": "CAT-1671-3886",
    "name": "Productivity"
  },
  "description": "Software development tools",
  "longDescription": "Used to build and test software", --TO remove
  "featured": false, --TO remove
  "icon": "/v1/public-catalog/categories/CAT-1671-3887/icon", --TO remove
  "status": "Draft",
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
