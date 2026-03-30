# Module

The Module object represents a module in the Marketplace platform.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="183">Field Name</th><th width="124">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary module identifier. </p><p>Example: MOD-1234</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the module. </p><p>Example: Invoices</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the module. </p><p>Example: Invoices module</p></td></tr><tr><td><code>accountTypes</code></td><td>string</td><td><p>Defines the presence of the module for each account type. </p><p>Example: Vendor</p></td></tr><tr><td><code>isEnabledByDefault</code></td><td>boolean</td><td><p>Defines whether the module is enabled by default. </p><p>Example: true</p></td></tr><tr><td><code>isConfigurable</code></td><td>boolean</td><td><p>Defines whether the module’s access can be changed. </p><p>Example: true</p></td></tr></tbody></table>

## Example response

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
