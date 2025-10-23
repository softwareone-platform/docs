# Subscriber

The Subscriber object manages the configuration of notifications for accounts.

It serves as the link between an account and a notification category, storing details about whether that category is enabled for the account and identifying the recipients who should receive notifications for it.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="155">Field</th><th width="130">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The primary identifier for the notification subscriber. </p><p>Example: NTS-1111-2222-1234</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>A relative reference to the object. </p><p>Example: /notifications/subscribers/NTS-1111-2222-1234</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the category. </p><p>Example: Orders</p></td></tr><tr><td>status</td><td><code>enum</code></td><td>Indicates if the category connected to the configuration is enabled or disabled for the account. The possible values are <code>Enabled</code> or <code>Disabled</code>. When disabled, no notifications are sent for the category. </td></tr><tr><td>note</td><td><code>string</code></td><td><p>Notes related to the category. </p><p>Example: Disabled because we are not interested in this category.</p></td></tr><tr><td>recipients</td><td><code>recipients</code></td><td><p>The recipient of the notification email. To receive a notification, the user must be in the <code>recipients.users</code> or be a part of a group within <code>recipients.userGroups</code>. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
   "recipients": {
       "users": [],
       "userGroups": []
   }
}
</code></pre></td></tr><tr><td>account</td><td><a href="../../accounts-api/account/"><code>account</code></a></td><td> A reference to the Account object.</td></tr><tr><td>category</td><td><a href="../categories/"><code>category</code></a></td><td><p>The name of the category. </p><p>Example: Orders.</p></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the Audit object with possible values, including <code>Created</code> or <code>Updated</code>.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="SUBSCRIBER OBJECT" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
	"id": "NTS-1111-2222-1234",
	"href": "/notifications/subscribers/NTS-1111-2222-1234",
	"status": "Enabled",
	"category": {
		"id": "NTC-1234-9876",
		"href": "/v1/notifications/categories/NTC-1234-9876",
		"name": "Orders",
		"shortDescription": "Includes updates about order confirmations, order status updates, and related communications."
	},
	"account": {
		"id": "AC-1111-2222",
		"href": "/accounts/accounts/AC-1111-2222",
		"type": "Client",
		"status": "Active",
		"name": "Agroasemex test copy 2",
		"icon": "/v1/accounts/accounts/AC-1111-2222/icon"
	},
	"recipients": {
		"users": [
			{
				"id": "USR-0000-0001",
				"href": "/accounts/users/USR-0000-0001",
				"name": "Will Smith"
			}
		],
		"userGroups": [
			{
				"id": "UGR-2459-0365",
				"href": "/accounts/user-groups/UGR-2459-0365",
				"name": "Administrators",
				"description": "Manages administrative tasks and resources within an organization.",
				"isDefault": true
			}
		]
	},
	"audit": {
		"created": {
			"at": "2023-12-15T10:17:11.179Z",
			"by": {
				"id": "USR-0000-0001",
				"href": "/accounts/users/USR-0000-0001",
				"name": "Will Smith"
			}
		},
		"updated": {
			"at": "2023-12-15T10:17:11.179Z",
			"by": {
				"id": "USR-0000-0001",
				"href": "/accounts/users/USR-0000-0001",
				"name": "Will Smith"
			}
		}
	}
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
