# Product

The Product object represents a collection of items and their relevant parameters curated into a cohesive group for business purposes. Defined by vendors, products are accessible through listings, providing a structured framework for transactional activities.&#x20;

The Product object contains the following properties:

<table><thead><tr><th width="178">Field</th><th width="123">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Product Identifier. </p><p></p><p>Example: PRD-1234-1234</p></td></tr><tr><td>href</td><td>string</td><td><p>Relative reference to product on API (always v1/products/{id}) </p><p></p><p>Example: /v1/products/PRD-1234-1234</p></td></tr><tr><td>name</td><td>string</td><td><p>Product name </p><p></p><p>Example: Microsoft 365 online services for commercial</p></td></tr><tr><td>shortDescription</td><td>string</td><td><p>Short description of product. </p><p></p><p>Example: Microsoft 365 and Office 365 are cloud-based productivity suites that offer a range of applications and services to help businesses of all sizes work more efficiently.</p></td></tr><tr><td>longDescription</td><td>string</td><td><p>Long description of product. </p><p></p><p>Example: Microsoft 365 and Office 365 are cloud-based productivity suites that offer a range of applications and services to help businesses of all sizes work more efficiently. These plans combine the familiar Microsoft Office desktop suite with cloud-based versions of Microsoft's next-generation communications and collaboration services (including Office for the web, Microsoft Exchange Online, Microsoft Teams, and Microsoft SharePoint Online) to help users be productive from virtually anywhere through the Internet.</p></td></tr><tr><td>website</td><td>string</td><td><p>URL for the product website. </p><p></p><p>Example: https://www.microsoft.com</p></td></tr><tr><td>icon</td><td>string</td><td><p>Product logo.</p><p></p><p>Example: /static/PRD-1234-1234/logo.png</p></td></tr><tr><td>externalIds</td><td>ExternalIds</td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "operations": "op-322-322",
}
</code></pre></td></tr><tr><td>vendor</td><td><a href="../../accounts-api/account/#account-object">Account</a></td><td><p>Reference to the vendor account object. </p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>status</td><td>status</td><td><p>Possible values: Draft, Pending, Published, and Unpublished. </p><p></p><p>See <a href="product-states.md">Product States</a>.</p></td></tr><tr><td>settings</td><td>ProductSettings</td><td><p><strong>Activate item selection validation:</strong></p><p>Used in the “Purchase wizard” to validate vendor-specific compatibility of selected items, before the order is submitted.</p><p></p><p><strong>Activate validation of change orders in a draft state</strong></p><p>Used to validate vendor-specific rules on a change order within the Purchase wizard (via existing agreement) and the Subscription edit screen</p><p><strong>Activate validation of product requests in a draft state</strong></p><p>Used to perform vendor-specific validation on the product’s request form before form submission.</p><p><strong>Activate validation of purchase orders in a draft state</strong></p><p>Used to perform vendor-specific validation of purchase order within the “Purchase wizard”</p><p><strong>Activate validation of purchase orders in a querying state</strong></p><p>Used to perform vendor-specific validation when client is responding to a purchase order where vendor has requested additional information from the client.</p><p><strong>Activate validation of termination order in a draft state</strong></p><p>Used to perform vendor-specific validation when client initiates termination order on an agreement or subscription. </p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
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
</code></pre></td></tr><tr><td>statistics</td><td>ProductStatistics</td><td><p>Product statistics. </p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "items": 110,
  "orders": 123,
  "agreements": 1,
  "subscriptions": 20
}
</code></pre></td></tr></tbody></table>

### ProductSettings <a href="#productsettings" id="productsettings"></a>

<table><thead><tr><th width="181">Field</th><th width="205">Type</th><th>Description</th></tr></thead><tbody><tr><td>productOrdering</td><td>boolean</td><td><p>Displays the <strong>Buy</strong> button on the product card, enabling clients to place an order for this product. </p><p></p><p>Example: true</p></td></tr><tr><td>itemSelection</td><td>boolean</td><td><p>Validates the compatibility of selected product items within the purchase order, supporting order processing. </p><p></p><p>Example: false</p></td></tr><tr><td>orderQueueChanges</td><td>boolean</td><td><p>Enables notifications of changes in the order queue. </p><p></p><p>Example: false</p></td></tr><tr><td>productRequests</td><td><a href="./#productrequestsettings">ProductRequestSettings</a></td><td><p>Settings for product requests page. </p><p></p><p>Example:  <a href="./#productrequestsettings">ProductRequestSettings</a></p></td></tr><tr><td>preValidation</td><td><a href="./#prevalidationsettings">PreValidationSettings</a></td><td><p>Settings for pre validation phase during purchase. </p><p></p><p>Example: <a href="./#prevalidationsettings">PreValidationSettings</a></p></td></tr></tbody></table>

