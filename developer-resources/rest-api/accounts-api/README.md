---
description: >-
  Use the Accounts API to manage accounts, users, and related entities
  programmatically.
---

# Accounts API

The **Accounts API** enables you to programmatically access and manage key account-related data within the Marketplace Platform.

It provides secure endpoints that allow you to perform operations such as creating, updating, and retrieving information about accounts, users, user groups, licensees, sellers, and API tokens.&#x20;

Additionally, the API supports retrieving a list of available modules within the platform and managing ERP system links.

<a href="https://editor-next.swagger.io/?url=https://api.platform.softwareone.com/public/v1/accounts/openapi.json" class="button primary">Try API</a><a href="https://api.platform.softwareone.com/public/v1/accounts/openapi.json" class="button secondary">Download API</a>

## Core Concepts

The Accounts API is built around the following core resources:

* **Account** - Represents a client account, vendor account, or operations account.
* **Account user** - Represents an account user.
* **API token** -  Represents an authentication token object.&#x20;
* **Buyer** - Represents entities that engage in commercial activities and are the recipients of `invoices` issued by SoftwareOne.
* **Cloud tenant** - Represents a `cloudTenant` object in the Marketplace.
* **ERP link** - Represents a connection between the buyer object and the seller object in the Marketplace.
* **Licensee** - Represents entities that consume the software products or services procured by the `buyer`.
* **Module** -  Represents modules available in the platform, for example Marketplace.
* **Seller** - Represents SoftwareOne entities (for example, SoftwareOne Canada) that buy software solutions from vendors and sell those solutions to clients.
* **User** - Represents users who can sign in to the platform using their credentials and perform operations associated with their permissions.
* **User group** - Represents a `userGroup` object in the Marketplace.

## Collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.&#x20;

Refer to the following capability matrix to see which roles are authorized to perform specific operations within each collection:

### Accounts

<table><thead><tr><th width="237">Capability</th><th width="132">Public</th><th width="120">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List accounts</td><td>❌</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get a specific account</td><td>❌</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create account</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Update account details</td><td>❌</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Disable account</td><td>❌</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Enable account</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Activate account</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Validate account</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Deactivate account</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Get an account icon</td><td>✅</td><td>❌</td><td>❌</td><td>❌</td></tr><tr><td>Upload an icon</td><td>❌</td><td><strong>✅</strong></td><td>✅</td><td>✅</td></tr></tbody></table>

### Account Users <a href="#account-users-collection" id="account-users-collection"></a>

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List all account users</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get account user</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create account user</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Delete account user</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Accept user invitation</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Resend user account invitation</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Send new invitation</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Assign user to the user group</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update user to group assignment</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Remove user from the user group</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### API tokens

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List API tokens</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get API token</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create API token</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Delete API token</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update API token</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Disable API token</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Enable API token</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### Buyers

<table><thead><tr><th width="237">Capability</th><th width="132">Public</th><th width="120">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List buyers</td><td>❌</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Get a specific buyer</td><td>❌</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Create buyer</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Update buyer</td><td>❌</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Disable buyer</td><td>❌</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Enable buyer</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Validate buyer</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Delete buyer</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Deactivate buyer</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Synchronize buyer</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Buyer transfer</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Buyer transfer details</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Get buyer icon</td><td><strong>✅</strong></td><td>❌</td><td>❌</td><td>❌</td></tr><tr><td>Upload an icon</td><td>❌</td><td><strong>✅</strong></td><td><strong>✅</strong></td><td><strong>✅</strong></td></tr></tbody></table>

### Cloud tenants

<table><thead><tr><th width="251">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List cloud tenants</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Get cloud tenant</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Create cloud tenant</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Delete cloud tenant</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Update cloud tenant</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>

### Sellers

<table><thead><tr><th width="217">Capability</th><th width="132">Public</th><th width="120">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List sellers</td><td>❌</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Get seller</td><td>❌</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Create seller</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Update seller</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Activate seller</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Deactivate seller</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Disable seller</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Enable seller</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Delete seller</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Get seller icon</td><td><strong>✅</strong></td><td>❌</td><td>❌</td><td>❌</td></tr><tr><td>Upload an icon</td><td>❌</td><td>❌</td><td>❌</td><td><strong>✅</strong></td></tr></tbody></table>

### ERP Link <a href="#erp-link-collection" id="erp-link-collection"></a>

<table><thead><tr><th width="232">Capability</th><th width="132">Public</th><th width="120">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List ERP links</td><td>❌</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Get ERP link</td><td>❌</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Update ERP link</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Unblock ERP link</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Block ERP link</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Get an ERP link icon</td><td>✅</td><td>❌</td><td>❌</td><td>❌</td></tr><tr><td>Upload an icon</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>

### Licensees <a href="#licensees-collection" id="licensees-collection"></a>

<table><thead><tr><th width="232">Capability</th><th width="132">Public</th><th width="120">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List licensees</td><td>❌</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Get licensee</td><td>❌</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Create licensee</td><td>❌</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Update licensee</td><td>❌</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Disable licensee</td><td>❌</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Enable licensee</td><td>❌</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Delete licensee</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Get a licensee icon</td><td>✅</td><td>❌</td><td>❌</td><td>❌</td></tr><tr><td>Upload an icon</td><td>❌</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### Modules <a href="#modules-collection" id="modules-collection"></a>

<table><thead><tr><th width="333">Capability</th><th width="120">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List modules</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>

### [Users](users/) <a href="#users-collection" id="users-collection"></a>

<table><thead><tr><th width="335">Capability</th><th width="139">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List users</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get user</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Check SSO configuration for the user</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get the accounts collections for the user</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Update user</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Set user password</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Block user</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Unblock user</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>

### User Groups <a href="#user-groups-collection" id="user-groups-collection"></a>

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List all user groups</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get user group</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create user group</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update user group</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Delete user group</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>
