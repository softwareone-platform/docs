# Parameter Group

## Parameter Group object

| Field          | Type                   | Description                                                                                                                                                                                                                              |
| -------------- | ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id             | string                 | <p>Platform </p><p>generated ID. </p><p></p><p>Example: "PGR-6790-8304-0001"</p>                                                                                                                                                         |
| href           | string                 | <p>Relative reference to object on API (always <code>/products/{product-id}/parameter-groups/{id}</code>). </p><p></p><p>Example: "/products/PRD-6790-8304-0171/parameter-groups/PGR-6790-8304-0001"</p>                                 |
| name           | string                 | <p>Name of the group. </p><p></p><p>Example: "Parameters"</p>                                                                                                                                                                            |
| label          | string                 | <p>Label displayed in the wizard steps selector. </p><p></p><p>Example: "Create agreement"</p>                                                                                                                                           |
| description    | string                 | <p>Description of the group. </p><p></p><p>Example: "When creating a new agreement with SoftwareOne, you have the option to establish a new Microsoft account or connect it to an existing account you already hold with Microsoft."</p> |
| displayOrder   | integer                | <p>Defines the display order. </p><p></p><p>Example: "100"</p>                                                                                                                                                                           |
| default        | boolean                | <p>Marks the default item group. </p><p></p><p>Example: "true"</p>                                                                                                                                                                       |
| parameterCount | integer                | <p>The number of parameters in the group. </p><p></p><p>Example: "5"</p>                                                                                                                                                                 |
| product        | [Product](../product/) | Reference to [Product ](../product/)object.                                                                                                                                                                                              |

## Example

{% tabs %}
{% tab title="Parameter Group Object" %}
```json
{
    "id": "PGR-6790-8304-0001",
    "href": "/products/PRD-6790-8304/parameter-groups/PGR-6790-8304-0001",
    "title": "Parameters",
    "label": "Create agreement",
    "description": "When creating a new agreement with SoftwareOne, you have the option to establish a new Microsoft account or connect it to an existing account you already hold with Microsoft.",
    "displayOrder": 100,
    "default": true,
    "product": {
        "id": "PRD-6790-8304-0171"
    }
}
```
{% endtab %}
{% endtabs %}
