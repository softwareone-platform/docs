# Rate

The Rate object represents an exchange rate between two currencies.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="139">Field</th><th width="160">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The primary identifier for the rate. </td></tr><tr><td><code>pair</code></td><td>object, core</td><td>Represents the currency <a href="../pair/"><code>pair</code></a> that this rate applies to.</td></tr><tr><td><code>externalId</code></td><td>string</td><td>The ID of the external system from where the rate is fetched. </td></tr><tr><td><code>recordDate</code></td><td>datetime</td><td>The date and time when this rate was fetched.</td></tr><tr><td><code>rate</code></td><td>number, core</td><td>The exchange rate from currency A to B. </td></tr><tr><td><code>status</code></td><td>string</td><td>Indicates whether the item is active or deleted.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>revision</code></td><td>integer, core</td><td>The entity's revision number.</td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% code title="RATE OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "FXR-1671-0642-0000",
  "pair": {
    "id": "FXP-1671-0642",
    "name": "EUR: GBP",
    "latestRate": {
      "rate": 0.88
    },
    "revision": 1
  },
  "externalId": "RATE-1234",
  "recordDate": "2024-05-09T14:40:28.958Z",
  "value": 1.1456,
  "status": "Active",
  "audit":{
    "created": {
      "at": "2024-04-08T06:30:05.807Z",
      "by": {
        "id": "USR-2172-2499",
        "revision": 1,
        "name": "John User"
      }
    },
    "updated": {
      "at": "2024-05-16T09:17:36.406Z",
      "by": {
        "id": "TKN-3836-7769",
        "revision": 1,
        "name": "My token"
      }
    },
    "deleted": {
      "at": "2024-05-17T09:17:36.406Z",
      "by": {
        "id": "TKN-3836-7769",
        "revision": 1,
        "name": "My token"
      }
    }
  },
  "revision": 1
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
