# Products

The Product object represents a collection of items and their relevant parameters curated into a cohesive group for business purposes. Defined by vendors, products are accessible through listings, providing a structured framework for transactional activities.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="178">Field</th><th width="172">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The identifier for the product.</p><p>Example: PRD-1234-1234</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>Relative reference to product on API (always v1/products/{id})</p><p>Example: /v1/products/PRD-1234-1234</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the product.</p><p>Example: Microsoft 365 online services for commercial</p></td></tr><tr><td>shortDescription</td><td><code>string</code></td><td><p>A short description of the product.</p><p>Example: Microsoft 365 and Office 365 are cloud-based productivity suites that offer a range of applications and services to help businesses of all sizes work more efficiently.</p></td></tr><tr><td>longDescription</td><td><code>string</code></td><td><p>A long description of the product.</p><p>Example: Microsoft 365 and Office 365 are cloud-based productivity suites that offer a range of applications and services to help businesses of all sizes work more efficiently. These plans combine the familiar Microsoft Office desktop suite with cloud-based versions of Microsoft's next-generation communications and collaboration services (including Office for the web, Microsoft Exchange Online, Microsoft Teams, and Microsoft SharePoint Online) to help users be productive from virtually anywhere through the Internet.</p></td></tr><tr><td>website</td><td><code>string</code></td><td><p>The URL for the product website.</p><p>Example: https://www.microsoft.com</p></td></tr><tr><td>icon</td><td><code>string</code></td><td><p>The product's logo.</p><p>Example: /static/PRD-1234-1234/logo.png</p></td></tr><tr><td>externalIds</td><td><a href="../../common-api-objects/externalids.md"><code>externalIds</code></a></td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "operations": "op-322-322",
}
</code></pre></td></tr><tr><td>vendor</td><td><a href="../../accounts-api/account/#account-object"><code>account</code></a></td><td><p>A reference to the vendor account object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>status</td><td><code>status</code></td><td><p>Possible values: <code>Draft</code>, <code>Pending</code>, <code>Published</code>, and <code>Unpublished</code>.</p><p>See <a href="product-states.md">Product States</a>.</p></td></tr><tr><td>settings</td><td><a href="./#productsettings"><code>productSettings</code></a></td><td><p><strong>Activate item selection validation:</strong></p><p>Used in the “Purchase wizard” to validate vendor-specific compatibility of selected items, before the order is submitted.</p><p><strong>Activate validation of change orders in a draft state</strong></p><p>Used to validate vendor-specific rules on a change order within the Purchase wizard (via existing agreement) and the Subscription edit screen</p><p><strong>Activate validation of product requests in a draft state</strong></p><p>Used to perform vendor-specific validation on the product’s request form before form submission.</p><p><strong>Activate validation of purchase orders in a draft state</strong></p><p>Used to perform vendor-specific validation of purchase order within the “Purchase wizard”</p><p><strong>Activate validation of purchase orders in a querying state</strong></p><p>Used to perform vendor-specific validation when client is responding to a purchase order where vendor has requested additional information from the client.</p><p><strong>Activate validation of termination order in a draft state</strong></p><p>Used to perform vendor-specific validation when client initiates termination order on an agreement or subscription.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
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
</code></pre></td></tr><tr><td>statistics</td><td><a href="./#productstatistics"><code>productStatistics</code></a></td><td><p>Product statistics.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "items": 110,
  "orders": 123,
  "agreements": 1,
  "subscriptions": 20
}
</code></pre></td></tr></tbody></table>

