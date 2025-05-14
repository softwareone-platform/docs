# Modules

The Module object represents a module in the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th width="172">Field</th><th width="100">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The primary module identifier. </p><p>Example: MOD-1234</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the module. </p><p>Example: Invoices</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>A description of the module. </p><p>Example: Invoices module</p></td></tr><tr><td>accountTypes</td><td><code>string</code></td><td><p>Defines the presence of the module for each account type. </p><p>Example: Vendor</p></td></tr><tr><td>isEnabledByDefault</td><td><code>boolean</code></td><td><p>Defines whether the module is enabled by default. </p><p>Example: true</p></td></tr><tr><td>isConfigurable</td><td><code>boolean</code></td><td><p>Defines whether the module’s access can be changed. </p><p>Example: true</p></td></tr></tbody></table>

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
