# API tokens

## Token Object

The `token` object represents an authentication token user in the Marketplace platform. This object contains the following properties:

<table data-full-width="false"><thead><tr><th>Field</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p>Primary API token identifier. </p><p></p><p>Example: "TKN-1671-0642"</p></td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td><p>Relative reference to object on API. </p><p></p><p>Example:  "/v1/accounts/accounts/ACC-1671-0642/tokens/TKN-4134-7330"</p></td></tr><tr><td><strong><code>name</code></strong></td><td>string</td><td><p>Name of the token. </p><p></p><p>Example: "Robot"</p></td></tr><tr><td><strong><code>description</code></strong></td><td>string</td><td><p>Token description.  </p><p></p><p>Example: "Test token"</p></td></tr><tr><td><strong><code>status</code></strong></td><td>string</td><td>Status of the token: Active,  Disabled, Deleted</td></tr><tr><td><strong><code>modules</code></strong></td><td><a href="../module/#module-object">Module</a></td><td>At least one modules validation when creating API Token.</td></tr><tr><td><strong><code>account</code></strong></td><td><a href="../account/#account-object">Account</a></td><td><p>Account under which the token has been defined. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "id": "ACC-123-123",
  "name": "Microsoft"
}
</code></pre></td></tr><tr><td><strong><code>token</code></strong></td><td>string</td><td>Authentication code.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="TOKEN OBJECT" %}
{% code lineNumbers="true" %}
```json
{
    "id": "TKN-4134-7330",
    "href": "/v1/accounts/accounts/ACC-1671-0642/tokens/TKN-4134-7330",
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
{% endtab %}
{% endtabs %}
