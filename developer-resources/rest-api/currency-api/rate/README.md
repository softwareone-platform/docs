# Rate

The Rate object represents an exchange rate between two currencies.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="140">Field Name</th><th width="162">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary identifier for the rate. </p><p>Example: FXR-1234-4678-0000-0001</p></td></tr><tr><td><code>pair</code></td><td>object</td><td><p>A reference to the currency <a href="../pair/"><code>pair</code></a> this rate applies to. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{ "id": "FXP-1234-4678" }
</code></pre></td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>The ID of the external system from where the rate is fetched. </p><p>Example: EXCHR-23456</p></td></tr><tr><td><code>recordDate</code></td><td>datetime</td><td>The date and time when this rate was fetched. Example: 2024-05-09T14:40:28.958Z</td></tr><tr><td><code>rate</code></td><td>number</td><td><p>The exchange rate from currency A to B. </p><p>Example: 1.3267</p></td></tr><tr><td><code>status</code></td><td>string</td><td>Indicates whether the item is active or deleted. Example: Active</td></tr><tr><td><code>audit</code></td><td>object</td><td><p>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
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
    },
  "deleted": {
    "at": "2024-05-17T09:17:36.406Z",
    "by": {
      "id": "TKN-3836-7769",
      "revision": 1,
      "name": "My token"
    }
  }
}
</code></pre></td></tr><tr><td><code>revision</code></td><td>integer</td><td><p>The entity revision number.</p><p>Example: 3</p></td></tr></tbody></table>

### Example response

{% code lineNumbers="true" %}
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
