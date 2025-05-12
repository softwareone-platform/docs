# API Tokens

The API Token object represents an authentication token user in the Marketplace platform. The object contains the following properties:

<table data-full-width="false"><thead><tr><th width="145">Field</th><th width="100">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The primary API token identifier.</p><p>Example: TKN-1671-0642</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>Relative reference to the object in the API.</p><p>Example: /v1/accounts/accounts/ACC-1671-0642/tokens/TKN-4134-7330</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the token.</p><p>Example: Robot</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>A description of the token.</p><p>Example: Test token</p></td></tr><tr><td>status</td><td><code>string</code></td><td>Token's status. Possible values: <code>Active</code>, <code>Disabled</code>, or <code>Deleted</code>.</td></tr><tr><td>modules</td><td><a href="../module/#module-object"><code>Module</code></a></td><td>Module validation when creating API Token.</td></tr><tr><td>account</td><td><a href="../account/#account-object"><code>Account</code></a></td><td><p>The account under which the token has been defined.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
  "id": "ACC-123-123",
  "name": "Microsoft"
}
</code></pre></td></tr><tr><td>token</td><td><code>string</code></td><td>Token's authentication code.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="TOKEN OBJECT" %}
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
{% endtab %}
{% endtabs %}
