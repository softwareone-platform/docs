# Business Objects & API Collection Reference

This topic lists all business objects available in the SoftwareOne Marketplace Platform REST API and the corresponding API collection endpoints used to access them.&#x20;

Use this page as a centralized reference to identify the correct object types and endpoints when designing integrations or reviewing platform capabilities.

## Business Objects

### Accounts

| Object Type                                 | Prefix | Example              |
| ------------------------------------------- | ------ | -------------------- |
| [Account](accounts-api/account/)            | `ACC-` | `ACC-1234-5678`      |
| [Buyer](accounts-api/buyer/)                | `BUY-` | `BUY-5171-6994`      |
| [Cloud Tenant](accounts-api/cloud-tenants/) | `CLT-` | `CLT-1976-5289`      |
| [ERP Link](accounts-api/erp-link/)          | `ERP-` | `ERP-1456-2363-9856` |
| [Licensee](accounts-api/licensee/)          | `LCE-` | `LCE-8499-1473-5603` |
| [Module](accounts-api/module/)              | `MOD-` | `MOD-1234`           |
| [Seller](accounts-api/seller/)              | `SEL-` | `SEL-6685-4945`      |
| [User](accounts-api/users/)                 | `USR-` | `USR-3758-7092`      |
| [Group](accounts-api/user-groups/)          | `UGR-` | `UGR-0601-5102`      |
| [Token](accounts-api/api-tokens/)           | `TKN-` | `TKN-9299-7556`      |

### Audit Trail

| Object Type                                     | Prefix | Example                   |
| ----------------------------------------------- | ------ | ------------------------- |
| [Audit Event Type](audit-api/audit-event-type/) | `AET-` | `AET-8784-9237`           |
| [Audit Record](audit-api/audit-record/)         | `AUD-` | `AUD-5681-1729-3068-0895` |

### Billing

<table><thead><tr><th width="268">Object Type</th><th width="196">Prefix</th><th>Example</th></tr></thead><tbody><tr><td><a href="billing-api/billing-attachment.md">Billing Attachment</a></td><td><code>JOA-</code></td><td><code>JOA-4710-3489</code></td></tr><tr><td><a href="billing-api/journal-charges/">Charge</a></td><td><code>CHG-</code></td><td><code>CHG-5841-6913-2879-2010-9301</code></td></tr><tr><td><a href="billing-api/credit-memo/">Credit Memo</a></td><td><code>CRD</code></td><td><code>CRD-8280-7533-0235-8348</code></td></tr><tr><td><a href="billing-api/credit-memo/credit-memo-lines.md">Credit Memo Line</a></td><td><code>CRL-</code></td><td><code>CRL-5974-2302-1490-9437</code></td></tr><tr><td><a href="billing-api/custom-ledger-object/">Custom Ledger</a></td><td><code>CLE-</code></td><td><code>CLE-5974-2384</code></td></tr><tr><td><a href="billing-api/invoice/">Invoice</a></td><td><code>INV-</code></td><td><code>INV-2078-0901-9457-5058</code></td></tr><tr><td><a href="billing-api/invoice-line.md">Invoice Line</a></td><td><code>INL-</code></td><td><code>INL-4836-8218-0290-3679</code></td></tr><tr><td><a href="billing-api/journal/">Journal</a></td><td><code>BJO-</code></td><td><code>BJO-7823-5971</code></td></tr><tr><td><a href="billing-api/ledger/">Ledger</a></td><td><code>BLE-</code></td><td><code>BLE-5694-5681</code></td></tr><tr><td><a href="billing-api/override/">Override</a></td><td><code>BOV-</code></td><td><code>BOV-5895-8712</code></td></tr><tr><td><a href="billing-api/statement/">Statement</a></td><td><code>SOM-</code></td><td><code>SOM-6005-1054-1535-5364</code></td></tr></tbody></table>

### Catalog

