# Credit Memo Lines

The Credit Memo Line object represents a record of a credit memo line generated in the ERP system.

<table><thead><tr><th width="127">Field</th><th width="200">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>A unique identifier for the credit memo line. </p><p>Example: CRL-8003-9067-8612-0001</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>A description of the credit memo line.</p><p>Example: Microsoft 365 Business Premium</p></td></tr><tr><td>description2</td><td><code>string</code></td><td><p>A secondary description of the credit memo line.</p><p>Example: Monthly Subs incl SoftwareOne Cloud Support Basic</p></td></tr><tr><td>documentNo</td><td><code>string</code></td><td><p>A reference to the document number.</p><p>Example: CH-CM-159960</p></td></tr><tr><td>erpData</td><td><a href="credit-memo-lines.md#creditmemoerpdata"><code>CreditMemoLineErpData</code></a></td><td><p>Represents the credit memo line fields from the ERP system. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
  "dataOrigin": 0,
  "navisionCountryCode": "SG",
  "primary": {
    "identifier": "UBS_GLOBAL",
    "value": "43233004",
    "version": "VERSION1"
  },
  "secondary": {
    "identifier": "STAR CODE",
    "value": "SEQ11G12J",
    "version": "1.0"
  },
  "rowVersion": 1646155461,
  "type": 2
}
</code></pre></td></tr><tr><td>itemNo</td><td><code>string</code></td><td><p>A reference to the item number.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
  "start": "2021-01-01 00:00:00.000Z",
  "end": "2021-01-29 00:00:00.000Z"
}
</code></pre></td></tr><tr><td>lineNo</td><td><code>int</code></td><td><p>A reference to the line number.</p><p>Example: 1000</p></td></tr><tr><td>price</td><td><a href="credit-memo-lines.md#creditmemolineprice"><code>CreditMemoLinePrice</code></a></td><td><p>The credit memo line price. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
  "amount": 15.0,
  "amountIncludingVat": 16.35,
  "discountAmount": 0.0,
  "invoiceDiscountAmount": 0.0,
  "lineAmount": 15.0,
  "purchaseCurrencyCode": "SGD",
  "purchaseCurrencyFactor": 0.0,
  "purchasePrice": 10.0,
  "purchasePriceLcy": 10.0,
  "purchasePriceTotal": 10.0,
  "purchasePriceTotalLcy": 10.0,
  "quantity": 1,
  "salesMarkup": 94.81,
  "salesMargin": 48.65,
  "unitPrice": 15.0,
  "vatBaseAmount": 15.0,
  "vatCalculationType": 0,
  "vatPercent": 9.0
}
</code></pre></td></tr></tbody></table>

## CreditMemoLineErpData <a href="#creditmemoerpdata" id="creditmemoerpdata"></a>

<table><thead><tr><th width="213">Field</th><th width="137">Type</th><th width="381">Description</th></tr></thead><tbody><tr><td>contractNo</td><td><code>string</code></td><td>Example: SG-CCO-388527</td></tr><tr><td>countryOfUsage</td><td><code>string</code></td><td>Example: SG</td></tr><tr><td>dataOrigin</td><td><code>integer</code></td><td>Example: 0</td></tr><tr><td>externalPositionNo</td><td><code>string</code></td><td>Example: 1</td></tr><tr><td>navisionCountryCode</td><td><code>string</code></td><td>Example: SG</td></tr><tr><td>parentItemNo</td><td><code>string</code></td><td>Example: X123.00086.ML</td></tr><tr><td>primary</td><td><code>erpCode</code></td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
  "identifier": "UBS_GLOBAL",
  "value": "43233004",
  "version": "VERSION1"
}
</code></pre></td></tr><tr><td>secondary</td><td><code>erpCode</code></td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
  "identifier": "STAR CODE",
  "value": "SEQ11G12J",
  "version": "1.0"
}
</code></pre></td></tr><tr><td>rowVersion</td><td><code>ulong</code></td><td>Example: 1646155461</td></tr><tr><td>responsibilityCenterCode</td><td><code>string</code></td><td>Example: WISC</td></tr><tr><td>swoPurchaseOrderNo</td><td><code>string</code></td><td>Example: US-RET-151037</td></tr><tr><td>type</td><td><code>integer</code></td><td>Example: 2.</td></tr><tr><td>unitOfMeasure</td><td><code>string</code></td><td>Example: Pieces</td></tr><tr><td>varAgreementNo</td><td><code>string</code></td><td>Example: US-VAG-101782</td></tr><tr><td>varPartnerNo</td><td><code>string</code></td><td>Example: US-VAR-109388</td></tr></tbody></table>

## CreditMemoLinePrice

<table><thead><tr><th width="213">Field</th><th width="137">Type</th><th width="381">Description</th></tr></thead><tbody><tr><td>amount</td><td><code>decimal</code></td><td>Example: 15.00000</td></tr><tr><td>amountIncludingVat</td><td><code>decimal</code></td><td>Example: 16.35000</td></tr><tr><td>discountAmount</td><td><code>decimal</code></td><td>Example: 0.00000</td></tr><tr><td>invoiceDiscountAmount</td><td><code>decimal</code></td><td>Example: 0.00000</td></tr><tr><td>lineAmount</td><td><code>decimal</code></td><td>Example: 15.00000</td></tr><tr><td>purchaseCurrencyCode</td><td><code>decimal</code></td><td>Example: SGD</td></tr><tr><td>purchaseCurrencyFactor</td><td><code>decimal</code></td><td>Example: 0.0000000000</td></tr><tr><td>purchasePrice</td><td><code>decimal</code></td><td>Example: 10.00000</td></tr><tr><td>purchasePriceLcy</td><td><code>decimal</code></td><td>Example: 10.00000</td></tr><tr><td>purchasePriceTotal</td><td><code>decimal</code></td><td>Example: 10.00000</td></tr><tr><td>purchasePriceTotalLcy</td><td><code>decimal</code></td><td>Example: 10.00000</td></tr><tr><td>quantity</td><td><code>integer</code></td><td>Example: 1</td></tr><tr><td>salesMargin</td><td><code>decimal</code></td><td>Example: 48.6500000000</td></tr><tr><td>salesMarkup</td><td><code>decimal</code></td><td>Example: 94.8100000000</td></tr><tr><td>unitPrice</td><td><code>decimal</code></td><td>Example: 15.00000</td></tr><tr><td>vatBaseAmount</td><td><code>decimal</code></td><td>Example: 15.00000</td></tr><tr><td>vatCalculationType</td><td><code>integer</code></td><td>Example: 0</td></tr><tr><td>vatPercent</td><td><code>decimal</code></td><td>Example: 9.00</td></tr></tbody></table>
