# Account User

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="144">Field</th><th width="139">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Red-only) The primary identifier for the account user.</td></tr><tr><td><code>user</code></td><td>object, core</td><td>Represents the <a href="../users/#user-object"><code>user</code></a> object.</td></tr><tr><td><code>account</code></td><td>object, core</td><td>Represents the <a href="../account/#account-object"><code>account</code></a> object.</td></tr><tr><td><code>invitation</code></td><td>string</td><td><p>(Red-only) The status of the invitation. Allowed values: </p><ul><li><code>Invited</code></li><li><code>Active</code></li><li><code>InvitationExpired</code></li></ul></td></tr><tr><td><code>groups</code></td><td>object</td><td>Represents the <a href="../user-groups/#group-object"><code>group</code></a> object containing a list of groups.</td></tr></tbody></table>

## Example

{% code title="ACCOUNT USER OBJECT" lineNumbers="true" %}
```json
{
    "$meta": {
        "pagination": {
            "offset": 0,
            "limit": 10,
            "total": 1
        },
        "omitted": [
            "audit"
        ]
    },
    "data": [
        {
            "id": "AUSR-4134-7183-7330",
            "user": {
                "id": "USR-6375-2499",
                "email": "janedoe@example.com",
                "firstName": "jane",
                "lastName": "doe"
            },
            "groups": [
                {
                    "id": "UGR-8447-7590",
                    "name": "Reto",
                    "description": "Mayer",
                    "logo": "",
                    "isDefault": false
                }
            ],
            "account": {
                "id": "ACC-1671-0642",
                "icon": null,
                "name": "This is my account."
            },
            "invitation": {
                "code": "TEST",
                "status": "Invited"
            }
        }
    ]
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
