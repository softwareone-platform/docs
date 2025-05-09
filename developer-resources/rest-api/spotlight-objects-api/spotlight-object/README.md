# Spotlight Object

A SpotlightObject represents an instance of spotlighted objects collections and its definition, along with RQL query definition used to retrieve items.

<table><thead><tr><th width="166">Field</th><th width="223">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>The unique identifier for the spotlight object in this format: SPO-&#x3C;QQQQ>-&#x3C;QQQQ>-&#x3C;XXXX>-&#x3C;XXXX>-&#x3C;XXXX></td></tr><tr><td>query</td><td><a href="../spotlight-query/">SpotlightQuery</a></td><td>The spotlight query object.</td></tr><tr><td>top</td><td>List&#x3C;<a href="spotlight-topitem.md">SpotlightTopItem</a>></td><td>List of the top 5 objects returned by the downstreamed RQL query.</td></tr><tr><td>total</td><td>int</td><td>Total number of objects available for downstream RQL.</td></tr><tr><td>audit</td><td>AuditObject</td><td><p>The audit information object. This object keeps track of changes to the spotlight object. Mainly when the cache key was refreshed for the last time, and by whom the action was initiated. </p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "updated": {
    "at": "2024-05-28T09:00:22.945Z",
}blic/accounts/acc-8989-32321.jpg",
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
      "href": "/public/v1/commerce/orders/ORD-6637-5331-9984",
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
