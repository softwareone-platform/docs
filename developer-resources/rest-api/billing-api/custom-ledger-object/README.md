# Custom Ledger

The Custom Ledger object is required to submit billing information for clients with manual billing activated. Only SoftwareOne Operations can access this object.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="168">Field Name</th><th width="171">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The unique identifier. Note that no nesting exists for this identifier.</p><p>Example: OUP-1234-1239</p></td></tr><tr><td><code>seller</code></td><td>object</td><td><p>A reference to the <a href="../../accounts-api/seller/"><code>seller</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "SEL-9121-8944",
    "name": "Software LN",
    "icon": "/static/SEL-9121-8944/icon.png"
}
</code></pre></td></tr><tr><td><code>vendor</code></td><td>object</td><td><p>A reference to the vendor <a href="../../accounts-api/account/"><code>account</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td><code>billingStartDate</code></td><td>dateTime</td><td><p>The billing start date.</p><p>Example: 2025-01-10T09:09:30.087Z</p></td></tr><tr><td><code>billingEndDate</code></td><td>dateTime</td><td><p>The billing end date.</p><p>Example: 2025-02-10T09:09:30.087Z30.087Z</p></td></tr><tr><td><code>currency</code></td><td>string</td><td><p>Custom ledger's currency.</p><p>Example: EUR</p></td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>The external ID or reference number. An optional value to match the Custom Ledger with external ERP systems.</p><p>Example: bill-12345609.</p></td></tr><tr><td><code>notes</code></td><td>string</td><td><p>Notes related to the custom ledger.</p><p>Example: Billing data for the import file.</p></td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the ledger. Allowed values: <code>draft</code>, <code>deleted</code>, <code>validating</code>, <code>validated</code>, <code>error</code>, <code>generating</code>, <code>queued</code>, or <code>completed</code>.</td></tr><tr><td><code>assignee</code></td><td>object</td><td><p>A reference to the <a href="../../accounts-api/users/"><code>user</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "USR-1234-1234-1234",
  "name": "John Smith",
  "icon": "/static/users/USR-1234-1234-1234.svg"
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>The <a href="../../common-api-objects/audit.md"><code>audit</code></a> object with allowed entries, including <code>created</code> or <code>updated</code>.</td></tr><tr><td><code>price</code></td><td>object</td><td><p>The custom ledger <a href="../journal/#pricesummary"><code>priceSummary</code></a> including the aggregated price values for all charges.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "totalPP": 229.8,
  "markup": 0.5013,
  "margin": 0.3339,  
  "totalSP": 356.7
}
</code></pre></td></tr><tr><td><code>processing</code></td><td>object</td><td><p>The custom ledger <a href="../journal/#processingsummary"><code>processingSummary</code></a> including the total charges and counts of ready, error, split, cancelled, and completed charges.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "total": 150,
  "ready": 140,
  "error": 6,
  "split": 4,
  "cancelled": 2,
  "completed": 0    
}
</code></pre></td></tr></tbody></table>
