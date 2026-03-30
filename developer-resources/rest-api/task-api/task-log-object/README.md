# Task Log Object

The Task Log objects represent additional information regarding the execution of the task. Examples of such information include:

* The task has been started.
* The task has failed due to an issue.
* The task is currently processing a specific step, for example, the 3rd step out of 5.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="156">Field Name</th><th width="170">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The ID of the task log record. </p><p>Example: TLR-1930-6351-9137-5141</p></td></tr><tr><td><code>task</code></td><td>task</td><td><p>A reference to the task containing this log. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "TSK-5498-1544-6054-5440",
  "name": "Transferring the buyer to a different account",
  "code": "platform.accounts.buyers.transfer"
}
</code></pre></td></tr><tr><td><code>severity</code></td><td>string</td><td><p>The severity of the task log.</p><p>Example: Warning</p></td></tr><tr><td><code>message</code></td><td>string</td><td><p>Message template.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">Starting buyer '{{BuyerId}}' transfer to '{{TargetAccountId}}'.
</code></pre></td></tr><tr><td><code>timestamp</code></td><td>date</td><td><p>The time of the log record. </p><p>Example: 2025-09-11 13:40:13.515Z</p></td></tr><tr><td><code>progress</code></td><td>decimal</td><td><p>The task progress in percentage. </p><p>Example: 21.3</p></td></tr><tr><td><code>eta</code></td><td>string (ISO 8601 datetime)</td><td><p>The estimation of finishing for the task, if available.  </p><p>Example: 2025-09-12 13:40:13.515Z</p></td></tr><tr><td><code>parameters</code></td><td>object</td><td><p>Optional message parameters. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "BuyerId": "BUY-4230-6788",
    "TargetAccountId": "ACC-4952-6625"
}
</code></pre></td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% tabs %}
{% tab title="SHORT FORM" %}
{% code overflow="wrap" lineNumbers="true" %}
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

{% tab title="FULL FORM" %}
{% code lineNumbers="true" %}
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
