# Currency API

The **Currency API** manages everything related to currencies and exchange rates in the SoftwareOne Marketplace.&#x20;

With this API, you can define currencies, create currency pairs (for example, EUR:USD), and define and manage exchange rates for those pairs. You can also perform additional operations, including:&#x20;

* Updating the currency to modify fields like name, code, precision (not status).
* Delete a currency (only if not used by a pair), currency pair, or rate.
* Modify the `externalId` and `notes` within a currency pair.
* Modify the currency rate, for example, to override a rate for hedging.

## Core Concepts

The Currency API is built around the following core resources:

* **Currency** - Represents the `currency` that sellers use on the platform to invoice their products.
* **Pairs** - Represents a currency pair, for example `GBP:EUR`.
* **Rates** - Represents an exchange rate between two currencies, used by sellers to invoice their products.

## Collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.&#x20;

Refer to the following capability matrix to see which roles are authorized to perform specific operations within each collection:

### Currency

<table><thead><tr><th width="199">Capability</th><th width="120">Client</th><th width="130">Vendor</th><th width="121">Operations</th><th>Exchange Module</th></tr></thead><tbody><tr><td>List currencies</td><td>✅</td><td>✅</td><td>✅</td><td>❌</td></tr><tr><td>Get currency details</td><td>✅</td><td>✅</td><td>✅</td><td>❌</td></tr><tr><td>Create currency </td><td>❌</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Modify currency </td><td>❌</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Delete currency </td><td>❌</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### Pairs

<table><thead><tr><th width="202">Capability</th><th width="124">Client</th><th width="118">Vendor</th><th width="134">Operations</th><th>Exchange Module</th></tr></thead><tbody><tr><td>List pairs</td><td>✅</td><td>✅</td><td>✅</td><td>❌</td></tr><tr><td>Get pair details</td><td>✅</td><td>✅</td><td>✅</td><td>❌</td></tr><tr><td>Create pair</td><td>❌</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Modify pair</td><td>❌</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Delete pair</td><td>❌</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### Rates

<table><thead><tr><th width="221">Capability</th><th width="103">Client</th><th width="115">Vendor</th><th width="139">Operations</th><th>Exchange Module</th></tr></thead><tbody><tr><td>List rates for a pair</td><td>✅</td><td>✅</td><td>✅</td><td>❌</td></tr><tr><td>Get specific rate for a pair</td><td>✅</td><td>✅</td><td>✅</td><td>❌</td></tr><tr><td>Create rate for a pair</td><td>❌</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Modify rate for a pair</td><td>❌</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Delete rate for a pair</td><td>❌</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>
