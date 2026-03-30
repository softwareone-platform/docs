# Buyer

The Buyer object represents an individual buyer in the Marketplace Platform.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="136">Field Name</th><th width="132">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary identifier for the buyer.</p><p>Example: BUY-1234-1234</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>A relative reference to the object in the API.</p><p>Example: /v1/accounts/buyers/BUY-1234-1234</p></td></tr><tr><td><code>status</code></td><td>string</td><td>The status of the buyer. Possible values are <code>enabled</code>, <code>active</code>, <code>disabled</code>, or <code>deleted</code>.</td></tr><tr><td><code>name</code></td><td>string</td><td><p>The buyer's name.</p><p>Example: Stark Industries</p></td></tr><tr><td><code>icon</code></td><td>string</td><td><p>The relative path to the buyer’s logo.</p><p>Example: /static/accounts/BUY-1234-1234/logo.png</p></td></tr><tr><td><code>externalIds</code></td><td>object</td><td><p>The <a href="../../common-api-objects/externalids.md">externalIds</a>.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
 "erpCompanyContact": "WW-CON-123456",
 "erpCustomer": "WW-SCU-123456"
}
</code></pre></td></tr><tr><td><code>address</code></td><td>object</td><td><p>The <a href="../../common-api-objects/address.md">address</a> of the buyer.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "addressLine1": "123 Main Street",
  "addressLine2": "Apt 4B",
  "postCode": "12345",
  "city": "Cityville",
  "state": "S",
  "country": "ST"
}
</code></pre></td></tr><tr><td><code>taxId</code></td><td>string</td><td><p>The buyer's tax ID.</p><p>Example: 12-34567890</p></td></tr><tr><td><code>account</code></td><td>object</td><td>A reference to the buyer’s <a href="../account/#account-object"><code>account</code></a> object.</td></tr><tr><td><code>sellers</code></td><td>object</td><td>A reference to the <a href="../seller/#seller-object"><code>seller</code></a> object.</td></tr><tr><td><code>contact</code></td><td>object</td><td><p>The details of the contact person.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "name": "Will Smith",
  "firstName": "Will",
  "lastName": "Smith",
  "email": "will.smith@adastraflex.com",
  "phone": null,
  "user": {
    "id":   "USR-0000-0001",
    "icon": null,
    "name": "Will Smith"
  }
}

</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Example response

{% tabs %}
{% tab title="SHORT FORM" %}
{% code overflow="wrap" lineNumbers="true" %}
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
