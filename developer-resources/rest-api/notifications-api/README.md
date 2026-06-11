---
description: Manage notifications, categories, and contacts with the Notifications API.
---

# Notifications API

The **Notifications API** allows you to manage and deliver notifications within the SoftwareOne Marketplace Platform. With this API, you can:

* Create and retrieve notification batches (emails) sent to specific categories and contacts. You can also retrieve attachments associated with those messages.
* Create and manage notification categories (such as orders, subscriptions, and more).
* Create and manage contacts. Contacts are the recipients who receive notifications.
* Retrieve sent messages and delivery information.

## Before you start

Review the shared API docs before you work with notifications resources.

* [Authentication](../)
* [URL structure](../../api-usage-and-reference/url-structure.md)
* [Error handling](../../api-usage-and-reference/errors-handling.md)

## Core concepts

The Notifications API is built around the following core resources:

* **Batch** – Represents an email being sent to a specific category and multiple contacts.
* **Category** – Represents a logical grouping of notifications (for example, orders or subscriptions). Categories help organize and control notification types.
* **Contact** – Represents a contact who receives the notifications.
* **Message** – Represents an individual notification sent to a contact, including delivery details and status.
* **Subscriber** – Handles the configuration of notifications for accounts. It's the connection between an account and a notification category.

## Browse collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.

Use the following links to jump to the collection you need:

