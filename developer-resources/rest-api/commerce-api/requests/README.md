# Requests

The Request object contains the following properties:

<table><thead><tr><th width="178">Field</th><th width="167">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>Primary identifier for the request.</p><p>Example: REQ-1671-0642</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>Relative reference to the object in the API.</p><p>Example: /v1/commerce/requests/REQ-1671-0642</p></td></tr><tr><td>status</td><td><code>string</code></td><td><p>The status of the request.</p><p>Example: Querying</p></td></tr><tr><td>client</td><td><a href="../../accounts-api/account/#account-object"><code>account</code></a></td><td><p>A reference to the client account object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{ 
  "id": "ACC-1234-4444",
  "name": "stark industries"
}
</code></pre></td></tr><tr><td>vendor</td><td><a href="../../accounts-api/account/"><code>account</code></a></td><td><p>A reference to the vendor account object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{ 
  "id": "ACC-1234-1111",
  "name": "Microsoft"
}
</code></pre></td></tr><tr><td>requester</td><td><a href="../../accounts-api/users/#user-object"><code>user</code></a></td><td><p>The client account user who created the request.</p><p>Example:</p><pre class="language-json"><code class="lang-json">{ 
  "id": "USR-1234-4444",
  "name": "John Smith"
}
</code></pre></td></tr><tr><td>assignee</td><td><a href="../../accounts-api/users/#user-object"><code>user</code></a></td><td><p>The vendor account user responsible for processing the request.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{ 
  "id": "USR-1234-1111",
  "name": "Santa Claus"
}
</code></pre></td></tr><tr><td>product</td><td><a href="../../catalog-api/product/"><code>product</code></a></td><td><p>A reference to the Product object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
  "id": "PRD-1111-1111-1111",
  "name": "Microsoft Office 365 NCE",
  "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>externalIds</td><td><code>object</code></td><td><p>A set of external ID identifiers.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
  "client": "12345678",
  "operations":	"07bf766b-c767-4293-9ab3",
  "vendor": "ABC-2023-C07-dbeee0b302c0"
}
</code></pre></td></tr><tr><td>parameters.order</td><td><a href="../../common-api-objects/order-parameter.md"><code>orderParameter</code></a></td><td><p>The values of the ordering parameters associated with the request.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">[
  {
    "id": "PRM-1234-1234-1234-1234",
    "name": "Tennant Id",
    "externalId": "tenant_id",
    "constraints": { ... },
    "value": "69b73824-ce76-4866-ad47-b615ae9d8998",
  }
]
</code></pre></td></tr><tr><td>error</td><td><code>errorObject</code></td><td><p>Error reported by validation procedure.</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
     "id": "E001234",
     "message": "Agreement provisioning failed due to unavailability of the item"
}
</code></pre></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td><p>A reference to the Audit object.</p><p>Possible values: <code>Created</code>, <code>Updated</code>, <code>Activated</code>, <code>Terminated</code> .</p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% tabs %}
{% tab title="SHORT FORM" %}
{% code lineNumbers="true" %}
```json
{
  "id": "REQ-1671-0642",
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
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
  }
}
```
{% endcode %}
{% endtab %}

{% tab title="FULL EXAMPLE" %}
{% code lineNumbers="true" %}
```json
{
  "id": "REQ-1671-0642",
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
{% endcode %}
{% endtab %}
{% endtabs %}
