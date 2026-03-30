# API Token

The API Token object represents a user authentication token within the platform.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="145">Field Name</th><th width="139">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary identifier for the token.</p><p>Example: TKN-1671-0642</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>The relative reference to the object in the API.</p><p>Example: /v1/accounts/accounts/ACC-1671-0642/tokens/TKN-4134-7330</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the token.</p><p>Example: Robot</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the token.</p><p>Example: Test token</p></td></tr><tr><td><code>status</code></td><td>string</td><td>The token's status. Allowed values: <code>active</code>, <code>disabled</code>, or  <code>deleted</code>. </td></tr><tr><td><code>modules</code></td><td><a href="../module/#module-object">module</a></td><td>Module validation when creating API Token.</td></tr><tr><td><code>account</code></td><td><a href="../account/#account-object">account</a></td><td><p>The account under which the token has been defined.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "ACC-123-123",
  "name": "Microsoft"
}
</code></pre></td></tr><tr><td><code>token</code></td><td>string</td><td>The token's authentication code.</td></tr></tbody></table>

## Example response

{% code lineNumbers="true" %}
```json
{
    "id": "TKN-4134-7330",
    "name": "Name",
    "description": "Description",
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
