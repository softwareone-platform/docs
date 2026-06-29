# Buyer

The Buyer object represents an individual buyer in the SoftwareOne Marketplace. Buyers are the recipients of invoices issued by SoftwareOne, and are essential for placing orders, creating agreements, and ordering subscriptions.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="145">Field</th><th width="163">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The primary identifier for the buyer.</td></tr><tr><td><code>status</code></td><td>string</td><td><p>The buyer's status. Allowed values: </p><ul><li><code>Enabled</code></li><li><code>Active</code></li><li><code>Disabled</code></li><li><code>Deleted</code></li></ul></td></tr><tr><td><code>name</code></td><td>string, core</td><td>The buyer's name.</td></tr><tr><td><code>icon</code></td><td>string</td><td>(Optional) The relative path to the buyer’s logo.</td></tr><tr><td><code>externalIds</code></td><td>object</td><td>(Optional) Represents the <a href="../../../api-usage-and-reference/common-api-objects/externalids.md"><code>externalIds</code></a> object.</td></tr><tr><td><code>address</code></td><td>object</td><td>(Optional) Represents the <a href="../../../api-usage-and-reference/common-api-objects/address.md"><code>address</code></a> object containing the buyer's address.</td></tr><tr><td><code>taxId</code></td><td>string</td><td>(Optional) The buyer's tax ID.</td></tr><tr><td><code>account</code></td><td>object</td><td>Represents the buyer’s <a href="../account/#account-object"><code>account</code></a> object.</td></tr><tr><td><code>sellers</code></td><td>object</td><td>Represents the <a href="../seller/#seller-object"><code>seller</code></a> object.</td></tr><tr><td><code>contact</code></td><td>object</td><td>Represents the <a href="../../notifications-api/contacts/"><code>contact</code></a> object, which contains details of the contact person.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Examples

{% tabs %}
{% tab title="MINIMAL EXAMPLE" %}
{% code title="BUYER OBJECT" overflow="wrap" lineNumbers="true" %}
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

{% tab title="COMPLETE EXAMPLE" %}
{% code title="BUYER OBJECT" lineNumbers="true" %}
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
