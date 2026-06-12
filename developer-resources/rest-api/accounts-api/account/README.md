# Account

Account object represents an individual account in the SoftwareOne Marketplace.&#x20;

This object contains the following attributes:

<table data-full-width="false"><thead><tr><th width="213">Field</th><th width="132.25">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1"><em>core</em></a></td><td>(Read-only) Unique identifier for the account.</td></tr><tr><td><code>type</code></td><td>string, core</td><td><p>The type of account. Allowed values are:</p><ul><li><code>Client</code></li><li><code>Vendor</code></li><li><code>Operations</code></li></ul></td></tr><tr><td><code>status</code></td><td>string, core</td><td><p>(Read-only) The status of the account. Allowed values are: </p><ul><li><code>Enabled</code></li><li><code>Active</code></li><li><code>Disabled</code></li></ul></td></tr><tr><td><code>name</code></td><td>string</td><td>The name of the account.</td></tr><tr><td><code>description</code></td><td>string</td><td>(Optional) A description of the account.</td></tr><tr><td><code>externalId</code></td><td>string</td><td>(Optional) The Customer Discount Group number.</td></tr><tr><td><code>externalName</code></td><td>string</td><td>The Customer Discount Group name.</td></tr><tr><td><code>serviceLevel</code></td><td>string</td><td><p>Service level for the account. Allowed values are: </p><ul><li><code>Essential</code></li><li><code>Elite</code></li><li><code>DSC</code></li></ul></td></tr><tr><td><code>address</code></td><td>object</td><td>The <a href="../../../api-usage-and-reference/common-api-objects/address.md"><code>address</code></a> of the company.</td></tr><tr><td><code>icon</code></td><td>string, core</td><td>The relative path to the account's logo.</td></tr><tr><td><code>website</code></td><td>string</td><td>The path to the company’s website.</td></tr><tr><td><code>technicalSupportEmail</code></td><td>string</td><td>The email address for technical support.</td></tr><tr><td><code>audit</code></td><td>object</td><td>Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr><tr><td><code>groups</code></td><td>object</td><td>Represents the <a href="../../../../modules-and-features/settings/groups/"><code>userGroup</code></a> object.</td></tr><tr><td><code>buyers</code></td><td>object</td><td>Represents the <a href="../buyer/"><code>buyer</code></a> object.</td></tr><tr><td><code>externalIDs</code></td><td>object</td><td>Represents the <code>externalId</code> for the account.</td></tr><tr><td><code>defaultLanguageCode</code></td><td>string</td><td>The default language code of the account.</td></tr></tbody></table>

## Examples

{% tabs %}
{% tab title="MINIMAL EXAMPLE" %}
{% code title="ACCOUNT OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "ACC-1671-0642",
  "type": "Client",
  "status": "Enabled",
  "name": "Stark industries",
  "description": "Stark industries procurement team.",
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
  "technicalSupportEmail": "jane@doe.com",
  "website": "https://example.com"  
}
```
{% endcode %}
{% endtab %}

{% tab title="COMPLETE EXAMPLE" %}
<pre class="language-json" data-title="ACCOUNT OBJECT" data-overflow="wrap" data-line-numbers><code class="lang-json"><strong>{
</strong>  "id": "ACC-1671-0642",
  "type": "Client",
  "status": "Enabled",
  "name": "Stark industries",
  "description": "Stark industries procurement team.",
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
  "technicalSupportEmail": "jane@doe.com",
  "website": "https://janedoeexample.com",
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
