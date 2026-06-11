# Task Log

The Task Log objects represent additional information regarding the execution of the task. Examples of such information include:

* The task has been started.
* The task has failed due to an issue.
* The task is currently processing a specific step, for example, the 3rd step out of 5.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="140">Field</th><th width="154">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The ID of the task log record. </td></tr><tr><td><code>task</code></td><td>task, core</td><td><p>A reference to the task containing this log. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "TSK-5498-1544-6054-5440",
  "name": "Transferring the buyer to a different account",
  "code": "platform.accounts.buyers.transfer"
}
</code></pre></td></tr><tr><td><code>severity</code></td><td>string</td><td>The severity of the task log.</td></tr><tr><td><code>message</code></td><td>string</td><td>Message template.</td></tr><tr><td><code>timestamp</code></td><td>date</td><td>The time of the log record. </td></tr><tr><td><code>progress</code></td><td>decimal</td><td>The task progress in percentage. </td></tr><tr><td><code>eta</code></td><td>string</td><td>(Optional) The estimated task completion time, if available (ISO‑8601 datetime).</td></tr><tr><td><code>parameters</code></td><td>object</td><td><p>(Optional) Message parameters. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "BuyerId": "BUY-4230-6788",
    "TargetAccountId": "ACC-4952-6625"
}
</code></pre></td></tr></tbody></table>

## Examples

{% tabs %}
{% tab title="MINIMAL EXAMPLE" %}
{% code title="THE TASK LOG OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
    "id": "TLR-1930-6351-9137-5141",
    "revision": 1,
    "task": {
        "id": "TSK-5498-1544-6054-5440",
        "name": "Transferring the buyer to a different account",
        "revision": 1,
        "status": "Completed",
        "code": "accounts.buyers.transfer"
    },
    "progress": 0,
    "eta": "2025-09-12 13:40:13.515Z",
    "severity": "Info",
    "message": "Starting buyer '{{BuyerId}}' transfer to '{{TargetAccountId}}'.",
    "timestamp": "2025-09-11T13:40:13.515Z",
    "parameters": {
        "BuyerId": "BUY-4230-6788",
        "TargetAccountId": "ACC-4952-6625"
    }
}
```
{% endcode %}
{% endtab %}

{% tab title="COMPLETE EXAMPLE" %}
{% code title="TASK LOG OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
    "id": "TLR-1930-6351-9137-5141",
    "revision": 1,
    "task": {
        "id": "TSK-5498-1544-6054-5440",
        "name": "Transferring the buyer to a different account",
        "revision": 1,
        "status": "Completed",
        "code": "accounts.buyers.transfer"
    },
    "progress": 0,
    "eta": "2025-09-12 13:40:13.515Z",
    "severity": "Info",
    "message": "Starting buyer '{{BuyerId}}' transfer to '{{TargetAccountId}}'.",
    "timestamp": "2025-09-11T13:40:13.515Z",
    "parameters": {
        "BuyerId": "BUY-4230-6788",
        "TargetAccountId": "ACC-4952-6625"
    },
    "audit": {
        "created": {
            "at": "2025-09-11T13:40:13.655Z",
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
