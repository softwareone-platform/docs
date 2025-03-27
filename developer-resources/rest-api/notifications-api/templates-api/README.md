# Templates API

## Template object

<table><thead><tr><th width="171">Field</th><th width="195">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Primary template identifier. </p><p></p><p>Example: TPL-5433-8787</p></td></tr><tr><td>href</td><td>string</td><td><p>Relative reference to object inside MPT API (always <code>/notifications/template/{id}</code>) </p><p></p><p>Example: /notifications/template/TPL-5433-8787</p></td></tr><tr><td>objectId</td><td>string</td><td><p>Id of an object this template should be used with, i.e., Product for order templates. </p><p></p><p>Example: PRD-3928-3231</p></td></tr><tr><td>objectType</td><td>enum</td><td><p>Type of an object this template should be rendered with. </p><p></p><p>Example: Order</p></td></tr><tr><td>objectStatus</td><td>string</td><td><p>Status of an object this template should be rendered with. </p><p></p><p>Example: Draft</p></td></tr><tr><td>default</td><td>boolean</td><td><p>If this is template is default template for specific combination of <code>objectId</code>, <code>objectType</code> and <code>objectStatus.</code></p><p></p><p>Example: false</p></td></tr><tr><td>account</td><td>Account</td><td><p>Reference to vendor Account object<br>filled in on creation according to user current account. </p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "href": "/accounts/accounts/ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>audit</td><td>AuditObject</td><td><p>Audit object with possible entries: created, updated, enabled, disabled according to the lifecycle of the object. </p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json"> {
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } },
  "enabled": { "at": "...", "by": { } },
  "disabled": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="Template Object" %}
```json
{
  "id": "TPL-5433-8787",
  "href": "/notifications/templates/TPL-5433-8787",
  "objectId": "PRD-3288-8799",
  "objectType": "order",
  "objectStatus": "draft",
  "default": "false",
  "content": "This is my new product template {{ PRM-3231-8989 }}",
  "audit": {
    "created": { "at": "...", "by": { } },
    "updated": { "at": "...", "by": { } }
  }
}
```
{% endtab %}
{% endtabs %}
