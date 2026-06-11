# Ledger

The Ledger object is created by the rating function within a specific Seller's context, based on the relevant entries of a Journal. Only SoftwareOne Operations can access the Ledgers.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="186">Field</th><th width="118.111083984375">Type</th><th width="374">Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) A unique identifier for the ledger. No nesting exists for this identifier.</td></tr><tr><td><code>journal</code></td><td>object</td><td><p>(Read-only) Represents the <a href="../journal/"><code>journal</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
 "id": "BJO-1234-5678",
 "name": "29 Nov 2024 #1"
}
</code></pre></td></tr><tr><td><code>status</code></td><td>enum</td><td><p>(Read-only) The status of the ledger. Allowed values:</p><ul><li><code>Rating</code></li><li><code>Error</code></li><li><code>Review</code></li><li><code>Generating</code></li><li><code>Generated</code> </li><li><code>Queued</code></li><li><code>Completed</code></li></ul></td></tr><tr><td><code>authorization</code></td><td>object</td><td><p>Represents the <a href="../../catalog-api/#authorization"><code>authorization</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "AUT-1234-4567",
    "href": "/authorization/ATH-1234-45678",
    "name": "Salesforce Enterprise License"
}
</code></pre></td></tr><tr><td><code>seller</code></td><td>object</td><td><p>(Read-only) Represents the <a href="../../accounts-api/seller/"><code>seller</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "SEL-9121-8944",
  "name": "Software LN",
  "icon": "/static/SEL-9121-8944/icon.png"
}
</code></pre></td></tr><tr><td><code>product</code></td><td>object</td><td><p>(Read-only) Represents the <a href="../../catalog-api/product/"><code>product</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
 "id": "PRD-1111-1111-1111",
  "name": "Microsoft Office 365 NCE",
  "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td><code>assignee</code></td><td>object</td><td><p>(Optional) Represents the <a href="../../accounts-api/users/"><code>user</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "USR-1234-1234-1234",
  "name": "John Smith",
  "icon": "/static/users/USR-1234-1234-1234.svg"
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object </td><td><p>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object with allowed values including: </p><ul><li><code>Created</code></li><li><code>Updated</code></li><li><code>Rating</code></li><li><code>Error</code></li><li><code>Review</code></li><li><code>Generating</code></li><li><code>Generated</code></li><li><code>Queued</code></li><li><code>Completed</code></li></ul></td></tr><tr><td><code>price</code></td><td>object</td><td><p>(Read-only) Represents the ledger <a href="../journal/#pricesummary"><code>priceSummary</code></a> , including aggregated price values for all ledger charges. Not all fields are visible to all actors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "totalPP": 229.8,
  "markup": 0.5013,
  "margin": 0.3339,  
  "totalSP": 356.7
}
</code></pre></td></tr><tr><td><code>processing</code></td><td>object</td><td><p>(Read-only) Represents the ledger <a href="../journal/#processingsummary"><code>processingSummary</code></a> including the total charges and counts of ready, error, split, cancelled, and completed charges.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "total": 150,
  "ready": 140,
  "error": 6,
  "split": 4,
  "cancelled": 2,
  "completed": 0    
}  
</code></pre></td></tr><tr><td><code>error</code></td><td>object</td><td><p>(Read-only)Represents the error details associated with the ledger entry, if any. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "BLE:0001",
  "message": "A critical error occurred during recalculation of charges."
}
</code></pre></td></tr></tbody></table>

## Example

{% code title="LEDGER OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
    "id": "BLE-3197-5868-4970-1115",
    "journal": {
        "id": "BJO-3197-5868",
        "name": "01 Jun 2025 #3",
        "dueDate": "2025-06-01T11:00:00.000Z"
    },
    "status": "Completed",
    "authorization": {
        "id": "AUT-4697-9467",
        "name": "CH",
        "currency": "CHF"
    },
    "owner": {
        "id": "SEL-4970-1115",
        "externalId": "CH",
        "address": {
            "country": "CH"
        },
        "name": "SoftwareONE Switzerland",
        "icon": "/v1/accounts/sellers/SEL-4970-1115/icon"
    },
    "seller": {
        "id": "SEL-4970-1115",
        "externalId": "CH",
        "address": {
            "country": "CH"
        },
        "name": "SoftwareONE Switzerland",
        "icon": "/v1/accounts/sellers/SEL-4970-1115/icon"
    },
    "product": {
        "id": "PRD-2507-2933",
        "name": "Microsoft Software Subscriptions",
        "externalIds": {},
        "icon": "/v1/catalog/products/PRD-2507-2933/icon",
        "status": "Published"
    },
    "price": {
        "currency": "CHF",
        "markup": 24.0000000000,
        "margin": 19.3535945696,
        "totalPP": 1045.50000,
        "totalSP": 1296.42000
    },
    "processing": {
        "total": 1,
        "ready": 1,
        "error": 0,
        "split": 0,
        "skipped": 0
    },
    "audit": {
        "rating": {},
        "error": {},
        "review": {},
        "generating": {},
        "generated": {},
        "queued": {},
        "completed": {},
        "created": {
            "at": "2025-05-09T16:53:27.301Z",
            "by": {
                "id": "USR-0000-0000",
                "name": "System"
            }
        },
        "updated": {
            "at": "2025-05-09T17:04:37.430Z",
            "by": {
                "id": "TKN-0291-1452",
                "name": "Marc Serrat",
                "icon": ""
            }
        }
    }
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
