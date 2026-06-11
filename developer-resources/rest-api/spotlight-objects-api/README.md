---
description: Use the Spotlight API to highlight key platform objects requiring attention.
---

# Spotlight API

The **Spotlight API** provides endpoints designed to highlight key platform objects that may need attention. These objects can include agreements, orders, subscriptions, invoices, and more.

The API consists of two primary endpoints: `spotlightObject` and `spotlightQuery`. With this API, you can:

* List all spotlighted objects.
* Invalidate or clear the cache for Spotlight objects.
* List the defined spotlight queries.
* Get details for a specific spotlight query.
* Update an existing spotlight query.

### Before you start <a href="#before-you-start" id="before-you-start"></a>

Review the shared API docs before you work with the spotlight resources.

* [Authentication](https://docs.platform.softwareone.com/~/changes/476/developer-resources/api-reference)
* [URL structure](https://docs.platform.softwareone.com/~/changes/476/developer-resources/guides/url-structure)
* [Error handling](https://docs.platform.softwareone.com/~/changes/476/developer-resources/guides/errors-handling)

### Core resources

The Spotlight API is built around the following core resources:

* **SpotlightObject** – Represents a collection of spotlighted objects.
* **SpotlightTopItem** – Represents individual top result items identified by `spotlightQuery`.
* **SpotlightQuery** – Represents the search query used to retrieve spotlighted data.

### Browse collection

The API is organized into a single collection containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.&#x20;

Refer to the following capability matrix to see which roles are authorized to perform specific operations within this collection:

<table><thead><tr><th width="231">Operation</th><th width="133">Method</th><th>Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="spotlight-object/list-spotlighted-objects.md">List spotlight objects</a></td><td>GET</td><td>Returns a list of spotlight result objects filtered by RQL query.</td><td>vendor, client, ops</td></tr><tr><td><a href="spotlight-object/invalidate-all-cache.md">Invalidate all cache</a></td><td>POST</td><td>Invalidates all cache keys for the account and buyer group.</td><td>vendor, client, ops</td></tr><tr><td><a href="spotlight-object/invalidate-cache.md">Invalidates cache</a></td><td>POST</td><td>Invalidates cache for a specific spotlight object.</td><td>vendor, client, ops</td></tr><tr><td><a href="spotlight-query/list-spotlight-queries.md">List spotlight queries</a></td><td>POST</td><td>Returns a list of spotlight queries.</td><td>vendor, client, ops</td></tr><tr><td><a href="spotlight-query/get-spotlight-query.md">Get spotlight query</a></td><td>GET</td><td>Gets a spotlight query.</td><td>vendor, client, ops</td></tr><tr><td><a href="spotlight-query/update-spotlight-query.md">Update spotlight query</a></td><td>PUT</td><td>Updates the definition or configuration of a spotlight query.</td><td>vendor, client, ops</td></tr></tbody></table>

