# Seller

The Seller object represents a seller in the Marketplace platform.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="166">Field</th><th width="154">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only)  Primary identifier for the seller.</td></tr><tr><td><code>status</code></td><td>string</td><td><p>The seller's status. Allowed values: </p><ul><li><code>Active</code></li><li><code>Disabled</code></li><li><code>Offline</code> </li><li><code>Deleted</code></li></ul></td></tr><tr><td><code>name</code></td><td>string, core</td><td>The name of the seller.</td></tr><tr><td><code>icon</code></td><td>string</td><td>(Optional) The relative path to the seller’s logo.</td></tr><tr><td><code>externalId</code></td><td>string, core</td><td>The external identifier.</td></tr><tr><td><code>address</code></td><td>object</td><td><p>The <a href="../../../api-usage-and-reference/common-api-objects/address.md"><code>address</code></a> of the seller.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "addressLine1": "123 Main Street",
  "addressLine2": "Apt 4B",
  "postCode": "12345",
  "city": "Cityville",
  "state": "S",
  "country": "ST"
}
</code></pre></td></tr><tr><td><code>currency</code></td><td>string</td><td>The currency of the seller.</td></tr><tr><td><code>buyers</code></td><td>object</td><td>Represents the <a href="../buyer/#buyer-object"><code>buyer</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Examples

{% tabs %}
{% tab title="MINIMAL EXAMPLE" %}
{% code title="SELLER OBJECT" lineNumbers="true" %}
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

{% tab title="COMPLETE EXAMPLE" %}
{% code title="THE SELLER OBJECT" lineNumbers="true" %}
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
