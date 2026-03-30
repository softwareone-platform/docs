# Ledger

The Ledger object is created by the rating function within a specific Seller's context, based on the relevant entries of a Journal. Only SoftwareOne Operations can access the Ledgers.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="153">Field Name</th><th width="186">Data Type</th><th width="374">Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>A unique identifier for the ledger. No nesting exists for this identifier.</p><p>Example: BLE-1234-1239</p></td></tr><tr><td><code>journal</code></td><td>object</td><td><p>A reference to the <a href="../journal/"><code>journal</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
 "id": "BJO-1234-5678",
 "name": "29 Nov 2024 #1"
}
</code></pre></td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the ledger. Allowed values: <code>draft</code>, <code>rating</code>, <code>error</code>, <code>ready</code>, <code>generating</code>, <code>generated</code> , <code>queued</code>, or <code>completed</code>.</td></tr><tr><td><code>seller</code></td><td>object</td><td><p>A reference to the <a href="../../accounts-api/seller/"><code>seller</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "SEL-9121-8944",
  "name": "Software LN",
  "icon": "/static/SEL-9121-8944/icon.png"
}
</code></pre></td></tr><tr><td><code>product</code></td><td>object</td><td><p>A reference to the <a href="../../catalog-api/product/"><code>product</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
 "id": "PRD-1111-1111-1111",
  "name": "Microsoft Office 365 NCE",
  "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td><code>currency</code></td><td>string</td><td><p>The currency of the ledger.</p><p>Example: EUR</p></td></tr><tr><td><code>assignee</code></td><td>object</td><td><p>A reference to the <a href="../../accounts-api/users/"><code>user</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "USR-1234-1234-1234",
  "name": "John Smith",
  "icon": "/static/users/USR-1234-1234-1234.svg"
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object </td><td>The <a href="../../common-api-objects/audit.md"><code>audit</code></a> object with allowed values as including <code>created</code> or <code>updated</code>.</td></tr><tr><td><code>price</code></td><td>object</td><td><p>The ledger <a href="../journal/#pricesummary"><code>priceSummary</code></a> including aggregated price values for all ledger charges.</p><p>Note that not all fields are visible to all actors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "totalPP": 229.8,
  "markup": 0.5013,
  "margin": 0.3339,  
  "totalSP": 356.7
}
</code></pre></td></tr><tr><td><code>processing</code></td><td>object</td><td><p>The ledger <a href="../journal/#processingsummary"><code>processingSummary</code></a> including the total charges and counts of ready, error, split, cancelled, and completed charges.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "total": 150,
  "ready": 140,
  "error": 6,
  "split": 4,
  "cancelled": 2,
  "completed": 0    
}
</code></pre></td></tr></tbody></table>
