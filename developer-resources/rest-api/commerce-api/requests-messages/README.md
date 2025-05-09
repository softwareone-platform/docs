# Requests Messages

The Request Message object represents a message object in the scope of the request. It contains the following properties:

<table><thead><tr><th width="119">Field</th><th width="136">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Primary identifier for the message.</p><p></p><p>Example: MSG-1212-3434-5656-7878</p></td></tr><tr><td>href</td><td>string</td><td><p>Relative reference to the object in the API. </p><p></p><p>Example: /v1/commerce/requests/REQ-1671-0642/messages/MSG-1212-3434-5656-7878</p></td></tr><tr><td>type</td><td>string</td><td><p>Type of message, such as User or System.</p><p></p><p>Example: User</p></td></tr><tr><td>content</td><td>string</td><td><p>Content of the message.</p><p></p><p>Example: I would like a discount of 5%.</p></td></tr><tr><td>request</td><td><a href="../requests/#request-object">Request</a></td><td><p>Reference to the Request object. </p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
     "id": "E001234",
     "message": "Agreement provisioning failed due to unavailability of the item"
}
</code></pre></td></tr><tr><td>audit</td><td>AuditObject</td><td><p>Audit object with entries, including Created and Updated. </p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% tabs %}
{% tab title="SHORT FORM" %}
```json
{
  "id": "MSG-1212-3434-5656-7878",
  "href": "/v1/commerce/requests/REQ-1671-0642/messages/MSG-1212-3434-5656-7878",
  "type": "User",
  "content": "would agree discount of 5%"
}
```
{% endtab %}

{% tab title="FULL EXAMPLE" %}
```json
{
  "id": "MSG-1212-3434-5656-7878",
  "href": "/v1/commerce/requests/REQ-1671-0642/messages/MSG-1212-3434-5656-7878",
  "type": "User",
  "content": "would agree discount of 5%",
  "request": {
    "id": "REQ-1671-0642"
  },
  "audit": {
    "created": { 
      "at": "2023-12-14T17:28:57.667Z", 
      "by": {
        "id": "USR-1234-1234-1234",
        "name": "John Smith"
      },
      "of": {
        "id": "ACC-1234-1234",
        "name": "Microsoft",
        "icon": "/static/ACC-1234-1234/account.png"
      }
    }
  }
}
```
{% endtab %}
{% endtabs %}
