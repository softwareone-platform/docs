# Module

## Module Object

The `module` object represents a module in the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th>Field</th><th width="141">Type</th><th width="218">Constraints</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p><code>READONLY</code> </p><p><code>IDX</code></p><p><code>CORE</code></p></td><td><p>Primary module identifier. </p><p></p><p>Example: "MOD-1234"</p></td></tr><tr><td><strong><code>name</code></strong></td><td>string</td><td><p><code>READONLY</code> </p><p><code>IDX</code></p><p><code>CORE</code></p></td><td><p>Name of the module. </p><p></p><p>Example: "Invoices"</p></td></tr><tr><td><strong><code>description</code></strong></td><td>string</td><td><p><code>READONLY</code></p><p><code>IDX</code></p><p><code>OPTIONAL</code></p></td><td><p>Description of the module. </p><p></p><p>Example: "Invoices module"</p></td></tr><tr><td><strong><code>accountTypes</code></strong></td><td>string</td><td><code>READONLY</code></td><td><p>Defines presence of module for each account type. </p><p></p><p>Example: ["vendor", "client", "operations"]</p></td></tr><tr><td><strong><code>isEnabledByDefault</code></strong></td><td>boolean</td><td><code>READONLY</code></td><td><p>Defines whether the module is enabled by default. </p><p></p><p>Example: "true"</p></td></tr><tr><td><strong><code>isConfigurable</code></strong></td><td>boolean</td><td><code>READONLY</code></td><td><p>Defines whether module’s access can be changed. </p><p></p><p>Example: "true"</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="MODULE OBJECT" %}
{% code lineNumbers="true" %}
```json
{
  "id": "MOD-1234",
  "name": "Invoices",
  "description": "Invoices module",
  "accountTypes": ["vendor", "client", "operations"],
  "isEnabledByDefault": true,
  "isConfigurable": false
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