<table><thead><tr><th>Object Type</th><th width="207">Prefix</th><th>Example</th></tr></thead><tbody><tr><td><a href="../../modules-and-features/catalog/products.md">Product</a></td><td><code>PRD-</code></td><td><code>PRD-2689-4589</code></td></tr><tr><td><a href="catalog-api/items/">Item</a></td><td><code>ITM-</code></td><td><code>ITM-2598-1496-3258</code></td></tr><tr><td><a href="catalog-api/item-group/">Item Group</a></td><td><code>IGR-</code></td><td><code>IGR-5895-5343-9056</code></td></tr><tr><td><a href="catalog-api/parameter-group/">Parameter Group</a></td><td><code>PGR-</code></td><td><code>PGR-3452-0864-2005</code></td></tr><tr><td><a href="catalog-api/parameter/">Parameter</a></td><td><code>PAR-</code></td><td><code>PAR-6064-5794-1256</code></td></tr><tr><td><a href="catalog-api/media/">Media</a></td><td><code>MED-</code></td><td><code>MED-8053-5894-1289</code></td></tr><tr><td><a href="catalog-api/documentation/">Document</a></td><td><code>DOC-</code></td><td><code>DOC-5841-7434-9044</code></td></tr><tr><td><a href="catalog-api/terms-and-conditions/">Terms and Conditions</a></td><td><code>TCS-</code></td><td><code>TCS-1795-2689-9856</code></td></tr><tr><td><a href="catalog-api/templates/">Template</a></td><td><code>TPL-</code></td><td><code>TPL-0215-9943-4590</code></td></tr><tr><td><a href="catalog-api/pricelists/">Price List</a></td><td><code>PRC-</code></td><td><code>PRC-8485-1289-3478</code></td></tr><tr><td><a href="catalog-api/pricelist-item/">Price List Item</a></td><td><code>PRI-</code></td><td><code>PRI-5804-4357-0742-1065</code></td></tr><tr><td><a href="catalog-api/listing/">Listing</a></td><td><code>LST-</code></td><td><code>LST-9635-2894</code></td></tr><tr><td><a href="catalog-api/authorization/">Authorization</a></td><td><code>AUT-</code></td><td><code>AUT-8914-4365</code></td></tr><tr><td><a href="catalog-api/units-of-measure/">Unit Of Measure</a></td><td><code>UNT-</code></td><td><code>UNT-5892</code></td></tr><tr><td><a href="catalog-api/pricing-policies/">Pricing Policy</a></td><td><code>PRP-</code></td><td><code>PRP-5634-4806-1075</code></td></tr><tr><td><a href="catalog-api/pricing-policies/#pricingpolicyattachment-object">Pricing Policy Attachment</a></td><td><code>PPA-</code></td><td><code>PPA-6324-1708-0298-3578</code></td></tr></tbody></table>

### Commerce

<table><thead><tr><th>Object Type</th><th width="231">Prefix</th><th>Example</th></tr></thead><tbody><tr><td><a href="commerce-api/agreements/">Agreement</a></td><td><code>AGR-</code></td><td><code>AGR-5896-1479-0269</code></td></tr><tr><td><a href="commerce-api/orders/">Order</a></td><td><code>ORD-</code></td><td><code>ORD-5879-2698-3893</code></td></tr><tr><td><a href="commerce-api/subscriptions/">Subscription</a></td><td><code>SUB-</code></td><td><code>SUB-1548-1246-0954</code></td></tr><tr><td><a href="commerce-api/requests/">Request</a></td><td><code>REQ-</code></td><td><code>REQ-7319-1974-9054</code></td></tr><tr><td><a href="commerce-api/line.md">Line</a></td><td><code>ALI-</code></td><td><code>ALI-6199-1408-4789-1964</code></td></tr><tr><td><a href="commerce-api/assets/">Asset</a></td><td><code>AST-</code></td><td><code>AST-5971-3179-2597</code></td></tr></tbody></table>

### Extensions

| Object Type                                  | Prefix | Example                   |
| -------------------------------------------- | ------ | ------------------------- |
| [Extension](extensions-api/extension/)       | `EXT-` | `EXT-5984-1232`           |
| [Category](extensions-api/category/)         | `EXC-` | `EXC-7310`                |
| [Document](extensions-api/document/)         | `EDM-` | `EDM-9741-3001-2984`      |
| [Media](extensions-api/media/)               | `EXM-` | `EXM-5674-1974-2684`      |
| [Term](extensions-api/terms/)                | `ETC-` | `ETC-2697-1456-9745`      |
| [Term Variant](extensions-api/variant/)      | `ETV-` | `ETV-2358-0125-3789-1158` |
| [Instance](extensions-api/instance/)         | `INS-` | `INS-5684-3645-8945-2156` |
| [Installation](extensions-api/installation/) | `EXI-` | `EXI-8945-2589-6485`      |

