# User Group

The User Group object represents a group containing users.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="159">Field</th><th width="152">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) Primary identifier for the group.</td></tr><tr><td><code>icon</code></td><td>string</td><td>(Optional) The relative path to the group's icon image or logo.</td></tr><tr><td><code>name</code></td><td>string, core</td><td>The name of the group.</td></tr><tr><td><code>description</code></td><td>string</td><td>(Optional) A description of the group.</td></tr><tr><td><code>modules</code></td><td>object</td><td>(Optional) Represents the <a href="../module/#module-object"><code>modules</code></a> object, which contains modules that the group members can access. </td></tr><tr><td><code>default</code></td><td>bool</td><td>Indicates if the group has been set as a default group within the account. An account can contain only one default group.</td></tr><tr><td><code>users</code></td><td>object</td><td>(Read-only)Represents the <a href="../users/"><code>user</code></a> object containing users assigned to the group. A group can be deleted only if no user is assigned.</td></tr></tbody></table>

## Example

{% code title="USER GROUP OBJECT" lineNumbers="true" %}
```json
{
	"id": "UGR-5116-6265",
	"name": "Jane Doe",
	"description": "This group contains all Accounts team members",
	"modules": [
		{
			"id": "MOD-1756-1452",
			"name": "Access management"
		},
		{
			"id": "MOD-9042-8216",
			"name": "Account management"
		}
	],
	"icon": "https://picsum.photos/210/201",
	"default": true,
    "users": [
        {
            "id": "USR-0000-0016",          
            "icon": null,
            "name": "Reto Mayer"
        }
    ]
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
