# Product

The `product` object represents a collection of items and their relevant parameters curated into a cohesive group for business purposes. Defined by Vendors, Products are accessible through Listings, providing a structured framework for transactional activities.

<table><thead><tr><th>Field</th><th width="109">Type</th><th>Constraints</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p><code>READONLY</code> </p><p><code>IDX</code></p></td><td><p>Product Identifier. </p><p></p><p>Example: "PRD-1234-1234"</p></td></tr><tr><td>href</td><td>string</td><td><code>READONLY</code></td><td><p>Relative reference to product on API (always v1/products/{id}) </p><p></p><p>Example: "/v1/products/PRD-1234-1234"</p></td></tr><tr><td>name</td><td>string</td><td><code>IDX</code></td><td><p>Product name </p><p></p><p>Example: "Microsoft 365 online services for commercial"</p></td></tr><tr><td>shortDescription</td><td>string</td><td><code>IDX</code></td><td><p>Short description of product. </p><p></p><p>Example: "Microsoft 365 and Office 365 are cloud-based productivity suites that offer a range of applications and services to help businesses of all sizes work more efficiently."</p></td></tr><tr><td>longDescription</td><td>string</td><td><p><code>IDX</code></p><p><code>MARKDOWN</code></p></td><td><p>Long description of product. </p><p></p><p>Example: "Microsoft 365 and Office 365 are cloud-based productivity suites that offer a range of applications and services to help businesses of all sizes work more efficiently. These plans combine the familiar Microsoft Office desktop suite with cloud-based versions of Microsoft's next-generation communications and collaboration services (including Office for the web, Microsoft Exchange Online, Microsoft Teams, and Microsoft SharePoint Online) to help users be productive from virtually anywhere through the Internet"</p></td></tr><tr><td>website</td><td>string</td><td><p><code>FINAL</code></p><p><code>IDX</code></p><p><code>URI</code></p></td><td><p>URL for Product website. </p><p></p><p>Example: "https://www.microsoft.com"</p></td></tr><tr><td>icon</td><td>string</td><td><p><code>FINAL</code> </p><p><code>IDX</code></p></td><td><p>Product logo (aka icon) </p><p></p><p>Example: "/static/PRD-1234-1234/logo.png"</p></td></tr><tr><td>externalIds</td><td>ExternalIds</td><td> </td><td><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "operations": "op-322-322",
}
</code></pre></td></tr><tr><td>vendor</td><td><a href="../../accounts-api/account/#account-object">Account</a></td><td><code>IDX</code></td><td><p>Reference to the vendor Account object. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "ACC-1234-1234",
    "href": "/accounts/accounts/ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>status</td><td>status<br></td><td><code>IDX</code></td><td>Possible values: Draft, Pending, Published, and Unpublished.</td></tr><tr><td>settings<br><br></td><td>ProductSettings</td><td> </td><td><p><strong>Activate item selection validation:</strong></p><p>Used in the “Purchase wizard” to validate vendor-specific compatibility of selected items, before the order is submitted.</p><p><strong>Activate order queue changes:</strong></p><p><strong>IMPORTANT: “Order queue changes“ setting is NOT for implementation</strong></p><p><strong>Activate validation of change orders in a draft state</strong></p><p>Used to validate vendor-specific rules on a change order within the Purchase wizard (via existing agreement) and Subscription edit screen</p><p><strong>Activate validation of product requests in a draft state</strong></p><p>Used to perform vendor-specific validation on the product’s request form before form submission.</p><p><strong>Activate validation of purchase orders in a draft state</strong></p><p>Used to perform vendor-specific validation of purchase order within the “Purchase wizard”</p><p><strong>Activate validation of purchase orders in a querying state</strong></p><p>Used to perform vendor-specific validation when client is responding to a purchase order where vendor has requested additional information from the client.</p><p><strong>Activate validation of termination order in a draft state</strong></p><p>Used to perform vendor-specific validation when client initiates termination order on an agreement or subscription. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
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
</code></pre></td></tr><tr><td>statistics</td><td>ProductStatistics</td><td><code>READONLY</code></td><td><p>Product statistics. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "items": 110,
  "orders": 123,
  "agreements": 1,
  "subscriptions": 20
}
</code></pre></td></tr></tbody></table>

