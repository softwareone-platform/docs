# Licensee

The Licensee object represents a licensee in the Marketplace platform.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="159">Field</th><th width="154">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The primary identifier for the licensee.</td></tr><tr><td><code>status</code></td><td>string</td><td><p>The status of the licensee. Allowed values: </p><ul><li><code>Enabled</code></li><li><code>Active</code></li><li><code>Disabled</code></li><li><code>Deleted</code></li></ul></td></tr><tr><td><code>name</code></td><td>string, core</td><td>The licensee's name.</td></tr><tr><td><code>icon</code></td><td>string</td><td>(Optional) A relative path to the licensee’s logo.</td></tr><tr><td><code>externalId</code></td><td>string, core</td><td>(Optional) The external identifier.</td></tr><tr><td><code>useBuyerAddress</code></td><td>boolean</td><td>(Optional) Defines whether the address should be copied from the buyer.</td></tr><tr><td><code>address</code></td><td>object</td><td><p>(Optional) The <a href="../../../api-usage-and-reference/common-api-objects/address.md"><code>address</code></a> of the licensee.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "addressLine1": "123 Main Street",
  "addressLine2": "Apt 4B",
  "postCode": "12345",
  "city": "Cityville",
  "state": "S",
  "country": "ST"
}
</code></pre></td></tr><tr><td><code>description</code></td><td>string</td><td>(Optional) A description of the licensee.</td></tr><tr><td><code>contact</code></td><td>object</td><td><p>The details of the contact person.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "name": "Reto Mayer",
  "firstName": "Reto",
  "lastName": "Mayer",
  "email": "reto.mayer@example.com",
  "phone": null,
  "user": {
    "id": "USR-0000-0001",
    "icon": null,
    "name": "Reto Mayer"
  },
  "address": {
    "addressLine1": "23 Main",
    "addressLine2": "Apt 4B",
    "postCode": "12345",
    "city": "Cityville",
    "state": "S",
    "country": "ST"
  }
}

</code></pre></td></tr><tr><td><code>buyer</code></td><td>object</td><td>Represents the <a href="../buyer/#buyer-object"><code>buyer</code></a> object.</td></tr><tr><td><code>seller</code></td><td>object</td><td>Represents the <a href="../seller/#seller-object"><code>seller</code></a> object.</td></tr><tr><td><code>account</code></td><td>object</td><td>Represents the <a href="../account/#account-object"><code>account</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Examples

{% tabs %}
{% tab title="MINIMAL EXAMPLE" %}
{% code title="LICENSEE OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "name": "Stark Industries Finance Dept",
  "externalId": "WW-CON-12345678",
  "status": "Active",
  "address": null,
  "useBuyerAddress": true,
  "icon": null,
  "description": null
}
```
{% endcode %}
{% endtab %}

{% tab title="COMPLETE EXAMPLE" %}
{% code title="LICENSEE OBJECT" lineNumbers="true" %}
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
