# Requests

## Request object

| Field                  | Type                                                  | Description                                                                                                                                                                                                                                                                                                                                                                       |
| ---------------------- | ----------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`id`**               | string                                                | <p>Primary Request identifier </p><p></p><p>Example: "REQ-1671-0642"</p>                                                                                                                                                                                                                                                                                                          |
| **`href`**             | string                                                | <p>Relative reference to object on API (always /v1/commerce/requests/{id}) </p><p></p><p>Example: "/v1/commerce/requests/REQ-1671-0642"</p>                                                                                                                                                                                                                                       |
| **`status`**           | string                                                | <p>Status of the request. </p><p></p><p>Example: "Querying"</p>                                                                                                                                                                                                                                                                                                                   |
| **`client`**           | [Account](../../accounts-api/account/#account-object) | <p>Reference to client Account object. </p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{ 
  "id": "ACC-1234-4444",
  "name": "stark industries"
}
</code></pre>                                                                                                                                                                                      |
| **`vendor`**           | [Account](../../accounts-api/account/#account-object) | <p>Reference to vendor Account object. </p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{ 
  "id": "ACC-1234-1111",
  "name": "Microsoft"
}
</code></pre>                                                                                                                                                                                             |
| **`requester`**        | [User](../../accounts-api/users/#user-object)         | <p>User of requester, in client account. </p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{ 
  "id": "USR-1234-4444",
  "name": "John Smith"
}
</code></pre>                                                                                                                                                                                          |
| **`assignee`**         | [User](../../accounts-api/users/#user-object)         | <p>User of vendor who is responsible to processing request. </p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{ 
  "id": "USR-1234-1111",
  "name": "Santa Claus"
}
</code></pre>                                                                                                                                                                      |
| **`product`**          | Product                                               | <p>Example:</p><pre class="language-json"><code class="lang-json">{
  "id": "PRD-1111-1111-1111",
  "href": "/catalog/products/PRD-1111-1111-1111",
  "name": "Microsoft Office 365 NCE",
  "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre>                                                                                                                         |
| **`externalIds`**      | ExternalIdsObject                                     | <p>Set of external IDs identifiers.</p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{
  "client": "12345678",
  "operations":	"07bf766b-c767-4293-9ab3",
  "vendor": "ABC-2023-C07-dbeee0b302c0"
}
</code></pre><p></p>                                                                                                                               |
| **`parameters.order`** | ParameterValue\[]                                     | <p>Request ordering parameters values </p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">[
  {
    "id": "PRM-1234-1234-1234-1234",
    "name": "Tennant Id",
    "externalId": "tennant_id",
    "constraints": { ... },
    "value": "69b73824-ce76-4866-ad47-b615ae9d8998",
  }
]
</code></pre>                                                      |
| **`error`**            | ErrorObject                                           | <p>Error reported by validation procedure. </p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{
     "id": "E001234",
     "message": "Agreement provisioning failed due to unavailability of the item"
}
</code></pre>                                                                                                                                 |
| **`audit`**            | AuditObject                                           | <p>Audit object with possible entries: created, updated, activated, terminated, according to lifecycle of the object. </p><p></p><p>Possible audit events: Created, Updated, and Querying. </p><p></p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre> |

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
