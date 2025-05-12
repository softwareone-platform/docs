# Buyer

The Buyer object represents an individual buyer within the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th width="136">Field</th><th width="132">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>Primary buyer identifier.</p><p>Example: BUY-1234-1234</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>Relative reference to the object in the API.</p><p>Example: /v1/accounts/buyers/BUY-1234-1234</p></td></tr><tr><td>status</td><td><code>string</code></td><td>Status: Enabled, Active, Disabled, Deleted</td></tr><tr><td>name</td><td><code>string</code></td><td><p>Buyer's name.</p><p>Example: Stark Industries</p></td></tr><tr><td>icon</td><td><code>string</code></td><td><p>Relative path to buyer’s logo.</p><p>Example: /static/accounts/BUY-1234-1234/logo.png</p></td></tr><tr><td>externalIds</td><td><code>BuyerExternalIdsObject</code></td><td><p>External identifier.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
 "erpCompanyContact": "WW-CON-123456",
 "erpCustomer": "WW-SCU-123456"
}
</code></pre></td></tr><tr><td>address</td><td><code>object</code></td><td><p>Address of the buyer.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
  "addressLine1": "123 Main Street",
  "addressLine2": "Apt 4B",
  "postCode": "12345",
  "city": "Cityville",
  "state": "S",
  "country": "ST"
}
</code></pre></td></tr><tr><td>taxId</td><td><code>string</code></td><td><p>Buyer's tax ID.</p><p>Example: 12-34567890</p></td></tr><tr><td>account</td><td><a href="../account/#account-object"><code>Account</code></a></td><td>Buyer’s account object.</td></tr><tr><td>sellers</td><td><a href="../seller/#seller-object"><code>Seller</code></a></td><td>Seller object.</td></tr><tr><td>contact</td><td><code>object</code></td><td><p>Contact person details.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
	"name": "Will Smith",
	"firstName": "Will",
	"lastName": "Smith",
	"email": "will.smith@adastraflex.com",
	"phone": null,
	"user": {
		"id": "USR-0000-0001",
		"icon": null,
		"name": "Will Smith"
	}
}
</code></pre></td></tr><tr><td>audit</td><td><code>object</code></td><td><p>Possible audit events: Created, Updated, Disabled, Enabled, Activated.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } },
  "disabled": { "at": "...", "by": { } },
  "enabled": { "at": "...", "by": { } },
  "activated": { "at": "...", "by": { } },
  "deleted": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="SHORT FORM" %}
{% code lineNumbers="true" %}
```json
{
	"id": "BUY-3911-2313",
	"contact": {
		"name": "Will Smith",
		"firstName": "Will",
		"lastName": "Smith",
		"email": "will.smith@adastraflex.com",
		"phone": null
	},
	"externalIds": {
		"erpCompanyContact": "WW-CON-123456",
		"erpCustomer": "WW-SCU-123456"
    },
	"status": "Active",
	"icon": null,
	"address": {
		"addressLine1": "PO Box 31",
		"addressLine2": "Victory Road",
		"postCode": "DE24 8BJ",
		"city": "Derby",
		"state": "Derbs",
		"country": "UK"
	},
	"taxId": "VAT1",
	"name": "Stark Industries"
}
```
{% endcode %}
{% endtab %}

{% tab title="FULL EXAMPLE" %}
{% code lineNumbers="true" %}
```json
{
	"id": "BUY-3911-2313",
	"contact": {
		"name": "Will Smith",
		"firstName": "Will",
		"lastName": "Smith",
		"email": "will.smith@adastraflex.com",
		"phone": null,
		"user": {
			"id": "USR-0000-0001",
			"icon": null,
			"invited": "2024-02-03T11:34:15.381Z",
			"joined": "2024-02-04T12:34:15.381Z",
			"lastLogin": "2024-02-05T13:34:15.381Z",
			"name": "Will Smith"
		}
	},
    "externalIds": {
		"erpCompanyContact": "WW-CON-123456",
		"erpCustomer": "WW-SCU-123456"
    },
	"status": "Active",
	"icon": null,
	"address": {
		"addressLine1": "PO Box 31",
		"addressLine2": "Victory Road",
		"postCode": "DE24 8BJ",
		"city": "Derby",
		"state": "Derbs",
		"country": "UK"
	},
	"taxId": "VAT1",
	"account": {
		"id": "ACC-5563-4382",
		"type": "Client",
		"status": "Active",
		"icon": null,
		"name": "AdAstraflexx"
	},
	"name": "Stark Industries",
	"sellers": [
		{
			"id": "SEL-1299-2079",
			"externalId": "SWO_CH",
			"name": "SoftwareOne AG"
		}
	],
	"audit": {
		"created": {
			"at": "2023-12-14T13:44:20.896Z",
			"by": {
				"id": "USR-0000-0001",
				"icon": null,
				"invited": "2024-02-03T11:34:15.383Z",
				"joined": "2024-02-04T12:34:15.383Z",
				"lastLogin": null,
				"name": "Will Smith"
			}
		},
		"updated": {
			"at": "2024-01-06T19:04:16.692Z",
			"by": {
				"id": "USR-0000-0001",
				"icon": null,
				"invited": "2024-02-03T11:34:15.383Z",
				"joined": "2024-02-04T12:34:15.383Z",
				"lastLogin": null,
				"name": "Will Smith"
			}
		}
	}
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
