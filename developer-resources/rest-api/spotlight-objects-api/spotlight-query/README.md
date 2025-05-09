# Spotlight Query

A SpotlightQuery defines the RQL query used to retrieve spotlighted objects from a collection.

<table><thead><tr><th width="208">ID</th><th width="203">type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Unique ID for the query itself. </p><p></p><p>Example: SPQ-9878-8864</p></td></tr><tr><td>name</td><td>string</td><td>Name of the query (core property).</td></tr><tr><td>template</td><td>string</td><td>Name of the UI template used to render data (core property)</td></tr><tr><td>invalidation</td><td>Invalidation structure</td><td>Settings for invalidating cached data.</td></tr><tr><td>interval</td><td>string</td><td>Interval for invalidating cached data.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="SPOTLIGHT QURERY" %}
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
{% endtab %}
{% endtabs %}
