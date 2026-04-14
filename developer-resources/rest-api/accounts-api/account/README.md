# Account

The `Account` object represents an individual account in the SoftwarOne Marketplace.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="200">Field Name</th><th width="149">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary identifier for the account.</p><p>Example: ACC-1671-0642</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>A relative reference to the object.</p><p>Example: /v1/accounts/accounts/ACC-1671-0642</p></td></tr><tr><td><code>type</code></td><td>string</td><td>The type of the account. Allowed values:  <code>client</code>, <code>vendor</code>, or <code>operations</code>.</td></tr><tr><td><code>status</code></td><td>string</td><td>The account's status on the platform. Allowed values: <code>enabled</code>, <code>active</code>, or <code>disabled</code>.</td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the account.</p><p>Example: Stark Industries</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>The account's description.</p><p>Example: Our company account</p></td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>External identifier - Customer Discount Group number.</p><p>Example: WW-1001111</p></td></tr><tr><td><code>externalName</code></td><td>string</td><td><p>External identifier - Customer Discount Group name.</p><p>Example: Stark Industries</p></td></tr><tr><td><code>serviceLevel</code></td><td>string</td><td>The service level offered to the account. Allowed values:  <code>essential</code>, <code>elite</code>, or  <code>DSC</code>.</td></tr><tr><td><code>address</code></td><td>object</td><td><p>The <a href="../../common-api-objects/address.md"><code>address</code></a> of the company.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "addressLine1": "123 Main Street",
  "addressLine2": "Apt 4B",
  "postCode": "12345",
  "city": "Cityville",
  "state": "S",
  "country": "ST"
}
</code></pre></td></tr><tr><td><code>icon</code></td><td>string</td><td><p>The relative path to the account's logo.</p><p>Example: /static/accounts/ACC-1671-0642/logo.png</p></td></tr><tr><td><code>website</code></td><td>string</td><td><p>The path to the company’s website.</p><p>Example: https://www.example.com</p></td></tr><tr><td><code>technicalSupportEmail</code></td><td>string</td><td><p>The email address for technical support.</p><p>Example: user@example.com</p></td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. Allowed values:  <code>created</code>, <code>updated</code>, <code>disabled</code>, <code>enabled</code>, or  <code>activated</code>.</td></tr><tr><td><code>groups</code></td><td>object</td><td>A reference to the <a href="../../../../modules-and-features/settings/groups/"><code>userGroup</code></a> object.</td></tr></tbody></table>

### Example response

{% tabs %}
{% tab title="SHORT FORM" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "ACC-1671-0642",
  "type": "Client",
  "status": "Enabled",
  "name": "You Are a Test Account",
  "description": "This is a test account",
  "externalId": "WW-1001111",
  "serviceLevel": "Express",
  "address": {
    "addressLine1": "123 Main Street",
    "addressLine2": "Apt 4B",
    "postCode": "12345",
    "city": "Cityville",
    "state": "S",
    "country": "ST"
  },
  "logo": null,
  "technicalSupportEmail": "user@example.com",
  "website": "https://example.com"
}
```
{% endcode %}
{% endtab %}

{% tab title="FULL EXAMPLE" %}
<pre class="language-json" data-line-numbers><code class="lang-json"><strong>{
</strong>  "id": "ACC-1671-0642",
  "type": "Client",
  "status": "Enabled",
  "name": "You Are a Test Account",
  "description": "This is a test account.",
  "externalId": "WW-1001111",
  "serviceLevel": "Express",
  "address": {
    "addressLine1": "123 Main Street",
    "addressLine2": "Apt 4B",
    "postCode": "12345",
    "city": "Cityville",
    "state": "S",
    "country": "ST"
  },
  "logo": null,
  "technicalSupportEmail": "user@example.com",
  "website": "https://example.com",
  "groups": [
		{
			"id": "UGR-9354-3382",
			"name": "Administrators",
			"description": "Manages administrative tasks and resources within an organization.",
			"logo": null,
			"isDefault": true
		}
  ],
  {
    "created": { "at": "2023-12-14T17:28:57.667Z", "by": { "id": "USR-1234-1234", "name": "John Smith" } },
    "updated": { "at": "2023-12-14T17:28:57.667Z", "by": { "id": "USR-1234-1234", "name": "John Smith" } },
    "disabled": { "at": "2023-12-14T17:28:57.667Z", "by": { "id": "USR-1234-1234", "name": "John Smith" } },
    "enabled": { "at": "2023-12-14T17:28:57.667Z", "by": { "id": "USR-1234-1234", "name": "John Smith" } },
    "activated": { "at": "2023-12-14T17:28:57.667Z", "by": { "id": "USR-1234-1234", "name": "John Smith" } }
  }
}
</code></pre>
{% endtab %}
{% endtabs %}
