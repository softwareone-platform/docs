# Task API

The **Task API** provides a standardized way to manage and track long-running or background operations in the Marketplace Platform.&#x20;

A task represents an operation that may take some time, has progress, task logs, and a result. With this API, you can:&#x20;

* Create a new task, for example, to start a buyer transfer.
* Update progress, ETA, and parameters within a task. Only the owner service or extension can update a task.&#x20;
* Get task results, which may include a `JSON` result or redirect to a resource if the result is a file.&#x20;
* Transition the task status to `queued`, `processing`, `completed`, `rescheduled`, or `failed`.
* Get detailed logs containing additional information regarding task execution.

## Core Concepts

The Task API is built around the following core resources:

* **Task** - Represents the state of an asynchronous, usually long-running operation.&#x20;
* **Task log** - Represents additional information regarding the execution of the task.

## Collections

The API is organized into collections. Refer to the following capability matrix to see which roles are authorized to perform specific operations within each collection:

### Tasks

<table><thead><tr><th width="202">Capability</th><th width="132">Service</th><th width="120">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List tasks</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get a specific task</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create task</td><td>✅</td><td>❌</td><td>❌</td><td>❌</td></tr><tr><td>Get a task result</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### Task log

<table><thead><tr><th width="203">Capability</th><th width="132">Services</th><th width="120">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List tasks</td><td>✅</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>
