# Units of Measure

The Unit of Measure object allows SoftwareOne associates to add and manage units of measure and assign a unique ID to each unit type. Vendors can also access the available unit types.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="150">Field</th><th width="163">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>A primary unit of measure identifier. </p><p>Example: UNT-7362</p></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the Audit object.</td></tr><tr><td>description</td><td><code>string</code></td><td><p>A description of the unit of measure. </p><p>Example: A person who utilizes the service.</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the unit of measure. </p><p>Example: User</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="UNIT OF MEASURE" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "UNT-7362", 
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
{% endcode %}
{% endtab %}
{% endtabs %}