### ProductRequestSettings <a href="#productrequestsettings" id="productrequestsettings"></a>

<table><thead><tr><th width="149">Field</th><th width="148">Type</th><th>Description</th></tr></thead><tbody><tr><td>enabled</td><td>boolean</td><td><p>Displays a request button on the product card, enabling clients to request more information about a product. </p><p></p><p>Example: true</p></td></tr><tr><td>name</td><td>string</td><td><p>Product name, which appears as a title within the request wizard. </p><p></p><p>Example: Contact us about Microsoft 365 Online Services</p></td></tr><tr><td>label</td><td>string</td><td><p>Label on the product listing card. </p><p></p><p>Example: Contact us</p></td></tr></tbody></table>

### PreValidationSettings <a href="#prevalidationsettings" id="prevalidationsettings"></a>

<table><thead><tr><th width="210">Field</th><th width="175">Type</th><th>Description</th></tr></thead><tbody><tr><td>purchaseOrderDraft</td><td>boolean</td><td><p>Validates purchase order during the creation and before the order is submitted. </p><p></p><p>Example: false</p></td></tr><tr><td>purchaseOrderQuerying</td><td>boolean</td><td><p>Validates purchase orders when the client is requested to provide more information to the vendor on that order.  </p><p></p><p>Example: false</p></td></tr><tr><td>changeOrderDraft</td><td>boolean</td><td><p>Validates change order during the creation and before the order is submitted. </p><p></p><p>Example: false</p></td></tr><tr><td>terminationOrder</td><td>boolean</td><td><p>Validates termination orders during the creation and before the order is submitted. </p><p></p><p>Example: false</p></td></tr><tr><td>productRequest</td><td>boolean</td><td><p>Validates the product request form while the client is filling in information and before the form is submitted. </p><p></p><p>Example: false</p></td></tr></tbody></table>

### ProductStatistics <a href="#productstatistics" id="productstatistics"></a>

<table><thead><tr><th width="190">Field</th><th width="186">Type</th><th>Description</th></tr></thead><tbody><tr><td>items</td><td>integer</td><td><p>Number of items assigned to the product. </p><p></p><p>Example: 1</p></td></tr><tr><td>orders</td><td>integer</td><td><p>Number of orders placed for the product. </p><p></p><p>Example: 2</p></td></tr><tr><td>agreements</td><td>integer</td><td><p>Number of agreements signed with the product. </p><p></p><p>Example: 4000</p></td></tr><tr><td>subscriptions</td><td>integer</td><td><p>Number of existing subscriptions with the product. </p><p></p><p>Example: 2</p></td></tr><tr><td>requests</td><td>integer</td><td><p>Number of requests related to the product. </p><p></p><p>Example: 100</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="PRODUCT OBJECT" %}
```json
{
  "id": "PRD-1234-1234",
  "name": "Microsoft 365 online services for commercial",
  "shortDescription": "Microsoft 365 and Office 365 are cloud-based productivity suites that offer a range of applications and services to help businesses of all sizes work more efficiently. These plans combine the familiar Microsoft Office desktop suite with cloud-based versions of Microsoft’s next-generation communications and collaboration services to help users be productive from virtually anywhere through the Internet.",
  "longDescription": "<p>Microsoft 365 and Office 365 are cloud-based productivity suites that offer a range of applications and services to help businesses of all sizes work more efficiently. These plans combine the familiar Microsoft Office desktop suite with cloud-based versions of Microsoft's next-generation communications and collaboration services (including Office for the web, Microsoft Exchange Online, Microsoft Teams, and Microsoft SharePoint Online) to help users be productive from virtually anywhere through the Internet. Microsoft 365 and Office 365 are available in a variety of plans to best meet the needs of your organization. For detailed plan information on subscriptions that enable users for Microsoft 365 and Office 365 platform, see the full subscription comparison table.</p>",
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
  },
  "statistics": {
    "item": 100,
    "orders": 123,
    "agreement": 1,
    "subscription": 20
  }
}
    
```
{% endtab %}
{% endtabs %}