## ProductSettings <a href="#productsettings" id="productsettings"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="181">Field</th><th width="217">Type</th><th>Description</th></tr></thead><tbody><tr><td>productOrdering</td><td><code>boolean</code></td><td><p>Displays the <strong>Buy</strong> button on the product card, enabling clients to place an order for this product.</p><p>Example: true</p></td></tr><tr><td>itemSelection</td><td><code>boolean</code></td><td><p>Validates the compatibility of selected product items within the purchase order, supporting order processing.</p><p>Example: false</p></td></tr><tr><td>orderQueueChanges</td><td><code>boolean</code></td><td><p>Enables notifications of changes in the order queue.</p><p>Example: false</p></td></tr><tr><td>productRequests</td><td><a href="./#productrequestsettings"><code>productRequestSettings</code></a></td><td>Settings for the product requests page.</td></tr><tr><td>preValidation</td><td><a href="./#prevalidationsettings"><code>preValidationSettings</code></a></td><td>Settings for the pre-validation phase during purchase.</td></tr></tbody></table>

## ProductRequestSettings <a href="#productrequestsettings" id="productrequestsettings"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="188">Field</th><th width="211">Type</th><th>Description</th></tr></thead><tbody><tr><td>enabled</td><td><code>boolean</code></td><td><p>Displays a request button on the product card, enabling clients to request more information about a product.</p><p>Example: true</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The product name, which appears as a title within the request wizard.</p><p>Example: Contact us about Microsoft 365 Online Services</p></td></tr><tr><td>label</td><td><code>string</code></td><td><p>The label on the product listing card.</p><p>Example: Contact us</p></td></tr></tbody></table>

## PreValidationSettings <a href="#prevalidationsettings" id="prevalidationsettings"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="210">Field</th><th width="175">Type</th><th>Description</th></tr></thead><tbody><tr><td>purchaseOrderDraft</td><td><code>boolean</code></td><td><p>Validates purchase order during the creation and before the order is submitted.</p><p>Example: false</p></td></tr><tr><td>purchaseOrderQuerying</td><td><code>boolean</code></td><td><p>Validates purchase orders when the client is requested to provide more information to the vendor on that order.</p><p>Example: false</p></td></tr><tr><td>changeOrderDraft</td><td><code>boolean</code></td><td><p>Validates change order during the creation and before the order is submitted.</p><p>Example: false</p></td></tr><tr><td>terminationOrder</td><td><code>boolean</code></td><td><p>Validates termination orders during the creation and before the order is submitted.</p><p>Example: false</p></td></tr><tr><td>productRequest</td><td><code>boolean</code></td><td><p>Validates the product request form while the client is filling in information and before the form is submitted.</p><p>Example: false</p></td></tr></tbody></table>

## ProductStatistics <a href="#productstatistics" id="productstatistics"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="211">Field</th><th width="172">Type</th><th>Description</th></tr></thead><tbody><tr><td>items</td><td><code>integer</code></td><td><p>The number of items assigned to the product.</p><p>Example: 1</p></td></tr><tr><td>orders</td><td><code>integer</code></td><td><p>The number of orders placed for the product.</p><p>Example: 2</p></td></tr><tr><td>agreements</td><td><code>integer</code></td><td><p>The number of agreements signed with the product.</p><p>Example: 4000</p></td></tr><tr><td>subscriptions</td><td><code>integer</code></td><td><p>The number of existing subscriptions to the product.</p><p>Example: 2</p></td></tr><tr><td>requests</td><td><code>integer</code></td><td><p>The number of requests related to the product.</p><p>Example: 100</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="PRODUCT OBJECT" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "PRD-1234-1234",
  "name": "Microsoft 365 online services for commercial",
  "shortDescription": "Microsoft 365 and Office 365 are cloud-based productivity suites that offer a range of applications and services to help businesses of all sizes work more efficiently.",
  "longDescription": "Microsoft 365 and Office 365 are cloud-based productivity suites that offer a range of applications and services to help businesses of all sizes work more efficiently. These plans combine the familiar Microsoft Office desktop suite with cloud-based versions of Microsoft's next-generation communications and collaboration services (including Office for the web, Microsoft Exchange Online, Microsoft Teams, and Microsoft SharePoint Online) to help users be productive from virtually anywhere through the Internet.",
  "website": "https://www.microsoft.com",
  "icon": "/static/PRD-1234-1234/logo.png",
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
{% endtab %}
{% endtabs %}
