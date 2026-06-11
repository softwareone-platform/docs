# Override

The Override object marks the clients as eligible for manual billing, bypassing automated billing.&#x20;

Assigning this object indicates that the client's billing requires flexibility and will be handled manually.&#x20;Only SoftwareOne Operations can see overrides.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="160">Field</th><th width="141">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) Unique identifier for the object. No nesting exists for this identifier. </td></tr><tr><td><code>client</code></td><td>object</td><td>(Read-only) Represents the client <a href="../../accounts-api/account/"><code>account</code></a> object. </td></tr><tr><td><code>vendor</code></td><td>object</td><td>(Read-only) Represents the vendor <a href="../../accounts-api/account/"><code>account</code></a> object. </td></tr><tr><td><code>status</code></td><td>enum</td><td>(Read-only) The override's status. Allowed values are <code>active</code> or <code>disabled</code>. </td></tr><tr><td><code>externalId</code></td><td>string, core</td><td>(Optional) The external identifier or reference number.</td></tr><tr><td><code>notes</code></td><td>string</td><td>(Optional) Notes associated with the override.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>



## Example

{% code title="OVERRIDE OBJECT" overflow="wrap" lineNumbers="true" expandable="true" %}
```json
{
    "id": "BOV-1345-6362",
    "client": {
        "id": "ACC-5563-4382",
        "type": "Client",
        "status": "Active",
        "name": "Adastraflex 2.0"
    },
    "vendor": {
        "id": "ACC-5500-0684",
        "type": "Vendor",
        "status": "Enabled",
        "name": "amando software"
    },
    "status": "Active",
    "externalId": "",
    "notes": "",
    "audit": {
        "active": {
          "at": "2025-04-16T17:48:19.726Z"
        },
        "disabled": {},
        "created": {
            "at": "2025-04-16T17:48:19.726Z"
        },
        "updated": {}
    }
}
```
{% endcode %}



[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
