# Users

The User object represents an individual user in the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th width="161">Field</th><th width="100">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The primary identifier for the user.</p><p>Example: USR-1671-0642</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>The relative reference to the object.</p><p>Example: /v1/accounts/users/USR-1671-0642</p></td></tr><tr><td>email</td><td><code>string</code></td><td><p>The email address of the user.</p><p>Example: will.smith@softwareone.com</p></td></tr><tr><td>status</td><td><code>string</code></td><td><p>The status of the user. Possible enum values:</p><p><code>New</code></p><p><code>Invited</code></p><p><code>Invitation</code></p><p><code>Expired</code></p><p><code>Active</code></p><p><code>Blocked</code></p><p><code>Disabled</code></p><p><code>Deleted</code></p><p></p><p>A user can have <code>Invited</code> or <code>InvitationExpired</code> status only if they haven't joined the account.</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the user.</p><p>Example: Will Smith</p></td></tr><tr><td>firstName</td><td><code>string</code></td><td><p>The first name of the user.</p><p>Example: Will</p></td></tr><tr><td>lastName</td><td><code>string</code></td><td><p>The last name of the user.</p><p>Example: Smith</p></td></tr><tr><td>phone</td><td><code>object</code></td><td><p>The country code and phone number of the user.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{ 
  "prefix": "+34",
  "number": "660707172"
}
</code></pre></td></tr><tr><td>SSO</td><td><code>bool</code></td><td><p>A flag to indicate if the user logs in using SSO.</p><p>Example: true</p></td></tr><tr><td>acceptedTerms</td><td><code>bool</code></td><td><p>A flag to indicate if the user has accepted the terms and conditions.</p><p>Example: true</p></td></tr><tr><td>accounts</td><td><a href="../account/#account-object"><code>Account</code></a></td><td><p>The list of accounts to which the user has been added.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">[
  {
    "id": "ACC-1671-0642",
    "name": "You Are a Test Account"
  }
]
</code></pre></td></tr><tr><td>groups</td><td><a href="../user-groups/#group-object"><code>Group</code></a></td><td><p>All groups that the user belongs to.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">[
  {
    "id": "UGR-5116-6265",
    "name": "Administrators"
  },
  {
    "id": "UGR-5116-6565",
    "name": "Fulfillment Managers"
  }
]
</code></pre></td></tr><tr><td>invitation</td><td><code>object</code></td><td><p>The invitation object. This is added only in the context of the account (on account sub-collection), and only in case of the user being invited.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
  "code": "910B14E6CB2343A09CB32F24BBC4BEF1",
  "status": "Invited"
}
</code></pre></td></tr><tr><td>invitation.code</td><td><code>string</code></td><td><p>The invitation code sent to user to invite them to the platform.</p><p>Example: 910B14E6CB2343A09CB32F24BBC4BEF1</p></td></tr><tr><td>invitation.status</td><td><code>string</code></td><td><p>The invitation status for the user in the account.</p><p>Example: Invited</p></td></tr><tr><td>audit</td><td><code>object</code></td><td><p>Represents the audit object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
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
