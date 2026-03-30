# Credit Memo

The Credit Memo object refers to a credit memo created within the ERP system.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="141">Field Name</th><th width="204">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>A unique identifier for the credit memo. </p><p>Example: CRD-3295-7900-0234</p></td></tr><tr><td><code>agreement</code></td><td>object</td><td><p>A reference to the <a href="../../commerce-api/agreements/"><code>agreement</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "AGR-2119-4550-8674-5962",
  "href": "/commerce/agreements/ACC-1234-1234",
  "name": "Microsoft Office 365 for My Company"
}
</code></pre></td></tr><tr><td><code>buyer</code></td><td>object</td><td><p>A reference to the <a href="../../accounts-api/buyer/"><code>buyer</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "BUY-3731-7971",
  "href": "/accounts/buyers/BUY-3731-7971",
  "name": "Adam Ruszczak",
  "icon": "/static/BUY-3731-7971/icon.png"
}
</code></pre></td></tr><tr><td><code>client</code></td><td>object</td><td><p>A reference to the <a href="../../accounts-api/account/"><code>account</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "ACC-1234-4444",
  "href": "/accounts/accounts/ACC-1234-4444",
  "name": "Best LLC",
  "icon": "/static/ACC-1234-4444/account.png"
}
</code></pre></td></tr><tr><td><code>erpData</code></td><td>object</td><td><p>Represents the credit memo fields from the ERP system. <a href="./#creditmemoerpdata"><code>creditMemoErpData</code></a></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">"erpData": {
    "addresses": {
        "billTo": {
            "name": "Siemens Canada Limited",
            "customerNo": "CA-SCU-100008",
            "addressLine1": "1550 Appleby Line",
            "city": "Burlington",
            "postCode": "L7L 6X7",
            "county": "ON",
            "country": "CND",
            "contactNo": "CA-CON-100040"
        },
        "licenseTo": {
            "name": "Siemens Canada Limited",
            "customerNo": "CA-SCU-100008",
            "addressLine1": "1550 Appleby Line",
            "city": "Burlington",
            "postCode": "L7L 6X7",
            "county": "ON",
            "country": "CND",
            "contactName": "Andrew Luther",
            "contactNo": "CA-CON-100047"
        },
        "sellTo": {
            "name": "Siemens Canada Limited",
            "customerNo": "CA-SCU-100008",
            "addressLine1": "1550 Appleby Line",
            "city": "Burlington",
            "postCode": "L7L 6X7",
            "county": "ON",
            "country": "CND",
            "contactNo": "CA-CON-100040"
        },
        "shipTo": {
            "name": "Siemens Canada Limited",
            "addressLine1": "1550 Appleby Line",
            "city": "Burlington",
            "postCode": "L7L 6X7",
            "county": "ON",
            "country": "CND"
        }
    },
    "appliesToDocNo": "460201",
    "currencyCode": "USD",
    "documentDate": "2025-07-25T00:00:00.000Z",
    "documentNo": "SG-CM-108834",
    "externalDocumentNo": "EXDONO_6786089946345",
    "externalDocumentNo2": "EXDONO2_919764016716",
    "navisionCountryCode": "SG",
    "postingDate": "2025-07-25T00:00:00.000Z",
    "rowVersion": 1645619029,
    "yourReference": "YourRef_180588433545113841284876514643996099936880"
}
</code></pre></td></tr><tr><td><code>licensee</code></td><td>object</td><td><p>A reference to the <a href="../../accounts-api/licensee/"><code>licensee</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "LCE-9625-9634",
  "href": "/accounts/licensees/LCE-9625-9634",
  "name": "John Smith",
  "icon": "/static/LCE-9625-9634/icon.png"
} 
</code></pre></td></tr><tr><td><code>lines</code></td><td>object</td><td><p>The list of <a href="credit-memo-lines.md"><code>creditMemoLine[]</code></a> associated with the credit memo.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">[
  {
    "id": "CRL-8003-9067-8612-0011",
    "description": "TeamViewer Corporate",
    "description2": "Subscription for 1 Year",
    "documentNo": "SG-CM-108852",
    "erpData": {
      "countryOfUsage": "CA",
      "dataOrigin": 0,
      "navisionCountryCode": "SG",
      "primary": {
        "identifier": ""
      },
      "secondary": {
        "identifier": ""
      },
      "rowVersion": 1646155471,
      "responsibilityCenterCode": "HN",
      "type": 2,
      "unitOfMeasure": "Pieces"
    },
    "itemNo": "TV02.00852.ML",
    "lineNo": 130000,
    "period": {
      "start": "1753-01-01T00:00:00.000Z",
      "end": "1753-01-01T00:00:00.000Z"
    },
    "price": {
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
  }
]
</code></pre></td></tr><tr><td><code>price</code></td><td>object</td><td><p>The <a href="./#creditmemopricesummary"><code>creditMemoPriceSummary</code></a> with aggregated price values for all credit memo lines. Note that not all fields are visible to all actors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "currency": "USD",
    "currencyFactor": 0.7829320806,
    "currencyFactor2": 0.7829320806,
    "margin": 33.3333333333,
    "markup": 50.0000000000,
    "totalPP": 20.00000,
    "totalSP": 30.00000,
    "totalST": 2.70000,
    "totalGT": 32.70000
}
</code></pre></td></tr><tr><td><code>product</code></td><td>object</td><td><p>A reference to the <a href="../../catalog-api/product/"><code>product</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td><code>seller</code></td><td>object</td><td><p>A reference to the <a href="../../accounts-api/seller/"><code>seller</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "SEL-9121-8944",
  "href": "/accounts/sellers/SEL-9121-8944",
  "name": "Software LN",
  "icon": "/static/SEL-9121-8944/icon.png"
}
</code></pre></td></tr><tr><td><code>status</code></td><td>enum</td><td><p>The status of the credit memo. </p><p>Example: Issued</p></td></tr><tr><td><code>vendor</code></td><td>object</td><td>A  reference to vendor<a href="../../accounts-api/account/"><code>account</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>A  reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Credit Memo ERP Data object <a href="#creditmemoerpdata" id="creditmemoerpdata"></a>

