# Account

## Account Object

The account object represents an individual account on the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th width="120">Field</th><th width="125">Type</th><th width="147">Constraints</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p><code>READONLY</code> </p><p><code>IDX</code> </p><p><code>CORE</code></p></td><td><p>Primary account identifier. </p><p></p><p>Example: "ACC-1671-0642"</p></td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td><p><code>READONLY</code> </p><p><code>CORE</code></p></td><td><p>Relative reference to object on API. </p><p></p><p>Example: "/v1/accounts/accounts/ACC-1671-0642"</p></td></tr><tr><td><strong><code>type</code></strong></td><td>string</td><td><p><code>IDX</code> </p><p><code>CORE</code></p></td><td><p>Type of the account (Client, Vendor, Operations)</p><p></p><p>Example: "Client"</p></td></tr><tr><td><strong><code>status</code></strong></td><td>string</td><td><p><code>IDX</code> </p><p><code>CORE</code></p></td><td><p>Status of the account (Enabled, Active, Disabled)</p><p></p><p>Example: "Enabled"</p></td></tr><tr><td><strong><code>name</code></strong></td><td>string</td><td><p><code>IDX</code> </p><p><code>CORE</code></p></td><td><p>Account name. </p><p></p><p>Example: "Stark Industries"</p></td></tr><tr><td><strong><code>description</code></strong></td><td>string</td><td><p><code>IDX</code> </p><p><code>OPTIONAL</code></p></td><td><p>Account description. </p><p></p><p>Example: "Our company account"</p></td></tr><tr><td><strong><code>externalId</code></strong></td><td>string</td><td><p><code>IDX</code> </p><p><code>OPTIONAL</code></p></td><td><p>External identifier - Customer Discount Group number.  </p><p></p><p>Example: "WW-1001111"</p></td></tr><tr><td><strong><code>externalName</code></strong></td><td>string</td><td><p><code>IDX</code> </p><p><code>OPTIONAL</code></p></td><td><p>External identifier - Customer Discount Group name. </p><p></p><p>Example: "Stark Industries"</p></td></tr><tr><td><strong><code>serviceLevel</code></strong></td><td>string</td><td><code>IDX</code> </td><td><p>Service level offered to the account (Essential, Elite, DSC)</p><p></p><p>Example: "Elite"</p></td></tr><tr><td><strong><code>address</code></strong></td><td>object</td><td><p><code>IDX</code> </p><p><code>OPTIONAL</code></p></td><td><p>Address of the company. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "addressLine1": "123 Main Street",
  "addressLine2": "Apt 4B",
  "postCode": "12345",
  "city": "Cityville",
  "state": "S",
  "country": "ST"
}
</code></pre></td></tr><tr><td><strong><code>icon</code></strong></td><td>string</td><td><p><code>OPTIONAL</code> </p><p><code>CORE</code></p></td><td><p>Relative path to account logo. </p><p></p><p>Example: "/static/accounts/ACC-1671-0642/logo.png"</p></td></tr><tr><td><strong><code>website</code></strong></td><td>string</td><td><p><code>IDX</code> </p><p><code>OPTIONAL</code></p></td><td><p>Path to company’s website. </p><p></p><p>Example: "https://www.example.com"</p></td></tr><tr><td><strong><code>technicalSupportEmail</code></strong></td><td>string</td><td><p><code>IDX</code> </p><p><code>OPTIONAL</code></p></td><td><p>Technical support email for some corner cases. </p><p></p><p>Example: "user@example.com"</p></td></tr><tr><td><strong><code>audit</code></strong></td><td>object</td><td><p><code>READONLY</code> </p><p><code>IDX</code></p></td><td><p>Possible audit events: Created, Updated, Disabled, Enabled, or Activated. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } },
  "disabled": { "at": "...", "by": { } },
  "enabled": { "at": "...", "by": { } },
  "activated": { "at": "...", "by": { } }
}
</code></pre></td></tr><tr><td><strong><code>groups</code></strong></td><td>UserGroup</td><td></td><td></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="SHORT FORM" %}
{% code lineNumbers="true" %}
```json
{
  "id": "ACC-1671-0642",
  "href": "/accounts/accounts/ACC-1671-0642",
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
<pre class="language-json"><code class="lang-json"><strong>{
</strong>  "id": "ACC-1671-0642",
  "href": "/accounts/accounts/ACC-1671-0642",
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
			"href": "/user-groups/UGR-9354-3382",
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