### ProductSettings <a href="#productsettings" id="productsettings"></a>

<table><thead><tr><th width="220">Field</th><th width="214">Type</th><th width="154">Constraints</th><th></th></tr></thead><tbody><tr><td>productOrdering</td><td>boolean</td><td><code>IDX</code></td><td><p>Displays “Buy” button on the product card, enabling clients to place an order for this product. </p><p></p><p>Example: "true"</p></td></tr><tr><td>itemSelection</td><td>boolean</td><td> </td><td><p>Validates compatibility of selected product items within the purchase order, supporting order processing. </p><p></p><p>Example: "false"</p></td></tr><tr><td>orderQueueChanges</td><td>boolean</td><td> </td><td><p>Enables notifications of changes in the order queue. </p><p></p><p>Example: "false"</p></td></tr><tr><td>productRequests</td><td><a href="./#productrequestsettings">ProductRequestSettings</a></td><td><code>OPTIONAL</code></td><td><p>Settings for product requests page. </p><p></p><p>Example:  <a href="./#productrequestsettings">ProductRequestSettings</a></p></td></tr><tr><td>preValidation</td><td><a href="./#prevalidationsettings">PreValidationSettings</a></td><td> </td><td><p>Settings for pre validation phase during purchase. </p><p></p><p>Example: <a href="./#prevalidationsettings">PreValidationSettings</a></p></td></tr></tbody></table>

### ProductRequestSettings <a href="#productrequestsettings" id="productrequestsettings"></a>

| Field   | Type    | Description                                                                                                                                     |
| ------- | ------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| enabled | boolean | <p>Displays request button on the product card, enabling clients to request more information about a product. </p><p></p><p>Example: "true"</p> |
| name    | string  | <p>This will appear as the title on the request wizard. </p><p></p><p>Example: "Contact us about Microsoft 365 Online Services"</p>             |
| label   | string  | <p>This will appear as the button label on the product listing card. </p><p></p><p>Example: "Contact us"</p>                                    |

### PreValidationSettings <a href="#prevalidationsettings" id="prevalidationsettings"></a>

| Field                 | Type    | Description                                                                                                                                        |
| --------------------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| purchaseOrderDraft    | boolean | <p>Validates purchase order during the creation and before the order is submitted. </p><p></p><p>Example: "false"</p>                              |
| purchaseOrderQuerying | boolean | <p>Validates purchase orders when client is requested to provide more information to the vendor on that order.  </p><p></p><p>Example: "false"</p> |
| changeOrderDraft      | boolean | <p>Validates change order during the creation and before the order is submitted. </p><p></p><p>Example: "false"</p>                                |
| terminationOrder      | boolean | <p>Validates termination orders during the creation and before the order is submitted. </p><p></p><p>Example: "false"</p>                          |
| productRequest        | boolean | <p>Validates the product request form while client is filling in information and before the form is submitted. </p><p></p><p>Example: "false"</p>  |

### ProductStatistics <a href="#productstatistics" id="productstatistics"></a>

| Field         | Type    | Constraints                                          | Description                                                                          |
| ------------- | ------- | ---------------------------------------------------- | ------------------------------------------------------------------------------------ |
| items         | integer | <p><code>READONLY</code></p><p><code>IDX</code></p>  | <p>Number of items assigned to the product. </p><p></p><p>Example: "1"</p>           |
| orders        | integer | <p><code>READONLY</code> </p><p><code>IDX</code></p> | <p>Number of orders placed with the product. </p><p></p><p>Example: "2"</p>          |
| agreements    | integer | <p><code>READONLY</code></p><p><code>IDX</code></p>  | <p>Number of agreements signed with the product. </p><p></p><p>Example: "4000"</p>   |
| subscriptions | integer | <p><code>READONLY</code> </p><p><code>IDX</code></p> | <p>Number of existing subscriptions with the product. </p><p></p><p>Example: "2"</p> |
| requests      | integer | <p><code>READONLY</code> </p><p><code>IDX</code></p> | <p>Number of requests related to the product. </p><p></p><p>Example: "100"</p>       |

