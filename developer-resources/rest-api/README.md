# REST API

The Marketplace Platform REST API lets you interact with the platform programmatically.&#x20;

Our API is organized around REST, has predictable resource-oriented URLs, uses [JSON-encoded](http://www.json.org/) representations, and standard [HTTP response codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes), authentication, and verbs.&#x20;

The platform offers several REST APIs for tasks, like managing orders and viewing users and accounts. Each API works similarly, whether you access it directly over HTTP or through helper libraries in various programming languages.

### Authentication

The Marketplace Platform uses [API tokens](../../modules-and-features/settings/api-tokens/) to authenticate requests. You can view and manage your API keys in the user interface of your account settings. Include your API token in the '**Authorization'** HTTP header with the '**Bearer**' prefix for authentication.&#x20;

For example, the following request could be used to retrieve a list of buyers:

```http
GET https://api.platform.softwareone.com/public/v1/accounts/buyers
Authorization: Bearer {TOKEN_VALUE}
```

Your API keys have permissions assigned to them, so keep them secure. Don't share your secret API keys in public areas, like GitHub or client-side code.

All API requests must be made over HTTPS. Calls made over plain HTTP will fail. API requests without authentication will also fail.

### Content type

The Marketplace Platform API expects the **content type** of API requests to be '**application/json**' in most cases (except for cases where 'multipart/form-data' is used to send attachments)

```http
GET https://api.platform.softwareone.com/public/v1/accounts/buyers
Authorization: Bearer {TOKEN_VALUE}
Content-Type: application/json
```

To communicate successfully with the Marketplace Platform APIs, ensure your API requests are formatted using the '**application/json**' content type. Using the wrong content type can result in unexpected behavior or errors.

### Overview video

Watch a short overview of how the Marketplace API works and how to get started.

{% embed url="https://youtu.be/uy5UABU3IW0?si=Sk920vUhK7fToww1" %}
Watch this video guide about working with Marketplace API.
{% endembed %}

### Browse APIs

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><a href="accounts-api/">Accounts API</a></td><td>Manage accounts, users, groups, &#x26; more. </td><td><a href="accounts-api/">accounts-api</a></td></tr><tr><td><a href="audit-api/">Audit API</a></td><td>Track and retrieve audit activity.</td><td><a href="audit-api/">audit-api</a></td></tr><tr><td><a href="billing-api/">Billing API</a></td><td>Work with invoices, statements, charges, &#x26; more.</td><td><a href="billing-api/">billing-api</a></td></tr><tr><td><a href="catalog-api/">Catalog API</a></td><td>Manage catalog, products, items, &#x26; more.</td><td><a href="catalog-api/">catalog-api</a></td></tr><tr><td><a href="commerce-api/">Commerce API</a></td><td>Manage orders, subscriptions, assets, &#x26; more.</td><td><a href="commerce-api/">commerce-api</a></td></tr><tr><td><a href="currency-api/">Currency API</a></td><td>Work with currencies, pairs, and exchange rates.</td><td><a href="currency-api/">currency-api</a></td></tr><tr><td><a href="extensions-api/">Extensions API</a></td><td>Manage extensions, installations, media, &#x26; more.</td><td><a href="extensions-api/">extensions-api</a></td></tr><tr><td><a href="helpdesk-api/">Helpdesk API</a></td><td>Manage cases, chats, feedback, &#x26; more.</td><td><a href="helpdesk-api/">helpdesk-api</a></td></tr><tr><td><a href="notifications-api/">Notifications API</a></td><td>Manage notifications, subscribers, &#x26; more.</td><td><a href="notifications-api/">notifications-api</a></td></tr><tr><td><a href="product-catalog-api/">Product Catalog API</a></td><td>Browse software products, manage profile, categories, &#x26; more.</td><td><a href="product-catalog-api/">product-catalog-api</a></td></tr><tr><td><a href="program-api/">Program API</a></td><td>Manage programs, enrollments, and certificates.</td><td><a href="program-api/">program-api</a></td></tr><tr><td><a href="spotlight-objects-api/">Spotlight API</a></td><td>Work with spotlight objects and queries.</td><td><a href="spotlight-objects-api/">spotlight-objects-api</a></td></tr><tr><td><a href="task-api/">Task API</a></td><td>Create tasks and retrieve task logs and results.</td><td><a href="task-api/">task-api</a></td></tr></tbody></table>
