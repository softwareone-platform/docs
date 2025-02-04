# Seller

## Seller Object

The `seller` object represents a seller in the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th width="162">Field</th><th width="100">Type</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p>Primary seller identifier. </p><p></p><p>Example: "SEL-1234-1234"</p></td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td><p>Relative reference to object on API. </p><p></p><p>Example: "/v1/accounts/sellers/SEL-1234-1234"</p></td></tr><tr><td><strong><code>status</code></strong></td><td>string</td><td>Status: Active , Disabled, Offline , Deleted</td></tr><tr><td><strong><code>name</code></strong></td><td>string</td><td><p>Seller's name. </p><p></p><p>Example: "SoftwareOne USA"</p></td></tr><tr><td><strong><code>icon</code></strong></td><td>string</td><td><p>Relative path to seller’s logo. </p><p></p><p>Example: "/static/accounts/SEL-1234-1234/logo.png"</p></td></tr><tr><td><strong><code>externalId</code></strong></td><td>string</td><td><p>External identifier. </p><p></p><p>Example: "WW-CON-123456"</p></td></tr><tr><td><strong><code>address</code></strong></td><td>object</td><td><p>Address of the seller. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "addressLine1": "123 Main Street",
  "addressLine2": "Apt 4B",
  "postCode": "12345",
  "city": "Cityville",
  "state": "S",
  "country": "ST"
}
</code></pre></td></tr><tr><td><strong><code>currency</code></strong></td><td>string</td><td></td></tr><tr><td><strong><code>buyers</code></strong></td><td><a href="../buyer/#buyer-object">Buyer</a></td><td></td></tr><tr><td><strong><code>audit</code></strong></td><td>object</td><td><p>Possible audit events: Created, Updated, Activated, Disabled, Deactivated, or Deleted</p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } },
  "activated": { "at": "...", "by": { } },
  "disabled": { "at": "...", "by": { } },
  "deactivated": { "at": "...", "by": { } },
  "deleted": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="SHORT FORM" %}
{% code lineNumbers="true" %}
```json
{
	"id": "SEL-7295-4834",
	"href": "/accounts/sellers/SEL-7295-4834",
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
	"href": "/accounts/sellers/SEL-7295-4834",
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
			"href": "/accounts/buyers/BUY-2321-7707",
			"name": "My first buyer"
		}
	],
	"audit": {
		"created": {
			"at": "2023-12-14T14:19:13.410Z",
			"by": {
				"id": "USR-0000-0001",
				"href": "/users/USR-0000-0001",
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
				"href": "/users/USR-0000-0001",
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
