# Requests Messages

## Request Message object

The Request Message represents a message object in the scope of the request.

| Field   | Type                                   | Description                                                                                                                                                                                                                                                                                                                                                                  |
| ------- | -------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id      | string                                 | <p>Primary message identifier </p><p></p><p>Example: "MSG-1212-3434-5656-7878"</p>                                                                                                                                                                                                                                                                                           |
| href    | string                                 | <p>Relative reference to object on API (always /v1/somewhere/items/{id}) </p><p></p><p>Example: "/v1/commerce/requests/REQ-1671-0642/messages/MSG-1212-3434-5656-7878"</p>                                                                                                                                                                                                   |
| type    | string                                 | <p>Type of message: User or System.</p><p></p><p>Example: "User"</p>                                                                                                                                                                                                                                                                                                         |
| content | string                                 | <p>Message contents </p><p></p><p>Example: "I would agree discount of 5%".</p>                                                                                                                                                                                                                                                                                               |
| request | [Request](../requests/#request-object) | <p>Reference to request, never sent in context of the Request - i.e. not set on subcollection /commerce/request/{id}/messages, but will be sent whithout this context.</p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{
     "id": "E001234",
     "message": "Agreement provisioning failed due to unavailability of the item"
}
</code></pre> |
| audit   | AuditObject                            | <p>Audit object with possible entries: Created. </p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre>                                                                                                                                              |

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
