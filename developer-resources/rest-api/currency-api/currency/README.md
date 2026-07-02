# Currency

The Currency object represents a currency used by the sellers to invoice their products.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-search="false"><thead><tr><th width="154">Field</th><th width="138">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) Primary identifier for the currency. </td></tr><tr><td><code>name</code></td><td>string, core</td><td>The currency name. </td></tr><tr><td><code>code</code></td><td>string, core</td><td>The currency's ISO code.</td></tr><tr><td><code>icon</code></td><td>string</td><td>The icon to be shown in grids and info cards.</td></tr><tr><td><code>precision</code></td><td>integer</td><td>The number of decimals supported by the currency. </td></tr><tr><td><code>statistics</code></td><td>object</td><td>Represents the <a href="./#currencystatistics"><code>statistics</code></a> object.</td></tr><tr><td><code>status</code></td><td>string</td><td>Indicates whether the item is <code>active</code> or <code>deleted</code>.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>revision</code></td><td>integer, core</td><td>Represents the entity revision number. </td></tr></tbody></table>

## Statistics object <a href="#currencystatistics" id="currencystatistics"></a>

<table><thead><tr><th width="131">Field</th><th width="124">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>sellerCount</code></td><td>integer</td><td>(Read-only) Number of sellers using this currency. </td></tr><tr><td><code>pairCount</code></td><td>integer</td><td>(Read-only) Number of pairs that use this currency. </td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% code title="CURRENCY OBJECT" overflow="wrap" lineNumbers="true" %}
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
