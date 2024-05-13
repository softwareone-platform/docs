# Account user

## Account User Object

The `user` object represents an individual user in the Marketplace platform. This object contains the following properties:&#x20;

<table data-full-width="false"><thead><tr><th width="233">Field</th><th>Type</th><th>Constraints</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p><code>READONLY</code> </p><p><code>IDX</code></p><p><code>CORE</code></p></td><td><p>Primary account user identifier. </p><p></p><p>Example: "AUSR-5709-0422-8243"</p></td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td><p><code>READONLY</code> </p><p><code>CORE</code></p></td><td><p>Relative reference to object on API (always <code>/v1/accounts/account-users/{id}</code>). </p><p></p><p>Example: "/v1/accounts/account-users/AUSR-5709-0422-8243"</p></td></tr><tr><td><strong><code>user</code></strong></td><td>User</td><td><code>CORE</code></td><td></td></tr><tr><td><strong><code>account</code></strong></td><td>Account</td><td><code>CORE</code></td><td><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "ACC-1671-0642",
  "href": "/accounts/ACC-1671-0642",
  "icon": null,
  "name": "You Are a Test Account"
}
</code></pre></td></tr><tr><td><strong><code>invitation</code></strong></td><td>Invitation.Status </td><td><code>READONLY</code> </td><td><p>Invitation information: Invited, Active, InvitationExpired </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "url": "https://client.softwareone.com/accept-invite?code=invitationCode",
  "status": "Invited"
}
</code></pre></td></tr><tr><td><strong><code>groups</code></strong></td><td>UserGroup</td><td></td><td><p>List of user groups. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">[
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
