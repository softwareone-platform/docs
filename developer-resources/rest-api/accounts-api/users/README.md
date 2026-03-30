# User

The User object represents a single user on the Marketplace platform.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="161">Field Name</th><th width="126">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary identifier for the user.</p><p>Example: USR-1671-0642</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>The relative reference to the object.</p><p>Example: /v1/accounts/users/USR-1671-0642</p></td></tr><tr><td><code>email</code></td><td>string</td><td><p>The email address of the user.</p><p>Example: will.smith@softwareone.com</p></td></tr><tr><td><code>status</code></td><td>string</td><td><p>The status of the user. Allowed values: <code>new</code>, <code>invited</code>, <code>invitation expired</code>, <code>active</code>, <code>blocked</code>, <code>disabled</code>, or <code>deleted</code>.</p><p></p><p>A user can have <code>invited</code> or <code>invitationExpired</code> status only if they have not joined the account.</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The full name of the user.</p><p>Example: Will Smith</p></td></tr><tr><td><code>firstName</code></td><td>string</td><td><p>The first name of the user.</p><p>Example: Will</p></td></tr><tr><td><code>lastName</code></td><td>string</td><td><p>The last name of the user.</p><p>Example: Smith</p></td></tr><tr><td><code>phone</code></td><td>object</td><td><p>The country code and phone number of the user.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ 
  "prefix": "+34",
  "number": "660707172"
}
</code></pre></td></tr><tr><td><code>SSO</code></td><td>bool</td><td><p>A flag to indicate if the user logs in using SSO.</p><p>Example: true</p></td></tr><tr><td><code>acceptedTerms</code></td><td>bool</td><td><p>A flag to indicate if the user has accepted the terms and conditions.</p><p>Example: true</p></td></tr><tr><td><code>accounts</code></td><td>object</td><td><p>The list of <a href="../account/#account-object">account</a> to which the user has been added.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "ACC-1671-0642",
    "name": "You Are a Test Account"
  }
]
</code></pre></td></tr><tr><td><code>groups</code></td><td>object</td><td><p>All <a href="../user-groups/#group-object">groups</a> that the user belongs to.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "UGR-5116-6265",
    "name": "Administrators"
  },
  {
    "id": "UGR-5116-6565",
    "name": "Fulfillment Managers"
  }
]
</code></pre></td></tr><tr><td><code>invitation</code></td><td>object</td><td><p>The invitation object. This is added only in the context of the account (on account sub-collection), and only in case of the user being invited.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "code": "910B14E6CB2343A09CB32F24BBC4BEF1",
  "status": "Invited"
}
</code></pre></td></tr><tr><td><code>invitation.code</code></td><td>string</td><td><p>The invitation code sent to user to invite them to the platform.</p><p>Example: 910B14E6CB2343A09CB32F24BBC4BEF1</p></td></tr><tr><td><code>invitation.status</code></td><td>string</td><td><p>The invitation status for the user in the account.</p><p>Example: Invited</p></td></tr><tr><td><code>audit</code></td><td>object</td><td><p>Represents the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "created": { ... },
    "updated": { ... },
    "joined": { ... },
    "login": { ... },
    "access": { ... }
}
</code></pre></td></tr></tbody></table>

## Example response

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
