# Buyers

The Buyer object represents an individual buyer within the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th width="136">Field</th><th width="132">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The primary identifier for the buyer.</p><p>Example: BUY-1234-1234</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>A relative reference to the object in the API.</p><p>Example: /v1/accounts/buyers/BUY-1234-1234</p></td></tr><tr><td>status</td><td><code>string</code></td><td><p>The status of the buyer.</p><p>Possible values: <code>Enabled</code>, <code>Active</code>, <code>Disabled</code>, or <code>Deleted</code></p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The buyer's name.</p><p>Example: Stark Industries</p></td></tr><tr><td>icon</td><td><code>string</code></td><td><p>The relative path to the buyer’s logo.</p><p>Example: /static/accounts/BUY-1234-1234/logo.png</p></td></tr><tr><td>externalIds</td><td><a href="../../common-api-objects/externalids.md"><code>externalIds</code></a></td><td><p>The external identifier.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
 "erpCompanyContact": "WW-CON-123456",
 "erpCustomer": "WW-SCU-123456"
}
</code></pre></td></tr><tr><td>address</td><td><a href="../../common-api-objects/address.md"><code>address</code></a></td><td><p>The address of the buyer.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "addressLine1": "123 Main Street",
  "addressLine2": "Apt 4B",
  "postCode": "12345",
  "city": "Cityville",
  "state": "S",
  "country": "ST"
}
</code></pre></td></tr><tr><td>taxId</td><td><code>string</code></td><td><p>The buyer's tax ID.</p><p>Example: 12-34567890</p></td></tr><tr><td>account</td><td><a href="../account/#account-object"><code>account</code></a></td><td>A reference to the buyer’s account object.</td></tr><tr><td>sellers</td><td><a href="../seller/#seller-object"><code>seller</code></a></td><td>A reference to the seller object.</td></tr><tr><td>contact</td><td><code>object</code></td><td><p>The details of the contact person.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
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
</code></pre></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the Audit object.</td></tr></tbody></table>

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
