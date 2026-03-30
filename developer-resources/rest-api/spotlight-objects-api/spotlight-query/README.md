# Spotlight Query

A Spotlight Query defines the RQL query used to retrieve spotlighted objects from a collection.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="174">Field Name</th><th width="184">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The unique ID for the query itself. </p><p>Example: SPQ-9878-8864</p></td></tr><tr><td><code>name</code></td><td>string</td><td>The name of the query (core property).</td></tr><tr><td><code>template</code></td><td>string</td><td>The name of the UI template used to render data (core property).</td></tr><tr><td><code>invalidation</code></td><td>invalidationStructure</td><td>Settings for invalidating cached data.</td></tr><tr><td><code>interval</code></td><td>string</td><td>Interval for invalidating cached data.</td></tr></tbody></table>

### Example response

{% code lineNumbers="true" %}
```json
{
  "id": "SPQ-1234-2345",
  "name": "Saved Orders",
  "template": "savedOrdersClient"
  "invalidation": {
    "interval": "1:00:00"
  }
}
```
{% endcode %}
