# Message

The Message object represents a single notification that was sent to a single contact.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="157">Field Name</th><th width="134">Data Type</th><th width="457">Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary identifier for the message. </p><p>Example: MSG-1234-9876-4442-4314</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>A relative reference to the object. </p><p>Example: /v1/notifications/messages/MSG-1234-9876-4442-4314</p></td></tr><tr><td><code>batch</code></td><td><a href="../batches/">batch</a></td><td><p>The <a href="../batches/"><code>batch</code></a> associated with the message. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "MST-1234-9876-3333"
}
</code></pre></td></tr><tr><td><code>contact</code></td><td>object</td><td><p>A reference to the <code>contact</code> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
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
}
</code></pre></td></tr><tr><td><code>account</code></td><td>object</td><td><p>A reference to the <code>account</code> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "ACC-1671-0642",
  "href": "/accounts/accounts/ACC-1671-0642",
  "type": "Client",
  "status": "Enabled",
  "name": "You Are a Test Account",
  "logo": "/accounts/accounts/ACC-1671-0642/logo.png"
}
</code></pre></td></tr><tr><td><code>status</code></td><td>enum</td><td>Allowed values: <code>queued</code>, <code>sent</code>, <code>bounced</code>, <code>complained</code>, or <code>discarded</code>.</td></tr><tr><td><code>subject</code></td><td>string</td><td><p>The subject line of the message. </p><p>Example: Check out the new service offering</p></td></tr><tr><td><code>category</code></td><td>object</td><td><p>A reference to the <a href="../categories/"><code>category</code></a> object.  </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "NTC-1234-9876",
  "href": "/v1/notifications/categories/NTC-1234-9876",
  "name": "Orders",
  "shortDescription": "Includes updates about order confirmations, order status updates, and related communications."
}
</code></pre></td></tr><tr><td><code>body</code></td><td> </td><td><p> Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">  "&#x3C;html>&#x3C;body>&#x3C;b>Hello&#x3C;/b>&#x3C;/body>&#x3C;/html>"
</code></pre></td></tr><tr><td><code>attachments</code></td><td>object</td><td><p>A reference to the <code>attachment</code> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td><p>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">"created": { 
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

## Example response

{% code lineNumbers="true" %}
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
