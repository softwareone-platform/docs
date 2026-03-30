# Currency

The Currency object represents a currency that is used by one or more sellers in our system to invoice their products.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="137">Field Name</th><th width="183">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary identifier for the currency. </p><p>Example: CUR-1234-4678</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The currency name. </p><p>Example: Euro</p></td></tr><tr><td><code>code</code></td><td>string</td><td><p>The ISO code for the currency. </p><p>Example: EUR</p></td></tr><tr><td><code>icon</code></td><td>string</td><td><p>The icon to be shown in the grids and info cards.</p><p>Example: http://icons.com/myicon.jpg</p></td></tr><tr><td><code>precision</code></td><td>integer</td><td><p>The number of decimals supported by the currency. </p><p>Example: 2</p></td></tr><tr><td><code>statistics</code></td><td>object (<a href="./#currencystatistics">currencyStatistics</a>)</td><td><p>A <code>JSON</code> representation of statistics.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "sellerCount": 2,
  "pairCount": 27
}
</code></pre></td></tr><tr><td><code>status</code></td><td>string</td><td>Indicates whether the item is <code>active</code> or <code>deleted</code>.</td></tr><tr><td><code>audit</code></td><td>object</td><td><p>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
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
</code></pre></td></tr><tr><td><code>revision</code></td><td>integer</td><td><p>The revision number. </p><p>Example: 3</p></td></tr></tbody></table>

### CurrencyStatistics <a href="#currencystatistics" id="currencystatistics"></a>

<table><thead><tr><th width="131">Field Name</th><th width="124">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>sellerCount</code></td><td>integer</td><td><p>The number of sellers using this currency. </p><p>Example: 35</p></td></tr><tr><td><code>pairCount</code></td><td>integer</td><td><p>The number of pairs that use this currency. </p><p>Example: 344</p></td></tr></tbody></table>

### Example response

{% code lineNumbers="true" %}
```json
{
  "id": "CUR-1671",
  "name": "Euro",
  "code": "EUR",
  "precision": 2,
  "status": "Active",
  "statistics": 
  {
    "sellerCount": 35,
    "pairCount": 344,  
  },
  "icon": "/v1/exchange/currencies/CUR-1671/icon",
  "revision": 1
}
```
{% endcode %}
