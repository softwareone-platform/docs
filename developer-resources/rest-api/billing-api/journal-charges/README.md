# Journal Charge

## Uploaded Charge object <a href="#uploaded-charge-properties" id="uploaded-charge-properties"></a>

<table><thead><tr><th width="199.111083984375">Name</th><th width="172">XLSX Column</th><th width="94">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>externalIds.vendor</code></td><td>Entry ID</td><td>string</td><td>Unique vendor entry ID.</td></tr><tr><td><code>externalIds.reference</code></td><td>External Reference</td><td>string</td><td>(Optional) Vendor-specific data, which might be used, for example, to detect the Marketplace order ID. </td></tr><tr><td><code>externalIds.invoice</code></td><td>Vendor Invoice Reference</td><td>string</td><td>Vendor-specific invoice ID.  </td></tr><tr><td><code>search.subscription.criteria</code></td><td>Subscription Search Criteria</td><td>string</td><td>The search criteria for the subscription.</td></tr><tr><td><code>search.subscription.value</code></td><td>Subscription Search Value</td><td>string</td><td>The subscription value .</td></tr><tr><td><code>search.order.criteria</code></td><td>Order Search Criteria</td><td>string</td><td>(Optional) The search criteria for the order. </td></tr><tr><td><code>search.order.value</code></td><td>Order Search Value</td><td>string</td><td>(Optional) The value of the order.</td></tr><tr><td><code>search.item.criteria</code></td><td>Item Search Criteria</td><td>string</td><td>The search criteria for the item. </td></tr><tr><td><code>search.item.value</code></td><td>Item Search Value</td><td>string</td><td>The value of the item. </td></tr><tr><td><code>period.start</code></td><td>Usage Start Time</td><td><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO 8601</a></td><td>Represents the start time of the entry. </td></tr><tr><td><code>period.end</code></td><td>Usage End Time</td><td><a href="https://en.wikipedia.org/wiki/ISO_8601">ISO 8601</a></td><td>Represents the end time for the entry. </td></tr><tr><td><code>quantity</code></td><td>Quantity</td><td>decimal</td><td>The quantity of the entry. </td></tr><tr><td><code>price.unitPP</code></td><td>Purchase Price</td><td>decimal</td><td>The purchase price of the entry.</td></tr><tr><td><code>price.PPx1</code></td><td>Total Purchase Price</td><td>decimal</td><td>The total purchase price of the entry.</td></tr><tr><td><code>segment</code></td><td>Market Segment</td><td>string</td><td>Examples: COM, GOV, EDU</td></tr><tr><td><code>description.value1</code></td><td>Description1</td><td>string</td><td>(Optional) Vendor-specific line 1 of the data.</td></tr><tr><td><code>description.value2</code></td><td>Description2</td><td>string</td><td>(Optional) Vendor-specific line 2 of the data.</td></tr><tr><td><code>attributes.agreementVendorId</code></td><td>Optional Agreement Vendor ID</td><td>string</td><td>(Optional) The Agreement Vendor ID.</td></tr><tr><td>attributes.segment</td><td>Market Segment</td><td>string</td><td>(Optional) COM, GOV, EDU</td></tr></tbody></table>

## Journal Charge object <a href="#journal-charge-object" id="journal-charge-object"></a>

