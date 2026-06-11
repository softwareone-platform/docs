# Spotlight

The Spotlight object represents a collection of spotlighted objects and their definition, along with the RQL query used to retrieve items.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="134">Field</th><th width="175">Type</th><th width="391">Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>The unique identifier for the spotlight object.</td></tr><tr><td><code>query</code></td><td>object</td><td>Represents the <a href="../spotlight-query/">spotlightQuery</a> object.</td></tr><tr><td><code>top</code></td><td><a href="spotlight-topitem.md">spotlightTopItem</a></td><td>A list of the top five objects returned by the downstreamed RQL query.</td></tr><tr><td><code>total</code></td><td>integer</td><td>The total number of objects available for downstream RQL.</td></tr><tr><td><code>audit</code></td><td>object</td><td>Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object, which tracks changes to the spotlight object. For example, when the cache key was last refreshed and who initiated the action.</td></tr></tbody></table>

## Example

{% code title="SPOTLIGHT OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "SPO-1234-5678-9012-3456-7890",
  "query": {
    "id": "SPQ-1234-2345",
    "name": "Saved Orders",
    "template": "savedOrdersClient"
  },
  "top": [
    {
      "id": "ORD-6637-5331-9984",
      "audit": {
        "updated": {
          "at": "2024-05-28T09:00:22.945Z"
        }
      },
      "icon": "/public/v1/catalog/products/PRD-6523-2229/icon",
      "name": "Order ORD-8373-6076-7130"
    }
  ],
  "total": 1,
  "audit": {
    "updated": {
      "at": "2024-05-28T09:00:22.945Z"
    }
  }
}
```
{% endcode %}
