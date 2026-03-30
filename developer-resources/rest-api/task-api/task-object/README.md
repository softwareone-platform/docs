# Task Object

A task represents the state of an asynchronous, usually long-running operation. Examples include, bulk migrations, transferring buyers, and more.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="155">Field Name</th><th width="148">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>Represents the task ID.</p><p>The task identifier includes the identifier of the service that owns it. The format is TSK-XXXX-YYYY-YYYY-YYYY, where XXXX corresponds to part of the Service identifier SVC-XXXX. </p><p>Example: TSK-0001-1234-1234-1234</p></td></tr><tr><td><code>status</code></td><td>enum</td><td>Represents the status of the task. A new task is created in either the <code>queued</code> (default) or <code>blocked</code> status.  </td></tr><tr><td><code>code</code></td><td>string</td><td><p>Represents a task code. Different task codes are responsible for different workflows, and are prefixed with the respective service namespace. </p><p>Example: platform.accounts.buyers.transfer</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the specific operation. </p><p>Example: Moving the buyer to a different account</p></td></tr><tr><td><code>queue</code></td><td>string</td><td><p>The queue name for the task execution, sourced by the task service, is prefixed with the controlling service namespace. Queues are independent in scope of execution; tasks in the queue are executed in First In, First Out order if <code>queued</code>. </p><p>Example: marketplace/platform/internal/buyers/commands</p></td></tr><tr><td><code>object</code></td><td>object</td><td><p>A reference to the business object related to the task.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "ORD-1234-1245-1234"
}
</code></pre></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the task. </p><p>Example: Moving buyer BUY-1234-1234 to account ACC-1234-1234, including 20 agreements.</p></td></tr><tr><td><code>parent</code></td><td>task</td><td><p>A reference to the parent task, if applicable. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
   "id": "TSK-1234-1234-1234-1234",
   "name": "Parent task name"
}
</code></pre></td></tr><tr><td><code>progress</code></td><td>float</td><td><p>The progress in percentage, ranging from 0 to 100. For tasks that have not yet started, the progress is not defined.</p><p>Example: 21.3</p></td></tr><tr><td><code>eta</code></td><td>string (ISO 8601 datetime)</td><td><p>The estimated completion time for the task, if applicable.</p><p>Example: 2020-12-09T16:09:53.012Z</p></td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="https://docs.platform.softwareone.com/~/changes/348/developer-resources/rest-api/common-api-objects/audit"><code>audit</code></a> object.</td></tr><tr><td><code>parameters</code></td><td> object</td><td><p>Optional parameters that can be used to store task-specific metadata. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "param1": {...},
  "param2": {...}
}
</code></pre></td></tr><tr><td><code>result</code></td><td>string</td><td><p>The URI, which reflects the results of the task execution. It could be either:</p><ul><li>A task-specific result object.</li><li>A relative URI to the resource, for example, a standard platform object or file.</li></ul><p>Example: /public/v1/system/tasks/TSK-1234-1234-1234/result</p></td></tr><tr><td><code>owner</code></td><td>service</td><td><p>The service that owns the task. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
   "id": "SVC-1234",
   "name": "Service A"
}
</code></pre></td></tr><tr><td><code>access</code></td><td><a href="../../accounts-api/account/">account</a></td><td><p>A list of <a href="../../accounts-api/account/"><code>account</code></a> with access to the task and its result. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  { "id": "ACC-1234-1234" },
  ...
]
</code></pre></td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% tabs %}
{% tab title="SHORT FORM" %}
{% code overflow="wrap" lineNumbers="true" %}
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

{% tab title="FULL EXAMPLE" %}
{% code lineNumbers="true" %}
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
