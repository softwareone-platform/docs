# Journal Charges

## Uploaded Charge <a href="#uploaded-charge-properties" id="uploaded-charge-properties"></a>

<table><thead><tr><th width="179">Field</th><th width="161">XLSX Column</th><th width="96">Type</th><th>Description</th></tr></thead><tbody><tr><td>externalIds.vendor</td><td>Entry ID</td><td><code>string</code></td><td>Represents a unique vendor entry ID. Example: 2876850566</td></tr><tr><td>externalIds.reference</td><td>External Reference</td><td><code>string</code></td><td><p>Optional vendor-specific data, which might be used, for example, to detect the Marketplace order ID. </p><p>Example: ORD-3270-2860-5617</p></td></tr><tr><td>externalIds.invoice</td><td>Vendor Invoice Reference</td><td><code>string</code></td><td><p>Represents the vendor-specific invoice ID.  </p><p>Example: 1234567890</p></td></tr><tr><td>search.subscription.criteria</td><td>Subscription Search Criteria</td><td><code>string</code></td><td><p>The search criteria for the specified subscription. </p><p>Example: subscription.externalIds.vendor</p></td></tr><tr><td>search.subscription.value</td><td>Subscription Search Value</td><td><code>string</code></td><td>The value of the subscription. Example: d77f96aec94563b671697ed752f81cNA</td></tr><tr><td>search.order.criteria</td><td>Order Search Criteria</td><td><code>string</code></td><td>The search criteria for the order. Example: order.id</td></tr><tr><td>search.order.value</td><td>Order Search Value</td><td><code>string</code></td><td>The value of the order. Example: ORD-3270-2860-5617</td></tr><tr><td>search.item.criteria</td><td>Item Search Criteria</td><td><code>string</code></td><td><p>The search criteria for the item. </p><p>Example: item.externalIds.vendor</p></td></tr><tr><td>search.item.value</td><td>Item Search Value</td><td><code>string</code></td><td>The value of the item. Example: 30005387CA</td></tr><tr><td>period.start</td><td>Usage Start Time</td><td><a href="https://en.wikipedia.org/wiki/ISO_8601"><code>ISO 8601</code></a></td><td>Represents the start time of the entry. Example: 2025-01-01T00:00:00Z</td></tr><tr><td>period.end</td><td>Usage End Time</td><td><a href="https://en.wikipedia.org/wiki/ISO_8601"><code>ISO 8601</code></a></td><td><p>Represents the end time for the entry. </p><p>Example: 2025-01-01T00:00:00Z</p></td></tr><tr><td>quantity</td><td>Quantity</td><td><code>decimal</code></td><td><p>The quantity of the entry. </p><p>Example: 10</p></td></tr><tr><td>price.unitPP</td><td>Purchase Price</td><td><code>decimal</code></td><td>The purchase price of the entry. Example: 253.83</td></tr><tr><td>price.PPx1</td><td>Total Purchase Price</td><td><code>decimal</code></td><td>The total purchase price of the entry. Example: 2538.3</td></tr><tr><td>segment</td><td>Market Segment</td><td><code>string</code></td><td>Examples: COM, GOV, EDU</td></tr><tr><td>description.value1</td><td>Description1</td><td><code>string</code></td><td>Vendor-specific line 1 of the data.</td></tr><tr><td>description.value2</td><td>Description2</td><td><code>string</code></td><td>Vendor-specific line 2 of the data.</td></tr></tbody></table>

## Journal Charge <a href="#journal-charge-object" id="journal-charge-object"></a>

