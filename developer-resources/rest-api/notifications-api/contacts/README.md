# Contact

The Contact object represents a contact who receives the notifications. Contact can be linked to a user in the platform. Each contact can manage its notification preferences at the category level.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="141">Field</th><th width="159">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) A primary identifier for the contact. </td></tr><tr><td><code>href</code></td><td>string, core</td><td>(Read-only) A relative reference to the object. </td></tr><tr><td><code>name</code></td><td>string, core</td><td>The display name of the contact.  </td></tr><tr><td><code>email</code></td><td>string, core</td><td>The email address of the contact.  </td></tr><tr><td><code>user</code></td><td>object, core</td><td><p>(Read-only) Indicates if the email belongs to a <a href="../../accounts-api/users/"><code>user</code></a> registered on the platform. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "USR-3773-5838",
  "href": "/accounts/users/USR-1234-9876",
  "name": "Will Smith",
  "email": "will.smith@softwareone.com"
}
</code></pre></td></tr><tr><td><code>optOuts</code></td><td>object</td><td><p>Represents the <a href="../categories/"><code>category</code></a> object, containing the list of notification categories the contact has chosen to opt out of. By default, a contact is opted into all published categories.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "NTC-1234-9876",
    "href": "/notifications/categories/NTC-1234-9876",
    "name": "Orders",
    "shortDescription": "Orders"
  }
]
</code></pre></td></tr><tr><td><code>status</code></td><td>enum</td><td>Indicates the status. Allowed values are <code>active</code> or <code>blocked</code>.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Example

{% code title="CONTACT OBJECT" overflow="wrap" lineNumbers="true" %}
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
