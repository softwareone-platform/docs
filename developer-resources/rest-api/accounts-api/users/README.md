# Users

The User object represents an individual user in the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th width="161">Field</th><th width="100">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Primary user identifier. </p><p></p><p>Example: USR-1671-0642</p></td></tr><tr><td>href</td><td>string</td><td><p>Relative reference to the object in the API </p><p></p><p>Example: /v1/accounts/users/USR-1671-0642</p></td></tr><tr><td>email</td><td>string</td><td><p>The email address of the user. </p><p></p><p>Example: will.smith@softwareone.com</p></td></tr><tr><td>status</td><td>string</td><td><p>Status of the user. </p><details><summary>enum values</summary><p><code>New</code> </p><p><code>Invited</code> </p><p><code>Invitation</code></p><p><code>Expired</code> </p><p><code>Active</code> </p><p><code>Blocked</code> </p><p><code>Disabled</code> </p><p><code>Deleted</code></p></details><p>A user can have the Invited or InvitationExpired status only if they haven't joined the account.</p></td></tr><tr><td>name</td><td>string</td><td><p>Name of the user. </p><p></p><p>Example: Will Smith</p></td></tr><tr><td>firstName</td><td>string</td><td><p>First name of the user. </p><p></p><p>Example: Will</p></td></tr><tr><td>lastName</td><td>string</td><td><p>Last name of the user. </p><p></p><p>Example: Smith</p></td></tr><tr><td>phone</td><td>object</td><td><p>Country code and phone number of the user.</p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ 
  "prefix": "+34",
  "number": "660707172"
}
</code></pre></td></tr><tr><td>SSO</td><td>bool</td><td><p>Flag if a user logs in using SSO. </p><p></p><p>Example: true</p></td></tr><tr><td>acceptedTerms</td><td>bool</td><td><p>Flag if the user has accepted the terms and conditions. </p><p></p><p>Example: true</p></td></tr><tr><td>accounts</td><td><a href="../account/#account-object">Account</a></td><td><p>List of accounts to which the user has been added, not included in the user's account sub-collection.</p><p></p><p>Example:  </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "ACC-1671-0642",
    "name": "You Are a Test Account"
  }
]
</code></pre></td></tr><tr><td>groups</td><td><a href="../user-groups/#group-object">Group</a></td><td><p>Groups that the user belongs to. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "UGR-5116-6265",
    "name": "Administrators"
  },
  {
    "id": "UGR-5116-6565",
    "name": "Fulfillment Managers"
  }
]
</code></pre></td></tr><tr><td>invitation</td><td>object</td><td><p>Added only in context of account (on account sub-collection), and only in case of user being invited. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "code": "910B14E6CB2343A09CB32F24BBC4BEF1",
  "status": "Invited"
}
</code></pre></td></tr><tr><td>invitation.code</td><td>string</td><td><p>The invitation code sent to user to invite them to the platform. </p><p></p><p>Example: 910B14E6CB2343A09CB32F24BBC4BEF1</p></td></tr><tr><td>invitation.status</td><td>string</td><td><p>Invitation status for the user in the account. </p><p></p><p>Example: Invited</p></td></tr><tr><td>audit</td><td>object</td><td><p>Represents the audit object.</p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "created": { ... },
    "updated": { ... },
    "joined": { ... },
    "login": { ... },
    "access": { ... }
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="USER OBJECT" %}
{% code lineNumbers="true" %}
```json
{
  "id": "USR-6375-2499",
  "href": "/v1/accounts/users/USR-6375-2499",
  "email": "test12.test@SWO1.com",
  "name": "John Smith",
  "firstName": "John",
  "lastName": "Smith",
  "status": "Invited",
  "phone": { 
      "prefix": "+34",
      "number": "660707172"
  },
  "accounts": [
		{
			"id": "ACC-1671-0642",
			"href": "/accounts/ACC-1671-0642",
			"icon": null,
			"name": "You Are a Test Account"
		}
  ],
  "group": [
      {
        "id": "UGR-5116-6265",
        "name": "Administrators"
      },
      {
        "id": "UGR-5116-6565",
        "name": "Fulfillment Managers"
      }
  ],
  "invitation": {
    "code": "910B14E6CB2343A09CB32F24BBC4BEF1",
    "status": "Invited"
  }
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
