# Contact

The Contact object represents a contact to which notifications are sent. Contact can but doesn’t have to be linked to a user on the platform. Each contact can manage its notification preferences on a category level. This object contains the following attributes:

<table><thead><tr><th width="170">Field</th><th width="121">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>A primary identifier for the contact. </p><p>Example: CTT-1234-9876-1234</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>A relative reference to the object. </p><p>Example: /v1/notifications/contacts/CTT-1234-9876-1234</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The contact's display name.  </p><p>Example: Jane Doe</p></td></tr><tr><td>email</td><td><code>string</code></td><td><p>The contact's email address.  </p><p>Example: Jane@starkindustries.com</p></td></tr><tr><td>user</td><td><a href="../../accounts-api/users/"><code>user</code></a></td><td><p>Indicates if the email belongs to a user registered on the platform. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "USR-3773-5838",
  "href": "/accounts/users/USR-1234-9876",
  "name": "Will Smith",
  "email": "will.smith@softwareone.com"
}
</code></pre></td></tr><tr><td>optOuts</td><td><a href="../categories/"><code>category</code></a></td><td><p>A list of notification categories that the contact has chosen to opt out of. By default, a contact is opted into all published categories. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "NTC-1234-9876",
    "href": "/notifications/categories/NTC-1234-9876",
    "name": "Orders",
    "shortDescription": "Orders"
  }
]
</code></pre></td></tr><tr><td>status</td><td><code>enum</code></td><td>The possible values are <code>Active</code> or <code>Blocked</code>.</td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td><p>A reference to the Audit object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">"created": { 
  "at": "2023-12-14T17:28:57Z", 
  "by": {
    "id": "UR-1234-1234-1234",
    "name": "John Smith",
    "icon": "/static/users/UR-1234-1234-1234.icon.svg"
  },
  "of": {
    "id": "ACC-1234-1234",
    "href": "/accounts/accounts/ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
  }
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="CONTACT OBJECT" %}
{% code lineNumbers="true" %}
```json
{
  "id": "CTT-1234-9876-1234",
  "href": "/v1/notifications/contacts/CTT-1234-9876-1234",
  "name": "Will Smith",
  "email": "will.smith@softwareone.com",
  "user": {
    "id": "USR-3773-5838",
    "href": "/accounts/users/USR-1234-9876",
    "name": "Will Smith",
    "email": "will.smith@softwareone.com"
  },
  "optOuts": [
    {
      "id": "NTC-1234-9876",
      "href": "/notifications/categories/NTC-1234-9876",
      "name": "Orders",
      "shortDescription": "Orders"
    }
  ],
  "status": "Active",
  "audit": {
    "created": {
      "at": "2023-12-14T17:28:57Z",
      "by": {
        "id": "UR-1234-1234-1234",
        "name": "John Smith",
        "icon": "/static/users/UR-1234-1234-1234.icon.svg"
      },
      "of": {
        "id": "ACC-1234-1234",
        "href": "/accounts/accounts/ACC-1234-1234",
        "name": "Microsoft",
        "icon": "/static/ACC-1234-1234/account.png"
      }
    }
  }
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
