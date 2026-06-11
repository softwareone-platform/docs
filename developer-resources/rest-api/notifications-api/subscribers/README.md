# Subscriber

The Subscriber object manages the configuration of notifications for accounts.

It serves as the link between an account and a notification category, storing details about whether that category is enabled for the account and identifying the recipients who should receive notifications for it.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="155">Field</th><th width="159">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The primary identifier for the notification subscriber. </td></tr><tr><td><code>href</code></td><td>string, core</td><td>(Read-only) A relative reference to the object. </td></tr><tr><td><code>name</code></td><td>string, core</td><td>(Read-only) The name of the category. </td></tr><tr><td><code>status</code></td><td>enum, core</td><td>Indicates if the category is <code>enabled</code> or <code>disabled</code>. If <code>disabled</code>, no notifications are sent for the category. </td></tr><tr><td><code>note</code></td><td>string</td><td>Notes related to the category. </td></tr><tr><td><code>recipients</code></td><td>recipients</td><td><p>The recipient of the notification email. To receive a notification, the user must be in the <code>recipients.users</code> or be a part of a group within <code>recipients.userGroups</code>. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
   "recipients": {
       "users": [],
       "userGroups": []
   }
}
</code></pre></td></tr><tr><td><code>account</code></td><td>object, core</td><td>(Read-only) Represents the <a href="../../accounts-api/account/"><code>account</code></a> object.</td></tr><tr><td><code>category</code></td><td>object, core</td><td>(Read-only) Represents the <a href="../categories/"><code>category</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Example

{% code title="SUBSCRIBER OBJECT" overflow="wrap" lineNumbers="true" %}
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
