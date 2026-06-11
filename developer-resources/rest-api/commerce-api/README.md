---
description: >-
  Use the Commerce API to manage orders, subscriptions, and agreements
  programmatically.
---

# Commerce API

The **Commerce API** enables you to create, retrieve, and manage orders, subscriptions, and agreements within the Marketplace Platform.

With this API, you can:

* Create new assets and manage the existing ones.
* Check the details of a specific order by its ID.
* Delete orders that are still in draft status (not yet submitted).
* Fail orders that can't be completed.
* Update, process, or complete orders as needed.
* Retrieve and manage files attached to agreements.
* Validate requests and manage the status of those requests.

## Before you start

Review the shared API docs before you work with commerce resources.

* [Authentication](../)
* [URL structure](../../api-usage-and-reference/url-structure.md)
* [Error handling](../../api-usage-and-reference/errors-handling.md)

## Core resources

The Commerce API is built around the following core resources:

* **Agreement** – Defines the relationship between the `seller`, `buyer`, and `licensee`.
* **Asset** – Represents a one-time purchased item or a perpetual license associated with an agreement.
* **Order** – Represents a request to create or modify an agreement, including purchasing, changing, or terminating `subscriptions` within an agreement.
* **Order asset** – Represents an asset created and managed in the context of an order.
* **Order subscription** – Represents a subscription created and managed in the context of an order.
* **Request** – Represents a request to the platform.
* **Subscription** – Represents a collection of items within the agreement. All items are connected to one `product`, one vendor, and one client, and share the same billing frequency and commitment terms.

## Browse collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.

Use the following links to jump to the collection you need:

