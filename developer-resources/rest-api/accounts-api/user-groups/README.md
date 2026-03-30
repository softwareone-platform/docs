# User Group

The User Group or Group object represents a user group in the Marketplace platform.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="140">Field Name</th><th width="125">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary identifier for the user group.</p><p>Example: UGR-1234-1234</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>A relative reference to the object within the API.</p><p>Example: /v1/accounts/groups/UGR-1234-1234</p></td></tr><tr><td><code>icon</code></td><td>string</td><td><p>The relative path to the token’s logo.</p><p>Example: /static/accounts/UGR-1234-1234/logo.png</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the user group.</p><p>Example: Stark Industries</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the group.</p><p>Example: Stark's marketing group</p></td></tr><tr><td><code>modules</code></td><td><a href="../module/#module-object">module</a></td><td><p>The <a href="../module/#module-object">modules</a> that the group members can access. </p><p>Example: Invoices</p></td></tr><tr><td><code>default</code></td><td>bool</td><td><p>Indicates if the user group is set as default within the account. There can be only one default user group per account.</p><p>Example: true</p></td></tr><tr><td><code>stats</code></td><td>stats</td><td><p>Statistics for the group. A group can be deleted only if the user count is <code>0</code>.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "users": 123
}
</code></pre></td></tr></tbody></table>

## Example response

{% code lineNumbers="true" %}
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
