---
description: >-
  Use the Accounts API to manage accounts, users, and related entities
  programmatically.
layout:
  width: wide
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
---

# Accounts API

The **Accounts API** enables you to programmatically access and manage key account-related data within the Marketplace Platform.

It provides secure endpoints that allow you to perform operations such as creating, updating, and retrieving information about accounts, users, user groups, licensees, sellers, and API tokens.

Additionally, the API supports retrieving a list of available modules within the platform and managing ERP system links.

## Before you start

Review the shared API docs before you work with account resources.

* [Authentication](../)
* [URL structure](../../api-usage-and-reference/url-structure.md)
* [Error handling](../../api-usage-and-reference/errors-handling.md)

## Core resources

The Accounts API is built around the following core resources:

* **Account** – Represents a client, vendor, or operations account.
* **Account user** – Represents an account user.
* **API token** – Represents an authentication token object.
* **Buyer** – Represents entities that engage in commercial activities and are the recipients of `invoices` issued by SoftwareOne.
* **Cloud tenant** – Represents a `CloudTenant` object in the Marketplace.
* **ERP link** – Represents a connection between the buyer object and the seller object in the Marketplace.
* **Licensee** – Represents entities that consume the software products or services procured by the `buyer`.
* **Module** – Represents modules available in the platform, for example, Marketplace.
* **Seller** – Represents SoftwareOne entities (for example, SoftwareOne Canada) that buy software solutions from vendors and sell those solutions to clients.
* **User** – Represents users who can sign in to the platform using their credentials and perform operations associated with their permissions.
* **User group** – Represents a `UserGroup` object in the Marketplace.

## Browse collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.

Use the following links to jump to the collection you need:

