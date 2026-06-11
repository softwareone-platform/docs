# Invoice

The Invoice object represents an invoice generated in the ERP system.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="156">Name</th><th width="147">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) Unique identifier for the invoice. No nesting exists for this identifier.</td></tr><tr><td><code>statement</code></td><td>object</td><td>(Read-only) Represents the <a href="../statement/"><code>statement</code></a> object.</td></tr><tr><td><code>billingType</code></td><td>enum</td><td>(Read-only) The type of billing. Allowed values: <code>automated</code> or <code>manual</code>. The values are based on the source of the linked statement, such as a manual upload or journal (automated).</td></tr><tr><td><code>status</code></td><td>enum</td><td><p>(Read-only) The invoice status. Allowed values are:</p><ul><li><code>Issued</code></li><li><code>Paid</code></li><li><code>Overdue</code></li></ul></td></tr><tr><td><code>client</code></td><td>object</td><td>(Read-only) Represents the client <a href="../../accounts-api/account/"><code>account</code></a> object.</td></tr><tr><td><code>buyer</code></td><td>object</td><td>(Read-only) Represents the <a href="../../accounts-api/buyer/"><code>buyer</code></a> object.</td></tr><tr><td><code>vendor</code></td><td>object</td><td>(Read-only) Represents the vendor <a href="../../accounts-api/account/"><code>account</code></a> object.</td></tr><tr><td><code>seller</code></td><td>object</td><td>(Read-only) Represents the <a href="../../accounts-api/seller/"><code>seller</code></a> object.</td></tr><tr><td><code>product</code></td><td>object</td><td>(Read-only) Represents the <a href="../../catalog-api/product/"><code>product</code></a> object.</td></tr><tr><td><code>agreement</code></td><td>object</td><td>(Read-only) Represents the <a href="../../commerce-api/agreements/"><code>agreement</code></a> object</td></tr><tr><td><code>licensee</code></td><td>object</td><td>(Read-only) Represents the <a href="../../accounts-api/licensee/"><code>licensee</code></a> object.</td></tr><tr><td><code>erpData</code></td><td>object</td><td><p>Represents the <a href="./#erpinvoicedata"><code>erpInvoiceData</code></a> object, which contains invoice fields from the ERP system.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "erpId": "DE-SCO-1234567",
  "documentNo": "4564564",
  "documentDate": "2025-01-15T12:05:34.087Z",
  "postingDate": "2025-01-15T16:45:24.123Z",
  "dueDate": "2025-02-10T12:05:34.087Z",
  "balanceDue": 123.23,
  "invoiceTotal": 123.23
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. Allowed values: <code>created</code> or <code>updated</code>.</td></tr><tr><td><code>price</code></td><td>object</td><td><p>(Read-only) The invoice price summary with aggregated price values for all invoice charges. </p><p>The <code>statementPriceSummary</code> object inherits from <a href="../journal/#pricesummary"><code>PriceSummary</code></a> and adds tax-related properties: <code>totalST</code> and <code>totalGT</code>.</p><p>Not all fields are visible to all actors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "totalPP": 229.8,
  "markup": 0.5013,
  "margin": 0.3339,  
  "totalSP": 356.57,
  "totalST": 55,
  "totalGT": 411.57
}
</code></pre></td></tr></tbody></table>

## ERPInvoiceData object <a href="#erpinvoicedata" id="erpinvoicedata"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="186">Field</th><th width="201">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>erpId</code></td><td>string</td><td>The identifier in the ERP system.</td></tr><tr><td><code>documentNo</code></td><td>string</td><td>The document number.</td></tr><tr><td><code>documentDate</code></td><td>dateTime</td><td>The document date.</td></tr><tr><td><code>postingDate</code></td><td>dateTime</td><td>The posting date.</td></tr><tr><td><code>dueDate</code></td><td>dateTime</td><td>The due date.</td></tr><tr><td><code>balanceDue</code></td><td>decimal</td><td>The balance due.</td></tr><tr><td><code>invoiceTotal</code></td><td>decimal</td><td>The invoice total.</td></tr><tr><td><code>yourReference</code></td><td>string</td><td>A custom reference (free text) or statement ID (fixed format).</td></tr><tr><td><code>addresses</code></td><td>erpAddressList</td><td><p>The list of addresses associated with the invoice. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "billTo": {
      "name": "Siemens Schweiz AG",
      "name2": "Kreditorenbuchhaltung",
      "customerNo": "CHC-SCU-100495",
      "addressLine1": "Freilagerstrasse 40 ",
      "city": "Zürich",
      "postCode": "8047",
      "country": "CH",
      "contactNo": "CHC-CON-101975"
  },
  "licenseTo": {
      "name": "Raiffeisen Schweiz Genossenschaft",
      "customerNo": "CH-SCU-102355",
      "addressLine1": "Raiffeisenplatz 4",
      "city": "St. Gallen",
      "postCode": "9001",
      "county": "SG",
      "country": "CH",
      "contactName": "Siemens license holder",
      "contactNo": "CH-CON-250378",
      "contactEmail": "support-snc.ch@siemens.com ",
      "contactPhone": "+41 71 225 87 70"
  },
  "sellTo": {
      "name": "Siemens Schweiz AG",
      "customerNo": "CHC-SCU-100493",
      "addressLine1": "Industriestrasse 22 CH",
      "city": "Volketswil",
      "postCode": "8604",
      "country": "CH",
      "contactNo": "CHC-CON-101971"
  },
  "shipTo": {
      "name": "Siemens Schweiz AG",
      "addressLine1": "Industriestrasse 22",
      "city": "Volketswil",
      "postCode": "8604",
      "country": "CH",
      "contactEmail": "support-snc.ch@siemens.com "
  }
}
</code></pre></td></tr><tr><td><code>referenceNumber</code></td><td>ErpReferenceNumber</td><td><p>The additional identifiers for the invoice. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "orderNo": "CH-CO-1249855",
  "ppqNo": "CH-PPQ-268267",
  "quoteNo": "CH-QU-477054"
}
</code></pre></td></tr><tr><td><code>payment</code></td><td>ErpPayment</td><td><p>The payment data associated with the invoice. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "methodCode": "BANK",
  "termsCode": "90DAYS"
}
</code></pre></td></tr></tbody></table>

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
