# Spotlight Object

The Spotlight Object represents a collection of spotlighted objects and their definition, along with the RQL query used to retrieve items.

<table><thead><tr><th width="166">Field</th><th width="223">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The unique identifier for the spotlight object in this format: </p><p>Example: SPO-1234-5678-9547-1234-8888</p></td></tr><tr><td>query</td><td><a href="../spotlight-query/"><code>spotlightQuery</code></a></td><td>A reference to the spotlight query object.</td></tr><tr><td>top</td><td><a href="spotlight-topitem.md"><code>spotlightTopItem</code></a></td><td>A list of the top five objects returned by the downstreamed RQL query.</td></tr><tr><td>total</td><td><code>integer</code></td><td>The total number of objects available for downstream RQL.</td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td><p>The audit information object. This object keeps track of changes to the spotlight object. Mainly when the cache key was refreshed for the last time, and by whom the action was initiated.</p><p>Example:</p><pre class="language-json"><code class="lang-json">{
  "updated": {
    "at": "2024-05 28T09:00:22.945Z",
}
</code></pre></td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% tabs %}
{% tab title="SPOTLIGHT OBJECT" %}
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
{% endtab %}
{% endtabs %}
