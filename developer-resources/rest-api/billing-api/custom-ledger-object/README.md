# Custom Ledger

The Custom Ledger object is required to submit billing information for clients with manual billing activated. Only SoftwareOne Operations can access this object.&#x20;

<table><thead><tr><th width="144">Field</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The unique identifier. Note that no nesting exists for this identifier.</p><p>Example: OUP-1234-1239</p></td></tr><tr><td>seller</td><td><a href="../../accounts-api/seller/"><code>seller</code></a></td><td><p>A reference to the Seller object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "SEL-9121-8944",
    "name": "Software LN",
    "icon": "/static/SEL-9121-8944/icon.png"
}
</code></pre></td></tr><tr><td>vendor</td><td><a href="../../accounts-api/account/"><code>account</code></a></td><td><p>A reference to the vendor account object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>billingStartDate</td><td><code>dateTime</code></td><td><p>The billing start date.</p><p>Example: 2025-01-10T09:09:30.087Z</p></td></tr><tr><td>billingEndDate</td><td><code>dateTime</code></td><td><p>The billing end date.</p><p>Example: 2025-02-10T09:09:30.087Z30.087Z</p></td></tr><tr><td>currency</td><td><code>string</code></td><td><p>Custom ledger's currency.</p><p>Example: EUR</p></td></tr><tr><td>externalId</td><td><code>string</code></td><td><p>The external ID or reference number. An optional value to match the Custom Ledger with external ERP systems.</p><p>Example: bill-12345609.</p></td></tr><tr><td>notes</td><td><code>string</code></td><td><p>Notes related to the custom ledger.</p><p>Example: Billing data for the import file.</p></td></tr><tr><td>status</td><td><code>enum</code></td><td><p>The status of the ledger. </p><p>Possible values: <code>Draft</code>, <code>Deleted</code>, <code>Validating</code>, <code>Validated</code>, <code>Error</code>, <code>Generating</code>, <code>Queued</code>, or <code>Completed</code>.</p></td></tr><tr><td>assignee</td><td><a href="../../accounts-api/users/"><code>user</code></a></td><td><p>A reference to the User object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "USR-1234-1234-1234",
  "name": "John Smith",
  "icon": "/static/users/USR-1234-1234-1234.svg"
}
</code></pre></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>The Audit object with possible entries, including <code>Created</code> or <code>Updated</code>.</td></tr><tr><td>price</td><td><a href="../journal/#pricesummary"><code>priceSummary</code></a></td><td><p>The custom ledger price summary including the aggregated price values for all charges.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "totalPP": 229.8,
  "markup": 0.5013,
  "margin": 0.3339,  
  "totalSP": 356.7
}
</code></pre></td></tr><tr><td>processing</td><td><a href="../journal/#processingsummary"><code>processingSummary</code></a></td><td><p>The custom ledger processing summary including the total charges and counts of ready, error, split, cancelled, and completed charges.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "total": 150,
  "ready": 140,
  "error": 6,
  "split": 4,
  "cancelled": 2,
  "completed": 0    
}
</code></pre></td></tr></tbody></table>

