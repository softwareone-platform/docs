# Licensee

The Licensee object represents a licensee in the Marketplace platform.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="159">Field Name</th><th width="115">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary identifier for the licensee.</p><p>Example: LCE-1234-1234-1234</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>A relative reference to the object in the API.</p><p>Example: /v1/accounts/licensees/LIC-1234-1234-1234"</p></td></tr><tr><td><code>status</code></td><td>string</td><td>The status of the licensee. Allowed values are <code>enabled</code>, <code>active</code>, <code>disabled</code>, or <code>deleted</code>.</td></tr><tr><td><code>name</code></td><td>string</td><td><p>The licensee's name.</p><p>Example: Stark Industries Finance Dept</p></td></tr><tr><td><code>icon</code></td><td>string</td><td><p>A relative path to the licensee’s logo.</p><p>Example: /static/accounts/LIC-1234-1234-1234/logo.png</p></td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>The external identifier.</p><p>Example: WW-CON-12345678</p></td></tr><tr><td><code>useBuyerAddress</code></td><td>boolean</td><td><p>Defines whether the address should be copied from the buyer.</p><p>Example: true</p></td></tr><tr><td><code>address</code></td><td>object</td><td><p>The <a href="../../common-api-objects/address.md"><code>address</code></a> of the licensee.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "addressLine1": "123 Main Street",
  "addressLine2": "Apt 4B",
  "postCode": "12345",
  "city": "Cityville",
  "state": "S",
  "country": "ST"
}
</code></pre></td></tr><tr><td><code>description</code></td><td>string</td><td>A description of the licensee.</td></tr><tr><td><code>contact</code></td><td>object</td><td><p>The details of the contact person.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "name": "Will Smith",
  "firstName": "Will",
  "lastName": "Smith",
  "email": "will.smith@adastraflex.com",
  "phone": null,
  "user": {
    "id": "USR-0000-0001",
    "icon": null,
    "name": "Will Smith",
  }
}
 "addressLine1": "123 Main Street",
  "addressLine2": "Apt 4B",
  "postCode": "12345",
  "city": "Cityville",
  "state": "S",
  "country": "ST"
}
</code></pre></td></tr><tr><td><code>buyer</code></td><td>object</td><td>A reference to the <a href="../buyer/#buyer-object"><code>buyer</code></a> object.</td></tr><tr><td><code>seller</code></td><td>object</td><td>A reference to the <a href="../seller/#seller-object"><code>seller</code></a> object.</td></tr><tr><td><code>account</code></td><td>object</td><td>A reference to the <a href="../account/#account-object"><code>account</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. Allowed values:  <code>created</code>, <code>updated</code>, <code>activated</code>, <code>disabled</code>, <code>deactivated</code>, or <code>deleted</code>.</td></tr></tbody></table>

## Example response

{% tabs %}
{% tab title="SHORT FORM" %}
{% code overflow="wrap" lineNumbers="true" %}
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
