# Module

The Module object represents a module in the Marketplace platform.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false" data-search="false"><thead><tr><th width="194">Field</th><th width="136">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) Primary identifier for the module. </td></tr><tr><td><code>name</code></td><td>string, core</td><td>(Read-only) Name of the module. </td></tr><tr><td><code>description</code></td><td>string, core</td><td>(Read-only)  A description of the module.</td></tr><tr><td><code>accountTypes</code></td><td>string</td><td>(Read-only)  Indicates the module availability for the account type. </td></tr><tr><td><code>isEnabledByDefault</code></td><td>boolean</td><td>(Read-only) Indicates whether the module is enabled by default.</td></tr><tr><td><code>isConfigurable</code></td><td>boolean</td><td>(Read-only)  Indicates whether module access can be changed. </td></tr><tr><td><code>paid</code></td><td>boolean, core</td><td>(Read-only) Indicates whether the module is fee-based.</td></tr><tr><td><code>settings</code></td><td>object, core</td><td><p>(Read-only) Defines the module setting.</p><ul><li><code>sharedAccount</code> – Defines whether there are multiple accounts with the same external ID.</li><li><code>configurable</code> – Defines whether the module access can be changed.</li><li><code>default</code> – Defines whether the module is enabled by default.</li><li><code>paid</code> – Defines whether the module is fee-based.</li></ul></td></tr><tr><td><code>filters</code></td><td>object, core</td><td>(Read-only) Defines the custom filters configuration.</td></tr></tbody></table>

## Example

{% code title="MODULE OBJECT" lineNumbers="true" %}
```json
{
  "id": "MOD-1234",
  "name": "Invoices",
  "description": "Invoices module",
  "accountTypes": ["vendor", "client", "operations"],
  "isEnabledByDefault": true,
  "isConfigurable": false,
  "paid": true,
  "settings": {
    "sharedAccount": true,
    "configurable": true,
    "default": true,
    "paid": false
  },
  "filters": {
    "group.buyers": [
      "selected",
      "all"
    ]
  }
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
