# Request

The Request object contains the following properties:

<table><thead><tr><th width="178">Field Name</th><th width="167">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary identifier for the request.</p><p>Example: REQ-1671-0642</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>Relative reference to the object in the API.</p><p>Example: /v1/commerce/requests/REQ-1671-0642</p></td></tr><tr><td><code>status</code></td><td>string</td><td><p>The status of the request.</p><p>Example: Querying</p></td></tr><tr><td><code>client</code></td><td>object</td><td><p>A reference to the client <a href="../../accounts-api/account/#account-object"><code>account</code></a>object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ 
  "id": "ACC-1234-4444",
  "name": "stark industries"
}
</code></pre></td></tr><tr><td><code>vendor</code></td><td>object</td><td><p>A reference to the vendor <a href="../../accounts-api/account/"><code>account</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ 
  "id": "ACC-1234-1111",
  "name": "Microsoft"
}
</code></pre></td></tr><tr><td><code>requester</code></td><td>object</td><td><p>The client account <a href="../../accounts-api/users/#user-object"><code>user</code></a> who created the request.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ 
  "id": "USR-1234-4444",
  "name": "John Smith"
}
</code></pre></td></tr><tr><td><code>assignee</code></td><td>object</td><td><p>The vendor account <a href="../../accounts-api/users/#user-object"><code>user</code></a>  responsible for processing the request.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ 
  "id": "USR-1234-1111",
  "name": "Santa Claus"
}
</code></pre></td></tr><tr><td><code>product</code></td><td>object</td><td><p>A reference to the <a href="../../catalog-api/product/"><code>product</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "PRD-1111-1111-1111",
  "name": "Microsoft Office 365 NCE",
  "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td><code>externalIds</code></td><td>object</td><td><p>A set of <code>externalID</code> identifiers.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "client": "12345678",
  "operations":	"07bf766b-c767-4293-9ab3",
  "vendor": "ABC-2023-C07-dbeee0b302c0"
}
</code></pre></td></tr><tr><td><code>parameters.order</code></td><td>object</td><td><p>The values of the <a href="../../common-api-objects/order-parameter.md"><code>orderParameter</code></a> associated with the request.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "PRM-1234-1234-1234-1234",
    "name": "Tennant Id",
    "externalId": "tenant_id",
    "constraints": { ... },
    "value": "69b73824-ce76-4866-ad47-b615ae9d8998",
  }
]
</code></pre></td></tr><tr><td><code>error</code></td><td>object</td><td><p>Error reported by validation procedure.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
     "id": "E001234",
     "message": "Agreement provisioning failed due to unavailability of the item"
}
</code></pre></td></tr><tr><td><code>audit</code></td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. Allowed values: <code>created</code>, <code>updated</code>, <code>activated</code>, or <code>terminated</code> .</td></tr></tbody></table>

## Example response <a href="#example" id="example"></a>

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
