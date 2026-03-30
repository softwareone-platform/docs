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

<a href="https://editor.swagger.io/?url=https://api.platform.softwareone.com/public/v1/spotlight/openapi.json" class="button primary">Try API</a><a href="https://api.platform.softwareone.com/public/v1/spotlight/openapi.json" class="button secondary">Download API</a>

## Core Concepts

The Spotlight API is built around the following core resources:

* **SpotlightObject** - Represents a collection of spotlighted objects.
* **SpotlightTopItem** - Represents individual top result items identified by `spotlightQuery`.
* **SpotlightQuery** - Represents the search query used to retrieve spotlighted data.

## Collection

The API is organized into a single collection, containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.&#x20;

Refer to the following capability matrix to see which roles are authorized to perform specific operations within this collection:

<table><thead><tr><th width="297">Capability</th><th width="152">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List spotlighted objects</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Invalidate a specific spotlight object</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Invalidates all cache objects</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

