# SpotlightObject

The Spotlight Object represents a collection of spotlighted objects and their definition, along with the RQL query used to retrieve items.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="134">Field Name</th><th width="223">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The unique identifier for the spotlight object in this format: </p><p>Example: SPO-1234-5678-9547-1234-8888</p></td></tr><tr><td><code>query</code></td><td>object</td><td>A reference to the <a href="../spotlight-query/">spotlightQuery</a> object.</td></tr><tr><td><code>top</code></td><td><a href="spotlight-topitem.md">spotlightTopItem</a></td><td>A list of the top five objects returned by the downstreamed RQL query.</td></tr><tr><td><code>total</code></td><td>integer</td><td>The total number of objects available for downstream RQL.</td></tr><tr><td><code>audit</code></td><td>object</td><td><p>The <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. This object keeps track of changes to the spotlight object. Mainly when the cache key was refreshed for the last time, and by whom the action was initiated.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "updated": {
    "at": "2024-05 28T09:00:22.945Z",
}
</code></pre></td></tr></tbody></table>

## Example response <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
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