### Notifications

| Object Type                                  | Prefix | Example                   |
| -------------------------------------------- | ------ | ------------------------- |
| [Webhook](notifications-api/webhook-api/)    | `WBH-` | `WBH-5987-1258`           |
| [Category](notifications-api/categories/)    | `NTC-` | `NTC-2987-6471`           |
| [Contact](notifications-api/contacts/)       | `CTT-` | `CTT-8925-0193`           |
| [Batch](notifications-api/batches/)          | `MST-` | `MST-5874-3684-5986`      |
| [Message](notifications-api/messages/)       | `MSG-` | `MSG-2589-4597-5689-2689` |
| [Subscriber](notifications-api/subscribers/) | `NTS-` | `NTS-5987-0126-9125`      |

### Program

| Object Type                                                            | Prefix | Example                   |
| ---------------------------------------------------------------------- | ------ | ------------------------- |
| [Program](program-api/program/)                                        | `PRG-` | `PRG-7432-9033`           |
| [Parameter Group](program-api/program/program-parameter-groups/)       | `PPG-` | `PPG-6456-5841-9785`      |
| [Program Parameter](program-api/program/program-parameters/)           | `PPM-` | `PPM-2589-6489-2587`      |
| [Program Media](program-api/program/program-media/)                    | `PMD-` | `PMD-2486-8946-2547`      |
| [Program Document](program-api/program/program-documents/)             | `PDM-` | `PDM-2686-7895-2389`      |
| [Program Terms](program-api/program/program-terms/)                    | `PTC-` | `PTC-1478-6974-2569`      |
| [Program Terms Variant](program-api/program/program-terms-variants/)   | `PTV-` | `PTV-2599-3474-2579-2395` |
| [Program Template](program-api/program/program-templates/)             | `PTM-` | `PTM-5977-5689-4785`      |
| [Certificate](program-api/certificate/)                                | `CER-` | `CER-9845-5647-2387`      |
| [Enrollment](program-api/enrollment/)                                  | `ENR-` | `ENR-3795-5796-1254`      |
| [Enrollment Attachment](program-api/enrollment/enrollment-attachment/) | `ENA-` | `ENA-9025-3547-8914-2368` |

### Spotlight

<table><thead><tr><th width="180">Object Type</th><th width="217">Prefix</th><th>Example</th></tr></thead><tbody><tr><td><a href="spotlight-objects-api/spotlight-object/">Spotlight</a></td><td><code>SPO-</code></td><td><code>SPO-&#x3C;5694>-&#x3C;8956>-&#x3C;1010>-&#x3C;3975>-&#x3C;2134></code></td></tr><tr><td><a href="spotlight-objects-api/spotlight-query/">SpotlightQuery</a></td><td><code>SPQ-</code></td><td><code>SPQ-2565-5895</code></td></tr><tr><td><a href="spotlight-objects-api/spotlight-object/spotlight-topitem.md">SpotlightTopItem</a></td><td>Not applicable</td><td>Not applicable</td></tr></tbody></table>

{% hint style="info" %}
SpotlightTopItem object does not have its own unique prefix. It uses the same ID prefix as the related object.
{% endhint %}

## Collections

### Accounts

<table><thead><tr><th width="259">Collection</th><th>Path</th></tr></thead><tbody><tr><td><a href="accounts-api/#accounts">Accounts</a></td><td><code>/public/v1/accounts/accounts</code></td></tr><tr><td><a href="accounts-api/#buyers">Buyers</a></td><td><code>/public/v1/accounts/buyers</code></td></tr><tr><td><a href="accounts-api/#cloud-tenants">Cloud Tenant</a></td><td><code>/public/v1/accounts/cloud-tenants</code></td></tr><tr><td><a href="accounts-api/#erp-link-collection">ERP Links</a></td><td><code>/public/v1/accounts/erp-links</code></td></tr><tr><td><a href="accounts-api/#licensees-collection">Licensees</a></td><td><code>/public/v1/accounts/licensees</code></td></tr><tr><td><a href="accounts-api/#modules-collection">Modules</a></td><td><code>/public/v1/modules</code></td></tr><tr><td><a href="accounts-api/#sellers">Sellers</a></td><td><code>/public/v1/accounts/sellers</code></td></tr><tr><td><a href="accounts-api/#api-tokens">Tokens</a></td><td><code>/public/v1/accounts/tokens</code></td></tr><tr><td><a href="accounts-api/#users-collection">Users</a></td><td><code>/public/v1/accounts/users</code></td></tr></tbody></table>

