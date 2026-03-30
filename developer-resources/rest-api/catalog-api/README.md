---
description: Manage your products programmatically using the Catalog API.
---

# Catalog API

The **Catalog API** enables you to create, retrieve, and manage products. You can also configure individual items as well as item groups through the API.&#x20;

Additionally, you can define parameters and parameter groups, and manage pricing with price lists. You can also create custom templates and product variants. The API also includes endpoints for managing product media, documents, listings, and terms and conditions.

<a href="https://editor-next.swagger.io/?url=https://api.platform.softwareone.com/public/v1/catalog/openapi.json" class="button primary">Try API</a><a href="https://api.platform.softwareone.com/public/v1/catalog/openapi.json" class="button secondary">Download API</a>

### Core Concepts

The Catalog API is built around the following core resources:

* **Authorization** - Represents the permissions and credentials that are required for interactions between sellers and vendors in the scope of a product.&#x20;
* **Document** - Used to upload product documentation (via an online link or file) to the `product` object.
* **Item** - Represent the individual stock-keeping units (SKUs) or transactable element of a product. Items are shown as a line item in an order.
* **Item group** - Represents a group of items.
* **Listing** - Represents a business entity that aligns a product with a specific SoftwareOne `seller`.
* **Media** - Enables vendors to add, view, or delete media from the `product` object.&#x20;
* **Product** - Represents a collection of `items` and their associated parameters organized into a unified group.
* **Parameter** - Allows vendors to define additional information that must be collected from and shared with the client, enabling the client to self-serve within the SoftwareOne Marketplace.
* **Parameter group** - Represents a group of `parameters`.
* **Pricelist** - Includes key pricing details such as sales and purchase prices, enabling vendors and operations to effectively manage and apply different price points for product items.&#x20;
* **Pricing policy** - Defines client-specific markup and pricing rules based on negotiated terms and special agreements.

## Collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.&#x20;

Refer to the following capability matrix to see which roles are authorized to perform specific operations within each collection:

### Authorization

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List authorizations</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get authorization</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create authorization</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Update authorization</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Delete authorization</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>

### Documents

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List documents</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get document</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create document</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update document</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Delete document</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Mark document for review</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Publish document</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Unpublish document</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### Items

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List items</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get item</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create item</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update item by ID</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete item</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Mark item for review</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Publish item</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Unpublish item</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### Item Group

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List item groups</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get item group</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create item group</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update item group</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete item group</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### Listings

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List all listings</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get listing</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create listing</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Update listing</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Delete listing</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>

### Media

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List product media</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get product media</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create product media</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update product media</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete product media</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Mark a media for review</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Publish a media for product</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Unpublish a media for product</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### Parameters

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List parameters for a product</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get parameter</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create parameter</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update parameter</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete parameter</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### Parameters Groups

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List parameter groups</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get parameter group</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create parameter group</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update parameter group</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete parameter group</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### Price Lists

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List price lists</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get price list</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create price list</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Update price list</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Delete price list</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>List price list items</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get price list items</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update price list items</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### Pricing Policy

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List pricing policies</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Get pricing policy</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Create pricing policy</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Update pricing policy</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Delete pricing policy</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Activate pricing policy</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Disable pricing policy</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>List of pricing policy attachments</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Get pricing policy attachment</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Create pricing policy attachment</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Update pricing policy attachment </td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Delete pricing policy attachment </td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>

### Product

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List products</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get product</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create product</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update product by ID</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete product</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Mark product for review</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Publish product</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Unpublish product</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Update product settings</td><td>❌</td><td>✅</td><td>❌</td></tr></tbody></table>

### Product Templates

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List product templates</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get product template</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create product template</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update product template</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete product templates</td><td>❌</td><td>✅</td><td>❌</td></tr></tbody></table>

### Terms

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List terms</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get terms</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create terms</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Update terms</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Delete terms</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Mark terms for review</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Publish terms</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Unpublish terms</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### Units of Measure

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List units of measure</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Get units of measure</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Create units of measure</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Update units of measure</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>

### Variant

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List variant</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get variant</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create variant</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Update variant</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Delete variant</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Mark variant for review</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Publish variant</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Unpublish variant</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>
