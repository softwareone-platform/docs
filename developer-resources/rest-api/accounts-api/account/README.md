# Accounts

The Account object represents an individual account on the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th width="200">Field</th><th width="149">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The primary identifier for the account.</p><p>Example: ACC-1671-0642</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>A relative reference to the object.</p><p>Example: /v1/accounts/accounts/ACC-1671-0642</p></td></tr><tr><td>type</td><td><code>string</code></td><td><p>The type of the account. </p><p>Possible values: <code>Client</code>, <code>Vendor</code>, or <code>Operations</code></p></td></tr><tr><td>status</td><td><code>string</code></td><td><p>The account's status on the platform. </p><p>Possible values: <code>Enabled</code>, <code>Active</code>, or <code>Disabled</code></p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the account.</p><p>Example: Stark Industries</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>The account's description.</p><p>Example: Our company account</p></td></tr><tr><td>externalId</td><td><code>string</code></td><td><p>External identifier - Customer Discount Group number.</p><p>Example: WW-1001111</p></td></tr><tr><td>externalName</td><td><code>string</code></td><td><p>External identifier - Customer Discount Group name.</p><p>Example: Stark Industries</p></td></tr><tr><td>serviceLevel</td><td><code>string</code></td><td><p>The service level offered to the account.</p><p>Possible values: <code>Essential</code>, <code>Elite</code>, or <code>DSC</code></p></td></tr><tr><td>address</td><td><a href="../../common-api-objects/address.md"><code>address</code></a></td><td><p>The address of the company.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "addressLine1": "123 Main Street",
  "addressLine2": "Apt 4B",
  "postCode": "12345",
  "city": "Cityville",
  "state": "S",
  "country": "ST"
}
</code></pre></td></tr><tr><td>icon</td><td><code>string</code></td><td><p>The relative path to the account's logo.</p><p>Example: /static/accounts/ACC-1671-0642/logo.png</p></td></tr><tr><td>website</td><td><code>string</code></td><td><p>The path to the company’s website.</p><p>Example: https://www.example.com</p></td></tr><tr><td>technicalSupportEmail</td><td><code>string</code></td><td><p>The email address for technical support.</p><p>Example: user@example.com</p></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td><p>A reference to the Audit object. </p><p>Possible values: <code>Created</code>, <code>Updated</code>, <code>Disabled</code>, <code>Enabled</code>, or <code>Activated</code>.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } },
  "disabled": { "at": "...", "by": { } },
  "enabled": { "at": "...", "by": { } },
  "activated": { "at": "...", "by": { } }
}
</code></pre></td></tr><tr><td>groups</td><td><a href="../../../../modules-and-features/settings/groups/"><code>userGroup</code></a></td><td>A reference to the User Group object.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="SHORT FORM" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "ACC-1671-0642",
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
