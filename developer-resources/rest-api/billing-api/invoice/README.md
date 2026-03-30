# Invoice

The Invoice object represents an invoice generated in the ERP system.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="131">Field Name</th><th width="204">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The unique identifier of the invoice. No nesting exists for this identifier.</p><p>Example: INV-123-567-321</p></td></tr><tr><td><code>statement</code></td><td>object</td><td><p>A reference to the <a href="../statement/"><code>statement</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "SOM-1234-5678-9876"
}
</code></pre></td></tr><tr><td><code>billingType</code></td><td>enum</td><td>The type of billing. Allowed values: <code>automated</code> or <code>manual</code>. The values are based on the source of the linked statement, such as a manual upload or journal (automated).</td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the invoice. Allowed values:  <code>issued</code>, <code>paid</code>, or <code>overdue</code>.</td></tr><tr><td><code>currency</code></td><td>string</td><td><p>The invoice currency.</p><p>Example: EUR</p></td></tr><tr><td><code>client</code></td><td>object</td><td><p>A reference to the client <a href="../../accounts-api/account/"><code>account</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
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
</code></pre></td></tr><tr><td><code>erpData</code></td><td>object (<a href="./#erpinvoicedata"><code>erpInvoiceData</code></a>)</td><td><p>The invoice fields from the ERP system.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "erpId": "DE-SCO-1234567",
  "documentNo": "4564564",
  "documentDate": "2025-01-15T12:05:34.087Z",
  "postingDate": "2025-01-15T16:45:24.123Z",
  "dueDate": "2025-02-10T12:05:34.087Z",
  "balanceDue": 123.23,
  "invoiceTotal": 123.23
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>The <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. Allowed values: <code>created</code> or <code>updated</code>.</td></tr><tr><td><code>price</code></td><td>object</td><td><p>The invoice price summary with aggregated price values for all invoice charges. The <code>statementPriceSummary</code> object inherits from <a href="../journal/#pricesummary"><code>PriceSummary</code></a> and adds tax-related properties: <code>totalST</code> and <code>totalGT</code>.</p><p>Note that not all fields are visible to all actors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "totalPP": 229.8,
  "markup": 0.5013,
  "margin": 0.3339,  
  "totalSP": 356.57,
  "totalST": 55,
  "totalGT": 411.57
}
</code></pre></td></tr></tbody></table>

### ERP Invoice Data object <a href="#erpinvoicedata" id="erpinvoicedata"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="164">Field Name</th><th width="149">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>erpId</code></td><td>string</td><td><p>Identifier in the ERP system.</p><p>Example: DE-SCO-1234567</p></td></tr><tr><td><code>documentNo</code></td><td>string</td><td><p>The document number.</p><p>Example: 4564564</p></td></tr><tr><td><code>documentDate</code></td><td>dateTime</td><td><p>The document date.</p><p>Example: 2025-01-15T12:05:34.087Z</p></td></tr><tr><td><code>postingDate</code></td><td>dateTime</td><td><p>The posting date.</p><p>Example: 2025-01-15T16:45:24.123Z</p></td></tr><tr><td><code>dueDate</code></td><td>dateTime</td><td><p>The due date.</p><p>Example: 2025-02-10T12:45:34.087Z</p></td></tr><tr><td><code>balanceDue</code></td><td>decimal</td><td><p>The balance due.</p><p>Example: 123.23</p></td></tr><tr><td><code>invoiceTotal</code></td><td>decimal</td><td><p>The invoice total.</p><p>Example: 123.23</p></td></tr></tbody></table>
