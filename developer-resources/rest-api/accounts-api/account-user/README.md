# Account User

The Account User object represents an individual user in the Marketplace platform. This object contains the following properties:&#x20;

<table data-full-width="false"><thead><tr><th width="139">Field</th><th width="152">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Primary account user identifier. </p><p></p><p>Example: AUSR-5709-0422-8243</p></td></tr><tr><td>href</td><td>string</td><td><p>Relative reference to the object in the API. </p><p></p><p>Example: /v1/accounts/account-users/AUSR-5709-0422-8243</p></td></tr><tr><td>user</td><td><a href="../users/#user-object">User</a></td><td>Reference to the User object.</td></tr><tr><td>account</td><td><a href="../account/#account-object">Account</a></td><td><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "ACC-1671-0642",
  "icon": null,
  "name": "You Are a Test Account"
}
</code></pre></td></tr><tr><td>invitation</td><td>Invitation.Status</td><td><p>Status of the invitation, such as Invited, Active, or invitation Expired.</p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "url": "https://client.softwareone.com/accept-invite?code=invitationCode",
  "status": "Invited"
}
</code></pre></td></tr><tr><td>groups</td><td><a href="../user-groups/#group-object">UserGroup</a></td><td><p>List of user groups. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "UGR-8447-7590",
    "name": "test2",
    "description": "test2",
    "logo": "",
    "isDefault": false
  }
]
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="ACCOUNT USER OBJECT" %}
{% code lineNumbers="true" %}
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
                "email": "test12.test@SWO1.com",
                "firstName": "test",
                "lastName": "test"
            },
            "groups": [
                {
                    "id": "UGR-8447-7590",
                    "name": "test2",
                    "description": "test2",
                    "logo": "",
                    "isDefault": false
                }
            ],
            "account": {
                "id": "ACC-1671-0642",
                "icon": null,
                "name": "You Are a Test Account"
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
{% endtab %}
{% endtabs %}
