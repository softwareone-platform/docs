# Request

The Request object contains the following properties:

<table data-search="false"><thead><tr><th width="170">Field</th><th width="137">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The primary identifier for the request.</td></tr><tr><td><code>status</code></td><td>string</td><td>The status of the request.</td></tr><tr><td><code>client</code></td><td>object</td><td>Represents the client <a href="../../accounts-api/account/#account-object"><code>account</code></a>object.</td></tr><tr><td><code>vendor</code></td><td>object</td><td>Represents the vendor <a href="../../accounts-api/account/"><code>account</code></a> object</td></tr><tr><td><code>requester</code></td><td>object</td><td>The client account <a href="../../accounts-api/users/#user-object"><code>user</code></a> who created the request.</td></tr><tr><td><code>assignee</code></td><td>object</td><td>(Optional) The vendor account <a href="../../accounts-api/users/#user-object"><code>user</code></a>  responsible for processing the request.</td></tr><tr><td><code>product</code></td><td>object</td><td>Represents the <a href="../../catalog-api/product/"><code>product</code></a> object.</td></tr><tr><td><code>externalIds</code></td><td>object</td><td>(Optional) A set of <a href="../../../api-usage-and-reference/common-api-objects/externalids.md"><code>externalID</code></a> identifiers.</td></tr><tr><td><code>parameters.order</code></td><td>object</td><td><p>(Optional) Values of the <a href="../../../api-usage-and-reference/common-api-objects/order-parameter.md"><code>orderParameter</code></a> associated with the request.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Examples <a href="#example" id="example"></a>

{% tabs %}
{% tab title="MINIMAL EXAMPLE" %}
{% code title="REQUEST OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "REQ-1671-0642",  
  "status": "Querying",
  "client": { 
    "id": "ACC-1234-4444",
    "name": "Rolls-Royce"
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

{% tab title="COMPLETE EXAMPLE" %}
{% code title="REQUEST OBJECT" overflow="wrap" lineNumbers="true" %}
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