* [Batches](./#batches)
* [Categories](./#categories)
* [Contacts](./#contacts)
* [Footer](./#footer)
* [Message](./#message)
* [Subscriber](./#subscriber)
* [Template](./#template)
* [Template Variant](./#template-variant)

### Batches

<details>

<summary>View Batches operations</summary>

| Operation                                               | Method | Description              | Access              |
| ------------------------------------------------------- | ------ | ------------------------ | ------------------- |
| [Create batch](batches/create-batch.md)                 | POST   | Creates a new batch.     | vendor, ops         |
| [List batches](batches/list-batches.md)                 | GET    | Gets a list of batches.  | vendor, ops         |
| [Get batch by id](batches/get-batch.md)                 | GET    | Gets batch details.      | vendor, ops         |
| [Get batch attachment](batches/get-batch-attachment.md) | GET    | Gets a batch attachment. | vendor, client, ops |

</details>

### Categories

<details>

<summary>View Categories operations</summary>

| Operation                                              | Method | Description                             | Access                       |
| ------------------------------------------------------ | ------ | --------------------------------------- | ---------------------------- |
| [Create category](categories/create-category.md)       | POST   | Creates a new notification category.    | ops                          |
| [List categories](categories/list-categories.md)       | GET    | Gets a list of notification categories. | vendor, client, ops, contact |
| [Get category by id](categories/get-category.md)       | GET    | Gets notification category details.     | vendor, client, ops, contact |
| [Update category](categories/update-category.md)       | PUT    | Updates a notification category.        | ops                          |
| [Delete category](categories/delete-category.md)       | DELETE | Deletes a notification category.        | ops                          |
| [Publish category](categories/publish-category.md)     | POST   | Publishes a notification category.      | ops                          |
| [Unpublish category](categories/unpublish-category.md) | POST   | Unpublishes a notification category.    | ops                          |

</details>

### Contacts

<details>

<summary>View Contacts operations</summary>

| Operation                                      | Method | Description              | Access                       |
| ---------------------------------------------- | ------ | ------------------------ | ---------------------------- |
| [Create contact](contacts/create-contact.md)   | POST   | Creates a new contact.   | ops                          |
| [List contacts](contacts/list-contacts.md)     | GET    | Gets a list of contacts. | vendor, client, ops, contact |
| [Get contact by id](contacts/get-contact.md)   | GET    | Gets contact details.    | vendor, client, ops, contact |
| [Update contact](contacts/update-contact.md)   | PUT    | Updates a contact.       | vendor, client, ops, contact |
| [Delete contact](contacts/delete-contact.md)   | DELETE | Deletes a contact.       | ops                          |
| [Block contact](contacts/block-contact.md)     | POST   | Blocks a contact.        | ops                          |
| [Unblock contact](contacts/unblock-contact.md) | POST   | Unblocks a contact.      | ops                          |

</details>

### Footer

<details>

<summary>View Footer operations</summary>

| Capability                               | Method | Description                                       | Access |
| ---------------------------------------- | ------ | ------------------------------------------------- | ------ |
| [Create footer](footer/create-footer.md) | POST   | Creates a new footer.                             | ops    |
| [Get footer](footer/get-footer.md)       | GET    | Retrieves a footer by id.                         | ops    |
| [List footer](footer/list-footers.md)    | GET    | Retrieves all footers.                            | ops    |
| [Update footer](footer/update-footer.md) | PUT    | Updates the footer content or sets it as default. | ops    |
| [Delete footer](footer/delete-footer.md) | DELETE | Permanently removes the footer.                   | ops    |

</details>

### Message

<details>

<summary>View Message operations</summary>

| Capability                                 | Method | Description             | Access              |
| ------------------------------------------ | ------ | ----------------------- | ------------------- |
| [List messages](messages/list-messages.md) | GET    | Retrieves all messages. | vendor, client, ops |
| [Get message](messages/get-message.md)     | GET    | Get a message by id.    | vendor, client, ops |

</details>

### Subscriber

<details>

<summary>View Subscriber operations</summary>

| Operation                                                                                       | Method | Description                                                                              | Access              |
| ----------------------------------------------------------------------------------------------- | ------ | ---------------------------------------------------------------------------------------- | ------------------- |
| [List subscribers](subscribers/list-subscribers.md)                                             | GET    | Gets a list of subscribers.                                                              | vendor, client, ops |
| [Get subscriber by id](subscribers/get-subscriber.md)                                           | GET    | Gets subscriber details.                                                                 | vendor, client, ops |
| [Update subscriber](subscribers/update-subscriber.md)                                           | PUT    | Modifies recipients of a given configuration.                                            | vendor, client, ops |
| [Disable subscriber](subscribers/disable-subscriber.md)                                         | POST   | Disables the category for the account.                                                   | vendor, client, ops |
| [Enable subscriber](subscribers/enable-subscriber.md)                                           | POST   | Enables the category for the account.                                                    | vendor, client, ops |
| [Get contacts in account and category](subscribers/get-contacts-within-account-and-category.md) | GET    | Returns contacts configured to receive notifications for the given account and category. | vendor, ops         |

</details>

### Template

<details>

<summary>View Template operations</summary>

| Capability                                         | Method | Description                                                             | Access      |
| -------------------------------------------------- | ------ | ----------------------------------------------------------------------- | ----------- |
| [List templates](template/list-templates.md)       | GET    | Gets a list of template.                                                | vendor, ops |
| [Create template](template/create-template.md)     | POST   | Creates a new template.                                                 | vendor, ops |
| [Get template](template/get-template.md)           | GET    | Gets template details.                                                  | vendor, ops |
| [Update template](template/update-template.md)     | PUT    | Updates template properties. Only speciic fields can be modified.       | vendor, ops |
| [Delete template](template/delete-template.md)     | DELETE | Permanently removes the template and all its language variants          | vendor, ops |
| [Activate template](template/activate-template.md) | POST   | Activates the template, making it available for sending notifications.  | vendor, ops |

</details>

### Template variant

<details>

<summary>View Template Variant operations</summary>

| Capability              | Method | Description                                                                                            | Access      |
| ----------------------- | ------ | ------------------------------------------------------------------------------------------------------ | ----------- |
| List template variant   | GET    | Gets a list of template variants                                                                       | vendor, ops |
| Create template variant | POST   | Adds a new language variant to the template with subject and body content for the specified language.  | vendor, ops |
| Get template variant    | GET    | Gets a template variant.                                                                               | vendor, ops |
| Update template variant | PUT    | Updates the subject and/or body content of the language variant. Only specific fields can be modified. | vendor, ops |
| Delete template variant | DELETE | Permanently removes the language variant from the template.                                            | vendor, ops |

</details>