* [Accounts](./#accounts)
* [Account Users](./#account-users-collection)
* [API Tokens](./#api-tokens)
* [Buyers](./#buyers)
* [Cloud Tenants](./#cloud-tenants)
* [Sellers](./#sellers)
* [ERP Link](./#erp-link)
* [Licensees](./#licensees-collection)
* [Modules](./#modules-collection)
* [Users](./#users-collection)
* [User Groups](./#user-groups-collection)

### Accounts

<details>

<summary>View Accounts operations</summary>

<table><thead><tr><th width="180">Operation</th><th width="113">Method</th><th width="267">Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="account/create-account.md">Create account</a></td><td>POST</td><td>Creates a new account.</td><td>ops</td></tr><tr><td><a href="account/update-account.md">Update account</a></td><td>PUT</td><td>Updates account details.</td><td>vendor, client, ops</td></tr><tr><td><a href="account/get-account.md">Get account</a></td><td>GET</td><td>Retrieves a single Account by its ID.</td><td>vendor, client, ops</td></tr><tr><td><a href="account/list-accounts.md">List accounts</a></td><td>GET</td><td>Retrieves the full Accounts collection.</td><td>vendor, client, ops</td></tr><tr><td><a href="account/enable-account.md">Enable account</a></td><td>POST</td><td>Re-enables a previously disabled account.</td><td>ops</td></tr><tr><td><a href="account/disable-account.md">Disable account</a></td><td>POST</td><td>Disables the account; users cannot log in.</td><td>ops</td></tr><tr><td><a href="account/activate-account.md">Activate account</a></td><td>POST</td><td>Activates an account that has been enabled.</td><td>ops</td></tr><tr><td><a href="account/validate-account.md">Validate account</a></td><td>POST</td><td>Validates account data before creation.</td><td>ops</td></tr><tr><td><a href="account/deactivate-account.md">Deactivate account</a></td><td>POST</td><td>Deactivates an active account.</td><td>ops</td></tr><tr><td><a href="account/get-account-icon.md">Get account icon</a></td><td>GET</td><td>Retrieves the account’s icon.</td><td>public</td></tr></tbody></table>

</details>

### Account Users <a href="#account-users-collection" id="account-users-collection"></a>

<details>

<summary>View Account Users operations</summary>

<table><thead><tr><th>Operation</th><th width="129">Method</th><th width="246">Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="account-user/create-account-user.md">Create account user</a></td><td>POST</td><td>Invites or re‑invites a user to the account.</td><td>vendor, client, ops</td></tr><tr><td><a href="account-user/list-account-users.md">List account users</a></td><td>GET</td><td>Lists all users assigned to the account.</td><td>vendor, client, ops</td></tr><tr><td><a href="account-user/get-account-user.md">Get account user</a></td><td>GET</td><td>Retrieves an account user by ID.</td><td>vendor, client, ops</td></tr><tr><td><a href="account-user/delete-account-user.md">Delete account user</a></td><td>DELETE</td><td>Removes a user from the account.</td><td>vendor, client, ops</td></tr><tr><td><a href="account-user/accept-user-invitation.md">Accept user invitation</a></td><td>POST</td><td>Accepts a user invitation to the account.</td><td>vendor, client, ops</td></tr><tr><td><a href="account-user/assign-user-to-a-group.md">Assign user to groups</a></td><td>POST</td><td>Assigns an account user to specific groups.</td><td>vendor, client, ops</td></tr><tr><td><a href="account-user/resend-user-invitation.md">Resend user invitation</a></td><td>POST</td><td>Resends an invitation to the account.</td><td>vendor, client, ops</td></tr><tr><td><a href="account-user/send-new-invitation.md">Send new invitation</a></td><td>POST</td><td>Sends a new invitation when the previous one expired.</td><td>vendor, client, ops</td></tr><tr><td><a href="account-user/update-user-to-group-assignment.md">Update user group assignment</a></td><td>PUT</td><td>Updates a user’s group assignment.</td><td>vendor, client, ops</td></tr><tr><td><a href="account-user/remove-user.md">Remove user from group</a></td><td>DELETE</td><td>Removes an account user from specific groups.</td><td>vendor, client, ops</td></tr></tbody></table>

</details>

### API Tokens

<details>

<summary>View API Tokens operations</summary>

| Operation                                                                                 | Method | Description                              | Access              |
| ----------------------------------------------------------------------------------------- | ------ | ---------------------------------------- | ------------------- |
| [Create API token](api-tokens/create-token.md)                                            | POST   | Creates an API token for the account.    | vendor, client, ops |
| [List API tokens](api-tokens/list-tokens.md)                                              | GET    | Retrieves the API tokens collection.     | vendor, client, ops |
| [Get API token](api-tokens/get-token.md)                                                  | GET    | Retrieves an API token by ID.            | vendor, client, ops |
| [Update API token](api-tokens/update-token.md)                                            | PUT    | Updates an existing API token.           | vendor, client, ops |
| [Delete API token](../../../modules-and-features/settings/api-tokens/delete-api-token.md) | DELETE | Deletes an API token.                    | vendor, client, ops |
| [Disable API token](api-tokens/disable-token.md)                                          | POST   | Disables an API token.                   | vendor, client, ops |
| [Enable API token](api-tokens/enable-token.md)                                            | POST   | Enables a previously disabled API token. | vendor, client, ops |

</details>

### Buyers

<details>

<summary>View Buyers operations</summary>

| Operation                                                     | Method | Description                                                                      | Access              |
| ------------------------------------------------------------- | ------ | -------------------------------------------------------------------------------- | ------------------- |
| [Create buyer](buyer/create-buyer.md)                         | POST   | Creates a buyer for the client account.                                          | ops                 |
| [List buyers](buyer/list-buyers.md)                           | GET    | Retrieves the buyers collection.                                                 | client, ops         |
| [Get buyer](buyer/get-buyer.md)                               | GET    | Retrieves a buyer by ID.                                                         | client, ops         |
| [Update buyer](buyer/update-buyer.md)                         | PUT    | Updates a buyer.                                                                 | client, ops         |
| [Disable buyer](buyer/disable-buyer.md)                       | POST   | Disables a buyer.                                                                | client, ops         |
| [Enable buyer](buyer/enable-buyer.md)                         | POST   | Enables a previously disabled buyer.                                             | ops                 |
| [Validate buyer](buyer/validate-buyer.md)                     | POST   | Validates buyer data.                                                            | ops                 |
| [Delete buyer](buyer/delete-buyer.md)                         | DELETE | Deletes a buyer.                                                                 | ops                 |
| [Deactivate buyer](buyer/deactivate-buyer.md)                 | POST   | Deactivates a buyer.                                                             | ops                 |
| [Synchronize buyer](buyer/synchronize-buyer.md)               | POST   | Synchronizes a buyer with the ERP system.                                        | ops                 |
| [Transfer buyer](buyer/buyer-transfer.md)                     | POST   | Transfers a buyer and its dependencies between accounts with same External ID.   | ops                 |
| [Get buyer transfer details](buyer/buyer-transfer-details.md) | GET    | Retrieves buyer transfer information, optionally validating destination account. | public              |
| [Get buyer icon](buyer/get-buyer-icon.md)                     | GET    | Retrieves the buyer’s icon.                                                      | vendor, client, ops |

</details>

### Cloud Tenants

<details>

<summary>View Cloud Tenants operations</summary>

| Operation                                                   | Method | Description                             | Access |
| ----------------------------------------------------------- | ------ | --------------------------------------- | ------ |
| [Create cloud tenant](cloud-tenants/create-cloud-tenant.md) | POST   | Creates a cloud tenant.                 | ops    |
| [List cloud tenants](cloud-tenants/list-cloud-tenants.md)   | GET    | Retrieves the cloud tenants collection. | ops    |
| [Get cloud tenant](cloud-tenants/get-cloud-tenant.md)       | GET    | Retrieves a cloud tenant by ID.         | ops    |
| [Update cloud tenant](cloud-tenants/update-cloud-tenant.md) | PUT    | Updates a cloud tenant.                 | ops    |
| [Delete cloud tenant](cloud-tenants/delete-cloud-tenant.md) | DELETE | Deletes a cloud tenant.                 | ops    |

</details>

### Sellers

<details>

<summary>View Sellers operations</summary>

| Operation                                        | Method | Description                                            | Access      |
| ------------------------------------------------ | ------ | ------------------------------------------------------ | ----------- |
| [Create seller](seller/create-seller.md)         | POST   | Creates a seller for the account.                      | ops         |
| [List sellers](seller/list-sellers.md)           | GET    | Retrieves the sellers collection.                      | client, ops |
| [Get seller](seller/get-seller.md)               | GET    | Retrieves a seller by ID.                              | client, ops |
| [Update seller](seller/update-seller.md)         | PUT    | Updates a seller.                                      | ops         |
| [Activate seller](seller/activate-seller.md)     | POST   | Activates a previously deactivated or disabled seller. | ops         |
| [Deactivate seller](seller/deactivate-seller.md) | POST   | Deactivates a seller.                                  | ops         |
| [Disable seller](seller/disable-seller.md)       | POST   | Disables a seller.                                     | ops         |
| [Delete seller](seller/delete-seller.md)         | DELETE | Deletes a seller.                                      | public      |
| [Get seller icon](seller/get-seller-icon.md)     | GET    | Retrieves the seller icon.                             | ops         |

</details>

### ERP Link <a href="#erp-link-collection" id="erp-link-collection"></a>

<details>

<summary>View ERP Link operations</summary>

| Operation                                        | Method | Description                         | Access      |
| ------------------------------------------------ | ------ | ----------------------------------- | ----------- |
| [List ERP links](erp-link/list-erp-links.md)     | GET    | Retrieves the ERP Links collection. | client, ops |
| [Get ERP link](erp-link/get-erp-link.md)         | GET    | Retrieves an ERP Link by ID.        | client, ops |
| [Update ERP link](erp-link/update-erp-link.md)   | PUT    | Updates an ERP Link.                | ops         |
| [Unblock ERP link](erp-link/unblock-erp-link.md) | POST   | Unblocks an ERP Link.               | ops         |
| [Block ERP link](erp-link/block-erp-link.md)     | POST   | Blocks an ERP Link.                 | ops         |

</details>

### Licensees <a href="#licensees-collection" id="licensees-collection"></a>

<details>

<summary>View Licensees operations</summary>

| Operation                                                                               | Method | Description                                    | Access      |
| --------------------------------------------------------------------------------------- | ------ | ---------------------------------------------- | ----------- |
| [Create licensee](../../../modules-and-features/settings/licensees/create-licensees.md) | POST   | Creates a licensee linking a Buyer and Seller. | client, ops |
| [List licensees](licensee/list-licensees.md)                                            | GET    | Retrieves the licensees collection.            | client, ops |
| [Get licensee](licensee/get-licensee.md)                                                | GET    | Retrieves a licensee by ID.                    | client, ops |
| [Update licensee](licensee/update-licensee.md)                                          | PUT    | Updates a licensee.                            | client, ops |
| [Disable licensee](licensee/disable-licensee.md)                                        | POST   | Disables a licensee.                           | client, ops |
| [Enable licensee](licensee/enable-licensee.md)                                          | POST   | Enables a previously disabled licensee.        | client, ops |
| [Delete licensee](licensee/delete-licensee.md)                                          | DELETE | Deletes a licensee.                            | ops         |
| [Get licensee icon](licensee/get-licensee-icon.md)                                      | GET    | Retrieves the licensee icon.                   | public      |

</details>

### Modules <a href="#modules-collection" id="modules-collection"></a>

<details>

<summary>View Modules operations</summary>

| Operation                              | Method | Description                                            | Access |
| -------------------------------------- | ------ | ------------------------------------------------------ | ------ |
| [List modules](module/list-modules.md) | GET    | Retrieves the list of modules available in the portal. | ops    |

</details>

### Users <a href="#users-collection" id="users-collection"></a>

<details>

<summary>View Users operations</summary>

| Operation                                               | Method | Description                                        | Access              |
| ------------------------------------------------------- | ------ | -------------------------------------------------- | ------------------- |
| [List users](users/list-users.md)                       | GET    | Retrieves the platform users collection.           | vendor, client, ops |
| [Get user](users/get-user.md)                           | GET    | Retrieves a user by ID.                            | vendor, client, ops |
| [Get SSO configuration](users/get-sso-configuration.md) | GET    | Retrieves SSO configuration for the user.          | vendor, client, ops |
| [Update user](users/update-user.md)                     | PUT    | Updates a user.                                    | vendor, client, ops |
| [Set user password](users/set-user-password.md)         | POST   | Sets password for non‑SSO users during onboarding. | vendor, client, ops |
| [Block user](users/block-user.md)                       | POST   | Blocks a user, preventing login.                   | ops                 |
| [Unblock user](users/unblock-user.md)                   | POST   | Unblocks a previously blocked user.                | ops                 |

</details>

### User Groups <a href="#user-groups-collection" id="user-groups-collection"></a>

<details>

<summary>View User Groups operations</summary>

| Operation                                             | Method | Description                           | Access              |
| ----------------------------------------------------- | ------ | ------------------------------------- | ------------------- |
| [Create user group](user-groups/create-user-group.md) | POST   | Creates a user group for the account. | vendor, client, ops |
| [List user groups](user-groups/list-user-groups.md)   | GET    | Retrieves the user groups collection. | vendor, client, ops |
| [Get user group](user-groups/get-user-group.md)       | GET    | Retrieves a user group by ID.         | vendor, client, ops |
| [Update user group](user-groups/update-user-group.md) | PUT    | Updates a user group.                 | vendor, client, ops |
| [Delete user group](user-groups/delete-user-group.md) | DELETE | Deletes a user group.                 | vendor, client, ops |

</details>
