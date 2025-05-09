# Licensee

The Licensee object represents a licensee in the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th width="210">Field</th><th width="100">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Primary licensee identifier. </p><p></p><p>Example: LCE-1234-1234-1234</p></td></tr><tr><td>href</td><td>string</td><td><p>Relative reference to the object in the API. </p><p></p><p>Example: /v1/accounts/licensees/LIC-1234-1234-1234"</p></td></tr><tr><td>status</td><td>string</td><td>Status of the licensee, such as Enabled, Active, Disabled, or Deleted.</td></tr><tr><td>name</td><td>string</td><td><p>Licensee's name. </p><p></p><p>Example: Stark Industries Finance Dept</p></td></tr><tr><td>icon</td><td>string</td><td><p>Relative path to licensee’s logo. </p><p></p><p>Example: /static/accounts/LIC-1234-1234-1234/logo.png</p></td></tr><tr><td>externalId</td><td>string</td><td><p>External identifier.</p><p></p><p>Example: WW-CON-12345678</p></td></tr><tr><td>useBuyerAddress</td><td>boolean</td><td><p>Defines whether the address should be copied from the buyer. </p><p></p><p>Example: true</p></td></tr><tr><td>address</td><td>object</td><td><p>Address of the licensee.</p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "addressLine1": "123 Main Street",
  "addressLine2": "Apt 4B",
  "postCode": "12345",
  "city": "Cityville",
  "state": "S",
  "country": "ST"
}
</code></pre></td></tr><tr><td>description</td><td>string</td><td>Description of the licensee.</td></tr><tr><td>contact</td><td>object</td><td><p>Contact person details. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
	"name": "Will Smith",
	"firstName": "Will",
	"lastName": "Smith",
	"email": "will.smith@adastraflex.com",
	"phone": null,
	"user": {
		"id": "USR-0000-0001",
		"href": "/users/USR-0000-0001",
		"icon": null,
		"name": "Will Smith"
	}
}
</code></pre></td></tr><tr><td>buyer</td><td><a href="../buyer/#buyer-object">Buyer</a></td><td>Reference to the Buyer object.</td></tr><tr><td>seller</td><td><a href="../seller/#seller-object">Seller</a></td><td>Reference to the Seller object.</td></tr><tr><td>account</td><td><a href="../account/#account-object">Account</a></td><td>Reference to the Account object.</td></tr><tr><td>audit</td><td>object</td><td><p>Possible audit events: Created, Updated, Activated, Disabled, Deactivated, or Deleted. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
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
	"id": "LCE-8893-6916-0000",
	"href": "/accounts/licensees/LCE-8893-6916-0000",
	"contact": null,
	"name": "Stark Industries",
	"externalId": null,
	"status": "Active",
	"address": null,
	"useBuyerAddress": false,
	"icon": null,
	"description": null
}
```
{% endcode %}
{% endtab %}

{% tab title="FULL EXAMPLE" %}
{% code lineNumbers="true" %}
```json
{
	"id": "LCE-8893-6916-0000",
	"href": "/accounts/licensees/LCE-8893-6916-0000",
	"contact": null,
	"name": "Stark Industries",
	"externalId": null,
	"status": "Active",
	"address": null,
	"useBuyerAddress": false,
	"icon": null,
	"description": null,
	"account": {
		"id": "ACC-5563-4382",
		"href": "/accounts/accounts/ACC-5563-4382",
		"type": "Client",
		"status": "Active",
		"icon": null,
		"name": "AdAstraflexx"
	},
	"buyer": {
		"id": "BUY-8928-0965",
		"href": "/accounts/buyers/BUY-8928-0965",
		"name": "Stark Industries"
	},
	"seller": {
		"id": "SEL-4717-3953",
		"href": "/accounts/sellers/SEL-4717-3953",
		"externalId": "SWO_CA",
		"name": "SoftwareOne Canada, Inc."
	}
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
