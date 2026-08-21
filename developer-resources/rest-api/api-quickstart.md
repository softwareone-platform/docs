---
description: Create an API token and make your first Marketplace Platform API request.
---

# API quickstart

Marketplace Platform REST APIs provide programmatic access to accounts, orders, subscriptions, billing, notifications, and other Marketplace resources.

Use this guide to create an API token and make your first API call.

{% stepper %}
{% step %}
### Before you start

Ensure that you have:

* Access to a Marketplace Platform account.
* Permission to create API tokens in the Marketplace.
* A tool for sending requests, such as Postman.
{% endstep %}

{% step %}
### Generate an API token

Marketplace Platform APIs use API tokens for authentication.

To create a token:

1. [Sign in](https://portal.platform.softwareone.com/) to your Marketplace account.
2. Open the main menu, then go to **Settings** > **API tokens**.
3. Select **Add**.
4. Complete the **Add API token** workflow. For detailed instructions, see [Create API token](../../modules-and-features/settings/api-tokens/create-api-token.md).
5. Copy the token value.
{% endstep %}

{% step %}
### Make your first API request

Once you have your API token, send a request to one of the available endpoints.&#x20;

All Marketplace Platform API endpoints use the following base URL:&#x20;

```
https://api.platform.softwareone.com
```

The following example uses the [Accounts API](accounts-api/) to retrieve a list of buyers in your account.

Send a `GET` request to the `/public/v1/accounts/buyers` endpoint:

```http
GET https://api.platform.softwareone.com/public/v1/accounts/buyers
Authorization: Bearer {TOKEN_VALUE}
Accept: application/json
```
{% endstep %}

{% step %}
### Review the response

If the request succeeds, the API returns a `200 OK` response and a list of buyers in the response body.&#x20;

{% code title="200 OK" overflow="wrap" lineNumbers="true" expandable="true" %}
```json
{
	"$meta": {
		"pagination": {
			"offset": 0,
			"limit": 10,
			"total": 1
		},
		"omitted": [
			"audit"
		]
	},
	"data": [
		{
			"id": "BUY-2844-0294",		
            "icon": "/buyers/BUY-2844-0294/icon",
			"contact": null,
			"externalIds": {
				"erpCompanyContact": "WW-CON-123456",
				"erpCustomer": "WW-SCU-123456"
			},
			"status": "Enabled",
			"icon": null,
			"address": {
				"addressLine1": "PO Box 31",
				"addressLine2": "Victory Road",
				"postCode": "DE24 8BJ",
				"city": "Derby",
				"state": "Derbs",
				"country": "UK"
	
	
					},
			"taxId": "VAT1",
			"account": {
				"id": "ACC-5563-4382",
				"href": "/accounts/ACC-5563-4382",
				"icon": null,
				"name": "Intelli Industries"
			},
			"name": "Rolls, Inc",
			"sellers": [
				{
					"id": "SEL-0578-5578",				
					"externalId": "SWO_CA",
					"name": "SoftwareOne Canada, Inc."
				}
			]
		}
	]
}
```
{% endcode %}

If the access token is invalid, the API returns  `401 Unauthorized`.&#x20;

If the token doesn't have permission to access the endpoint, the API returns `403 Forbidden`. Note that access to this endpoint depends on the account type associated with the token, rather than the enabled modules. The token must belong to a **client** or **ops** account. For more HTTP status codes, see [Error handling](../api-usage-and-reference/errors-handling.md).
{% endstep %}
{% endstepper %}

### Continue building with Marketplace Platform APIs

After successfully authenticating, you can use the same API token to access other Marketplace APIs. Choose a common integration scenario to continue building with the platform.

<table data-card-size="large" data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th><th data-hidden data-card-cover data-type="image">Cover image</th></tr></thead><tbody><tr><td><strong>Manage accounts and users</strong></td><td>Create and manage accounts, users, groups, and API tokens.</td><td><a href="accounts-api/">accounts-api</a></td><td></td></tr><tr><td><strong>Manage orders and subscriptions</strong></td><td>Manage orders, subscriptions, assets, and agreements.</td><td><a href="commerce-api/">commerce-api</a></td><td></td></tr><tr><td><strong>Access billing data</strong></td><td>Retrieve invoices, statements, charges, and billing information.</td><td><a href="billing-api/">billing-api</a></td><td></td></tr><tr><td><strong>Manage products and catalogs</strong></td><td>Browse and manage products, catalogs, and related metadata.</td><td><a href="catalog-api/">catalog-api</a></td><td></td></tr><tr><td><strong>Manage notifications</strong></td><td>Send notifications, manage recipients and categories, and track message delivery.</td><td><a href="notifications-api/">notifications-api</a></td><td></td></tr></tbody></table>

{% hint style="info" %}
Looking for additional APIs or guidance? See [Browse APIs](./#browse-apis) and [API Usage & Reference](../api-usage-and-reference/).
{% endhint %}
