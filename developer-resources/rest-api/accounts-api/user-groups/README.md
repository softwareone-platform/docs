# User Group

The User Group object represents a user group in the Marketplace platform.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="140">Field</th><th width="125">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The primary identifier for the user group.</p><p>Example: UGR-1234-1234</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>A relative reference to the object within the API.</p><p>Example: /v1/accounts/groups/UGR-1234-1234</p></td></tr><tr><td>icon</td><td><code>string</code></td><td><p>The relative path to the token’s logo.</p><p>Example: /static/accounts/UGR-1234-1234/logo.png</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the user group.</p><p>Example: Stark Industries</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>A description of the group.</p><p>Example: Stark's marketing group</p></td></tr><tr><td>modules</td><td><a href="../module/#module-object"><code>module</code></a></td><td><p>The modules that the group members can access. </p><p>Example: Invoices</p></td></tr><tr><td>default</td><td><code>bool</code></td><td><p>Indicates if the user group is set as default within the account. There can be only one default user group per account.</p><p>Example: true</p></td></tr><tr><td>stats</td><td><code>stats</code></td><td><p>Statistics for the group. A group can be deleted only if the user count is 0.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "users": 123
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="USER GROUP OBJECT" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "UGR-5116-6265",
  "name": "Test-1",
  "description": "My finance group",
  "modules": [
    {
      "id": "MOD-1756-1452",
      "name": "Access management"
    },
    {
      "id": "MOD-9042-8216",
      "name": "Account management"
    }
  ],
  "icon": "https://picsum.photos/210/201",
  "default": true,
  "stats": {
    "users": 123
  }
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
