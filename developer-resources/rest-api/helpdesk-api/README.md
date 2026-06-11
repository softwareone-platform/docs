# Helpdesk API

The **Helpdesk API** is a REST API used by the Marketplace Platform that allows you to configure the Helpdesk framework. It enables you to:

* Create and manage support cases.
* Transition the case state to querying, processing, or completed.
* Create, retrieve, and manage feedback entries and attachments.
* Configure forms, parameters, and parameter groups to define what data is collected when someone raises a case/feedback.
* Use queues to manage how cases are routed.

## Before you start <a href="#before-you-start" id="before-you-start"></a>

Review the shared API docs before you work with helpdesk resources.

* [Authentication](../#authentication)
* [URL structure](../../api-usage-and-reference/url-structure.md)
* [Error handling](../../api-usage-and-reference/errors-handling.md)

## Core resources

The Helpdesk API is built around the following core resources:

* **Case** - Represents an interaction between Client, Vendor, or Operations users.
* **Chat** - Represents a conversation between parties in the Marketplace platform. These could be direct (1:1), group chats, or case discussions.
* **Feedback** - Represents feedback submitted by `client`, `vendor`, or `operations` users through the platform.&#x20;
* **Form** - Represents a configurable questionnaire used to collect onboarding information.
* **Queue** - Represents a logical grouping of cases that share similar business problems. Queues can be created for specific purposes, such as customer onboarding, billing issues, or any other business scenario deemed relevant by the operator.

## Browse collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.

Use the following links to jump to the collection you need:

* [Case](./#case)
* [Chat](./#chat)
* [Feedback](./#feedback)
* [Form](./#form)
* [Parameter Definition](./#parameter-definition)
* [Parameter Group](./#parameter-group)
* [Queue ](./#queue)

### Case

<details>

<summary>View Case operations</summary>

| Operation                              | Method | Description                                 | Access              |
| -------------------------------------- | ------ | ------------------------------------------- | ------------------- |
| [Create case](case/create-case.md)     | POST   | Creates a new support case.                 | vendor, client, ops |
| [Complete case](case/complete-case.md) | POST   | Sets a support case to _Completed_ status.  | vendor, client, ops |
| [Process case](case/process-case.md)   | POST   | Sets a support case to _Processing_ status. | vendor, client, ops |
| [Query case](case/query-case.md)       | POST   | Sets a support case to _Querying_ status.   | vendor, client, ops |
| [List cases](case/list-cases.md)       | GET    | Gets a list of support cases.               | vendor, client, ops |
| [Get case by id](case/get-case.md)     | GET    | Gets a support case by id.                  | vendor, client, ops |
| [Update case](case/update-case.md)     | PUT    | Updates an existing support case.           | vendor, client, ops |

</details>

### Chat

<details>

<summary>View Chat operations</summary>

| Operation                                                  | Method | Description                                                                       | Access              |
| ---------------------------------------------------------- | ------ | --------------------------------------------------------------------------------- | ------------------- |
| [Create chat](chat/create-chat.md)                         | POST   | Creates a new chat with an icon using multipart form data.                        | vendor, client, ops |
| [List chats](chat/list-chats.md)                           | GET    | Gets a list of chats with support for filtering, sorting, and pagination.         | ops                 |
| [Get chat by id](chat/get-chat.md)                         | GET    | Retrieves a chat by id; supports selecting specific fields.                       | vendor, client, ops |
| [Update chat](chat/update-chat.md)                         | PUT    | Updates an existing chat and allows replacing its icon using multipart form data. | vendor, client, ops |
| [Add chat participants](chat/add-chat-participants.md)     | POST   | Adds new chat participants.                                                       | vendor, client, ops |
| [List chat participants](chat/list-chat-participants.md)   | GET    | Gets a list of chat participants.                                                 | vendor, client, ops |
| [Get chat participant by id](chat/get-chat-participant.md) | GET    | Gets a chat participant.                                                          | vendor, client, ops |
| [Update chat participant](chat/update-chat-participant.md) | PUT    | Updates an existing chat participant.                                             | vendor, client, ops |
| [Remove chat participant](chat/remove-chat-participant.md) | DELETE | Removes a participant from the chat.                                              | vendor, client, ops |
| [Add chat attachments](chat/add-chat-attachment.md)        | POST   | Adds attachments to an existing chat.                                             | vendor, client, ops |
| [Update chat attachment](chat/update-chat-attachment.md)   | PUT    | Updates chat attachment data.                                                     | vendor, client, ops |
| [Delete chat attachment](chat/delete-chat-attachment.md)   | DELETE | Deletes a chat attachment by id.                                                  | vendor, client, ops |
| [Create chat link](chat/create-chat-link.md)               | POST   | Creates a new link.                                                               | vendor, client, ops |
| [List chat links](chat/list-chat-links.md)                 | GET    | Gets a list of chat links.                                                        | vendor, client, ops |
| [Update chat link](chat/update-chat-link.md)               | PUT    | Updates a chat link.                                                              | vendor, client, ops |
| [Delete chat link](chat/delete-chat-link.md)               | DELETE | Deletes a chat link by id.                                                        | vendor, client, ops |

</details>

### Feedback

<details>

<summary>View Feedback operations</summary>

| Operation                                                            | Method | Description                                                                   | Access              |
| -------------------------------------------------------------------- | ------ | ----------------------------------------------------------------------------- | ------------------- |
| [Create feedback](feedback/create-feedback.md)                       | POST   | Creates a new feedback entry with attachments using multipart form data.      | vendor, client, ops |
| [List feedback](feedback/list-feedback.md)                           | GET    | Gets a list of feedback entries; supports filtering, sorting, and pagination. | vendor, client, ops |
| [Get feedback by id](feedback/get-feedback.md)                       | GET    | Retrieves a feedback entry by id; supports selecting specific fields.         | vendor, client, ops |
| [Update feedback](feedback/update-feedback.md)                       | PUT    | Updates an existing feedback entry.                                           | vendor, client, ops |
| [Delete feedback](feedback/delete-feedback.md)                       | DELETE | Deletes a feedback entry by id.                                               | vendor, client, ops |
| [Review feedback](feedback/review-feedback.md)                       | POST   | Marks a feedback entry as reviewed.                                           | ops                 |
| [Add feedback attachment](feedback/add-feedback-attachment.md)       | POST   | Adds attachments to an existing feedback.                                     | vendor, client, ops |
| [List feedback attachments](feedback/list-feedback-attachments.md)   | GET    | Gets attachments for a feedback entry.                                        | vendor, client, ops |
| [Get feedback attachment](feedback/get-feedback-attachment.md)       | GET    | Gets a feedback attachment by id.                                             | vendor, client, ops |
| [Delete feedback attachment](feedback/delete-feedback-attachment.md) | POST   | Deletes a feedback attachment by id.                                          | vendor, client, ops |

</details>

### Form

<details>

<summary>View Form operations</summary>

| Operation                                | Method | Description               | Access              |
| ---------------------------------------- | ------ | ------------------------- | ------------------- |
| [Create form](form/create-form.md)       | POST   | Creates a new form.       | vendor, client, ops |
| [List forms](form/list-forms.md)         | GET    | Gets a list of forms.     | vendor, client, ops |
| [Get form by id](form/get-form.md)       | GET    | Retrieves a form by id.   | vendor, client, ops |
| [Update form](form/update-form.md)       | PUT    | Updates an existing form. | vendor, client, ops |
| [Delete form](form/delete-form.md)       | DELETE | Deletes a form by id.     | vendor, client, ops |
| [Publish form](form/publish-form.md)     | POST   | Publishes a form.         | vendor, client, ops |
| [Unpublish form](form/unpublish-form.md) | POST   | Unpublishes a form.       | vendor, client, ops |

</details>

### Parameter Definition

<details>

<summary>View Parameter Definition operations</summary>

| Operation                                                                          | Method | Description                               | Access              |
| ---------------------------------------------------------------------------------- | ------ | ----------------------------------------- | ------------------- |
| [Create parameter definition](parameter-definition/create-parameter-definition.md) | POST   | Creates a new parameter definition.       | client, vendor, ops |
| [List parameters definition](parameter-definition/list-parameter-definition.md)    | GET    | Gets a list of parameter definitions.     | client, vendor, ops |
| [Get parameter definition by id](parameter-definition/get-parameter-definition.md) | GET    | Retrieves a parameter definition by id.   | client, vendor, ops |
| [Update parameter definition](parameter-definition/update-parameter-definition.md) | PUT    | Updates an existing parameter definition. | client, vendor, ops |
| [Delete parameter definition](parameter-definition/delete-parameter-definition.md) | DELETE | Deletes an existing parameter definition. | client, vendor, ops |

</details>

### Parameter Group

<details>

<summary>View Parameter Group operations</summary>

<table><thead><tr><th>Operation</th><th width="118">Method</th><th>Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="parameter-group/create-parameter-group.md">Create parameter group</a></td><td>POST</td><td>Creates a new parameter group from the request payload.</td><td>client, vendor, ops</td></tr><tr><td><a href="parameter-group/list-parameter-group.md">List parameter groups</a></td><td>GET</td><td>Gets a list of parameter groups.</td><td>client, vendor, ops</td></tr><tr><td><a href="parameter-group/get-parameter-group.md">Get parameter group by id</a></td><td>GET</td><td>Retrieves a parameter group by id.</td><td>client, vendor, ops</td></tr><tr><td><a href="parameter-group/update-parameter-group.md">Update parameter group</a></td><td>PUT</td><td>Updates an existing parameter group.</td><td>client, vendor, ops</td></tr><tr><td><a href="parameter-group/delete-parameter-group.md">Delete parameter group</a></td><td>DELETE</td><td>Deletes an existing parameter group by id.</td><td>client, vendor, ops</td></tr><tr><td><a href="parameter-group/add-parameter-to-group.md">Add parameter to group</a></td><td>POST</td><td>Adds a parameter to a parameter group.</td><td>client, vendor, ops</td></tr><tr><td><a href="parameter-group/list-parameters-in-a-parameter-group.md">List group parameters</a></td><td>GET</td><td>Lists parameters in a parameter group.</td><td>client, vendor, ops</td></tr><tr><td><a href="parameter-group/get-parameter-in-a-parameter-group.md">Get parameter in a parameter group</a></td><td>GET</td><td>Retrieves a parameter within a parameter group by id.</td><td>client, vendor, ops</td></tr><tr><td><a href="parameter-group/update-parameter-in-group.md">Update parameter in group</a></td><td>PUT</td><td>Updates a parameter’s display order within a group.</td><td>client, vendor, ops</td></tr><tr><td><a href="parameter-group/remove-parameter-from-group.md">Remove parameter from group</a></td><td>DELETE</td><td>Removes a parameter from a parameter group.</td><td>client, vendor, ops</td></tr></tbody></table>

</details>

### Queue

<details>

<summary>View Queue operations</summary>

| Operation                                 | Method | Description                        | Access              |
| ----------------------------------------- | ------ | ---------------------------------- | ------------------- |
| [Create queue](queue/create-queue.md)     | POST   | Creates a new queue.               | vendor, client, ops |
| [List queues](queue/list-queues.md)       | GET    | Gets a list of queues.             | vendor, client, ops |
| [Get queue by id](queue/get-queue.md)     | GET    | Retrieves a queue by id.           | vendor, client, ops |
| [Update queue](queue/update-queue.md)     | PUT    | Updates an existing queue.         | vendor, client, ops |
| [Delete queue](queue/delete-queue.md)     | DELETE | Deletes an existing queue by id.   | vendor, client, ops |
| [Activate queue](queue/activate-queue.md) | POST   | Sets the queue status to active.   | vendor, client, ops |
| [Disable queue](queue/disable-queue.md)   | POST   | Sets the queue status to disabled. | vendor, client, ops |

</details>
