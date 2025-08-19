# Cloud Tenants

A Cloud Tenant represents a cloud tenant object in the Marketplace Platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th width="186">Field</th><th width="149">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The primary identifier for the cloud tenant.</p><p>Example: CLT-1234-9876</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the cloud tenant. </p><p>Example: AdAstraflex</p></td></tr><tr><td>status</td><td><code>string</code></td><td><p>The status of the cloud tenant.  </p><p>Possible values: <code>Active</code>, <code>Disabled</code>, or <code>Deleted</code></p></td></tr><tr><td>account</td><td><a href="../account/"><code>account</code></a></td><td>The account to which the cloud tenant is assigned.</td></tr><tr><td>type</td><td><code>string</code></td><td><p>The type of cloud tenant. </p><p>Example: Csp365</p></td></tr><tr><td>externalId</td><td><code>object</code></td><td>A reference to <a href="./#cloud-tenant-external-ids">Cloud Tenant External IDs</a>.</td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the Audit object. </td></tr></tbody></table>

## Cloud Tenant External IDs <a href="#cloud-tenant-external-ids" id="cloud-tenant-external-ids"></a>

<table data-full-width="false"><thead><tr><th width="191">Field</th><th width="113">Type</th><th>Description</th></tr></thead><tbody><tr><td>pyraTenantId</td><td><code>string</code></td><td><p>Indicates the PYC tenant ID. </p><p>Example: ce4b61dd-9426-4b4a-855f-6162f790a457</p></td></tr><tr><td>cloudConsumptionId</td><td><code>string</code></td><td><p>Indicates the unique identifier of this cloud tenant in PYC.</p><p>Example: f94c03b5-c2ee-478a-964c-bfb591a7a205</p></td></tr><tr><td>providerId</td><td><code>string</code></td><td><p>Indicates the object identifier within the cloud provider, like AWS, Azure, and more. </p><p>Example: de14dafc-9323-40ed-bdbd-cbf32311d59e</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="CLOUD TENANT OBJECT" %}
{% code lineNumbers="true" %}
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
{% endtab %}
{% endtabs %}
