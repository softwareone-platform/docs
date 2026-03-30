# Unit of Measure

The Unit of Measure object allows SoftwareOne associates to add and manage units of measure and assign a unique ID to each unit type. Vendors can also access the available unit types.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="150">Field Name</th><th width="163">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>A primary unit of measure identifier. </p><p>Example: UNT-7362</p></td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the unit of measure. </p><p>Example: A person who utilizes the service.</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the unit of measure. </p><p>Example: User</p></td></tr></tbody></table>

## Example response

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
