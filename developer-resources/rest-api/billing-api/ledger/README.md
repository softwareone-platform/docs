# Ledger

The Ledger object is created by the rating function within a specific Seller's context, based on the relevant entries of a Journal. Only SoftwareOne Operations can access the Ledgers.

<table><thead><tr><th width="153">Field</th><th width="190">Type</th><th width="374">Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Unique identifier for the ledger. Note that no nesting exists for this identifier.</p><p>Example: BLE-1234-1239</p></td></tr><tr><td>journal</td><td><a href="../journal/">Journal</a></td><td><p>Reference to the Journal object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
 "id": "BJO-1234-5678",
 "name": "29 Nov 2024 #1"
}
</code></pre></td></tr><tr><td>status</td><td>LedgerStatus enum</td><td><p>Status of the ledger.</p><p>Example: Completed</p></td></tr><tr><td>seller</td><td><a href="../../accounts-api/seller/">Seller</a></td><td><p>Reference to the Seller object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "SEL-9121-8944",
  "name": "Software LN",
  "icon": "/static/SEL-9121-8944/icon.png"
}
</code></pre></td></tr><tr><td>product</td><td><a href="../../catalog-api/product/">Product</a></td><td><p>Reference to the Product object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
 "id": "PRD-1111-1111-1111",
  "name": "Microsoft Office 365 NCE",
  "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>currency</td><td>string</td><td><p>Currency of the ledger.</p><p>Example: EUR</p></td></tr><tr><td>assignee</td><td><a href="../../accounts-api/users/">User</a></td><td><p>Reference to the User object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "USR-1234-1234-1234",
  "name": "John Smith",
  "icon": "/static/users/USR-1234-1234-1234.svg"
}
</code></pre></td></tr><tr><td>audit</td><td>AuditObject</td><td>Audit object with these possible entries: Created or Updated.</td></tr><tr><td>price</td><td><a href="../journal/#pricesummary">PriceSummary</a></td><td><p>The ledger price summary including aggregated price values for all ledger charges.</p><p>Note that not all fields are visible to all actors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "totalPP": 229.8,
  "markup": 0.5013,
  "margin": 0.3339,  
  "totalSP": 356.7
}
</code></pre></td></tr><tr><td>processing</td><td><a href="../journal/#processingsummary">ProcessingSummary</a></td><td><p>The ledger processing summary including the total charges and counts of ready, error, split, cancelled, and completed charges.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "total": 150,
  "ready": 140,
  "error": 6,
  "split": 4,
  "cancelled": 2,
  "completed": 0    
}
</code></pre></td></tr></tbody></table>
