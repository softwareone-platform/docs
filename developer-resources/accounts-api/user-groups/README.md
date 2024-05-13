# User groups

## Group Object

The `group` object represents a user group in the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th>Field</th><th width="117">Type</th><th>Constraints</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p><code>READONLY</code></p><p><code>IDX</code></p><p><code>CORE</code></p></td><td><p>Primary group identifier. </p><p></p><p>Example: "UGR-1234-1234"</p></td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td><p><code>READONLY</code> </p><p><code>CORE</code></p></td><td><p>Relative reference to object on API. </p><p></p><p>Example: "/v1/accounts/groups/UGR-1234-1234"</p></td></tr><tr><td><strong><code>icon</code></strong></td><td>string</td><td><code>OPTIONAL</code></td><td><p>Relative path to token’s logo. </p><p></p><p>Example: "/static/accounts/UGR-1234-1234/logo.png"</p></td></tr><tr><td><strong><code>name</code></strong></td><td>string</td><td><p><code>IDX</code></p><p><code>CORE</code></p></td><td><p>Group name. </p><p></p><p>Example: "Stark Industries"</p></td></tr><tr><td><strong><code>description</code></strong></td><td>string</td><td><code>OPTIONAL</code></td><td><p>Group description. </p><p></p><p>Example: "Stark's marketing group"</p></td></tr><tr><td><strong><code>modules</code></strong></td><td><a href="../module/#module-object">Module</a></td><td><code>OPTIONAL</code></td><td><p>List of modules available for the group. </p><p></p><p>Example: "Invoices"</p></td></tr><tr><td><strong><code>default</code></strong></td><td>bool</td><td></td><td><p>Indicated if the user group is set as default in the account. There is only one default user-group per account. </p><p></p><p>Example: "true"</p></td></tr><tr><td><strong><code>stats</code></strong></td><td>stats</td><td><code>READONLY</code> </td><td><p>Statistics of the group. A </p><p>group can be deleted only if the UsersCount is <code>0</code>.  </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "users": 123
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="GROUP OBJECT" %}
{% code lineNumbers="true" %}
```json
{
	"id": "UGR-5116-6265",
	"href": "/user-groups/UGR-5116-6265",
	"name": "Test-1",
	"description": "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.",
	"modules": [
		{
			"id": "MOD-1756-1452",
			"name": "Access management"
		},
		{
			"id": "MOD-9042-8216",
			"name": "Account management"
		}
	],
	"icon": "https://picsum.photos/210/201",
	"default": true,
	"stats": {
		"users": 123
	}
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
