# Task API

The **Task API** provides a standardized way to manage and track long-running or background operations in the Marketplace Platform.&#x20;

A task represents an operation that may take some time, has progress, task logs, and a result. With this API, you can:&#x20;

* Create a new task, for example, to start a buyer transfer.
* Update progress, ETA, and parameters within a task. Only the owner service or extension can update a task.&#x20;
* Get task results, which may include a `JSON` result or redirect to a resource if the result is a file.&#x20;
* Transition the task status to `queued`, `processing`, `completed`, `rescheduled`, or `failed`.
* Get detailed logs containing additional information regarding task execution.

## Before you begin

Review the shared API docs before you work with task resources.

* [Authentication](https://docs.platform.softwareone.com/~/changes/476/developer-resources/api-reference)
* [URL structure](https://docs.platform.softwareone.com/~/changes/476/developer-resources/guides/url-structure)
* [Error handling](https://docs.platform.softwareone.com/~/changes/476/developer-resources/guides/errors-handling)

## Core resources

The Task API is built around the following core resources:

* **Task** – Represents the state of an asynchronous, usually long-running operation.&#x20;
* **Task log** – Represents additional information regarding the execution of the task.

## Browse collections

The API is organized into collections. Refer to the following capability matrix to see which roles are authorized to perform specific operations within each collection:

### Tasks

<table><thead><tr><th width="196">Operation</th><th width="105">Method</th><th width="214">Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="task/create-task.md">Create task</a></td><td>POST</td><td>Creates a task.</td><td>svc</td></tr><tr><td><a href="task/list-tasks.md">List tasks</a></td><td>GET</td><td>Gets a list of tasks.</td><td>ops, svc, vendor, client</td></tr><tr><td><a href="task/get-task.md">Get task by id</a></td><td>GET</td><td>Gets a task by id.</td><td>ops, svc, vendor, client</td></tr><tr><td><a href="task/get-task-result.md">Get task result</a></td><td>GET</td><td>Redirects to a platform resource or returns a result JSON value.</td><td>ops, svc, vendor, client</td></tr></tbody></table>

### Task log

<table><thead><tr><th width="141">Operation</th><th width="155">Method</th><th width="297">Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="task-log/get-task-logs.md">Get task logs</a></td><td>GET</td><td>Gets the log records for a task.</td><td>ops, svc</td></tr></tbody></table>
