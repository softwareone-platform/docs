# Pair

The Pair object represents an exchange rate between two currencies, used by one or more sellers in our system to invoice their products.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-search="false"><thead><tr><th width="133">Field</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The primary identifier for the currency. </td></tr><tr><td><code>externalId</code></td><td>string</td><td>(Optional) The identifier within the external system. </td></tr><tr><td><code>name</code></td><td>string, core</td><td>(Read-only) User‑friendly name. Auto‑generated from the ISO codes of both currencies.</td></tr><tr><td><code>source</code></td><td>object</td><td>Represents the source <a href="../currency/"><code>currency</code></a> object.</td></tr><tr><td><code>destination</code></td><td>object</td><td>Represents the destination <a href="../currency/"><code>currency</code></a> object.</td></tr><tr><td><code>notes</code></td><td>string</td><td>The optional text that was provided when creating the rate. </td></tr><tr><td><code>latestRate</code></td><td>rate, core</td><td>The <a href="../rate/"><code>rate</code></a> of exchange from source to destination. </td></tr><tr><td><code>updatedAt</code></td><td>datetime</td><td>The date when the rate was last updated. </td></tr><tr><td><code>agreements</code></td><td>integer</td><td>(Read-only) Number of agreements currently using this pair. </td></tr><tr><td><code>status</code></td><td>string</td><td>Indicates whether the item is <code>active</code> or <code>deleted</code>. </td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>primary</code></td><td>bool</td><td>(Read-only) Indicates if the pair is primary. </td></tr><tr><td><code>reverse</code></td><td>pair</td><td>(Read-only) Indicates reverse pair.</td></tr><tr><td><code>revision</code></td><td>integer, core</td><td>The entity's revision number.</td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% code title="PAIR OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "$meta": {
    "pagination": {
      "offset": 0,
      "limit": 10,
      "total": 261
    },
    "omitted": [
      "audit"
    ]
  },
  "data": [
    {
      "id": "FXP-0000-0001",
      "name": "EUR: USD",
      "revision": 1,
      "externalId": "EXT-1234",
      "notes": "notes",
      "source": {
        "id": "CUR-1234",
        "name": "Euro",
        "code": "EUR",
        "revision": 1
      },
      "destination": {
        "id": "CUR-2345",
        "name": "Dollar",
        "code": "USD",
        "revision": 1
      },
      "latestRate": {
        "id": "FXR-1234-8907",
        "rate": "4.23658350000",
        "revision": 1
      },
      "primary": "true",
      "reverse": {
        "id": "FXP-0000-0002",
        "name": "USD: EUR",
        "revision": 1,
        "latestRate": {
          "id": "FXR-1234-8909",
          "rate": "0.1",
          "revision": 1
        }
      },
      "agreements": 0,
      "status": "Active"
    }
  ]
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
