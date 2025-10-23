# Ledgers

The Ledger object is created by the rating function within a specific Seller's context, based on the relevant entries of a Journal. Only SoftwareOne Operations can access the Ledgers.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="153">Field</th><th width="186">Type</th><th width="374">Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>A unique identifier for the ledger. No nesting exists for this identifier.</p><p>Example: BLE-1234-1239</p></td></tr><tr><td>journal</td><td><a href="../journal/"><code>journal</code></a></td><td><p>A reference to the Journal object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
 "id": "BJO-1234-5678",
 "name": "29 Nov 2024 #1"
}
</code></pre></td></tr><tr><td>status</td><td><code>enum</code></td><td>The status of the ledger with the possible values as <code>Draft</code>, <code>Rating</code>, <code>Error</code>, <code>Ready</code>, <code>Generating</code>, <code>Generated</code> , <code>Queued</code>, or <code>Completed</code>.</td></tr><tr><td>seller</td><td><a href="../../accounts-api/seller/"><code>seller</code></a></td><td><p>A reference to the Seller object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "SEL-9121-8944",
  "name": "Software LN",
  "icon": "/static/SEL-9121-8944/icon.png"
}
</code></pre></td></tr><tr><td>product</td><td><a href="../../catalog-api/product/"><code>product</code></a></td><td><p>A reference to the Product object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
 "id": "PRD-1111-1111-1111",
  "name": "Microsoft Office 365 NCE",
  "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>currency</td><td><code>string</code></td><td><p>The currency of the ledger.</p><p>Example: EUR</p></td></tr><tr><td>assignee</td><td><a href="../../accounts-api/users/"><code>user</code></a></td><td><p>A reference to the User object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "USR-1234-1234-1234",
  "name": "John Smith",
  "icon": "/static/users/USR-1234-1234-1234.svg"
}
</code></pre></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>Audit object with these possible values, including <code>Created</code> or <code>Updated</code>.</td></tr><tr><td>price</td><td><a href="../journal/#pricesummary"><code>priceSummary</code></a></td><td><p>The ledger price summary including aggregated price values for all ledger charges.</p><p>Note that not all fields are visible to all actors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "totalPP": 229.8,
  "markup": 0.5013,
  "margin": 0.3339,  
  "totalSP": 356.7
}
</code></pre></td></tr><tr><td>processing</td><td><a href="../journal/#processingsummary"><code>processingSummary</code></a></td><td><p>The ledger processing summary including the total charges and counts of ready, error, split, cancelled, and completed charges.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "total": 150,
  "ready": 140,
  "error": 6,
  "split": 4,
  "cancelled": 2,
  "completed": 0    
}
</code></pre></td></tr></tbody></table>
