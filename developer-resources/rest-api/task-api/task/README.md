# Task

A task represents the state of an asynchronous, usually long-running operation. Examples include, bulk migrations, transferring buyers, and more.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="155">Field</th><th width="161">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) Represents the task ID. The task identifier includes the identifier of the service that owns it. The format is TSK-XXXX-YYYY-YYYY-YYYY, where XXXX corresponds to part of the Service identifier SVC-XXXX. </td></tr><tr><td><code>status</code></td><td>enum, core</td><td>Represents the status of the task. A new task is created in either the <code>queued</code> (default) or <code>blocked</code> status.  </td></tr><tr><td><code>code</code></td><td>string, core</td><td>Represents a task code. Different task codes are responsible for different workflows, and are prefixed with the respective service namespace. </td></tr><tr><td><code>name</code></td><td>string, core</td><td><p>The name of the specific operation. </p><p>Example: Moving the buyer to a different account</p></td></tr><tr><td><code>queue</code></td><td>string</td><td>The queue name for the task execution, sourced by the task service, is prefixed with the controlling service namespace. Queues are independent in scope of execution; tasks in the queue are executed in First In, First Out order if <code>queued</code>. </td></tr><tr><td><code>object</code></td><td>object</td><td><p>A reference to the business object related to the task.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "ORD-1234-1245-1234"
}
</code></pre></td></tr><tr><td><code>description</code></td><td>string</td><td>A description of the task. </td></tr><tr><td><code>parent</code></td><td>task</td><td><p>(Optional) Represents the parent task, if applicable. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
   "id": "TSK-1234-1234-1234-1234",
   "name": "Parent task name"
}
</code></pre></td></tr><tr><td><code>progress</code></td><td>float</td><td>(Optional) The progress in percentage, ranging from 0 to 100. Applies only to tasks that have started.</td></tr><tr><td><code>eta</code></td><td>string</td><td>The estimated completion time for the task, if applicable, in the ISO 8601 datetime format.</td></tr><tr><td><code>audit</code></td><td>object</td><td>Represents the <a href="https://docs.platform.softwareone.com/~/changes/348/developer-resources/rest-api/common-api-objects/audit"><code>audit</code></a> object.</td></tr><tr><td><code>parameters</code></td><td>object</td><td><p>(Optional) Parameters that can be used to store task-specific metadata. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "param1": {...},
  "param2": {...}
}
</code></pre></td></tr><tr><td><code>result</code></td><td>string</td><td><p>(Optional) The URI, which reflects the results of the task execution. It could be either:</p><ul><li>A task-specific result object.</li><li>A relative URI to the resource, for example, a standard platform object or file.</li></ul></td></tr><tr><td><code>owner</code></td><td>service</td><td><p>The service that owns the task. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
   "id": "SVC-1234",
   "name": "Service A"
}
</code></pre></td></tr><tr><td><code>access</code></td><td>object</td><td>A list of <a href="../../accounts-api/account/"><code>account</code></a> with access to the task and its result. </td></tr></tbody></table>

## Examples

{% tabs %}
{% tab title="MINIMAL EXAMPLE" %}
{% code title="THE TASK OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
    "id": "TSK-0001-2474-4798-1266",
    "name": "Transferring the buyer to a different account",
    "revision": 1,
    "status": "Completed",
    "code": "accounts.buyers.transfer",
    "queue": "marketplace/platform/internal/buyers/commands",
    "object": {
        "id": "BUY-1190-0394"
    },
    "description": "Transferring buyer 'BUY-1190-0394' to account 'ACC-5563-4382'",
    "progress": 100,
    "parameters": {
        "BuyerId": "BUY-1190-0394",
        "TargetAccountId": "ACC-5563-4382"
    },
    "result": "/public/v1/accounts/buyers/BUY-1190-0394",
    "owner": {
        "id": "SVC-0001",
        "name": "platform",
        "revision": 1
    }
}
```
{% endcode %}
{% endtab %}

{% tab title="COMPLETE EXAMPLE" %}
{% code title="TASK OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
    "id": "TSK-0001-2474-4798-1266",
    "name": "Transferring the buyer to a different account",
    "revision": 1,
    "status": "Completed",
    "code": "accounts.buyers.transfer",
    "queue": "marketplace/platform/internal/buyers/commands",
    "object": {
        "id": "BUY-1190-0394"
    },
    "description": "Transferring buyer 'BUY-1190-0394' to account 'ACC-5563-4382'",
    "progress": 100,
    "parameters": {
        "BuyerId": "BUY-1190-0394",
        "TargetAccountId": "ACC-5563-4382"
    },
    "result": "/public/v1/accounts/buyers/BUY-1190-0394",
    "owner": {
        "id": "SVC-0001",
        "name": "platform",
        "revision": 1
    },
    "access": [
        {
            "id": "ACC-0000-0001",
            "name": "SoftwareONE (Backoffice)",
            "revision": 1,
            "type": "Operations",
            "status": "Active"
        }
    ],
    "audit": {
        "started": {
            "at": "2025-09-04T09:03:09.702Z",
            "by": {
                "id": "SVC-0001",
                "name": "platform",
                "revision": 1
            }
        },
        "completed": {
            "at": "2025-09-04T09:03:20.668Z",
            "by": {
                "id": "SVC-0001",
                "name": "platform",
                "revision": 1
            }
        },
        "created": {
            "at": "2025-09-04T09:03:08.790Z",
            "by": {
                "id": "SVC-0001",
                "name": "platform",
                "revision": 1
            }
        },
        "updated": {
            "at": "2025-09-04T09:03:20.669Z",
            "by": {
                "id": "SVC-0001",
                "name": "platform",
                "revision": 1
            }
        }
    }
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
