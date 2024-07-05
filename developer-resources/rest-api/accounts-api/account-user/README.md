# Account User

## Account User Object

The `user` object represents an individual user in the Marketplace platform. This object contains the following properties:&#x20;

<table data-full-width="false"><thead><tr><th>Field</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p>Primary account user identifier. </p><p></p><p>Example: "AUSR-5709-0422-8243"</p></td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td><p>Relative reference to object on API (always /v1/accounts/account-users/{id}). </p><p></p><p>Example: "/v1/accounts/account-users/AUSR-5709-0422-8243"</p></td></tr><tr><td><strong><code>user</code></strong></td><td><a href="../users/#user-object">User</a></td><td></td></tr><tr><td><strong><code>account</code></strong></td><td><a href="../account/#account-object">Account</a></td><td><pre class="language-json" data-line-numbers><code class="lang-json">{
  "id": "ACC-1671-0642",
  "href": "/accounts/ACC-1671-0642",
  "icon": null,
  "name": "You Are a Test Account"
}
</code></pre></td></tr><tr><td><strong><code>invitation</code></strong></td><td>Invitation.Status</td><td><p>Invitation information: Invited, Active, InvitationExpired </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "url": "https://client.softwareone.com/accept-invite?code=invitationCode",
  "status": "Invited"
}
</code></pre></td></tr><tr><td><strong><code>groups</code></strong></td><td><a href="../user-groups/#group-object">UserGroup</a></td><td><p>List of user groups. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">[
  {
    "id": "UGR-8447-7590",
    "href": "/user-groups/UGR-8447-7590",
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
            "href": "/account-users/AUSR-4134-7183-7330",
            "user": {
                "id": "USR-6375-2499",
                "href": "/users/USR-6375-2499",
                "email": "test12.test@SWO1.com",
                "firstName": "test",
                "lastName": "test"
            },
            "groups": [
                {
                    "id": "UGR-8447-7590",
                    "href": "/user-groups/UGR-8447-7590",
                    "name": "test2",
                    "description": "test2",
                    "logo": "",
                    "isDefault": false
                }
            ],
            "account": {
                "id": "ACC-1671-0642",
                "href": "/accounts/ACC-1671-0642",
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
