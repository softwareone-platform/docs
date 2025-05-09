# Statement

The Statement object represents entries generated in the scope of an agreement from the corresponding ledger.&#x20;

Statements are visible to clients, enabling them to reconcile their consumption as necessary. The Statement object contains the following properties:

<table><thead><tr><th width="180">Field</th><th width="217">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Unique identifier for the statement. Note that no nesting exists for this identifier. </p><p></p><p>Example: SOM-1234-5678-9876</p></td></tr><tr><td>ledger</td><td><a href="../ledger/">Ledger</a></td><td><p>Reference to the Ledger object for automated billing. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "BLE-1234-1239"
}
</code></pre></td></tr><tr><td>operationsUpload</td><td>OperationsUpload</td><td><p>Reference to the Operations Upload object for manual billing. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "OUP-5678-9876"
}
</code></pre></td></tr><tr><td>type</td><td>StatementType enum</td><td><p>Type of statement, such as debit or credit. </p><p></p><p>Example: Debit</p></td></tr><tr><td>billingType</td><td>BillingType enum</td><td><p>Based on the source of the statement, such as manual upload (Manual) or journal (automated). </p><p></p><p>Example: Manual</p></td></tr><tr><td>status</td><td>StatementStatus enum</td><td><p>Status of the statement. </p><p></p><p>Example: Issued</p></td></tr><tr><td>currency</td><td>string</td><td><p>Statement currency. </p><p></p><p>Example: EUR</p></td></tr><tr><td>client</td><td><a href="../../accounts-api/account/">Account</a></td><td><p>Reference to the client account object. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-4444",
    "name": "Best LLC",
    "icon": "/static/ACC-1234-4444/account.png"
}
</code></pre></td></tr><tr><td>buyer</td><td><a href="../../accounts-api/buyer/">Buyer</a></td><td><p>Reference to the buyer object. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "BUY-3731-7971",
    "name": "Adam Ruszczak",
    "icon": "/static/BUY-3731-7971/icon.png"
}
</code></pre></td></tr><tr><td>vendor</td><td>Account</td><td><p>Reference to vendor account object. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>seller</td><td><a href="../../accounts-api/seller/">Seller</a></td><td><p>Reference to the seller object. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "SEL-9121-8944",
    "name": "Software LN",
    "icon": "/static/SEL-9121-8944/icon.png"
}
</code></pre></td></tr><tr><td>product</td><td><a href="../../catalog-api/product/">Product</a></td><td><p>Reference to the product object. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>agreement</td><td><a href="../../commerce-api/agreements/">Agreement</a></td><td><p>Reference to the agreement object. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "AGR-2119-4550-8674-5962",
    "name": "Microsoft Office 365 for My Company"
}
</code></pre></td></tr><tr><td>licensee</td><td><a href="../../accounts-api/licensee/">Licensee</a></td><td><p>Reference to the licensee object. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "LCE-9625-9634",
    "name": "John Smith",
    "icon": "/static/LCE-9625-9634/icon.png"
}
</code></pre></td></tr><tr><td>externalId</td><td>string</td><td><p>Identifier in the ERP system. </p><p></p><p>Example: DE-SCO-1234567</p></td></tr><tr><td>audit</td><td>AuditObject</td><td><p>Audit object with possible entries: Created or Updated. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr><tr><td>price</td><td>StatementPriceSummary</td><td><p>The statement price summary with aggregated price values for all statement charges.</p><p></p><p>The StatementPriceSummary object inherits from PriceSummary and adds tax-related properties: <code>TotalST</code> and <code>TotalGT</code></p><p></p><p>Note that not all fields are visible to all actors.</p></td></tr><tr><td>processing</td><td><a href="../journal/#processingsummary">ProcessingSummary</a></td><td><p>The statement processing summary including the total charges and counts of ready, error, split, cancelled, and completed charges. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "total": 150,
  "ready": 140,
  "error": 6,
  "split": 4,
  "cancelled": 2,
  "completed": 0    
}
</code></pre></td></tr></tbody></table>
