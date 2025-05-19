# Licensee

The Licensee object represents a licensee in the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th width="159">Field</th><th width="115">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The primary identifier for the licensee.</p><p>Example: LCE-1234-1234-1234</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>A relative reference to the object in the API.</p><p>Example: /v1/accounts/licensees/LIC-1234-1234-1234"</p></td></tr><tr><td>status</td><td><code>string</code></td><td><p>The status of the licensee. </p><p>Possible values: <code>Enabled</code>, <code>Active</code>, <code>Disabled</code>, or <code>Deleted</code>.</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The licensee's name.</p><p>Example: Stark Industries Finance Dept</p></td></tr><tr><td>icon</td><td><code>string</code></td><td><p>A relative path to the licensee’s logo.</p><p>Example: /static/accounts/LIC-1234-1234-1234/logo.png</p></td></tr><tr><td>externalId</td><td><code>string</code></td><td><p>The external identifier.</p><p>Example: WW-CON-12345678</p></td></tr><tr><td>useBuyerAddress</td><td><code>boolean</code></td><td><p>Defines whether the address should be copied from the buyer.</p><p>Example: true</p></td></tr><tr><td>address</td><td><code>object</code></td><td><p>The address of the licensee.</p><p>Example:</p><pre class="language-json"><code class="lang-json">{
  "addressLine1": "123 Main Street",
  "addressLine2": "Apt 4B",
  "postCode": "12345",
  "city": "Cityville",
  "state": "S",
  "country": "ST"
}
</code></pre></td></tr><tr><td>description</td><td><code>string</code></td><td>A description of the licensee.</td></tr><tr><td>contact</td><td><code>object</code></td><td><p>The details of the contact person.</p><p>Example:</p><pre class="language-json"><code class="lang-json">{
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
</code></pre></td></tr><tr><td>buyer</td><td><a href="../buyer/#buyer-object"><code>buyer</code></a></td><td>A reference to the Buyer object.</td></tr><tr><td>seller</td><td><a href="../seller/#seller-object"><code>seller</code></a></td><td>A reference to the Seller object.</td></tr><tr><td>account</td><td><a href="../account/#account-object"><code>account</code></a></td><td>A reference to the Account object.</td></tr><tr><td>audit</td><td><code>object</code></td><td><p>Possible audit events: <code>Created</code>, <code>Updated</code>, <code>Activated</code>, <code>Disabled</code>, <code>Deactivated</code>, or <code>Deleted</code>.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
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
		"type": "Client",
		"status": "Active",
		"icon": null,
		"name": "AdAstraflexx"
	},
	"buyer": {
		"id": "BUY-8928-0965",
		"name": "Stark Industries"
	},
	"seller": {
		"id": "SEL-4717-3953",
		"externalId": "SWO_CA",
		"name": "SoftwareOne Canada, Inc."
	}
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
