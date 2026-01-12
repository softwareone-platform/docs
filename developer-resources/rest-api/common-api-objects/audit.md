# Audit

The `Audit` object records events related to the object. Each event contains two key components: 'at,' which specifies the last time the event occurred, and 'by,' which indicates who performed the event.

Events do not represent the complete history of the object. They are a cache that retains only the most recent occurrence of each type of event. For example, if an order is updated multiple times, only the latest update will be reflected in the Audit object.

Events cannot be set directly through API calls, which means they are ignored in input during both creation (`POST`) and update (`PUT`) operations.

Events can be either common or specific to the object. In such cases, they should follow the state diagram of the object. The same operation can be reflected in multiple events if it is logically reasonable. For example, if an order is approved and some data within the order has changed in one operation, both the updated and approved events must be recorded.

<table><thead><tr><th width="141">Field</th><th width="178">Type</th><th>Description</th></tr></thead><tbody><tr><td>&#x3C;event></td><td><code>object</code></td><td>Indicates when the last event occurred and the event's initiator. If the event has not occurred yet, the entire object (along with its key) is omitted from the audit object.</td></tr><tr><td>&#x3C;event>.at</td><td><code>dateTime</code></td><td>The date of the event. </td></tr><tr><td>&#x3C;event>.by</td><td><a href="../accounts-api/users/"><code>user</code></a> or <a href="../accounts-api/api-tokens/"><code>token</code></a></td><td>A reference to the object of the actor who initiated the action. This can be a user or a token.</td></tr><tr><td>&#x3C;event>.of</td><td><a href="../accounts-api/account/"><code>account</code></a></td><td>A reference to the account on behalf of which the action was executed.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="AUDIT OBJECT" %}
{% code lineNumbers="true" %}
```json
{
  "audit": {
    "created": { 
      "at": "2023-12-14T17:28:57Z", 
      "by": {
        "id": "USR-1234-1234-1234",
        "name": "John Smith",
        "icon": "/static/users/UR-1234-1234-1234.icon.svg"
      },
      "of": {
        "id": "ACC-1234-1234",
        "href": "/accounts/accounts/ACC-1234-1234",
        "name": "Microsoft",
        "icon": "/static/ACC-1234-1234/account.png"
      }
    },
    "updated": { 
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