<table><thead><tr><th width="145">Field</th><th width="116">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>The ID of the charge. </td></tr><tr><td><code>status</code></td><td>enum</td><td>Allowed values are  <code>ready</code> or <code>error</code>.</td></tr><tr><td><code>type</code></td><td>enum</td><td>Allowed values are <code>automated</code> or <code>manual</code>.</td></tr><tr><td><code>parent</code></td><td>charge</td><td><p>(Optional) A reference to the parent charge for split billing cases, includes one parent split for the number of children charges. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "CHG-1234-1234-1234-1234-1234"
}
</code></pre></td></tr><tr><td><code>buyer</code></td><td>object</td><td><p>Represents the <a href="../../accounts-api/buyer/"><code>buyer</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "BUY-0355-0939",
  "href": "/accounts/buyers/BUY-0355-0939",
  "name": "TEST_BUYER30_rec"
}
</code></pre></td></tr><tr><td><code>seller</code></td><td>object</td><td><p>Represents the <a href="../../accounts-api/seller/"><code>seller</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "SEL-9512-0354",
  "href": "/accounts/sellers/SEL-9512-0354",
  "name": "TEST_SELLER30_rec"
}
</code></pre></td></tr><tr><td><code>ledger</code></td><td>object</td><td><p>Represents the <a href="../ledger/"><code>ledger</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "BLE-6084-5502-9512-0354"
}
</code></pre></td></tr><tr><td><code>statement</code></td><td>object</td><td><p>Represents the <a href="../statement/"><code>statement</code></a> object.  </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "SOM-6084-5502-5163-5035-5953",
  "type": "Debit"
}
</code></pre></td></tr><tr><td><code>licensee</code></td><td>object</td><td><p>Represents the <a href="../../accounts-api/licensee/"><code>licensee</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "LCE-4563-7526-8099",
  "href": "/accounts/licensees/LCE-4563-7526-8099",
  "name": "TEST_LICENSEE30_rec"
}
</code></pre></td></tr><tr><td><code>agreement</code></td><td>object</td><td><p>Represents the <a href="../../commerce-api/agreements/"><code>agreement</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "AGR-5163-5035-5953",
  "href": "/commerce/agreements/AGR-5163-5035-5953",
  "status": "Active",
  "name": "TEST_AGREEMENT30_rec_1"
}
</code></pre></td></tr><tr><td><code>subscription</code></td><td>object</td><td><p>Represents the <a href="../../commerce-api/subscriptions/"><code>subscription</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "SUB-7342-6318-2370",
  "href": "/commerce/subscriptions/SUB-7342-6318-2370",
  "name": "TEST_SUBSCRIPTION30_rec_1"
}
</code></pre></td></tr><tr><td><code>item</code></td><td>object</td><td><p>Represents the <a href="../../catalog-api/items/"><code>item</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "ITM-5333-3116-0002",
  "href": "/items/ITM-5333-3116-0002",
  "name": "TEST_SUBSCRIPTIONITEM30_rec"
}
</code></pre></td></tr><tr><td><code>authorization</code></td><td>object</td><td><p>A reference to the <a href="../../catalog-api/authorization/"><code>authorization</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "AUT-2173-6546",
  "href": "/catalog/authorizations/AUT-2173-6546",
  "name": "MY_TEST_AUTHORIZATION30_rec"
}
</code></pre></td></tr><tr><td><code>vendor</code></td><td>object</td><td><p>Represents the vendor <a href="../../accounts-api/account/"><code>account</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "ACC-3647-5309",
  "href": "/accounts/accounts/ACC-3647-5309",
  "name": "TEST_VENDOR30_rec"
}
</code></pre></td></tr><tr><td><code>price</code></td><td>price</td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "unitPP": 92.09375679688615,
    "unitSP": 101.30313247657476,
    "PPx1": 184.1875135937723,
    "SPx1": 202.60626495314952,
    "markup": 10,
    "margin": 9.0909090909
}
</code></pre></td></tr><tr><td><code>erpData</code></td><td>object</td><td><p>ERP system related data.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "scu": "1",
    "cco": "ATC-CCO-112612",
    "erpItemId": "AO03.22961.MP"
}
</code></pre></td></tr><tr><td><code>attributes</code></td><td>object</td><td><p>Various attributes taken from the input file. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "documentNumber": "AGR-0605-6606-7993",
    "orderType": "Direct",
    "externalDocumentNo": "4500776612",
    "externalDocumentNo2": "AGR-0605-6606-7993",
    "yourReference": "Adobe VIP Marketplace Prinzhorn Holding GmbH"
}
</code></pre></td></tr></tbody></table>

## Examples

