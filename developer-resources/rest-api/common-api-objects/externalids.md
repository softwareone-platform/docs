# ExternalIds

The ExternalIds object contains a set of external identifiers. ExternalIDs are assigned during a PUT (update) or POST (create) request. Clients can update only their own External IDs,&#x20;Vendors can update only their own External IDs, and SoftwareOne Operations can update only the ID related to their specific operation.

<table><thead><tr><th width="193">Field</th><th width="107">Type</th><th>Description</th></tr></thead><tbody><tr><td>externalIds.client</td><td><code>string</code></td><td>The client-specific external ID, visible to clients.</td></tr><tr><td>externalIds.operations</td><td><code>string</code></td><td>The operations-specific external Id, visible to operations.</td></tr><tr><td>externalIds.vendor</td><td><code>string</code></td><td>The vendor-specific external Id, visible for vendors.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="EXTERNALID OBJECT" %}
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
