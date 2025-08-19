# ERP Links

The ERP Link represents a connection between a [Buyer](../buyer/) and a [Seller ](../../../../modules-and-features/settings/sellers/)object in the Marketplace. The ERP Link object contains the following properties:

<table data-full-width="false"><thead><tr><th width="199">Field</th><th width="162">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The primary identifier for the ERP link.</p><p>Example: ERP-1234-1234.</p></td></tr><tr><td>status</td><td><code>enum</code></td><td><p>The status of the object.</p><p>Possible values: <code>Active</code> or <code>Blocked</code></p></td></tr><tr><td>note</td><td><code>string</code></td><td></td></tr><tr><td>name</td><td><code>string</code></td><td><p>Represents the buyer and seller names.</p><p>Example: AGCO Corporation - SoftwareONE Argentina</p></td></tr><tr><td>externalIds</td><td>BuyerExternalIdsObject</td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
	"erpCompanyContact": "WW-CON-123456",
	"erpCustomer": "WW-SCU-123456",
	"erpCustomerDiscountGroup": "WW-12345"
}
</code></pre></td></tr><tr><td>address</td><td><a href="../../common-api-objects/address.md"><code>address</code></a></td><td>The address of the buyer in the given Seller instance. </td></tr><tr><td>companyName</td><td><code>string</code></td><td><p>The name of the Buyer in the given Seller instance.</p><p>Example: AGCO Corporation</p></td></tr><tr><td>buyer</td><td><a href="../buyer/"><code>buyer</code></a></td><td>A reference to the Buyer object.</td></tr><tr><td>seller</td><td><a href="../seller/"><code>seller</code></a></td><td>A reference to the Seller object.</td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td><p>A reference to the Audit object. </p><p>Possible values: <code>Created</code>, <code>Updated</code>, <code>Blocked</code>,  or <code>Unblocked</code>.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } },
  "blocked": { "at": "...", "by": { } },
  "unblocked": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="ERP LINK OBJECT" %}
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
{% endtab %}
{% endtabs %}
