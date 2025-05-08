# Spotlight TopItem

SpotlightTopItem represents spotlighted items picked up by SpotlightQuery, and it's used to feed the frontend template with data. It contains core properties and object-specific properties

Spotlight as a service is object-agnostic in terms of not keeping track of the domain object schema. SpotlightTopItem contract is a result of a downstreamed RQL query and is taken as is (JSON string).&#x20;

This means that the list of properties is object-specific and may change depending on the executed RQL query.

<table data-header-hidden><thead><tr><th>Field</th><th width="203">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>The core unique identifier for each item.</td></tr><tr><td>href</td><td>string</td><td>Relative reference to object on API.</td></tr><tr><td>{object-specific-properties}</td><td>string</td><td>List of object specific properites, as a result of downstreamed RQL query.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="Spotlight TopItem" %}
{% code lineNumbers="true" %}
```json
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
```
{% endcode %}
{% endtab %}
{% endtabs %}
