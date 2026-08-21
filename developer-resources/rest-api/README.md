# REST API

The Marketplace Platform REST API allows you to interact with the platform programmatically.&#x20;

The APIs are organized around REST principles, use predictable resource-oriented URLs, [JSON-encoded](http://www.json.org/) representations, and standard HTTP methods and status codes.

Each API works similarly, whether you access it directly over HTTP or through helper libraries in various programming languages.

### Common use cases

Use Marketplace APIs to:

* Manage accounts, users, and groups.
* Automate order processing and fulfillment workflows.
* Manage orders, subscriptions, and assets.
* Retrieve billing and financial data.
* Synchronize Marketplace data with external business systems.
* Integrate and manage notification workflows.

### Authentication

Marketplace Platform uses [API tokens](../../modules-and-features/settings/api-tokens/) for authentication.

Include your API token in the `Authorization` HTTP header with the `Bearer` scheme.&#x20;

Your API keys have permissions assigned to them, so keep them secure. Don't share your secret API keys in public areas, like GitHub or client-side code.

### HTTPS requirements

All API requests must be made over HTTPS.&#x20;

Requests sent over HTTP are not supported. API requests without authentication will fail.

### Content-type requirements

Most Marketplace API endpoints expect requests to use the `application/json` content type. Endpoints that support file uploads may require `multipart/form-data` instead.

```http
GET https://api.platform.softwareone.com/public/v1/accounts/buyers
Authorization: Bearer {TOKEN_VALUE}
Content-Type: application/json
```

To communicate successfully with the APIs, ensure your API requests are formatted using the `application/json` content type.&#x20;

Using the wrong content type may result in unexpected behavior or errors.

### Browse APIs

<table data-search="false"><thead><tr><th width="225">API</th><th>Description</th><th data-hidden data-type="content-ref"></th></tr></thead><tbody><tr><td><a href="accounts-api/">Accounts API</a></td><td>Manage accounts, users, groups, &#x26; more. </td><td><a href="accounts-api/">accounts-api</a></td></tr><tr><td><a href="audit-api/">Audit API</a></td><td>Track and retrieve audit activity.</td><td><a href="audit-api/">audit-api</a></td></tr><tr><td><a href="billing-api/">Billing API</a></td><td>Work with invoices, statements, charges, &#x26; more.</td><td><a href="billing-api/">billing-api</a></td></tr><tr><td><a href="catalog-api/">Catalog API</a></td><td>Manage catalog, products, items, &#x26; more.</td><td><a href="catalog-api/">catalog-api</a></td></tr><tr><td><a href="commerce-api/">Commerce API</a></td><td>Manage orders, subscriptions, assets, &#x26; more.</td><td><a href="commerce-api/">commerce-api</a></td></tr><tr><td><a href="currency-api/">Currency API</a></td><td>Work with currencies, pairs, and exchange rates.</td><td><a href="currency-api/">currency-api</a></td></tr><tr><td><a href="extensions-api/">Extensions API</a></td><td>Manage extensions, installations, media, &#x26; more.</td><td><a href="extensions-api/">extensions-api</a></td></tr><tr><td><a href="helpdesk-api/">Helpdesk API</a></td><td>Manage cases, chats, feedback, &#x26; more.</td><td><a href="helpdesk-api/">helpdesk-api</a></td></tr><tr><td><a href="notifications-api/">Notifications API</a></td><td>Manage notifications, subscribers, &#x26; more.</td><td><a href="notifications-api/">notifications-api</a></td></tr><tr><td><a href="product-catalog-api/">Product Catalog API</a></td><td>Browse software products, manage profile, categories, &#x26; more.</td><td><a href="product-catalog-api/">product-catalog-api</a></td></tr><tr><td><a href="program-api/">Program API</a></td><td>Manage programs, enrollments, and certificates.</td><td><a href="program-api/">program-api</a></td></tr><tr><td><a href="spotlight-objects-api/">Spotlight API</a></td><td>Work with spotlight objects and queries.</td><td><a href="spotlight-objects-api/">spotlight-objects-api</a></td></tr><tr><td><a href="task-api/">Task API</a></td><td>Create tasks and retrieve task logs and results.</td><td><a href="task-api/">task-api</a></td></tr></tbody></table>
