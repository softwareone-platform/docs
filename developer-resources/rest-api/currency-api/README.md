# Currency API

The **Currency API** manages everything related to currencies and exchange rates in the SoftwareOne Marketplace.&#x20;

With this API, you can define currencies, create currency pairs (for example, EUR: USD), and define and manage exchange rates for those pairs. You can also perform additional operations, including:&#x20;

* Updating the currency to modify fields like name, code, and precision (not status).
* Delete a currency (only if not used by a pair), currency pair, or rate.
* Modify the `externalId` and `notes` within a currency pair.
* Modify the currency rate, for example, to override a rate for hedging.

## Before you start

Review the shared API docs before you work with currency resources.

* [Authentication](../)
* [URL structure](../../api-usage-and-reference/url-structure.md)
* [Error handling](../../api-usage-and-reference/errors-handling.md)

## Core concepts

The Currency API is built around the following core resources:

* **Currency** – Represents the `currency` that sellers use to invoice their products.
* **Pairs** – Represents a currency pair, for example `GBP:EUR`.
* **Rates** – Represent an exchange rate between two currencies, used by sellers to invoice their products.

## Browse collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.&#x20;

See the following sections to determine which roles are authorized to perform specific operations within each collection:

### Currency

<table><thead><tr><th width="198">Operation</th><th width="134">Method</th><th>Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="currency/create-currency.md">Create currency</a></td><td>POST</td><td>Creates a new currency.</td><td>ops, exchange-module</td></tr><tr><td><a href="currency/list-currencies.md">List currencies</a></td><td>GET</td><td>Gets a list of currencies.</td><td>vendor, client, ops</td></tr><tr><td><a href="currency/get-currency.md">Get currency by id</a></td><td>GET</td><td>Gets currency details.</td><td>vendor, client, ops</td></tr><tr><td><a href="currency/update-currency.md">Modify currency</a></td><td>PUT</td><td>Modifies an existing currency.</td><td>ops, exchange-module</td></tr><tr><td><a href="currency/delete-currency.md">Delete currency</a></td><td>DELETE</td><td>Changes a currency’s status to deleted.</td><td>ops, exchange-module</td></tr></tbody></table>

### Pairs

<table><thead><tr><th width="213">Operation</th><th width="121">Method</th><th>Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="pair/create-currency-pair.md">Create currency pair</a></td><td>POST</td><td>Creates matched pairs.</td><td>ops, exchange-module</td></tr><tr><td><a href="pair/list-currency-pairs.md">List currency pairs</a></td><td>GET</td><td>Gets a list of pairs.</td><td>vendor, client, ops</td></tr><tr><td><a href="pair/get-currency-pair.md">Get currency pair by id</a></td><td>GET</td><td>Gets pair details.</td><td>vendor, client, ops</td></tr><tr><td><a href="pair/update-currency-pair.md">Update currency pairs</a></td><td>PUT</td><td>Modifies pairs.</td><td>ops, exchange-module</td></tr><tr><td><a href="pair/delete-currency-pairs.md">Delete currency pairs</a></td><td>DELETE</td><td>Modifies the status of pairs to deleted.</td><td>ops, exchange-module</td></tr></tbody></table>

### Rates

<table><thead><tr><th width="192">Operation</th><th width="120">Method</th><th>Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="rate/create-rate.md">Bulk create rates</a></td><td>POST</td><td>Creates matched rates.</td><td>ops, exchange-module</td></tr><tr><td><a href="rate/list-rates.md">List rates</a></td><td>GET</td><td>Gets a list of rates between two currencies.</td><td>vendor, client, ops</td></tr><tr><td><a href="rate/get-rate.md">Get rate by id</a></td><td>GET</td><td>Gets a specific rate between two currencies at a given point in time.</td><td>vendor, client, ops</td></tr><tr><td><a href="rate/modify-rates.md">Bulk update rates</a></td><td>PUT</td><td>Modifies matched rates.</td><td>ops, exchange-module</td></tr><tr><td><a href="rate/delete-rates.md">Bulk delete rates</a></td><td>DELETE</td><td>Modifies the status of matched rates to deleted.</td><td>ops, exchange-module</td></tr></tbody></table>
