# Pair

The Pair object represents an exchange rate between two currencies, used by one or more sellers in our system to invoice their products.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="133">Field Name</th><th width="146">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary identifier for the currency. </p><p>Example: CUR-1234-4678</p></td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>The identifier within the external system. </p><p>Example: EXCH-1234</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The currency name auto-generated using the ISO codes of both currencies. </p><p>Example: USD > EUR</p></td></tr><tr><td><code>source</code></td><td>object</td><td><p>A reference to the source <a href="../currency/"><code>currency</code></a>. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{ "id": "CUR-1234-0000"}
</code></pre></td></tr><tr><td><code>destination</code></td><td>object</td><td><p>A reference to the <a href="../currency/"><code>currency</code></a> currency. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{ "id": "CUR-1456-0000"}
</code></pre></td></tr><tr><td><code>notes</code></td><td>string</td><td><p>The optional text that was provided when creating the rate. </p><p>Example: "Represents the exchange rate between USD and EUR."</p></td></tr><tr><td><code>latestRate</code></td><td>rate</td><td><p>The <a href="../rate/"><code>rate</code></a> of exchange from source to destination. </p><p>Example: 0.8723</p></td></tr><tr><td><code>updatedAt</code></td><td>datetime</td><td><p>The date when the rate was last updated. </p><p>Example: 2024-04-08T06:30:05.807Z</p></td></tr><tr><td><code>agreements</code></td><td>integer</td><td><p>The number of agreements currently using this pair. </p><p>Example: 34</p></td></tr><tr><td><code>status</code></td><td>string</td><td>Indicates whether the item is <code>active</code> or <code>deleted</code>. </td></tr><tr><td><code>audit</code></td><td>object</td><td><p>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
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
}  "id": "FXP-0000-0002",
    "name": "USD: EUR",
    "revision": 1,
    "latestRate": {
      "id": "FXR-1234-8909",
      "rate": "0.1",
      "revision": 1
    }
  }
}
</code></pre></td></tr><tr><td><code>primary</code></td><td>bool</td><td><p>Indicates if the pair is primary. </p><p>Example: true</p></td></tr><tr><td><code>reverse</code></td><td>pair</td><td><p>Indicates reverse pair.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "reverse": {
    "id": "FXP-0000-0002",
    "name": "USD:EUR",
    "revision": 1,
    "latestRate": {
      "id": "FXR-1234-8909",
      "rate": "0.1",
      "revision": 1
    }
  }
}
</code></pre></td></tr><tr><td><code>revision</code></td><td>integer</td><td><p>The entity revision number.</p><p>Example: 3</p></td></tr></tbody></table>

### Example response

{% code lineNumbers="true" %}
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
