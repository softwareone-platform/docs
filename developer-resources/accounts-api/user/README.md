# User

## User Object

The `user` object represents an individual user in the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th width="223">Field</th><th width="122">Type</th><th width="161">Constraints</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p><code>READONLY</code></p><p><code>IDX</code></p><p><code>CORE</code></p></td><td><p>Primary user identifier. </p><p></p><p>Example: "USR-1671-0642"</p></td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td><p><code>READONLY</code> </p><p><code>CORE</code></p></td><td><p>Relative reference to object on API (always /v1/accounts/users/{id}). </p><p></p><p>Example: "/v1/accounts/users/USR-1671-0642"</p></td></tr><tr><td><strong><code>email</code></strong></td><td>string</td><td><code>IDX</code></td><td><p>Email address of the user. </p><p></p><p>Example: "will.smith@softwareone.com"</p></td></tr><tr><td><strong><code>status</code></strong></td><td>string</td><td><code>READONLY</code> </td><td><p>Status of the user. </p><details><summary>enum values</summary><p><code>New</code> </p><p><code>Invited</code> </p><p><code>Invitation</code></p><p><code>Expired</code> </p><p><code>Active</code> </p><p><code>Blocked</code> </p><p><code>Disabled</code> </p><p><code>Deleted</code></p></details><p>A user can have the Invited or InvitationExpired status only if they haven't joined the account.</p></td></tr><tr><td><strong><code>name</code></strong></td><td>string</td><td><p><code>READONLY</code></p><p><code>IDX</code></p></td><td><p>User's name. </p><p></p><p>Example: "Will Smith"</p></td></tr><tr><td><strong><code>firstName</code></strong></td><td>string</td><td><code>IDX</code></td><td><p>First name of the user. </p><p></p><p>Example: "Will"</p></td></tr><tr><td><strong><code>lastName</code></strong></td><td>string</td><td><code>IDX</code></td><td><p>Last name of the user. </p><p></p><p>Example: "Smith"</p></td></tr><tr><td><strong><code>phone</code></strong></td><td>object</td><td><code>IDX</code></td><td><p>User's country code and phone number.</p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{ 
  "prefix": "+34",
  "number": "660707172"
}
</code></pre></td></tr><tr><td><strong><code>SSO</code></strong></td><td>bool</td><td><code>READONLY</code></td><td><p>Flag if a user logs using SSO. </p><p></p><p>Example: "true"</p></td></tr><tr><td><strong><code>acceptedTerms</code></strong></td><td>bool</td><td><code>READONLY</code></td><td><p>Flag if user has accepted terms and conditions. </p><p></p><p>Example: "true"</p></td></tr><tr><td><strong><code>accounts</code></strong></td><td><a href="../account/#account-object">Account</a></td><td><code>IDX</code></td><td><p>List of accounts that user is added to, not returned on users account sub-collection. </p><p></p><p>Example:  </p><pre class="language-json" data-line-numbers><code class="lang-json">[
  {
    "id": "ACC-1671-0642",
    "name": "You Are a Test Account"
  }
]
</code></pre></td></tr><tr><td><strong><code>groups</code></strong></td><td><a href="../user-groups/#group-object">Group</a></td><td></td><td><p>Groups that the user belongs to. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">[
  {
    "id": "UGR-5116-6265",
    "name": "Administrators"
  },
  {
    "id": "UGR-5116-6565",
    "name": "Fulfillment Managers"
  }
]
</code></pre></td></tr><tr><td><strong><code>settings</code></strong></td><td></td><td><code>OPTIONAL</code></td><td></td></tr><tr><td><strong><code>invitation</code></strong></td><td>object</td><td><code>OPTIONAL</code></td><td><p>Added only in context of account (on account sub-collection), and only in case of user being invited. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "code": "910B14E6CB2343A09CB32F24BBC4BEF1",
  "status": "Invited"
}
</code></pre></td></tr><tr><td><strong><code>invitation.code</code></strong></td><td>string</td><td><p><code>READONLY</code></p><p><code>OPTIONAL</code></p></td><td><p>Invitation code sent to user to invite them to the platform. </p><p></p><p>Example: "910B14E6CB2343A09CB32F24BBC4BEF1"</p></td></tr><tr><td><strong><code>invitation.status</code></strong></td><td>string</td><td><p><code>READONLY</code></p><p><code>OPTIONAL</code></p></td><td><p>Invitation status for the user in account. </p><p></p><p>Example: "Invited"</p></td></tr><tr><td><strong><code>audit</code></strong></td><td>object</td><td><p><code>READONLY</code></p><p><code>IDX</code></p></td><td><p>Meaning of audit events:<br>On GLobal User</p><ul><li><code>created</code> - when user was created (once in lifecycle).</li><li><code>updated</code> - when user parameters changed last time.</li><li><code>login</code> - when user last time logged in.</li><li><code>blocked</code> - when user was blocked last time.</li></ul><p>On account subcollection, in additional to above:</p><ul><li><code>invited</code> - when user was invited into account (dropped on join).</li><li><code>joined</code> - when user was accepted invitation to account.</li><li><code>access</code> - when user last time switched to the account context. </li></ul><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
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
