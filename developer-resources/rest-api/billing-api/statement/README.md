# Statements

The Statement object represents entries generated in the scope of an agreement from the corresponding ledger.

Statements are visible to clients, enabling them to reconcile their consumption as necessary. The Statement object contains the following properties:

<table><thead><tr><th width="180">Field</th><th width="199">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The unique identifier for the statement. No nesting exists for this identifier.</p><p>Example: SOM-1234-5678-9876</p></td></tr><tr><td>ledger</td><td><a href="../ledger/"><code>ledger</code></a></td><td><p>A reference to the Ledger object for automated billing.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "BLE-1234-1239"
}
</code></pre></td></tr><tr><td>operationsUpload</td><td><code>operationsUpload</code></td><td><p>A reference to the Operations Upload object for manual billing.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "OUP-5678-9876"
}
</code></pre></td></tr><tr><td>type</td><td><code>enum</code></td><td>The type of statement. The possible values are <code>Debit</code> or <code>Credit</code>.</td></tr><tr><td>billingType</td><td><code>enum</code></td><td><p>The type of billing. The possible values are <code>Automated</code> or <code>Manual</code> .  </p><p>The values are based on the source of the statement, such as manual upload (Manual) or journal (automated).</p></td></tr><tr><td>status</td><td><code>enum</code></td><td>The status of the statement. The possible values are <code>Generated</code>, <code>Queued</code>, <code>Error</code>, <code>Cancelled</code>, <code>Pending</code>, or <code>Issued</code>.</td></tr><tr><td>currency</td><td><code>string</code></td><td><p>The statement's currency.</p><p>Example: EUR</p></td></tr><tr><td>client</td><td><a href="../../accounts-api/account/"><code>account</code></a></td><td><p>A reference to the Client Account object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-4444",
    "name": "Best LLC",
    "icon": "/static/ACC-1234-4444/account.png"
}
</code></pre></td></tr><tr><td>buyer</td><td><a href="../../accounts-api/buyer/"><code>buyer</code></a></td><td><p>A reference to the Buyer object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "BUY-3731-7971",
    "name": "Adam Ruszczak",
    "icon": "/static/BUY-3731-7971/icon.png"
}
</code></pre></td></tr><tr><td>vendor</td><td><a href="../../accounts-api/account/"><code>account</code></a></td><td><p>A reference to the Vendor Account object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>seller</td><td><a href="../../accounts-api/seller/"><code>seller</code></a></td><td><p>A reference to the Seller object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "SEL-9121-8944",
    "name": "Software LN",
    "icon": "/static/SEL-9121-8944/icon.png"
}
</code></pre></td></tr><tr><td>product</td><td><a href="../../catalog-api/product/"><code>product</code></a></td><td><p>A reference to the Product object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>agreement</td><td><a href="../../commerce-api/agreements/"><code>agreement</code></a></td><td><p>A reference to the Agreement object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "AGR-2119-4550-8674-5962",
    "name": "Microsoft Office 365 for My Company"
}
</code></pre></td></tr><tr><td>licensee</td><td><a href="../../accounts-api/licensee/"><code>licensee</code></a></td><td><p>A reference to the Licensee object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "LCE-9625-9634",
    "name": "John Smith",
    "icon": "/static/LCE-9625-9634/icon.png"
}
</code></pre></td></tr><tr><td>externalId</td><td><code>string</code></td><td><p>The identifier in the ERP system.</p><p>Example: DE-SCO-1234567</p></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the Audit object with possible values including,  <code>Created</code> or <code>Updated</code>.</td></tr><tr><td>price</td><td><code>statementPriceSummary</code></td><td><p>The statement price summary with aggregated price values for all statement charges.</p><p>The StatementPriceSummary object inherits from <a href="../journal/#pricesummary">PriceSummary</a> and adds these tax-related properties: <code>TotalST</code> and <code>TotalGT</code> .</p><p>Note that not all fields are visible to all actors.</p></td></tr><tr><td>processing</td><td><a href="../journal/#processingsummary"><code>processingSummary</code></a></td><td><p>The statement processing summary including the total charges and counts of ready, error, split, cancelled, and completed charges.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "total": 150,
  "ready": 140,
  "error": 6,
  "split": 4,
  "cancelled": 2,
  "completed": 0    
}
</code></pre></td></tr></tbody></table>
