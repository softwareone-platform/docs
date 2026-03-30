# Batch

The Batch object represents an email being sent to a specific category and multiple contacts.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="124">Field Name</th><th width="140">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>A primary identifier for the batch. </p><p>Example: MST-1234-9876-3333</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>A relative reference to the object. </p><p>Example: /v1/notifications/batches/MST-1234-9876-3333</p></td></tr><tr><td><code>category</code></td><td><a href="../categories/">category</a></td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "NTC-1234-9876",
  "href": "/v1/notifications/categories/NTC-1234-9876",
  "name": "Orders",
  "shortDescription": "Includes updates about order confirmations, order status updates, and related communications."
}
</code></pre></td></tr><tr><td><code>account</code></td><td>object</td><td>A reference to the <a href="../../accounts-api/account/"><code>account</code></a> object.</td></tr><tr><td><code>subject</code></td><td>string</td><td><p>The subject line for the email. </p><p>Example: Check out the new service offering</p></td></tr><tr><td><code>body</code></td><td>string</td><td>The body of the message.</td></tr><tr><td><code>attachments</code></td><td>object</td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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

</code></pre></td></tr></tbody></table>

## Example response

{% code lineNumbers="true" %}
```json
{
  "id": "MST-1234-9876-3333",
  "href": "/v1/notifications/batches/MST-1234-9876-3333",
  "category": {
    "id": "NTC-1234-9876",
    "href": "/v1/notifications/categories/NTC-1234-9876",
    "name": "Orders",
    "shortDescription": "Includes updates about order confirmations, order status updates, and related communications."
  },
  "account": {
    "id": "ACC-5131-0044",
    "href": "/accounts/accounts/ACC-5131-0044",
    "type": "Client",
    "status": "Active",
    "name": "SURFMARKET BV"
  },  
  "subject": "Order published",
  "body": "<b>Hello</b>",
}
```
{% endcode %}
