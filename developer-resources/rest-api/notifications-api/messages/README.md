# Message

The Message object represents a single notification that was sent to a single contact.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="139">Field</th><th width="155">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The primary identifier for the message. </td></tr><tr><td><code>href</code></td><td>string, core</td><td>(Read-only) A relative reference to the object.</td></tr><tr><td><code>batch</code></td><td>object, core</td><td>(Read-only) Represents the <a href="../batches/"><code>batch</code></a> associated with the message. </td></tr><tr><td><code>contact</code></td><td>object, core</td><td>Represents the <code>contact</code> object.</td></tr><tr><td><code>account</code></td><td>object</td><td>Represents the <code>account</code> object. </td></tr><tr><td><code>status</code></td><td>enum, core</td><td><p>Allowed values are</p><ul><li><code>Queued</code></li><li><code>Sent</code></li><li><code>Bounced</code></li><li><code>Complained</code></li><li><code>Discarded</code></li></ul></td></tr><tr><td><code>subject</code></td><td>string, core</td><td><p>The subject line of the message. </p><p>Example: Check out the new service offering</p></td></tr><tr><td><code>category</code></td><td>object, core</td><td>Represents the <a href="../categories/"><code>category</code></a> object.  </td></tr><tr><td><code>body</code></td><td> </td><td>Represents the body text.</td></tr><tr><td><code>attachments</code></td><td>object</td><td><p>(Read-only) Represents the <code>attachment</code> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "ATT-1234-1234-1234",
    "name": "Some mail attachment",
    "contentType": "application/octet-stream",
    "fileSize": 1234,
    "fileName": "SomeFile.pdf",
    "href": "/v1/notifications/messages/attachments/ATT-1234-1234-1234"
  },
  {
    "id": "ATT-9876-9876-9876",
    "name": "Some other mail attachment",
    "contentType": "application/octet-stream",
    "fileSize": 9876,
    "fileName": "SomeOtherFile.pdf",
    "href": "/v1/notifications/messages/attachments/ATT-9876-9876-9876"
  }
]
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Example

{% code title="MESSAGE OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
      "id": "MSG-1234-9876-4442-4314",
      "href": "/v1/notifications/messages/MSG-1234-9876-4442-4314",
      "batch": {
        "id": "MST-1234-9876-3333"
      },
      "contact": {
        "id": "CTT-1234-9876-1234",
        "href": "/v1/notifications/contacts/CTT-1234-9876-1234",
        "name": "Will Smith",
        "email": "will.smith@softwareone.com",
        "user": {
          "id": "USR-3773-5838",
          "href": "/accounts/users/USR-1234-9876",
          "name": "Will Smith",
          "email": "will.smith@softwareone.com"
        }
      },
      "account": {
        "id": "ACC-1671-0642",
        "href": "/accounts/accounts/ACC-1671-0642",
        "type": "Client",
        "status": "Enabled",
        "name": "You Are a Test Account",
        "logo": "/accounts/accounts/ACC-1671-0642/logo.png"
      },
      "status": "Sent",
      "subject": "Check out the new service offering",
      "body": "<html><body><b>Hello</b></body></html>",
      "category": {
        "id": "NTC-1234-9876",
        "href": "/v1/notifications/categories/NTC-1234-9876",
        "name": "Orders",
        "shortDescription": "Includes updates about order confirmations, order status updates, and related communications."
      },
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
