# Module

The Module object represents a module in the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th width="191">Field</th><th width="100">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Primary module identifier. </p><p></p><p>Example: MOD-1234</p></td></tr><tr><td>name</td><td>string</td><td><p>Name of the module. </p><p></p><p>Example: Invoices</p></td></tr><tr><td>description</td><td>string</td><td><p>Description of the module. </p><p></p><p>Example: Invoices module</p></td></tr><tr><td>accountTypes</td><td>string</td><td><p>Defines the presence of the module for each account type. </p><p></p><p>Example: Vendor</p></td></tr><tr><td>isEnabledByDefault</td><td>boolean</td><td><p>Defines whether the module is enabled by default. </p><p></p><p>Example: true</p></td></tr><tr><td>isConfigurable</td><td>boolean</td><td><p>Defines whether the module’s access can be changed. </p><p></p><p>Example: true</p></td></tr></tbody></table>

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
