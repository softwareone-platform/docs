# Statement

The Statement object represents entries generated in the scope of an agreement from the corresponding ledger. Statements are visible to clients, enabling them to reconcile their consumption as necessary.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="180">Field Name</th><th width="199">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The unique identifier for the statement. No nesting exists for this identifier.</p><p>Example: SOM-1234-5678-9876</p></td></tr><tr><td><code>ledger</code></td><td>object </td><td><p>A reference to the <a href="../ledger/"><code>ledger</code></a> object for automated billing.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "BLE-1234-1239"
}
</code></pre></td></tr><tr><td><code>operationsUpload</code></td><td>object </td><td><p>A reference to the <code>operationsUpload</code> object for manual billing.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "OUP-5678-9876"
}
</code></pre></td></tr><tr><td><code>type</code></td><td>enum</td><td>The type of statement. Allowed values:  <code>debit</code> or <code>credit</code>.</td></tr><tr><td><code>billingType</code></td><td>enum</td><td>The type of billing. Allowed values:  <code>automated</code> or <code>manual</code> .  The values are based on the source of the statement, such as manual upload (manual) or journal (automated).</td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the statement. Allowed values: <code>generated</code>, <code>queued</code>, <code>error</code>, <code>cancelled</code>, <code>pending</code> or <code>issued</code>.</td></tr><tr><td><code>currency</code></td><td>string</td><td><p>The statement's currency.</p><p>Example: EUR</p></td></tr><tr><td><code>client</code></td><td>object</td><td><p>A reference to the client <a href="../../accounts-api/account/"><code>account</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-4444",
    "name": "Best LLC",
    "icon": "/static/ACC-1234-4444/account.png"
}
</code></pre></td></tr><tr><td><code>buyer</code></td><td>object</td><td><p>A reference to the <a href="../../accounts-api/buyer/"><code>buyer</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "BUY-3731-7971",
    "name": "Adam Ruszczak",
    "icon": "/static/BUY-3731-7971/icon.png"
}
</code></pre></td></tr><tr><td><code>vendor</code></td><td>object</td><td><p>A reference to the vendor <a href="../../accounts-api/account/"><code>account</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td><code>seller</code></td><td>object</td><td><p>A reference to the <a href="../../accounts-api/seller/"><code>seller</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "SEL-9121-8944",
    "name": "Software LN",
    "icon": "/static/SEL-9121-8944/icon.png"
}
</code></pre></td></tr><tr><td><code>product</code></td><td>object</td><td><p>A reference to the <a href="../../catalog-api/product/"><code>product</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td><code>agreement</code></td><td>object</td><td><p>A reference to the <a href="../../commerce-api/agreements/"><code>agreement</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "AGR-2119-4550-8674-5962",
    "name": "Microsoft Office 365 for My Company"
}
</code></pre></td></tr><tr><td><code>licensee</code></td><td>object</td><td><p>A reference to the <a href="../../accounts-api/licensee/"><code>licensee</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "LCE-9625-9634",
    "name": "John Smith",
    "icon": "/static/LCE-9625-9634/icon.png"
}
</code></pre></td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>The identifier in the ERP system.</p><p>Example: DE-SCO-1234567</p></td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. Allowed values: <code>created</code> or <code>updated</code>.</td></tr><tr><td><code>price</code></td><td>object</td><td><p>The <code>statementPriceSummary</code> with aggregated price values for all statement charges.</p><p>The <code>statementPriceSummary</code> object inherits from <a href="../journal/#pricesummary"><code>PriceSummary</code></a> and adds <code>totalST</code> and <code>totalGT</code>. Note that not all fields are visible to all actors.</p></td></tr><tr><td><code>processing</code></td><td>object</td><td><p>The statement <a href="../journal/#processingsummary"><code>processingSummary</code></a> including the total charges and counts of ready, error, split, cancelled, and completed charges.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "total": 150,
  "ready": 140,
  "error": 6,
  "split": 4,
  "cancelled": 2,
  "completed": 0    
}
</code></pre></td></tr></tbody></table>
