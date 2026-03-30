# Account User

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="139">Field Name</th><th width="170">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary account user identifier.</p><p>Example: AUSR-5709-0422-8243</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>A relative reference to the object in the API.</p><p>Example: /v1/accounts/account-users/AUSR-5709-0422-8243</p></td></tr><tr><td><code>user</code></td><td>object</td><td>A reference to the <a href="../users/#user-object"><code>user</code></a> object.</td></tr><tr><td><code>account</code></td><td>object</td><td><p>A reference to the <a href="../account/#account-object"><code>account</code></a> object. </p><pre class="language-json" data-line-numbers><code class="lang-json">{ 
  "id": "ACC-1671-0642",
  "icon": null,
  "name": "You Are a Test Account"
}
</code></pre></td></tr><tr><td><code>invitation</code></td><td>invitation.status</td><td><p>The status of the invitation. Allowed values: <code>invited</code>,  <code>active</code>, or <code>invitationExpired</code>.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "url": "https://client.softwareone.com/accept-invite?code=invitationCode",
  "status": "Invited"
}
</code></pre></td></tr><tr><td><code>groups</code></td><td><a href="../user-groups/#group-object">userGroup</a></td><td><p>A list of user groups.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "UGR-8447-7590",
    "name": "test2",
    "description": "test2",
    "logo": "",
    "isDefault": false
  }
]
</code></pre></td></tr></tbody></table>

## Example response

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
