# Category

The Category object represents a software category or sub-category. It is used to classify software in the Public Catalog.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="179">Field</th><th width="119">Type</th><th width="119">Core field</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>core</td><td>(Read-only) An identifier for the category.</td></tr><tr><td><code>externalId</code></td><td>string</td><td>–</td><td>Identifier in the external system.</td></tr><tr><td><code>parentCategory</code></td><td>object</td><td>–</td><td>Represents the parent <a href="../../extensions-api/category/"><code>category</code></a>. If <code>null</code>, then this is a top-level category. </td></tr><tr><td><code>name</code></td><td>string, core</td><td>core</td><td>A user-friendly name of the category.</td></tr><tr><td><code>icon</code></td><td>string, core</td><td>core</td><td>Icon to be shown on grids and info cards </td></tr><tr><td><code>description</code></td><td>string</td><td>–</td><td>A short description of the category </td></tr><tr><td><code>longDescription</code></td><td>string</td><td>–</td><td>A long description of the category </td></tr><tr><td><code>featured</code></td><td>bool</td><td>–</td><td>Indicates whether this product should be featured on the UI. </td></tr><tr><td><code>status</code></td><td>string, core</td><td>core</td><td><p>Indicates the status of the category. Allowed values are</p><ul><li><code>Draft</code></li><li><code>Published</code></li><li><code>Unpublished</code></li><li><code>Deleted</code></li></ul></td></tr><tr><td><code>audit</code></td><td>object</td><td>–</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>revision</code></td><td>integer, core</td><td>core</td><td>The entity's revision number.</td></tr></tbody></table>

## Example

{% code title="CATEGORY OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "CAT-1671-3887",
  "externalId": "arK9uX45",
  "name": "Development",
  "parentCategory": {
    "id": "CAT-1671-3886",
    "name": "Productivity"
  },
  "description": "Software development tools",
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