<table><thead><tr><th width="177">Field</th><th width="148">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The ID of the charge. </p><p>Example: CHG-1234-1234-1234-1234-1234</p></td></tr><tr><td>status</td><td><code>enum</code></td><td>Possible values:  <code>Ready</code> or <code>Error</code></td></tr><tr><td>type</td><td><code>enum</code></td><td>Possible values:  <code>Automated</code> or <code>Manual</code></td></tr><tr><td>parent</td><td><code>charge</code></td><td><p>Optional reference to the parent charge for split billing cases, includes one parent split for the number of children charges. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "CHG-1234-1234-1234-1234-1234"
}
</code></pre></td></tr><tr><td>buyer</td><td><a href="../../accounts-api/buyer/"><code>buyer</code></a></td><td><p>A reference to the Buyer object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "BUY-0355-0939",
  "href": "/accounts/buyers/BUY-0355-0939",
  "name": "TEST_BUYER30_rec"
}
</code></pre></td></tr><tr><td>seller</td><td><a href="../../accounts-api/seller/"><code>seller</code></a></td><td><p>A reference to the Seller object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "SEL-9512-0354",
  "href": "/accounts/sellers/SEL-9512-0354",
  "name": "TEST_SELLER30_rec"
}
</code></pre></td></tr><tr><td>ledger</td><td><a href="../ledger/"><code>ledger</code></a></td><td><p>A reference to the Ledger object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "BLE-6084-5502-9512-0354"
}
</code></pre></td></tr><tr><td>statement</td><td><a href="../statement/"><code>statement</code></a></td><td><p>A reference to the Statement object.  </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "SOM-6084-5502-5163-5035-5953",
  "type": "Debit"
}
</code></pre></td></tr><tr><td>licensee</td><td><a href="../../accounts-api/licensee/"><code>licensee</code></a></td><td><p>A reference to the Agreement object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "LCE-4563-7526-8099",
  "href": "/accounts/licensees/LCE-4563-7526-8099",
  "name": "TEST_LICENSEE30_rec"
}
</code></pre></td></tr><tr><td>agreement</td><td><a href="../../commerce-api/agreements/"><code>agreement</code></a></td><td><p>A reference to the Agreement object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "AGR-5163-5035-5953",
  "href": "/commerce/agreements/AGR-5163-5035-5953",
  "status": "Active",
  "name": "TEST_AGREEMENT30_rec_1"
}
</code></pre></td></tr><tr><td>subscription</td><td><a href="../../commerce-api/subscriptions/"><code>subscription</code></a></td><td><p>A reference to the Subscription object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "SUB-7342-6318-2370",
  "href": "/commerce/subscriptions/SUB-7342-6318-2370",
  "name": "TEST_SUBSCRIPTION30_rec_1"
}
</code></pre></td></tr><tr><td>item</td><td><a href="../../catalog-api/items/"><code>item</code></a></td><td><p>A reference to the Item object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "ITM-5333-3116-0002",
  "href": "/items/ITM-5333-3116-0002",
  "name": "TEST_SUBSCRIPTIONITEM30_rec"
}
</code></pre></td></tr><tr><td>authorization</td><td><a href="../../catalog-api/authorization/"><code>authorization</code></a></td><td><p>A reference to the Authorization object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "AUT-2173-6546",
  "href": "/catalog/authorizations/AUT-2173-6546",
  "name": "MY_TEST_AUTHORIZATION30_rec"
}
</code></pre></td></tr><tr><td>vendor</td><td><a href="../../accounts-api/account/"><code>account</code></a></td><td><p>A reference to the vendor Account object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "ACC-3647-5309",
  "href": "/accounts/accounts/ACC-3647-5309",
  "name": "TEST_VENDOR30_rec"
}
</code></pre></td></tr><tr><td>price</td><td><code>price</code></td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "unitPP": 92.09375679688615,
    "unitSP": 101.30313247657476,
    "PPx1": 184.1875135937723,
    "SPx1": 202.60626495314952
    "markup": 10,
    "margin": 9.0909090909
}
</code></pre></td></tr><tr><td>erpData</td><td><code>object</code></td><td><p>ERP system related data.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "scu": "1",
    "cco": "ATC-CCO-112612",
    "erpItemId": "AO03.22961.MP"
}
</code></pre></td></tr><tr><td>attributes</td><td><code>object</code></td><td><p>Various attributes taken from the input file. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "documentNumber": "AGR-0605-6606-7993",
    "orderType": "Direct",
    "externalDocumentNo": "4500776612",
    "externalDocumentNo2": "AGR-0605-6606-7993",
    "yourReference": "Adobe VIP Marketplace Prinzhorn Holding GmbH"
}
</code></pre></td></tr></tbody></table>

## Examples <a href="#examples" id="examples"></a>

{% tabs %}
{% tab title="UPLOADED CHARGE" %}
{% code overflow="wrap" lineNumbers="true" %}
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
{% code overflow="wrap" lineNumbers="true" %}
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
    "name": "CHRISTINA_TEST_LICENSEE30_rec"
  },
  "product": {
    "id": "PRD-5333-3116",
    "href": "/catalog/products/PRD-5333-3116",
    "name": "CHRISTINA_TEST_PRODUCT30_rec",
    "icon": "/v1/catalog/products/PRD-5333-3116/icon"
  },
  "agreement": {
    "id": "AGR-5163-5035-5953",
    "href": "/commerce/agreements/AGR-5163-5035-5953",
    "status": "Active",
    "name": "CHRISTINA_TEST_AGREEMENT30_rec_1"
  },
  "subscription": {
    "id": "SUB-7342-6318-2370",
    "href": "/commerce/subscriptions/SUB-7342-6318-2370",
    "name": "CHRISTINA_TEST_SUBSCRIPTION30_rec_1"
  },
  "item": {
    "id": "ITM-5333-3116-0002",
    "href": "/items/ITM-5333-3116-0002",
    "name": "CHRISTINA_TEST_SUBSCRIPTIONITEM30_rec"
  },
  "authorization": {
    "id": "AUT-2173-6546",
    "href": "/catalog/authorizations/AUT-2173-6546",
    "name": "CHRISTINA_TEST_AUTHORIZATION30_rec"
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
    "name": "CHRISTINA_TEST_CLIENT30_rec"
  },
  "buyer": {
    "id": "BUY-0355-0939",
    "href": "/accounts/buyers/BUY-0355-0939",
    "name": "CHRISTINA_TEST_BUYER30_rec"
  },
  "vendor": {
    "id": "ACC-3647-5309",
    "href": "/accounts/accounts/ACC-3647-5309",
    "name": "CHRISTINA_TEST_VENDOR30_rec"
  },
  "seller": {
    "id": "SEL-9512-0354",
    "href": "/accounts/sellers/SEL-9512-0354",
    "name": "CHRISTINA_TEST_SELLER30_rec"
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