* [Assets](./#assets)
* [Agreements](./#agreements)
* [Orders](./#orders)
* [Order Subscriptions](./#order-subscriptions)
* [Order Assets](./#order-assets)
* [Requests](./#requests)
* [Subscriptions](./#subscriptions)

### Assets

<details>

<summary>View Assets operations</summary>

<table><thead><tr><th width="158">Operation</th><th width="127">Method</th><th width="232">Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="assets/create-asset.md">Create asset</a></td><td>POST</td><td>Creates an active asset that is globally retrievable.</td><td>vendor</td></tr><tr><td><a href="assets/list-assets.md">List assets</a></td><td>GET</td><td>Gets all assets.</td><td>vendor, client, ops</td></tr><tr><td><a href="assets/get-asset.md">Get asset by id</a></td><td>GET</td><td>Gets an asset by id.</td><td>vendor, client, ops</td></tr><tr><td><a href="assets/update-asset.md">Update asset</a></td><td>PUT</td><td>Updates an asset by id.</td><td>vendor, client, ops</td></tr><tr><td><a href="assets/terminate-asset.md">Terminate asset</a></td><td>POST</td><td>Sets an asset’s status to terminated and terminates all related entitlements.</td><td>vendor</td></tr><tr><td><a href="assets/render-asset-template.md">Render asset template</a></td><td>GET</td><td>Renders an asset’s template by id.</td><td>vendor, client, ops</td></tr></tbody></table>

</details>

### Agreements

<details>

<summary>View Agreements operations</summary>

<table><thead><tr><th width="218">Operation</th><th width="124">Method</th><th>Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="agreements/create-agreement.md">Create agreement</a></td><td>POST</td><td>Creates an agreement administratively.</td><td>ops</td></tr><tr><td><a href="agreements/list-agreements.md">List agreements</a></td><td>GET</td><td>Gets a list of agreements.</td><td>vendor, client, ops</td></tr><tr><td><a href="agreements/get-agreement.md">Get agreement by id</a></td><td>GET</td><td>Gets an agreement by id.</td><td>vendor, client, ops</td></tr><tr><td><a href="agreements/update-agreement.md">Update agreement</a></td><td>PUT</td><td>Updates some properties of an agreement.</td><td>vendor, client, ops</td></tr><tr><td><a href="agreements/render-agreement-template.md">Render agreement template</a></td><td>GET</td><td>Renders the template for an agreement by id.</td><td>vendor, client, ops</td></tr><tr><td><a href="agreements/create-agreement-attachment.md">Create agreement attachment</a></td><td>POST</td><td>Creates an agreement attachment by uploading a file.</td><td>vendor, ops</td></tr><tr><td><a href="agreements/list-agreement-attachments.md">List agreement attachments</a></td><td>GET</td><td>Gets a list of agreement attachments.</td><td>vendor, client, ops</td></tr><tr><td><a href="agreements/get-agreement-attachment.md">Get agreement attachment by id</a></td><td>GET</td><td>Gets an agreement attachment by id.</td><td>vendor, client, ops</td></tr><tr><td><a href="agreements/delete-agreement-attachment.md">Delete agreement attachment</a></td><td>DELETE</td><td>Deletes an agreement attachment.</td><td>vendor, ops</td></tr></tbody></table>

</details>

### Orders

<details>

<summary>View Orders operations</summary>

| Operation                                                | Method | Description                                                            | Access              |
| -------------------------------------------------------- | ------ | ---------------------------------------------------------------------- | ------------------- |
| [Create order](orders/create-new-order.md)               | POST   | Creates a new order for a specified agreement or creates an agreement. | client              |
| [List orders](orders/list-orders.md)                     | GET    | Gets a list of orders visible to the user.                             | vendor, client, ops |
| [Get order by id](orders/get-order.md)                   | GET    | Gets an order by id.                                                   | vendor, client, ops |
| [Update order](orders/update-order.md)                   | PUT    | Updates some properties of an order.                                   | vendor, client, ops |
| [Validate order](orders/validate-order.md)               | POST   | Validates the state of an order.                                       | vendor, client, ops |
| [Process order](orders/process-order.md)                 | POST   | Changes an order’s status to processing.                               | vendor, client, ops |
| [Query order](orders/query-order.md)                     | POST   | Changes an order’s status to querying.                                 | vendor              |
| [Complete order](orders/complete-order.md)               | POST   | Changes an order’s status to complete.                                 | vendor              |
| [Fail order](orders/fail-order.md)                       | POST   | Changes an order’s status to failed.                                   | vendor, ops         |
| Notify client about order                                | POST   | Sends an email reminder to the client.                                 | ops                 |
| [Delete order](orders/delete-order.md)                   | DELETE | Deletes an order.                                                      | client              |
| [Render order template](orders/render-order-template.md) | GET    | Renders the template for an order by id.                               | vendor, client, ops |

</details>

### Order Subscriptions

<details>

<summary>View Order Subscriptions operations</summary>

| Operation                                                               | Method | Description                                                            | Access              |
| ----------------------------------------------------------------------- | ------ | ---------------------------------------------------------------------- | ------------------- |
| [Create order subscription](subscriptions/create-order-subscription.md) | POST   | Creates a new subscription and adds it to the order.                   | vendor              |
| [List order subscriptions](subscriptions/list-subscriptions-1.md)       | GET    | Returns a list of all subscriptions for the order visible to the user. | vendor, client, ops |
| [Get order subscription by id](subscriptions/get-order-subscription.md) | GET    | Returns a subscription with the given id that exists in the order.     | vendor, client, ops |
| [Update order subscription](subscriptions/update-order-subscription.md) | PUT    | Updates an existing subscription within the order.                     | vendor              |
| [Remove order subscription](subscriptions/remove-order-subscription.md) | DELETE | Removes a subscription from the order.                                 | vendor              |

</details>

### Order Assets

<details>

<summary>View Order Assets operations</summary>

| Operation                                          | Method | Description                                                       | Access              |
| -------------------------------------------------- | ------ | ----------------------------------------------------------------- | ------------------- |
| [Create order asset](orders/create-order-asset.md) | POST   | Creates a draft asset that is only retrievable through the order. | vendor              |
| [List order assets](orders/list-order-assets.md)   | GET    | Gets all order assets.                                            | vendor, client, ops |
| Get order asset by id                              | GET    | Gets an order asset by id.                                        | vendor, client, ops |
| [Update order asset](orders/update-order-asset.md) | PUT    | Updates an order asset by id.                                     | vendor, client, ops |
| [Delete order asset](orders/delete-order-asset.md) | DELETE | Deletes an order asset by id.                                     | vendor              |

</details>

### Requests

<details>

<summary>View Requests operations</summary>

| Operation                                        | Method | Description                                | Access              |
| ------------------------------------------------ | ------ | ------------------------------------------ | ------------------- |
| [Create request](requests/create-request.md)     | POST   | Creates a new request.                     | client, ops         |
| [List requests](requests/list-requests.md)       | GET    | Gets a list of requests.                   | vendor, client, ops |
| [Get request by id](requests/get-request.md)     | GET    | Gets a request by id.                      | vendor, client, ops |
| [Update request](requests/update-request.md)     | PUT    | Updates some properties of a request.      | vendor, ops         |
| [Validate request](requests/validate-request.md) | POST   | Performs the request validation procedure. | vendor, client, ops |
| [Process request](requests/process-request.md)   | POST   | Moves a request to the processing state.   | vendor, client, ops |
| [Query request](requests/query-request.md)       | POST   | Moves a request to the querying state.     | vendor, ops         |
| [Complete request](requests/complete-request.md) | POST   | Moves a request to the completed state.    | vendor, client, ops |

</details>

### Subscriptions

<details>

<summary>View Subscriptions operations</summary>

| Operation                                                                                                     | Method | Description                                     | Access              |
| ------------------------------------------------------------------------------------------------------------- | ------ | ----------------------------------------------- | ------------------- |
| [Create subscription](subscriptions/create-subscription.md)                                                   | POST   | Creates a subscription.                         | vendor              |
| [List subscriptions](subscriptions/list-subscriptions.md)                                                     | GET    | Gets a list of subscriptions in all agreements. | vendor, client, ops |
| [Get subscription by id](subscriptions/get-subscription.md)                                                   | GET    | Gets a subscription in an agreement by id.      | vendor, client, ops |
| [Update subscription](subscriptions/update-subscription.md)                                                   | PUT    | Updates a subscription.                         | vendor, client, ops |
| [Terminate subscription](../../../modules-and-features/marketplace/subscriptions/terminate-a-subscription.md) | POST   | Terminates a subscription.                      | vendor              |
| [Render subscription template](subscriptions/render-subscriptions-template.md)                                | GET    | Renders a subscription’s template.              | vendor, client, ops |

</details>
