# Custom Ledger

The Custom Ledger object is required to submit billing information for clients with manual billing activated. Only SoftwareOne Operations can access this object.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="168">Field</th><th width="164">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The unique identifier. No nesting exists for this identifier.</td></tr><tr><td><code>name</code></td><td>string, core</td><td>The name of the custom ledger.</td></tr><tr><td><code>externalIds</code></td><td><a href="../../../api-usage-and-reference/common-api-objects/externalids.md">externalIds</a>, core</td><td>(Optional) The external IDs for vendors and operations.</td></tr><tr><td><code>seller</code></td><td>object</td><td>(Read-only) Represents the <a href="../../accounts-api/seller/"><code>seller</code></a> object.</td></tr><tr><td><code>vendor</code></td><td>object</td><td>(Read-only) Represents the vendor <a href="../../accounts-api/account/"><code>account</code></a> object.</td></tr><tr><td><code>billingStartDate</code></td><td>dateTime, core</td><td>The billing start date.</td></tr><tr><td><code>billingEndDate</code></td><td>dateTime, core</td><td>The billing end date.</td></tr><tr><td><code>notes</code></td><td>string</td><td>(Optional) Notes related to the custom ledger.</td></tr><tr><td><code>status</code></td><td>enum</td><td><p>The status of the ledger. Allowed values are: </p><ul><li><code>Draft</code></li><li><code>Deleted</code></li><li><code>Validating</code></li><li><code>Validated</code></li><li><code>Error</code></li><li><code>Generating</code></li><li> <code>Queued</code></li><li><code>Completed</code></li></ul></td></tr><tr><td><code>assignee</code></td><td>object</td><td>(Optional) Represents the <a href="../../accounts-api/users/"><code>user</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>price</code></td><td>object</td><td>(Read-only) The custom ledger <a href="../journal/#pricesummary"><code>priceSummary</code></a> including the aggregated price values for all charges.</td></tr><tr><td><code>processing</code></td><td>object</td><td>(Read-only) The custom ledger <a href="../journal/#processingsummary"><code>processingSummary</code></a> including the total charges and counts of ready, error, split, cancelled, and completed charges.</td></tr><tr><td><code>error</code></td><td>object</td><td>Represents the <code>billingEntityError</code> object containing error details associated with the custom ledger entry, if any.</td></tr></tbody></table>

## Example

{% code title="CUSTOM LEDGER OBJECT" lineNumbers="true" %}
```json
{
    "id": "CLE-6666-0422",
    "name": "Test 3",
    "externalIds": {},
    "seller": {
        "id": "SEL-4970-1115",
        "externalId": "CH",
        "address": {
            "country": "CH"
        },
        "name": "SoftwareONE Switzerland",
        "icon": "/v1/accounts/sellers/SEL-4970-1115/icon"
    },
    "vendor": {
        "id": "ACC-9226-9856",
        "type": "Vendor",
        "status": "Active",
        "name": "Adobe"
    },
    "billingStartDate": "2025-05-15T22:00:00.000Z",
    "billingEndDate": "2025-05-15T22:00:00.000Z",
    "status": "Completed",
    "price": {
        "currency": {
            "purchase": "EUR",
            "sale": "EUR",
            "rate": 1.0000000000
        },
        "markup": 8.7083671812,
        "margin": 8.0107607234,
        "totalPP": 5170.20000,
        "totalSP": 5620.44000
    },
    "processing": {
        "total": 3,
        "ready": 3,
        "error": 0,
        "split": 0,
        "skipped": 0
    },
    "audit": {
        "draft": {
            "at": "2025-05-16T12:59:40.112Z",
            "by": {
                "id": "USR-0000-0043",
                "name": "Marc Serrat",
                "icon": "/v1/accounts/users/USR-0000-0043/icon"
            }
        },
        "deleted": {},
        "validating": {
            "at": "2025-05-16T12:59:49.507Z",
            "by": {
                "id": "USR-0000-0043",
                "name": "Marc Serrat",
                "icon": "/v1/accounts/users/USR-0000-0043/icon"
            }
        },
        "validated": {
            "at": "2025-05-16T12:59:52.560Z",
            "by": {
                "id": "USR-0000-0000",
                "name": "System"
            }
        },
        "error": {},
        "generating": {
            "at": "2025-05-16T12:59:59.976Z",
            "by": {
                "id": "USR-0000-0043",
                "name": "Marc Serrat",
                "icon": "/v1/accounts/users/USR-0000-0043/icon"
            }
        },
        "generated": {
            "at": "2025-05-16T13:00:02.131Z",
            "by": {
                "id": "USR-0000-0000",
                "name": "System"
            }
        },
        "queued": {
            "at": "2025-05-16T13:00:15.103Z",
            "by": {
                "id": "USR-0000-0043",
                "name": "Marc Serrat",
                "icon": "/v1/accounts/users/USR-0000-0043/icon"
            }
        },
        "completed": {
            "at": "2025-05-16T13:04:15.596Z",
            "by": {
                "id": "TKN-0291-1452",
                "name": "Marc Serrat",
                "icon": ""
            }
        },
        "created": {
            "at": "2025-05-16T12:59:40.112Z",
            "by": {
                "id": "USR-0000-0043",
                "name": "Marc Serrat",
                "icon": "/v1/accounts/users/USR-0000-0043/icon"
            }
        },
        "updated": {
            "at": "2025-05-16T13:04:15.596Z",
            "by": {
                "id": "TKN-0291-1452",
                "name": "Marc Serrat",
                "icon": ""
            }
        }
    }
}
```
{% endcode %}



[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
