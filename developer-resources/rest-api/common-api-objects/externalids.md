# External IDs

The `External IDs` object contains a set of external identifiers.&#x20;

External IDs are assigned during a `PUT` (update) or `POST` (create) request. Clients can update only their own External IDs,&#x20;
Vendors can update only their own External IDs, and SoftwareOne Operations can update only the ID related to their specific operation.

<table><thead><tr><th width="193">Field</th><th width="107">Type</th><th>Description</th></tr></thead><tbody><tr><td>externalIds.client</td><td><code>string</code></td><td>The client-specific external ID, visible to clients.</td></tr><tr><td>externalIds.operations</td><td><code>string</code></td><td>The operations-specific external Id, visible to operations.</td></tr><tr><td>externalIds.vendor</td><td><code>string</code></td><td>The vendor-specific external Id, visible for vendors.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="EXTERNAL ID OBJECT" %}
{% code lineNumbers="true" %}
```json
{
  "client": "12345678",
  "operations":	"07bf766b-c767-4293-9ab3",
  "vendor": "ABC-2023-C07-dbeee0b302c0"
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

## Semantics and typical usage

Many resources (agreements, orders, subscriptions, etc.) expose an **externalIds** property. It stores key identifiers from actors that interact with the object but are not part of the marketplace (vendor, client, operations). Each actor can set and see only their own key; the meaning of each key depends on the resource and the actor.

- **externalIds.vendor** — On agreements and related resources, the vendor often stores the **external unique identifier of the contract** in their system (e.g. Microsoft account ID, Adobe client ID). Use it to correlate platform objects with vendor-side contracts or systems.
- **externalIds.client** — The client can use this for **programmatic access** or to store a reference that matters on their side (e.g. blanket order ID, open order ID, or an internal reference). Useful when looking up an order or agreement "by our reference" or "by our ID".
- **externalIds.operations** — Used by SoftwareOne operations for their own identifiers and processes.

Which keys exist and who can read/write them depends on the resource and the caller; check the resource schema and visibility rules. To filter by an external ID in RQL, use the field path (e.g. `eq(externalIds.vendor,"ABC-123")` or `eq(externalIds.client,"my-ref-456")`) when the resource exposes it.
