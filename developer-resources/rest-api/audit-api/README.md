---
description: Use the Audit API to track and retrieve activity logs programmatically.
---

# Audit API

The **Audit API** enables you to track and retrieve activity logs across the Marketplace Platform, so you have full visibility into key actions taken by users or systems.

Use this API to create audit records, list logged events for monitoring or compliance, and retrieve details for specific events.

## Before you start

Review the shared API docs before you work with audit resources.

* [Authentication](../)
* [URL structure](../../api-usage-and-reference/url-structure.md)
* [Error handling](../../api-usage-and-reference/errors-handling.md)

## Core resources

The Audit API is built around the following core resources:

* **Audit record** – Represents a detailed record of an event that took place within the platform.
* **Audit event types** – Represents the event types used within the platform.

## Browse collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.

See the following sections to determine which roles are authorized to perform specific operations within each collection:

### Audit Records

| Operation                                                    | Method | Description                             | Access              |
| ------------------------------------------------------------ | ------ | --------------------------------------- | ------------------- |
| [Create audit record](audit-record-1/create-audit-record.md) | POST   | Creates an audit record.                | vendor, client, ops |
| [List audit records](audit-record-1/list-audit-records.md)   | GET    | Retrieves the audit records collection. | vendor, client, ops |
| [Get audit record](audit-record-1/get-audit-records.md)      | GET    | Retrieves an audit record by ID.        | vendor, ops         |

### Audit Event Types

| Operation                                                            | Method | Description                                        | Access              |
| -------------------------------------------------------------------- | ------ | -------------------------------------------------- | ------------------- |
| [List audit event types](audit-event-type/list-audit-event-types.md) | GET    | Retrieves the list of all known audit event types. | vendor, client, ops |