{% tabs %}
{% tab title="UPLOADED CHARGE" %}
{% code title="UPLOADED CHARGE OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
    "externalIds": {
      "vendor": "TEST_CHARGE_001"
      "reference": null,
      "invoice": "2000005957",
    },
    "search": {
      "subscription": {
        "criteria": "subscription.externalIds.vendor",
        "value": "86c4f6b8-ead5-4752-9075-1d2caec6a7cc"
      },
      "item": {
        "criteria": "item.externalIds.vendor",
        "value": "73927560-e5f2-4be4-bdb3-7f6069f0bf94"
      }
    },
    "period": {
      "start": "2025-01-01T00:00:00Z",
      "end": "2025-01-31T23:59:59Z"
    },
    "quantity": 2,
    "price": {
      "unitPP": 93.10961859011398,
      "PPx1": 186.21923718022796
    },
    "segment": "COM"
}
```
{% endcode %}
{% endtab %}

{% tab title="JOURNAL CHARGE" %}
{% code title="JOURNAL CHARGE OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
    "id": "CHG-6084-5502-0000-0000-0100",
    "type": "Automated",
    "externalIds": {
      "vendor": "TEST_CHARGE_001"
      "reference": null,
      "invoice": "2000005957",
    },
    "search": {
      "subscription": {
        "criteria": "subscription.externalIds.vendor",
        "value": "86c4f6b8-ead5-4752-9075-1d2caec6a7cc"
      },
      "item": {
        "criteria": "item.externalIds.vendor",
        "value": "73927560-e5f2-4be4-bdb3-7f6069f0bf94"
      }
    },
    "period": {
      "start": "2025-01-01T00:00:00Z",
      "end": "2025-01-31T23:59:59Z"
    },
    "quantity": 2,
    "segment": "COM",
    "ledger": {
      "id": "BLE-6084-5502-9512-0354"
    },
  "licensee": {
    "id": "LCE-4563-7526-8099",
    "href": "/accounts/licensees/LCE-4563-7526-8099",
    "name": "TEST_LICENSEE30_rec"
  },
  "product": {
    "id": "PRD-5333-3116",
    "href": "/catalog/products/PRD-5333-3116",
    "name": "TEST_PRODUCT30_rec",
    "icon": "/v1/catalog/products/PRD-5333-3116/icon"
  },
  "agreement": {
    "id": "AGR-5163-5035-5953",
    "href": "/commerce/agreements/AGR-5163-5035-5953",
    "status": "Active",
    "name": "TEST_AGREEMENT30_rec_1"
  },
  "subscription": {
    "id": "SUB-7342-6318-2370",
    "href": "/commerce/subscriptions/SUB-7342-6318-2370",
    "name": "TEST_SUBSCRIPTION30_rec_1"
  },
  "item": {
    "id": "ITM-5333-3116-0002",
    "href": "/items/ITM-5333-3116-0002",
    "name": "TEST_SUBSCRIPTIONITEM30_rec"
  },
  "authorization": {
    "id": "AUT-2173-6546",
    "href": "/catalog/authorizations/AUT-2173-6546",
    "name": "TEST_AUTHORIZATION30_rec"
  },
  "statement": {
    "id": "SOM-6084-5502-5163-5035-5953",
    "type": "Debit",
  },
  "startDate": "2025-01-01T00:00:00.000Z",
  "endDate": "2025-01-31T23:59:59.000Z",
  "client": {
    "id": "ACC-8119-0187",
    "href": "/accounts/accounts/ACC-8119-0187",
    "name": "TEST_CLIENT30_rec"
  },
  "buyer": {
    "id": "BUY-0355-0939",
    "href": "/accounts/buyers/BUY-0355-0939",
    "name": "TEST_BUYER30_rec"
  },
  "vendor": {
    "id": "ACC-3647-5309",
    "href": "/accounts/accounts/ACC-3647-5309",
    "name": "TEST_VENDOR30_rec"
  },
  "seller": {
    "id": "SEL-9512-0354",
    "href": "/accounts/sellers/SEL-9512-0354",
    "name": "TEST_SELLER30_rec"
  },
  "price": {
    "unitPP": 92.09375679688615,
    "totalPP": 184.1875135937723,
    "markup": 10,
    "margin": 9.0909090909,
    "unitSP": 101.30313247657476,
    "totalSP": 202.60626495314952
  }
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