<table><thead><tr><th width="221">Field Name</th><th width="165">Data Type</th><th width="381">Description</th></tr></thead><tbody><tr><td><code>addresses</code></td><td>object</td><td><p>The list of addresses associated with the invoice.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "billTo": {
      "name": "Stark Industries",
      "name2": "Incorporated",
      "customerNo": "CHC-SCU-007007",
      "addressLine1": "Freilagerstrasse 007 ",
      "city": "Zürich",
      "postCode": "8047",
      "country": "CH",
<strong>      "contactNo": "CHC-CON-100000"
</strong>  },
  "licenseTo": {
      "name": "Jane Doe",
      "customerNo": "CH-SCU-1011111",
      "addressLine1": "Raiffeisenplatz 4",
      "city": "St. John",
      "postCode": "4001",
      "county": "SG",
      "country": "CH",
      "contactName": "Stark license holder",
      "contactNo": "CH-CON-300300",
      "contactEmail": "support@stark.com ",
      "contactPhone": "+41 71 225 0007"
  },
  "sellTo": {
      "name": "Stark Industries",
      "customerNo": "CHC-SCU-100000",
      "addressLine1": "Industries 22 CH",
      "city": "St. John",
      "postCode": "4001",
      "country": "CH",
      "contactNo": "CHC-CON-1011111"
  },
  "shipTo": {
      "name": "Stark AG",
      "addressLine1": "Industries 44",
      "city": "Volketswil",
      "postCode": "4500",
      "country": "CH",
      "contactEmail": "support-@stark.com "
  }
}
</code></pre></td></tr><tr><td><code>appliesToDocNo</code></td><td>string</td><td><p>Applies to document number.</p><p>Example: 460201</p></td></tr><tr><td><code>currencyCode</code></td><td>string</td><td><p>Represents the currency code.</p><p>Example: USD</p></td></tr><tr><td><code>documentDate</code></td><td>DateTimeOffset</td><td><p>Represents the document date.</p><p>Example: 2025-07-25T00:00:00.000Z</p></td></tr><tr><td><code>documentNo</code></td><td>string</td><td><p>Represents the document number. </p><p>Example: SG-CM-108834</p></td></tr><tr><td><code>externalDocumentNo</code></td><td>string</td><td>Represents the external document number. Example: EXDONO_6786089946345</td></tr><tr><td><code>externalDocumentNo2</code></td><td>string</td><td>Represents the external document number 2. Example: EXDONO2_919764016716</td></tr><tr><td><code>insideSalesCode</code></td><td>string</td><td><p>Represents the inside sales code. </p><p>Example: DOMAIN\JAN.SAGER</p></td></tr><tr><td><code>navisionCountryCode</code></td><td>string</td><td>Represents the country code in our ERP system. Example: SG</td></tr><tr><td><code>postingDate</code></td><td>DateTimeOffset</td><td><p>Represents the posting date. </p><p>Example: 2025-01-15T16:45:24.123Z</p></td></tr><tr><td><code>responsibilityCenterCode</code></td><td>string</td><td><p>Represents the code of the responsibility centre.</p><p>Example: BUENOSAIRE.</p></td></tr><tr><td><code>rowVersion</code></td><td>string</td><td><p>Represents the version of the row. </p><p>Example: 1645619029.</p></td></tr><tr><td><code>salesPersonCode</code></td><td>string</td><td>Represents the code for the sales person. Example: BR-FPA.</td></tr><tr><td><code>shipmentMethodCode</code></td><td>string</td><td><p>Represents the code of the shipment method.</p><p>Example: EMAIL.</p></td></tr><tr><td><code>vatRegistrationNo</code></td><td>string</td><td>Represents the VAT registration number. Example: 30-53619620-6.</td></tr><tr><td><code>yourReference</code></td><td>string</td><td><p>Custom reference (free text) or the statement ID (fixed format).</p><p>Example: YourRef_180588433545113841284876514643996099936880.</p></td></tr></tbody></table>

## Credit Memo Price Summary object

<table><thead><tr><th width="162">Field Name</th><th width="182">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>currency</code></td><td>string</td><td><p>Represents the currency code. </p><p>Example: USD</p></td></tr><tr><td><code>currencyFactor</code></td><td>decimal</td><td><p>Represents the currency factor. </p><p>Example: 0.7829320806</p></td></tr><tr><td><code>currencyFactor2</code></td><td>decimal</td><td><p>Represents the currency factor 2. </p><p>Example: 0.7829320806</p></td></tr><tr><td><code>margin</code></td><td>decimal</td><td><p>Represents the margin. </p><p>Example: 33.3333333333</p></td></tr><tr><td><code>markup</code></td><td>decimal</td><td><p>Represents the markup.</p><p>Example: 50.0000000000</p></td></tr><tr><td><code>totalGT</code></td><td>decimal</td><td><p>Represents the total gross amount. </p><p>Example: 32.70000</p></td></tr><tr><td><code>totalPP</code></td><td>decimal</td><td><p>Represents the total purchase price. </p><p>Example: 20.00000</p></td></tr><tr><td><code>totalSP</code></td><td>decimal</td><td><p>Represents the total sales price. </p><p>Example: 30.00000</p></td></tr><tr><td><code>totalST</code></td><td>decimal</td><td><p>Represents the total sales tax. </p><p>Example: 2.70000</p></td></tr></tbody></table>
