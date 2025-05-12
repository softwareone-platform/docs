---
hidden: true
---

# Journal Message

The Journal Message object represents a Message object in the scope of the journal.

<table><thead><tr><th width="143">Field</th><th width="193">Type</th><th></th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Primary identifier for the message.  </p><p>Example: MSG-1212-3434-5656-7878</p></td></tr><tr><td>href</td><td>string</td><td><p>Relative reference to the object in the API. </p><p>Example: /v1/billing/journals/BJO-1234-5678/messages/MSG-1212-3434-5656-7878</p></td></tr><tr><td>account</td><td><a href="../accounts-api/account/">Account</a></td><td><p>Reference to the Account object within the journal message was created. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "ACC-1234-1234",
    "href": "/accounts/accounts/ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>type</td><td>string</td><td><p>Type of message. Possible entries include User or<br>System.</p><p>Example: User</p></td></tr><tr><td>content</td><td>string</td><td><p>Content of the message. </p><p>Example: Journal charges file uploaded</p></td></tr><tr><td>journal</td><td><a href="journal/">Journal</a></td><td><p>Reference to the Journal object. </p><p>Example:</p><pre data-overflow="wrap" data-line-numbers><code>{
  "id": "BJO-1234-5678"
}
</code></pre></td></tr><tr><td>audit</td><td>AuditObject</td><td><p>Audit object with possible entries: Created. </p><p>Example:</p><pre data-overflow="wrap" data-line-numbers><code>{
"created": { "at": "...", "by": { } }
}
</code></pre></td></tr><tr><td>visibility</td><td>Visibility Object</td><td><p>Visibility settings for the message. </p><p>Example:</p><pre data-overflow="wrap" data-line-numbers><code>{
  "client": true,
  "operations": true,
  "vendor": true
}
</code></pre></td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% tabs %}
{% tab title="SHORT FORM" %}
```json
{
  "id": "MSG-1212-3434-5656-7878",
  "href": "/v1/billing/journals/BJO-1234-5678/messages/MSG-1212-3434-5656-7878",
  "type": "User",
  "content": "Journal charges file uploaded"
}
```
{% endtab %}

{% tab title="LONG EXAMPLE" %}
```json
{
  "id": "MSG-1212-3434-5656-7878",
  "href": "/v1/billing/journals/BJO-1234-5678/messages/MSG-1212-3434-5656-7878",
  "account": {
    "id": "ACC-1234-1234",
    "href": "/accounts/accounts/ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/v1/accounts/accounts/ACC-1234-1234/icon"
  },
  "type": "User",
  "content": "Journal charges file uploaded",
  "journal": {
    "id": "BJO-1234-5678"
  },
  "audit": {
    "created": { 
      "at": "2024-12-03T11:28:57.667Z", 
      "by": {
        "id": "USR-1234-1234-1234",
        "name": "John Smith"
      }
    }
  },
  "visibility": {
    "client": true,
    "operations": true,
    "vendor": true
  }
}
```
{% endtab %}
{% endtabs %}
