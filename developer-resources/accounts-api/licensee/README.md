# Licensee

## Licensee Object

The `licensee` object represents a licensee in the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th>Field</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p>Primary licensee identifier. </p><p></p><p>Example: "LCE-1234-1234-1234"</p></td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td><p>Relative reference to object on API. </p><p></p><p>Example: "/v1/accounts/licensees/LIC-1234-1234-1234"</p></td></tr><tr><td><strong><code>status</code></strong></td><td>string</td><td><p>Status: Enabled </p><p>Active, Disabled, Deleted</p></td></tr><tr><td><strong><code>name</code></strong></td><td>string</td><td><p>Licensee's name. </p><p></p><p>Example: "Stark Industries Finance Dept"</p></td></tr><tr><td><strong><code>icon</code></strong></td><td>string</td><td><p>Relative path to licensee’s logo. </p><p></p><p>Example: "/static/accounts/LIC-1234-1234-1234/logo.png"</p></td></tr><tr><td><strong><code>externalId</code></strong></td><td>string</td><td><p>External identifier .</p><p></p><p>Example: "WW-CON-12345678"</p></td></tr><tr><td><strong><code>useBuyerAddress</code></strong></td><td>boolean</td><td><p>Defines whether address should be copied from  buyer. </p><p></p><p>Example: "true"</p></td></tr><tr><td><strong><code>address</code></strong></td><td>object</td><td><p>Address of the licensee.</p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "addressLine1": "123 Main Street",
  "addressLine2": "Apt 4B",
  "postCode": "12345",
  "city": "Cityville",
  "state": "S",
  "country": "ST"
}
</code></pre></td></tr><tr><td><strong><code>description</code></strong></td><td>string</td><td>Description of the licensee.</td></tr><tr><td><strong><code>contact</code></strong></td><td>object</td><td><p>Contact person details. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
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
</code></pre></td></tr><tr><td><strong><code>buyer</code></strong></td><td><a href="../buyer/#buyer-object">Buyer</a></td><td></td></tr><tr><td><strong><code>seller</code></strong></td><td><a href="../seller/#seller-object">Seller</a></td><td></td></tr><tr><td><strong><code>account</code></strong></td><td><a href="../account/#account-object">Account</a></td><td></td></tr><tr><td><strong><code>audit</code></strong></td><td>object</td><td><p>Possible audit events: Created, Updated, Activated, Disabled, Deactivated, or Deleted. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
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
