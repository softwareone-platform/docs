# Cloud Tenant

Cloud Tenant represents a cloud tenant object in the Marketplace Platform.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false" data-search="false"><thead><tr><th width="159">Field</th><th width="162">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The primary identifier for the cloud tenant.</td></tr><tr><td><code>name</code></td><td>string, core</td><td>The name of the cloud tenant. </td></tr><tr><td><code>status</code></td><td>string</td><td><p>The status of the cloud tenant. Allowed values: </p><ul><li><code>Active</code></li><li><code>Disabled</code></li><li><code>Deleted</code></li></ul></td></tr><tr><td><code>account</code></td><td>object</td><td>The <a href="../account/"><code>account</code></a> to which the cloud tenant is assigned.</td></tr><tr><td><code>type</code></td><td>string</td><td>(Read-only) The type of cloud tenant. </td></tr><tr><td><code>externalId</code></td><td>object</td><td>(Read-only) Represents the <a href="./#cloud-tenant-external-ids"><code>CloudTenantExternalIDs</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Cloud Tenant External IDs object <a href="#cloud-tenant-external-ids" id="cloud-tenant-external-ids"></a>

<table data-full-width="false"><thead><tr><th width="213">Field</th><th width="125">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>pyraTenantId</code></td><td>string</td><td>(Read-only) The PYC tenant ID. </td></tr><tr><td><code>cloudConsumptionId</code></td><td>string</td><td>(Read-only) The unique identifier of this cloud tenant in PYC.</td></tr><tr><td><code>providerId</code></td><td>string</td><td>(Read-only) The object identifier within the cloud provider, like AWS, Azure, and more. </td></tr></tbody></table>

## Example

{% code title="CLOUD TENANT OBJECT" lineNumbers="true" %}
```json
{
    "id": "CLT-3206-7146",   
    "account": {
        "id": "ACC-2253-2884",      
        "type": "Client",
        "status": "Active",
        "name": "AdAstrafleX"
    },
    "externalIds": {
        "cloudConsumptionId": "012b2a18-1df0-473f-8759-c3c019b54486",
        "providerId": "7270638c-ca21-4500-ac82-25dca634566a",
        "pyraTenantId": "c6469e97-302a-408a-8589-2122a0bb725d"
    },
    "name": "AdAstraflex Germany",
    "status": "Active",
    "type": "CspAzure",
    "audit": {
        "created": {
            "at": "2024-12-12T11:17:44.042Z",
            "by": {
                "id": "TKN-9299-7556",              
                "name": "Migration token"
            }
        }
    }
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
