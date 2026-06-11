# API Token

An API Token represents a user authentication token within the platform.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="174">Field</th><th width="154">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The primary identifier for the token.</td></tr><tr><td><code>name</code></td><td>string, core</td><td>The name of the token.</td></tr><tr><td><code>description</code></td><td>string</td><td>(Optional) A description of the token.</td></tr><tr><td><code>icon</code></td><td>string, core</td><td>(Optional) The relative path to the API token icon.</td></tr><tr><td><code>status</code></td><td>string</td><td><p>(Read-only) The token's status. Allowed values: </p><ul><li><code>Active</code></li><li><code>Disabled</code></li><li><code>Deleted</code></li></ul></td></tr><tr><td><code>modules</code></td><td><a href="../module/#module-object">module</a></td><td>Module validation when creating API token.</td></tr><tr><td><code>account</code></td><td>object</td><td><p>Represents the <a href="../account/#account-object">account</a> object under which the token has been defined.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "ACC-123-123",
  "name": "Microsoft"
}
</code></pre></td></tr><tr><td><code>token</code></td><td>string</td><td>(Read-only) The token's authentication code.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Example

{% code title="API TOKEN OBJECT" lineNumbers="true" %}
```json
{
    "id": "TKN-4134-7330",
    "name": "access token",
    "description": "Token for Marketplace",
    "icon": "",
    "status": "Active",
    "modules": [
        {
            "id": "MOD-1756-1452"
        },
        {
            "id": "MOD-9042-8216"
        }
    ],
    "token": "CODE"
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
