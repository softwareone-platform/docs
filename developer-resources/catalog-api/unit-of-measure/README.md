# Unit of Measure

## Unit of Measure object

The Unit of Measure element allows Operations Associates the ability to add and manage units of measures, along with assigning each unit type a unique Unit Type ID. The Unit of Measure Module will allow Vendors options of available unit types.

| Field       | Type                                                                                                            | Description                                                                                                                                                         |
| ----------- | --------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id          | string                                                                                                          | <p>Primary unit of measure identifier. </p><p></p><p>Example: "UNT-7362"</p>                                                                                        |
| href        | string                                                                                                          | <p>Relative reference to object on API (always<code>/units-of-measure/{id}</code>). </p><p></p><p>Example: "/v1/units-of-measure/UNT-7362"</p>                      |
| audit       | [AuditObject](https://softwareone.atlassian.net/wiki/spaces/GPTEAM/pages/5216272944/API+Components#AuditObject) | Audit object with possible entries: created, updated, activated, terminated, according to lifecycle of the object. Possible audit events: **created**, **updated.** |
| description | string                                                                                                          | <p>Description of unit of measure. </p><p></p><p>Example: "A person who utilises the service"</p>                                                                   |
| name        | string                                                                                                          | <p>Name of unit of measure. </p><p></p><p>Example: "User"</p>                                                                                                       |

## Example

{% tabs %}
{% tab title="UNIT OF MEASURE OBJECT" %}
```
{
  "id": "UNT-7362",
  "href": "/v1/units-of-measure/UNT-7362",
  "audit": {
    "created": {
      "at": "<dateTime>",
      "by": {
        "id": "<string>"
      }
    },
    "updated": {
      "at": "<dateTime>",
      "by": {
        "id": "<string>"
      }
    }
  },
  "description": "A person who utilises the service",
  "name": "User
}
```
{% endtab %}
{% endtabs %}
