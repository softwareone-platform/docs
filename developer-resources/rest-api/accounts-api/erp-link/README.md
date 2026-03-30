# ERP Link

The ERP Link represents a connection between a [Buyer](../buyer/) and a [Seller ](../../../../modules-and-features/settings/sellers/)object in the Marketplace.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="144">Field Name</th><th width="123">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary identifier for the ERP link.</p><p>Example: ERP-1234-1234.</p></td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the object. The allowed values are <code>active</code> or <code>blocked</code>.</td></tr><tr><td><code>note</code></td><td>string</td><td></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The names of the buyer and seller.</p><p>Example: AGCO Corporation - SoftwareOne Argentina</p></td></tr><tr><td><code>externalIds</code></td><td>object</td><td><p>A reference to the <code>buyerExternalIdsObject</code>.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
	"erpCompanyContact": "WW-CON-123456",
	"erpCustomer": "WW-SCU-123456",
	"erpCustomerDiscountGroup": "WW-12345"
}
</code></pre></td></tr><tr><td><code>address</code></td><td>object</td><td>The <a href="../../common-api-objects/address.md"><code>address</code></a> of the buyer in the given seller instance. </td></tr><tr><td><code>companyName</code></td><td>string</td><td><p>The name of the buyer in the given seller instance.</p><p>Example: AGCO Corporation</p></td></tr><tr><td><code>buyer</code></td><td>object</td><td>A reference to the <a href="../buyer/"><code>buyer</code></a> object.</td></tr><tr><td><code>seller</code></td><td>object</td><td>A reference to the <a href="../seller/"><code>seller</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. Allowed values: <code>created</code>, <code>updated</code>, <code>blocked</code>, or <code>unblocked</code>.</td></tr></tbody></table>

## Example response

{% code lineNumbers="true" %}
```json
{
	"id": "ERP-0808-7934-2576",
	"buyer": {
		"id": "BUY-0808-7934",		
		"name": "AGCO Corporation"
	},
	"seller": {
		"id": "SEL-1968-2576",		
		"externalId": "AR",
		"name": "SoftwareONE Argentina",
		"icon": "/v1/accounts/sellers/SEL-1968-2576/icon"
	},
	"name": "AGCO Corporation - SoftwareONE Argentina",
	"status": "Active",
	"externalIds": {
		"erpCompanyContact": "US-CON-183485",
		"erpCustomer": "US-SCU-117126",
		"accountExternalId": "WW-100502"
	},
	"address": {
		"addressLine1": "4205 River Green Pkwy",
		"postCode": "30096",
		"city": "DULUTH",
		"state": "GA",
		"country": "US"
	},
    "companyName": "AGCO Corporation",
	"audit": {
		"created": {
			"at": "2025-01-21T12:27:31.716Z",
			"by": {
				"id": "TKN-4113-7170",			
				"name": "[DO NOT REMOVE] Navision Extension"
			}
		},
		"updated": {
			"at": "2025-03-10T12:45:04.479Z",
			"by": {
				"id": "TKN-8915-3154",				
				"name": "Jakub Parteka Token"
			}
		}
	}
}
```
{% endcode %}
