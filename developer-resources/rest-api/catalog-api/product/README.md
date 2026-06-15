# Product

The Product object represents a collection of items and their relevant parameters curated into a cohesive group for business purposes. Defined by vendors, products are accessible through listings, providing a structured framework for transactional activities.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="178">Field</th><th width="151">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The identifier for the product.</td></tr><tr><td><code>name</code></td><td>string, core</td><td>The name of the product.</td></tr><tr><td><code>shortDescription</code></td><td>string</td><td>A short description of the product.</td></tr><tr><td><code>longDescription</code></td><td>string</td><td>A long description of the product.</td></tr><tr><td><code>website</code></td><td>string</td><td>The URL for the product website.</td></tr><tr><td><code>icon</code></td><td>string, core</td><td>A logo of the product.</td></tr><tr><td><code>externalIds</code></td><td>object, core</td><td>Represents the <a href="../../../api-usage-and-reference/common-api-objects/externalids.md"><code>externalIds</code></a> object.</td></tr><tr><td><code>vendor</code></td><td>object</td><td>Represents the vendor <a href="../../accounts-api/account/#account-object"><code>account</code></a> object.</td></tr><tr><td><code>status</code></td><td>string, core</td><td><p>Represents the product status. Allowed values are:</p><ul><li><code>Draft</code></li><li><code>Pending</code></li><li><code>Published</code></li><li><code>Unpublished</code></li></ul></td></tr><tr><td><code>settings</code></td><td>object</td><td><p>Represents the <a href="./#productsettings"><code>productSettings</code></a> object.</p><p><strong>Activate item selection validation:</strong></p><p>Used in the “Purchase wizard” to validate vendor-specific compatibility of selected items, before the order is submitted.</p><p><strong>Activate validation of change orders in a draft state</strong></p><p>Used to validate vendor-specific rules on a change order within the Purchase wizard (via existing agreement) and the Subscription edit screen</p><p><strong>Activate validation of product requests in a draft state</strong></p><p>Used to perform vendor-specific validation on the product’s request form before form submission.</p><p><strong>Activate validation of purchase orders in a draft state</strong></p><p>Used to perform vendor-specific validation of purchase order within the “Purchase wizard”</p><p><strong>Activate validation of purchase orders in a querying state</strong></p><p>Used to perform vendor-specific validation when client is responding to a purchase order where vendor has requested additional information from the client.</p><p><strong>Activate validation of termination order in a draft state</strong></p><p>Used to perform vendor-specific validation when client initiates termination order on an agreement or subscription.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "productOrdering": true,
  "productRequests": {
    "enabled": true,
    "title": "Contact us about Microsoft 365 Online Services",
    "label": "Contact us"
  },
  "itemSelection": false,
  "orderQueueChanges": false,
  "preValidation": {
    "purchaseOrderDraft": false,
    "purchaseOrderQuerying": false,
    "changeOrderDraft": false,
    "terminationOrder": false,
    "productRequest": false
  }
} 
</code></pre></td></tr><tr><td><code>statistics</code></td><td>object</td><td>(Read-only) Represents the <a href="./#productstatistics"><code>productStatistics</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

### Product Settings object <a href="#productsettings" id="productsettings"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="214">Field</th><th width="121">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>productOrdering</code></td><td>boolean</td><td>Displays the <strong>Buy</strong> button, enabling clients to place an order.</td></tr><tr><td><code>itemSelection</code></td><td>boolean</td><td>Validates the compatibility of selected product items within the purchase order.</td></tr><tr><td><code>orderQueueChanges</code></td><td>boolean</td><td>Enables notifications of changes in the order queue.</td></tr><tr><td><code>sendCostToErp</code></td><td>boolean</td><td>Allows cost price values to pass through to final billing.</td></tr><tr><td><code>productRequests</code></td><td>object</td><td>(Optional) Represents the <a href="./#productrequestsettings"><code>productRequestSettings</code></a> object, which defines the settings for the product requests page.</td></tr><tr><td><code>preValidation</code></td><td>object</td><td>Represents the <a href="./#productstatistics"><code>productStatistics</code></a> object, which contains settings used during the pre‑validation phase of the purchase process.</td></tr><tr><td><code>splitBilling</code></td><td>object</td><td>Represents the <a href="./#splitbillingsettings-object"><code>splitBillingSettings</code> </a>object.</td></tr><tr><td><code>subscriptionCessation</code></td><td>object</td><td>Represents the <a href="./#subscriptioncessationsettings"><code>subscriptionCessationSettings</code></a> object, which contains settings related to product cessation.</td></tr></tbody></table>

