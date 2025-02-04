# Requests

## Request object

<table><thead><tr><th width="241">Field</th><th width="167">Type</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p>Primary Request identifier </p><p></p><p>Example: "REQ-1671-0642"</p></td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td><p>Relative reference to object on API (always /v1/commerce/requests/{id}) </p><p></p><p>Example: "/v1/commerce/requests/REQ-1671-0642"</p></td></tr><tr><td><strong><code>status</code></strong></td><td>string</td><td><p>Status of the request. </p><p></p><p>Example: "Querying"</p></td></tr><tr><td><strong><code>client</code></strong></td><td><a href="../../accounts-api/account/#account-object">Account</a></td><td><p>Reference to client Account object. </p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{ 
  "id": "ACC-1234-4444",
  "name": "stark industries"
}
</code></pre></td></tr><tr><td><strong><code>vendor</code></strong></td><td><a href="../../accounts-api/account/#account-object">Account</a></td><td><p>Reference to vendor Account object. </p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{ 
  "id": "ACC-1234-1111",
  "name": "Microsoft"
}
</code></pre></td></tr><tr><td><strong><code>requester</code></strong></td><td><a href="../../accounts-api/users/#user-object">User</a></td><td><p>User of requester, in client account. </p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{ 
  "id": "USR-1234-4444",
  "name": "John Smith"
}
</code></pre></td></tr><tr><td><strong><code>assignee</code></strong></td><td><a href="../../accounts-api/users/#user-object">User</a></td><td><p>User of vendor who is responsible to processing request. </p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{ 
  "id": "USR-1234-1111",
  "name": "Santa Claus"
}
</code></pre></td></tr><tr><td><strong><code>product</code></strong></td><td>Product</td><td><p>Example:</p><pre class="language-json"><code class="lang-json">{
  "id": "PRD-1111-1111-1111",
  "href": "/catalog/products/PRD-1111-1111-1111",
  "name": "Microsoft Office 365 NCE",
  "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td><strong><code>externalIds</code></strong></td><td>ExternalIdsObject</td><td><p>Set of external IDs identifiers.</p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{
  "client": "12345678",
  "operations":	"07bf766b-c767-4293-9ab3",
  "vendor": "ABC-2023-C07-dbeee0b302c0"
}
</code></pre><p></p></td></tr><tr><td><strong><code>parameters.order</code></strong></td><td>ParameterValue[]</td><td><p>Request ordering parameters values </p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">[
  {
    "id": "PRM-1234-1234-1234-1234",
    "name": "Tennant Id",
    "externalId": "tennant_id",
    "constraints": { ... },
    "value": "69b73824-ce76-4866-ad47-b615ae9d8998",
  }
]
</code></pre></td></tr><tr><td><strong><code>error</code></strong></td><td>ErrorObject</td><td><p>Error reported by validation procedure. </p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{
     "id": "E001234",
     "message": "Agreement provisioning failed due to unavailability of the item"
}
</code></pre></td></tr><tr><td><strong><code>audit</code></strong></td><td>AuditObject</td><td><p>Audit object with possible entries: created, updated, activated, terminated, according to lifecycle of the object. </p><p></p><p>Possible audit events: Created, Updated, and Querying. </p><p></p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% tabs %}
{% tab title="SHORT FORM" %}
```json
{
  "id": "REQ-1671-0642",
  "href": "/commerce/requests/REQ-1671-0642",
  "status": "Querying",
  "client": { 
    "id": "ACC-1234-4444",
    "name": "Stark-industries"
  },
  "vendor": { 
    "id": "ACC-1234-1111",
    "name": "Microsoft"
  },
  "requester": { 
    "id": "USR-1234-4444",
    "name": "John Smith"
  },
  "assignee": { 
    "id": "USR-1234-1111",
    "name": "Santa Claus"
  },
  "product": {
    "id": "PRD-1111-1111-1111",
    "href": "/catalog/products/PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
  }
}
```
{% endtab %}

{% tab title="FULL EXAMPLE" %}
```json
{
  "id": "REQ-1671-0642",
  "href": "/commerce/requests/REQ-1671-0642",
  "status": "Querying",
  "client": { 
    "id": "ACC-1234-4444",
    "name": "Stark-industries"
  },
  "vendor": { 
    "id": "ACC-1234-1111",
    "name": "Microsoft"
  },
  "requester": { 
    "id": "USR-1234-4444",
    "name": "John Smith"
  },
  "assignee": { 
    "id": "USR-1234-1111",
    "name": "Santa Claus"
  },
  "product": {
    "id": "PRD-1111-1111-1111",
    "href": "/catalog/products/PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
  },
  "externalIds": {
    "client": "12345678",
    "operations":	"07bf766b-c767-4293-9ab3",
    "vendor": "ABC-2023-C07-dbeee0b302c0"
  },
  "audit": {
    "created": { "at": "2023-12-14T17:28:57.667Z", "by": { "id": "USR-1234-1234", "name": "John Smith" } },
    "updated": { "at": "2023-12-14T17:28:57.667Z", "by": { "id": "USR-1234-1234", "name": "John Smith" } }
  }
}
```
{% endtab %}
{% endtabs %}
