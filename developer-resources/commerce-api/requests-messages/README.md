# Requests Messages

## Requests Messages object

The Request Message represents a Message object in the scope of the Request.

| Field     | Type          | Constraints                           | Description                                                                                                                                                                                                                               |
| --------- | ------------- | ------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Field** | **Type**      | **Constraints**                       | **Description**                                                                                                                                                                                                                           |
| id        | string        | READONLY IDX                          | <p>Primary message identifier </p><p></p><p>Example: "MSG-1212-3434-5656-7878"</p>                                                                                                                                                        |
| href      | string        | READONLY                              | <p>Relative reference to object on API (always /v1/somewhere/items/{id}) </p><p></p><p>Example: "/v1/commerce/requests/REQ-1671-0642/messages/MSG-1212-3434-5656-7878"</p>                                                                |
| type      | string        | <p>READONLY IDX<br>User<br>System</p> | <p>Type of message </p><p></p><p>Example: "User"</p>                                                                                                                                                                                      |
| content   | string        | MARKUP                                | <p>Message contents </p><p></p><p>Example: "I would agree discount of 5%"</p>                                                                                                                                                             |
| request   | Ref\<Request> | IDX HIDDEN                            | <p>Reference to request, never sent in context of the Request - i.e. not set on subcollection /commerce/request/{id}/messages, but will be sent whithout this context </p><p></p><p>Example: "<code>{ "id": "REQ-1671-0642" }</code>"</p> |
| audit     | AuditObject   | READONLY IDX                          | <p>Audit object with possible entries: <strong>created</strong>. </p><p></p><p>Example: "<code>{ "created": { "at": "...", "by": { } } }</code>"</p>                                                                                      |

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
