---
description: Manage orders, subscriptions, and agreements using the Commerce API
---

# Commerce API

The **Commerce API** enables you to create, retrieve, and manage your orders, subscriptions, and agreements within the SoftwareOne Marketplace. With this API, you can also:

* Create new assets and manage the existing ones.
* Check the details of a specific order by its ID.
* Delete orders that are still in draft status (not yet submitted).
* Fail orders that can't be completed.
* Update, process, or complete orders as needed.
* Retrieve and manage files attached to agreements.
* Validate requests and manage the status of those requests.

<a href="https://editor-next.swagger.io/?url=https://api.platform.softwareone.com/public/v1/commerce/openapi.json" class="button primary">Try API</a><a href="https://api.platform.softwareone.com/public/v1/commerce/openapi.json" class="button secondary">Download API</a>

## Core Concepts

The Commerce API is built around the following core resources:

* **Asset** - Represents a one-time purchased item or a perpetual license associated with an agreement.
* **Agreement** - Defines the relationship between the `seller`, `buyer`, and `licensee`.
* **Request** - Represents a request to the platform.
* **Order** - Represents a request to create or modify an agreement, including purchasing, changing, or terminating `subscriptions` within an agreement..
* **Subscription** - Represents a collection of items within the agreement. All items are connected to one `product`, one vendor, and one client (the same as the agreement) and have the same billing frequency and commitment terms.

## Collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.&#x20;

Refer to the following capability matrix to see which roles are authorized to perform specific operations within each collection:

### Assets

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List assets</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get asset</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create asset</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update asset</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Terminate asset</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Render an asset’s template by id</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### Agreements

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List agreements</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get agreement</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create agreements</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Update agreements</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Render agreement template</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>List agreement attachments</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get agreement attachment</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create agreement attachment</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Delete agreement attachment</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### Orders

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List orders</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get order</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create order</td><td>✅</td><td>❌</td><td>❌</td></tr><tr><td>Update order</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Validate order</td><td>✅</td><td>✅</td><td>❌</td></tr><tr><td>Process order</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Query order</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Complete order</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Fail order</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Remind client about an order</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Delete order</td><td>✅</td><td>❌</td><td>❌</td></tr><tr><td>Render order template</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### Order Subscription

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List subscriptions</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get order subscription</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create order subscription</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update order subscription</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Remove order subscription</td><td></td><td></td><td></td></tr></tbody></table>

### Order Assets

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List all order assets</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create order asset</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update order asset</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Delete order asset</td><td>❌</td><td>✅</td><td>❌</td></tr></tbody></table>

### Requests

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List requests</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get request</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Create request</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update request</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Validate request</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Process request</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Query request</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Complete request</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>List request messages</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get request message</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create request message</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>List request attachments</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get request attachment</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create request attachment</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Delete request attachment</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### Subscriptions

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List subscriptions</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get subscription</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create subscription</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update subscription</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Terminate subscription</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Render subscription template</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>