### Audit Trail

<table><thead><tr><th width="260">Collection</th><th>Path</th></tr></thead><tbody><tr><td><a href="audit-api/#audit-event-type">Audit Event Types</a></td><td><code>/public/v1/audit/event-types</code></td></tr><tr><td><a href="audit-api/#audit-records">Audit Records</a></td><td><code>/public/v1/audit/records</code></td></tr></tbody></table>

### Billing

<table><thead><tr><th width="263">Collection</th><th>Path</th></tr></thead><tbody><tr><td><a href="billing-api/#ledger-charges">Credit Memo</a></td><td><code>/public/v1/billing/credit-memos</code></td></tr><tr><td><a href="billing-api/#ledger-charges-1">Custom Ledgers</a></td><td><code>/public/v1/billing/custom-ledgers</code></td></tr><tr><td><a href="billing-api/#ledger-charges-2">Invoices</a></td><td><code>/public/v1/billing/invoices</code></td></tr><tr><td><a href="billing-api/#journals-collection">Journals</a></td><td><code>/public/v1/billing/journals</code></td></tr><tr><td><a href="billing-api/#ledgers-collection">Ledgers</a></td><td><code>/public/v1/billing/ledgers</code></td></tr><tr><td><a href="billing-api/#ledger-charges-3">Overrides</a></td><td><code>/public/v1/billing/overrides</code></td></tr><tr><td><a href="billing-api/#ledger-charges-4">Statements</a></td><td><code>/public/v1/billing/statements</code></td></tr></tbody></table>

### Catalog

<table><thead><tr><th width="298">Collection</th><th>Path</th></tr></thead><tbody><tr><td><a href="catalog-api/#product">Products</a></td><td><code>/public/v1/catalog/products</code></td></tr><tr><td>Items</td><td><code>/public/v1/catalog/products/{id}/items</code></td></tr><tr><td><a href="catalog-api/#item-groups">Item Groups</a></td><td><code>/public/v1/catalog/products/{id}/item-groups</code></td></tr><tr><td><a href="catalog-api/#parameters-groups">Parameter Groups</a></td><td><code>/public/v1/catalog/products/{id}/parameter-groups</code></td></tr><tr><td><a href="catalog-api/#parameters">Parameters</a></td><td><code>/public/v1/catalog/products/{id}/parameters</code></td></tr><tr><td><a href="catalog-api/#media">Media</a></td><td><code>/public/v1/catalog/products/{id}/media</code></td></tr><tr><td><a href="catalog-api/#documents">Documents</a></td><td><code>/public/v1/catalog/products/{id}/documents</code></td></tr><tr><td><a href="catalog-api/#terms">Terms and Conditions</a></td><td><code>/public/v1/catalog/products/{id}/terms</code></td></tr><tr><td><a href="catalog-api/#product-templates">Templates</a></td><td><code>/public/v1/catalog/products/{id}/templates</code></td></tr><tr><td><a href="catalog-api/#items">Items</a></td><td><code>/public/v1/catalog/items</code></td></tr><tr><td><a href="catalog-api/#price-lists">Price Lists</a></td><td><code>/public/v1/catalog/price-lists</code></td></tr><tr><td><a href="catalog-api/#price-lists">Price List Items</a></td><td><code>/public/v1/catalog/price-lists/{id}/items</code></td></tr><tr><td><a href="catalog-api/#listings">Listings</a></td><td><code>/public/v1/catalog/listings</code></td></tr><tr><td><a href="catalog-api/#authorization">Authorizations</a></td><td><code>/public/v1/catalog/authorizations</code></td></tr><tr><td><a href="catalog-api/#units-of-measure">Units of Measure</a></td><td><code>/public/v1/catalog/units-of-measure</code></td></tr><tr><td><a href="catalog-api/#pricing-policy">Pricing Policies</a></td><td><code>/public/v1/catalog/pricing-policies</code></td></tr></tbody></table>

### Commerce

