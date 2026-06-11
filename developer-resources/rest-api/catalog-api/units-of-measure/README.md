# Unit of Measure

The Unit of Measure object allows SoftwareOne associates to add and manage units of measure and assign a unique ID to each unit type. Vendors can also access the available unit types.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="150">Field</th><th width="163">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) A primary unit of measure identifier. </td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>description</code></td><td>string</td><td>A description of the unit of measure. </td></tr><tr><td><code>name</code></td><td>string</td><td>(Read-only) The name of the unit of measure. </td></tr></tbody></table>

## Example

{% code title="UNIT OF MEASURE OBJECT" overflow="wrap" lineNumbers="true" %}
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
  "description": "A person who utilizes the service",
  "name": "User"
}
```
{% endcode %}
