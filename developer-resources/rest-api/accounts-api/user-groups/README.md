# User Groups

The Group object represents a user group in the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th width="140">Field</th><th width="125">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Primary group identifier. </p><p></p><p>Example: UGR-1234-1234</p></td></tr><tr><td>href</td><td>string</td><td><p>Relative reference to the object in the API. </p><p></p><p>Example: /v1/accounts/groups/UGR-1234-1234</p></td></tr><tr><td>icon</td><td>string</td><td><p>Relative path to the token’s logo. </p><p></p><p>Example: /static/accounts/UGR-1234-1234/logo.png</p></td></tr><tr><td>name</td><td>string</td><td><p>Group name. </p><p></p><p>Example: Stark Industries</p></td></tr><tr><td>description</td><td>string</td><td><p>Group description. </p><p></p><p>Example: Stark's marketing group</p></td></tr><tr><td>modules</td><td><a href="../module/#module-object">Module</a></td><td><p>List of modules available for the group. </p><p></p><p>Example: Invoices</p></td></tr><tr><td>default</td><td>bool</td><td><p>Indicates if the user group is set as default in the account. There is only one default user group per account. </p><p></p><p>Example: true</p></td></tr><tr><td>stats</td><td>stats</td><td><p>Statistics of the group. A group can be deleted only if the user count is 0.  </p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
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