<table><thead><tr><th width="263">Collection</th><th>Path</th></tr></thead><tbody><tr><td><a href="commerce-api/#agreements">Agreements</a></td><td><code>/public/v1/commerce/agreements</code></td></tr><tr><td><a href="commerce-api/#orders">Orders</a></td><td><code>/public/v1/commerce/orders</code></td></tr><tr><td><a href="commerce-api/#subscriptions">Subscriptions</a></td><td><code>/public/v1/commerce/subscriptions</code></td></tr><tr><td><a href="commerce-api/#requests">Requests</a></td><td><code>/public/v1/commerce/requests</code></td></tr><tr><td><a href="commerce-api/#assets">Assets</a></td><td><code>/public/v1/commerce/assets</code></td></tr></tbody></table>

### Extension

<table><thead><tr><th width="257">Collection</th><th>Path</th></tr></thead><tbody><tr><td><a href="extensions-api/#extension">Extension</a></td><td><code>/public/v1/extensibility/extensions</code></td></tr><tr><td><a href="extensions-api/#categories">Categories</a></td><td><code>/public/v1/extensibility/categories</code></td></tr><tr><td><a href="extensions-api/#documents">Documents</a></td><td><code>/public/v1/extensibility/extensions/{id}/documents</code></td></tr><tr><td><a href="extensions-api/#media">Media</a></td><td><code>/public/v1/extensibility/extensions/{id}/media</code></td></tr><tr><td><a href="extensions-api/#terms">Terms</a></td><td><code>/public/v1/extensibility/extensions/{id}/terms</code></td></tr><tr><td>Hosting</td><td><code>/public/v1/extensibility/hosting</code></td></tr><tr><td><a href="extensions-api/#instance">Instances</a></td><td><code>/public/v1/extensibility/instances/{eid}</code></td></tr><tr><td><a href="extensions-api/#installation">Installations</a></td><td><code>/public/v1/extensibility/installations</code></td></tr></tbody></table>

### Notifications

<table><thead><tr><th width="262">Collection</th><th>Path</th></tr></thead><tbody><tr><td><a href="notifications-api/webhook-api/">Webhooks</a></td><td><code>/public/v1/notifications/webhooks</code></td></tr><tr><td><a href="notifications-api/#categories">Categories</a></td><td><code>/public/v1/notifications/categories</code></td></tr><tr><td><a href="notifications-api/#contacts">Contacts</a></td><td><code>/public/v1/notifications/contacts</code></td></tr><tr><td><a href="notifications-api/#batches">Batches</a></td><td><code>/public/v1/notifications/batches</code></td></tr><tr><td><a href="notifications-api/#messages">Messages</a></td><td><code>/public/v1/notifications/messages</code></td></tr><tr><td><a href="notifications-api/#subscribers">Subscribers</a></td><td><code>/public/v1/notifications/subscribers</code></td></tr></tbody></table>

### Program

<table><thead><tr><th width="263">Collection</th><th>Path</th></tr></thead><tbody><tr><td><a href="program-api/#programs">Programs</a></td><td><code>/public/v1/program/programs</code></td></tr><tr><td><a href="program-api/#program-parameter-groups">Parameter Groups</a></td><td><code>/public/v1/program/programs/{id}/parameter-groups</code></td></tr><tr><td><a href="program-api/#program-parameters">Parameters</a></td><td><code>/public/v1/program/programs/{id}/parameters</code></td></tr><tr><td><a href="program-api/#program-media">Media</a></td><td><code>/public/v1/program/programs/{id}/media</code></td></tr><tr><td><a href="program-api/#program-documents">Documents</a></td><td><code>/public/v1/program/programs/{id}/documents</code></td></tr><tr><td><a href="program-api/#program-terms">Terms and Conditions</a></td><td><code>/public/v1/program/programs/{id}/terms</code></td></tr><tr><td><a href="program-api/#program-templates">Templates</a></td><td><code>/public/v1/program/programs/{id}/templates</code></td></tr><tr><td><a href="program-api/#certificates">Certificates</a></td><td><code>/public/v1/program/certificates</code></td></tr><tr><td><a href="program-api/#enrollments">Enrollments</a></td><td><code>/public/v1/program/enrollments</code></td></tr></tbody></table>

### Spotlight

<table><thead><tr><th width="258">Collection</th><th>Path</th></tr></thead><tbody><tr><td><a href="spotlight-objects-api/#collection">Spotlight</a></td><td><code>/v1/spotlight/objects</code></td></tr></tbody></table>
