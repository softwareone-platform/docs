# Helpdesk API

The **Helpdesk API** is a REST API used by the Marketplace Platform that allows you to configure the Helpdesk framework. It enables you to:

* Create and manage support cases.
* Transition the case state to querying, processing, or completed.
* Create, retrieve, and manage feedback entries as well as attachments.
* Configure forms, parameters, and parameter groups to define what data is collected when someone raises a case/feedback.
* Use queues to manage how cases are routed.

## Core Concepts

The Helpdesk API is built around the following core resources:

* **Case** - Represents an interaction between Client, Vendor, or Operations users.
* **Chat** - Represents a conversation between parties in the Marketplace platform. These could be direct (1:1), group chats, or case discussions.
* **Feedback** - Represents feedback submitted by `client`, `vendor`, or `operations` users through the platform.&#x20;
* **Form** - Represents a configurable questionnaire used to collect onboarding information.
* **Queue** - Represents a logical grouping of cases that share similar business problems. Queues can be created for specific purposes, such as customer onboarding, billing issues, or any other business scenario deemed relevant by the operator.

## Collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.&#x20;

Refer to the following capability matrix to see which roles are authorized to perform specific operations within each collection:

### Cases

<table data-full-width="false"><thead><tr><th width="287">Capability</th><th>Client</th><th>Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List all cases</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get case</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create case</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update case</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Set case status to querying</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Set case status to processing</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Set case status to completed</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### Chat

<table data-full-width="false"><thead><tr><th width="287">Capability</th><th>Client</th><th>Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>Create chat</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>List all chats</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Get chat</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update chat</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>List chat participants</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get chat participant</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create participant</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update participant</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Leave chat</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>List chat messages</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create chat message</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update chat message</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Delete chat message</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>List chat attachments</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get chat attachment</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Add chat attachment</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update chat attachment</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Delete chat attachment</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>List links in a chat</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update chat link</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create chat link</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Delete chat link</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### Feedback

<table data-full-width="false"><thead><tr><th width="284">Capability</th><th>Client</th><th>Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List feedback</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get feedback by ID</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create feedback</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update feedback</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update status to reviewed</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Create feedback attachment</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>List attachments for feedback</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get attachment by ID for feedback</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update attachment by ID</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Delete feedback attachment</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Delete feedback</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### Forms

<table data-full-width="false"><thead><tr><th width="284">Capability</th><th>Client</th><th>Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List all forms</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get form</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create form</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update form</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Publish form</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Unpublish form</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Delete form</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### Queues

<table data-full-width="false"><thead><tr><th width="284">Capability</th><th>Client</th><th>Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List all queues</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get queue</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create queue</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update queue</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Activate queue</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Disable queue</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Delete queue</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### Parameter Definition

<table data-full-width="false"><thead><tr><th width="282">Capability</th><th>Client</th><th>Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List all parameters in helpdesk</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get parameter </td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create parameter definition</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update parameter definition</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Delete parameter definition</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### Parameter Groups

<table data-full-width="false"><thead><tr><th width="332">Capability</th><th width="160">Client</th><th width="140">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List all parameter groups defined in Helpdesk</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get parameter group</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create parameter group</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update parameter group</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Delete parameter group</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get all parameters within a parameter group</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get parameter within a parameter group</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Adds parameter to parameter group</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Updates a parameter’s display order within parameter group</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Remove parameter from parameter group</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>
