# Statement

The Statement object represents entries generated in the scope of an agreement from the corresponding ledger. Statements are visible to clients, enabling them to reconcile their consumption as necessary.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="180">Field</th><th width="137">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The unique identifier for the statement. No nesting exists for this identifier.</td></tr><tr><td><code>ledger</code></td><td>object </td><td><p>(Read-only) (Optional) Represents the <a href="../ledger/"><code>ledger</code></a> object for automated billing.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "BLE-1234-1239"
}
</code></pre></td></tr><tr><td><code>customLedger</code></td><td>object </td><td>Represents the <code>customLedger</code> object for manual billing.</td></tr><tr><td><code>externalIds</code></td><td>object </td><td>(Optional) Represents the external identifiers used for the client and for vendor/operations systems.</td></tr><tr><td><code>type</code></td><td>enum</td><td>(Optional) The type of statement. Allowed values are <code>debit</code> or <code>credit</code>.</td></tr><tr><td><code>billingType</code></td><td>enum</td><td>The type of billing. The allowed values  <code>automated</code> or <code>manual</code> are based on the source of the statement, such as manual upload (manual) or journal (automated).</td></tr><tr><td><code>status</code></td><td>enum</td><td><p>The status of the statement. Allowed values are </p><ul><li><code>Generated</code></li><li><code>Queued</code></li><li><code>Error</code></li><li><code>Cancelled</code></li><li><code>Pending</code></li><li><code>Issued</code></li></ul></td></tr><tr><td><code>currency</code></td><td>string</td><td>The currency of the statement.</td></tr><tr><td><code>client</code></td><td>object</td><td>(Read-only) Represents the client <a href="../../accounts-api/account/"><code>account</code></a> object.</td></tr><tr><td><code>buyer</code></td><td>object</td><td><p>(Read-only) Represents the <a href="../../accounts-api/buyer/"><code>buyer</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "BUY-3731-7971",
    "name": "Adam Ruszczak",
    "icon": "/static/BUY-3731-7971/icon.png"
}
</code></pre></td></tr><tr><td><code>vendor</code></td><td>object</td><td><p>(Read-only) Represents the vendor <a href="../../accounts-api/account/"><code>account</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td><code>seller</code></td><td>object</td><td><p>(Read-only) Represents the <a href="../../accounts-api/seller/"><code>seller</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "SEL-9121-8944",
    "name": "Software LN",
    "icon": "/static/SEL-9121-8944/icon.png"
}
</code></pre></td></tr><tr><td><code>product</code></td><td>object</td><td><p>(Read-only) (Optional) Represents the <a href="../../catalog-api/product/"><code>product</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td><code>agreement</code></td><td>object</td><td><p>(Read-only) (Optional) Represents the <a href="../../commerce-api/agreements/"><code>agreement</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "AGR-2119-4550-8674-5962",
    "name": "Microsoft Office 365 for My Company"
}
</code></pre></td></tr><tr><td><code>licensee</code></td><td>object</td><td><p>(Read-only) (Optional) Represents the <a href="../../accounts-api/licensee/"><code>licensee</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "LCE-9625-9634",
    "name": "John Smith",
    "icon": "/static/LCE-9625-9634/icon.png"
}
</code></pre></td></tr><tr><td><code>externalId</code></td><td>string, core</td><td>(Optional) The identifier in the ERP system.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. Allowed values: <code>created</code> or <code>updated</code>.</td></tr><tr><td><code>price</code></td><td>object</td><td><p>(Read-only) Represents the <code>statementPriceSummary</code> object with aggregated price values for all statement charges.</p><p>The <code>statementPriceSummary</code> object inherits from <a href="../journal/#pricesummary"><code>PriceSummary</code></a> and adds <code>totalST</code> and <code>totalGT</code>. Note that not all fields are visible to all actors.</p></td></tr><tr><td><code>processing</code></td><td>object</td><td>(Read-only) Represents the statement <a href="../journal/#processingsummary"><code>processingSummary</code></a> including the total charges and counts of ready, error, split, cancelled, and completed charges.</td></tr><tr><td><code>statusNotes</code></td><td>object</td><td>(Read-only) (Optional) Contains additional notes or messages about the status of the statement, if applicable.</td></tr><tr><td><code>error</code></td><td>object</td><td><p>(Read-only) (Optional) Represents the <code>error</code> object containing error details associated with the statement entry, if any. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "SOM:0001",
  "message": "The debit statement contains a negative price, which is invalid."
}

</code></pre></td></tr><tr><td><code>invoice</code></td><td>object</td><td>(Read-only) (Optional) Represents the <a href="../invoice/"><code>Invoice</code></a> object.</td></tr></tbody></table>

## Example

{% code title="STATEMENT OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
    "id": "SOM-3197-5868-3617-1129-0665",
    "externalIds": {
        "erpId": "CH-CO-1249923"
    },
    "ledger": {
        "id": "BLE-3197-5868-4970-1115",
        "owner": {
            "id": "SEL-4970-1115",
            "externalId": "CH",
            "address": {
                "addressLine1": "Riedenmatt 4",
                "postCode": "6000",
                "city": "Stans",
                "state": "N/A",
                "country": "CH"
            },
            "name": "SoftwareONE Switzerland",
            "icon": "/v1/accounts/sellers/SEL-4970-1115/icon"
        }
    },
    "type": "Debit",
    "billingType": "Automated",
    "status": "Issued",
    "client": {
        "id": "ACC-3287-0000",
        "type": "Client",
        "status": "Active",
        "name": "FRX company"
    },
    "buyer": {
        "id": "BUY-1369-5376",
        "name": "Schelling AG"
    },
    "vendor": {
        "id": "ACC-6502-7513",
        "type": "Vendor",
        "status": "Enabled",
        "name": "CSP Microsoft",
        "icon": "/v1/accounts/accounts/ACC-6502-7513/icon"
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
    "agreement": {
        "id": "AGR-3617-1129-0665",
        "status": "Active",
        "name": "Microsoft Software Subscriptions"
    },
    "licensee": {
        "id": "LCE-3639-3419-3755",
        "name": "Billing test licensee"
    },
    "price": {
        "currency": {
            "purchase": "CHF",
            "sale": "CHF",
            "rate": 1.0000000000
        },
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
        "generated": {},
        "queued": {},
        "error": {},
        "cancelled": {},
        "pending": {},
        "issued": {},
        "generating": {},
        "created": {
            "at": "2025-05-09T16:53:51.607Z",
            "by": {
                "id": "USR-0000-0000",
                "name": "System"
            }
        },
        "updated": {
            "at": "2025-05-09T17:04:37.310Z",
            "by": {
                "id": "TKN-0291-1452",
                "name": "Jane Doe",
                "icon": ""
            }
        }
    }
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
