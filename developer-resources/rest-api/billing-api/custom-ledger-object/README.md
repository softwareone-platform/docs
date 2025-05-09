# Custom Ledger Object

The Custom Ledger object is required to submit billing information for clients with manual billing activated.&#x20;

Only SoftwareOne Operations can access this object, containing the following properties:

<table><thead><tr><th width="197">Field</th><th width="186">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Unique identifier. Note that no nesting exists for this identifier. </p><p></p><p>Example: OUP-1234-1239</p></td></tr><tr><td>seller</td><td><a href="../../accounts-api/seller/">Seller</a></td><td><p>Reference to the Seller object. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "SEL-9121-8944",
    "href": "/accounts/sellers/SEL-9121-8944",
    "name": "Software LN",
    "icon": "/static/SEL-9121-8944/icon.png"
}
</code></pre></td></tr><tr><td>vendor</td><td>Account</td><td><p>Reference to the vendor account object. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "href": "/accounts/accounts/ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>billingStartDate</td><td>DateTime</td><td><p>Billing start date. </p><p></p><p>Example: 2025-01-10T09:09:30.087Z</p></td></tr><tr><td>billingEndDate</td><td>DateTime</td><td><p>Billing end date. </p><p></p><p>Example: 2025-02-10T09:09:30.087Z30.087Z</p></td></tr><tr><td>currency</td><td>string</td><td><p>Custom ledger's currency. </p><p></p><p>Example: EUR</p></td></tr><tr><td>externalId</td><td>string</td><td><p>Reference number. An optional value to match the Custom Ledger with external ERP systems. </p><p></p><p>Example: bill-12345609.</p></td></tr><tr><td>notes</td><td>string</td><td><p>Notes related to the custom ledger.</p><p></p><p>Example: Billing data of the NAV import file</p></td></tr><tr><td>status</td><td>ManualUploadStatus enum</td><td><p>Status of the ledger. </p><p></p><p>Example: Validated</p></td></tr><tr><td>assignee</td><td><a href="../../accounts-api/users/">User</a></td><td><p>Reference to the User object. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "USR-1234-1234-1234",
  "name": "John Smith",
  "icon": "/static/users/USR-1234-1234-1234.svg"
}
</code></pre></td></tr><tr><td>audit</td><td>AuditObject</td><td><p>Audit object with possible entries, including created or updated. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr><tr><td>price</td><td><a href="../journal/#pricesummary">PriceSummary</a></td><td><p>Custom Ledger price summary including the aggregated price values for all charges. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "totalPP": 229.8,
  "markup": 0.5013,
  "margin": 0.3339,  
  "totalSP": 356.7
}
</code></pre></td></tr><tr><td>processing</td><td><a href="../journal/#processingsummary">ProcessingSummary</a></td><td><p>Custom Ledger processing summary including the total charges and counts of ready, error, split, cancelled, and completed charges. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "total": 150,
  "ready": 140,
  "error": 6,
  "split": 4,
  "cancelled": 2,
  "completed": 0    
}
</code></pre></td></tr></tbody></table>

\
