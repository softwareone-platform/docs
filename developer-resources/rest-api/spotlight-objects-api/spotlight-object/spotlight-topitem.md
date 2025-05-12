# Spotlight TopItem

The SpotlightTopItem represents references to the platform objects picked up by SpotlightQuery.

The SpotlightTopItem is used to provide data to the frontend template. It includes both core properties and object-specific properties. Spotlight operates as a service that is object-agnostic, meaning it does not maintain the schema of domain objects. The SpotlightTopItem contract is a result of a downstreamed RQL query and is utilized as is in a JSON string. This indicates that the list of properties is object-specific and may change depending on the RQL query executed.

<table><thead><tr><th width="245">Field</th><th width="203">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td>The core unique identifier for each item.</td></tr><tr><td>href</td><td><code>string</code></td><td>Relative reference to object on API.</td></tr><tr><td>{object-specific-properties}</td><td><code>string</code></td><td>List of object specific properites, as a result of downstreamed RQL query.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="SPOTLIGHT TOPITEM" %}
```json
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
```
{% endtab %}
{% endtabs %}
