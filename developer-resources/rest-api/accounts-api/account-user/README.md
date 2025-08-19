# Account Users

The Account Users object contains the following properties:

<table data-full-width="false"><thead><tr><th width="139">Field</th><th width="170">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The primary account user identifier.</p><p>Example: AUSR-5709-0422-8243</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>A relative reference to the object in the API.</p><p>Example: /v1/accounts/account-users/AUSR-5709-0422-8243</p></td></tr><tr><td>user</td><td><a href="../users/#user-object"><code>user</code></a></td><td>A reference to the User object.</td></tr><tr><td>account</td><td><a href="../account/#account-object"><code>account</code></a></td><td><p>A reference to the Account object. </p><pre class="language-json" data-line-numbers><code class="lang-json">{ 
  "id": "ACC-1671-0642",
  "icon": null,
  "name": "You Are a Test Account"
}
</code></pre></td></tr><tr><td>invitation</td><td><code>invitation.status</code></td><td><p>The status of the invitation. Possible values: <code>Invited</code>, <code>Active</code>, or <code>Invitation Expired</code>.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "url": "https://client.softwareone.com/accept-invite?code=invitationCode",
  "status": "Invited"
}
</code></pre></td></tr><tr><td>groups</td><td><a href="../user-groups/#group-object"><code>userGroup</code></a></td><td><p>A lList of user groups.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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
{% code overflow="wrap" lineNumbers="true" %}
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
