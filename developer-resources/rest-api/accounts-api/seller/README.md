# Sellers

The Seller object represents a seller in the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th width="135">Field</th><th width="112">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The primary seller identifier.</p><p>Example: SEL-1234-1234</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>The relative reference to the object in the API.</p><p>Example: /v1/accounts/sellers/SEL-1234-1234</p></td></tr><tr><td>status</td><td><code>string</code></td><td>The seller's status. Possible values are <code>Active</code>, <code>Disabled</code>, <code>Offline</code> , or <code>Deleted</code>.</td></tr><tr><td>name</td><td><code>string</code></td><td><p>The seller's name.</p><p>Example: SoftwareOne USA</p></td></tr><tr><td>icon</td><td><code>string</code></td><td><p>The relative path to the seller’s logo.</p><p>Example: /static/accounts/SEL-1234-1234/logo.png</p></td></tr><tr><td>externalId</td><td><code>string</code></td><td><p>The external identifier.</p><p>Example: WW-CON-123456</p></td></tr><tr><td>address</td><td><a href="../../common-api-objects/address.md"><code>address</code></a></td><td><p>The address of the seller.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "addressLine1": "123 Main Street",
  "addressLine2": "Apt 4B",
  "postCode": "12345",
  "city": "Cityville",
  "state": "S",
  "country": "ST"
}
</code></pre></td></tr><tr><td>currency</td><td><code>string</code></td><td>The seller's currency.</td></tr><tr><td>buyers</td><td><a href="../buyer/#buyer-object"><code>buyer</code></a></td><td>A reference to the Buyer object.</td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the Audit object.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="SHORT FORM" %}
{% code lineNumbers="true" %}
```json
{
	"id": "SEL-7295-4834",
	"externalId": "SWO_CH",
	"status": "Active",
	"icon": null,
	"currency": "USD",
	"address": {
		"addressLine1": "Some street",
		"addressLine2": null,
		"postCode": "P0S C0D3",
		"city": "Some city",
		"state": "SS",
		"country": "CH"
	},
	"name": "SoftwareOne AG"
}
```
{% endcode %}
{% endtab %}

{% tab title="FULL EXAMPLE" %}
{% code lineNumbers="true" %}
```json
{
	"id": "SEL-7295-4834",
	"externalId": "SWO_CH",
	"status": "Active",
	"icon": null,
	"currency": "USD",
	"address": {
		"addressLine1": "Some street",
		"addressLine2": null,
		"postCode": "P0S C0D3",
		"city": "Some city",
		"state": "SS",
		"country": "CH"
	},
	"name": "SoftwareOne AG",
	"buyers": [
		{
			"id": "BUY-2321-7707",
			"name": "My first buyer"
		}
	],
	"audit": {
		"created": {
			"at": "2023-12-14T14:19:13.410Z",
			"by": {
				"id": "USR-0000-0001",
				"icon": null,
				"invited": "2024-02-03T11:59:55.933Z",
				"joined": "2024-02-04T12:59:55.933Z",
				"lastLogin": null,
				"name": "Will Smith"
			}
		},
		"updated": {
			"at": "2024-01-24T09:33:09.073Z",
			"by": {
				"id": "USR-0000-0001",
				"icon": null,
				"invited": "2024-02-03T11:59:55.933Z",
				"joined": "2024-02-04T12:59:55.933Z",
				"lastLogin": "2024-02-05T13:59:55.933Z",
				"name": "Will Smith"
			}
		}
	}
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
