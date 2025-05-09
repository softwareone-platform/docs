# Invoice

The Invoice object represents an invoice generated in the ERP system. This object contains the following properties:

<table><thead><tr><th width="113">Field</th><th width="229">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Unique identifier of the invoice. Note that no nesting exists for this identifier. </p><p></p><p>Example: INV-123-567-321</p></td></tr><tr><td>statement</td><td><a href="../statement/">Statement</a></td><td><p>Reference to the statement object. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "SOM-1234-5678-9876"
}
</code></pre></td></tr><tr><td>billingType</td><td>BillingType enum</td><td><p>Based on the source of the linked statement, such as a manual upload or journal (automated). </p><p></p><p>Example: Manual</p></td></tr><tr><td>status</td><td>InvoiceStatus enum</td><td><p>Invoice status. </p><p></p><p>Example: Issued</p></td></tr><tr><td>currency</td><td>string</td><td><p>Invoice currency. </p><p></p><p>Example: EUR</p></td></tr><tr><td>client</td><td><a href="../../accounts-api/account/">Account</a></td><td><p>Reference to the client account object. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "ACC-1234-4444",
  "name": "Best LLC",
  "icon": "/static/ACC-1234-4444/account.png"
}   
</code></pre></td></tr><tr><td>buyer</td><td><a href="../../accounts-api/buyer/">Buyer</a></td><td><p>Reference to the buyer object. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "BUY-3731-7971",
    "name": "Adam Ruszczak",
    "icon": "/static/BUY-3731-7971/icon.png"
}
</code></pre></td></tr><tr><td>vendor</td><td>Account</td><td><p>Reference to the vendor account object. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
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
</code></pre></td></tr><tr><td>erpData</td><td><a href="./#erpinvoicedata">ErpInvoiceData</a></td><td><p>Invoice fields from the ERP system. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "erpId": "DE-SCO-1234567",
  "documentNo": "4564564",
  "documentDate": "2025-01-15T12:05:34.087Z",
  "postingDate": "2025-01-15T16:45:24.123Z",
  "dueDate": "2025-02-10T12:05:34.087Z",
  "balanceDue": 123.23,
  "invoiceTotal": 123.23
}
</code></pre></td></tr><tr><td>audit</td><td>AuditObject</td><td><p>Audit object with possible entries: Created or Updated. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr><tr><td>price</td><td>StatementPriceSummary</td><td><p>The invoice price summary with aggregated price values for all invoice charges.</p><p></p><p>The StatementPriceSummary object inherits from PriceSummary and adds tax-related properties: <code>TotalST</code> and <code>TotalGT</code></p><p></p><p>Note that not all fields are visible to all actors. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "totalPP": 229.8,
  "markup": 0.5013,
  "margin": 0.3339,  
  "totalSP": 356.57,
  "totalST": 55,
  "totalGT": 411.57
}
</code></pre></td></tr></tbody></table>

### ErpInvoiceData <a href="#erpinvoicedata" id="erpinvoicedata"></a>

<table><thead><tr><th width="215">Field</th><th width="176">Type</th><th>Description</th></tr></thead><tbody><tr><td>erpId</td><td>string</td><td><p>Identifier in the ERP system. </p><p></p><p>Example: DE-SCO-1234567</p></td></tr><tr><td>documentNo</td><td>string</td><td><p>Document number. </p><p></p><p>Example: 4564564</p></td></tr><tr><td>documentDate</td><td>DateTime</td><td><p>Document date. </p><p></p><p>Example: 2025-01-15T12:05:34.087Z</p></td></tr><tr><td>postingDate</td><td>DateTime</td><td><p>Posting date. </p><p></p><p>Example: 2025-01-15T16:45:24.123Z</p></td></tr><tr><td>dueDate</td><td>DateTime</td><td><p>Due date. </p><p></p><p>Example: 2025-02-10T12:45:34.087Z</p></td></tr><tr><td>balanceDue</td><td>decimal</td><td><p>Balance due. </p><p></p><p>Example: 123.23</p></td></tr><tr><td>invoiceTotal</td><td>decimal</td><td><p>Invoice total. </p><p></p><p>Example: 123.23</p></td></tr></tbody></table>