### Product Request Settings object <a href="#productrequestsettings" id="productrequestsettings"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="188">Field</th><th width="129">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>enabled</code></td><td>boolean</td><td>Displays a request button on the product card, enabling clients to request more information about a product.</td></tr><tr><td><code>name</code></td><td>string</td><td>The product name, which appears as a title within the request wizard.</td></tr><tr><td><code>label</code></td><td>string</td><td>The label on the product listing card.</td></tr></tbody></table>

### Product Statistics object <a href="#productstatistics" id="productstatistics"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="155">Field</th><th width="134">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>items</code></td><td>integer</td><td>(Read-only) Number of items assigned to the product.</td></tr><tr><td><code>orders</code></td><td>integer</td><td>(Read-only) Number of orders placed for the product.</td></tr><tr><td><code>agreements</code></td><td>integer</td><td>(Read-only) Number of agreements signed with the product.</td></tr><tr><td><code>subscriptions</code></td><td>integer</td><td>(Read-only) Number of existing subscriptions to the product.</td></tr><tr><td><code>requests</code></td><td>integer</td><td>(Read-only) Number of requests related to the product.</td></tr></tbody></table>

### Split Billing Settings object

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="140">Field</th><th width="129">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>enabled</code></td><td>boolean</td><td>Displays the split‑billing button in the dropdown, allowing clients and operations teams to enable split billing for this product.</td></tr><tr><td><code>type</code></td><td>string</td><td>Defines the type of split billing. Allowed values are <code>orderBased</code> or <code>percentageBased</code>.</td></tr></tbody></table>

### Subscription Cessation Settings object <a href="#subscriptioncessationsettings" id="subscriptioncessationsettings"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="140">Field</th><th width="129">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>enabled</code></td><td>boolean</td><td>Specifies whether the product cessation functionality is enabled for this product.</td></tr><tr><td><code>mode</code></td><td>string</td><td><p>Specifies the cessation mode. Allowed values are:</p><ul><li><code>Termination</code></li><li><code>Auto-renewal</code></li><li><code>Termination or Auto-renewal</code></li></ul></td></tr></tbody></table>

### Pre-Validation Settings object

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="210">Field</th><th width="139">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>purchaseOrderDraft</code></td><td>boolean</td><td>Validates purchase order during the creation and before the order is submitted.</td></tr><tr><td><code>purchaseOrderQuerying</code></td><td>boolean</td><td>Validates purchase orders when the client is requested to provide more information to the vendor on that order.</td></tr><tr><td><code>changeOrderDraft</code></td><td>boolean</td><td>Validates change order during the creation and before the order is submitted.</td></tr><tr><td><code>terminationOrder</code></td><td>boolean</td><td>Validates termination orders during the creation and before the order is submitted.</td></tr><tr><td><code>productRequest</code></td><td>boolean</td><td>Validates the product request form while the client is filling in information and before the form is submitted.</td></tr></tbody></table>

### Example

{% code title="PRODUCT OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "PRD-1234-1234",  
  "name": "Microsoft 365 online services for commercial",
  "shortDescription": "Microsoft 365 and Office 365 are cloud-based productivity suites that offer a range of applications and services to help businesses of all sizes work more efficiently. These plans combine the familiar Microsoft Office desktop suite with cloud-based versions of Microsoft’s next-generation communications and collaboration services to help users be productive from virtually anywhere through the Internet.",
  "longDescription": "<p>Microsoft 365 and Office 365 are cloud-based productivity suites that offer a range of applications and services to help businesses of all sizes work more efficiently. These plans combine the familiar Microsoft Office desktop suite with cloud-based versions of Microsoft's next-generation communications and collaboration services (including Office for the web, Microsoft Exchange Online, Microsoft Teams, and Microsoft SharePoint Online) to help users be productive from virtually anywhere through the Internet. Microsoft 365 and Office 365 are available in a variety of plans to best meet the needs of your organization. For detailed plan information on subscriptions that enable users for the Microsoft 365 and Office 365 platforms, see the full subscription comparison table.</p>",
  "website": "https://www.microsoft.com",
  "icon": "/static/PRD-1234-1234/logo.png"
  "vendor": {
      "id": "ACC-1234-1234"
  },
  "state": "Published",
  "settings":{
    "productOrdering": true,
    "productRequests": {
      "enabled": true,
      "name": "Contact us about Microsoft 365 Online Services",
      "label": "Contact us."
    },
    "itemSelection": false,
    "orderQueueChanges": false,
    "preValidation": {
      "purchaseOrderDraft": false,
      "purchaseOrderQuerying": false,
      "changeOrderDraft": false,
      "terminationOrder": false,
      "productRequest": false
    }
  },
  "statistics": {
    "item": 100,
    "orders": 123,
    "agreement": 1,
    "subscription": 20
  }
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
