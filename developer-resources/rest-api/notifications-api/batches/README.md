# Batch

The Batch object represents an email being sent to a specific category and multiple contacts.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-search="false"><thead><tr><th width="156">Field</th><th width="154">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) A primary identifier for the batch. </td></tr><tr><td><code>href</code></td><td>string, core</td><td>(Read-only) A relative reference to the object. </td></tr><tr><td><code>category</code></td><td>object, core</td><td>Represents the <a href="../categories/"><code>category</code></a> object.</td></tr><tr><td><code>account</code></td><td>object, core</td><td>Represents the <a href="../../accounts-api/account/"><code>account</code></a> object.</td></tr><tr><td><code>subject</code></td><td>string, core</td><td>The subject line of the notification email. </td></tr><tr><td><code>body</code></td><td>string</td><td>The body of the message.</td></tr><tr><td><code>attachments</code></td><td>object</td><td><p>(Read-only) Represents the <code>attachment</code> object. Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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

## Example

{% code title="BATCH OBJECT" overflow="wrap" lineNumbers="true" %}
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
