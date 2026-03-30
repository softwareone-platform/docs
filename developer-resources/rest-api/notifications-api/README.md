---
description: Manage notifications, categories, and contacts with the Notifications API.
---

# Notifications API

The **Notifications API** allows you to manage and deliver notifications within the SoftwareOne Marketplace Platform. With this API, you can:

* Create and retrieve notification batches (emails) sent to specific categories and contacts. You can also retrieve attachments associated with those messages.
* Create and manage notification categories (such as, orders, subscriptions, and more).
* Create and manage contacts. Contacts are the recipients who receive notifications.
* Retrieve sent messages and delivery information.

<a href="https://editor-next.swagger.io/?url=https://api.platform.softwareone.com/public/v1/notifications/openapi.json" class="button primary">Try API</a><a href="https://api.platform.softwareone.com/public/v1/notifications/openapi.json" class="button secondary">Download API</a>

## Core Concepts

The Notifications API is built around the following core resources:

* **Batch** - Represents an email being sent to a specific category and multiple contacts.
* **Category** - Represents a logical grouping of notifications (for example, orders or subscriptions). Categories help organize and control notification types.
* **Contact** - Represents a contact who receives the notifications.
* **Message** - Represents an individual notification sent to a contact, including delivery details and status.
* **Subscriber** - Handles the configuration of notifications for accounts. It's the connection between an account and a notification category.

## Collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.

Refer to the following capability matrix to see which roles are authorized to perform specific operations within each collection:

### Batches

<table><thead><tr><th width="245">Capability</th><th width="152">Client</th><th width="165">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List batches</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Get batch</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Create batch</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Get batch attachment</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### Categories

<table><thead><tr><th width="225">Capability</th><th width="132">Contact</th><th width="120">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List categories</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get category</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create category</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Update category</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Publish category</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Unpublish category</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Delete category</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>

### Contacts

<table><thead><tr><th width="214">Capability</th><th width="132">Contact</th><th width="120">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List contacts </td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get contact</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create contact</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Update contact</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Block contact</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Unblock contact</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Delete contact</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>

### Footer

<table><thead><tr><th width="221">Capability</th><th width="152">Client</th><th width="148">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List footers</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Get footer</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Create footer</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Update footer</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Delete footer</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>

### Messages

<table><thead><tr><th width="221">Capability</th><th width="152">Client</th><th width="148">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List messages</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get message</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### Subscribers

<table><thead><tr><th width="268">Capability</th><th width="156">Client</th><th width="129">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List subscribers</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get subscriber</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Disable subscriber</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Enable subscriber</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update subscriber</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get contacts in account and category</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### Templates

<table><thead><tr><th width="274">Capability</th><th>Client</th><th>Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List templates</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Create template</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Get template</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Update template</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Delete template</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Activate template</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### Template Variant

<table><thead><tr><th width="274">Capability</th><th>Client</th><th>Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List template variant</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Create template variant</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Get template variant</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Update template variant</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Delete template variant</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>
