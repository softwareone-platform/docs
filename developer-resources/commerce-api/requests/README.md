# Requests

## Request object

| Field                                              | Type              | Constraint                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                               |
| -------------------------------------------------- | ----------------- | --------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`id`**                                           | string            | <p><code>READONLY</code> </p><p><code>IDX</code></p>                                                                        | <p>Primary Request identifier </p><p></p><p>Example: "REQ-1671-0642"</p>                                                                                                                                                                                                                                                                  |
| **`href`**                                         | string            | `READONLY`                                                                                                                  | <p>Relative reference to object on API (always /v1/commerce/requests/{id}) </p><p></p><p>Example: "/v1/commerce/requests/REQ-1671-0642"</p>                                                                                                                                                                                               |
| **`status`**                                       | string            | <p><code>IDX</code><br><code>Draft</code><br><code>Querying</code><br><code>Processing</code><br><code>Completed</code></p> | <p>Status of the request. </p><p></p><p>Example: "Querying"</p>                                                                                                                                                                                                                                                                           |
| **`client`**                                       | Ref\<Account>     | `IDX`                                                                                                                       | <p>Reference to client Account object. </p><p></p><p>Example: "<code>{ "id": "ACC-1234-4444", "name": "stark industries" }</code>"</p>                                                                                                                                                                                                    |
| **`vendor`**                                       | Ref\<Account>     | `IDX`                                                                                                                       | <p>Reference to vendor Account object. </p><p></p><p>Example: "<code>{ "id": "ACC-1234-1111", "name": "Microsoft" }</code></p>                                                                                                                                                                                                            |
| **`requester`**                                    | Ref\<User>        | `IDX`                                                                                                                       | <p>User of requester, in client account. </p><p></p><p>Example: "<code>{ "id": "USR-1234-4444", "name": "John Smith" }</code>"</p>                                                                                                                                                                                                        |
| **`assignee`**                                     | Ref\<User>        | <p><code>IDX</code> </p><p><code>OPTIONAL</code></p>                                                                        | <p>User of vendor who is responsible to processing request. </p><p></p><p>Example: "<code>{ "id": "USR-1234-1111", "name": "Jane Doe" }"</code></p>                                                                                                                                                                                       |
| **`product`**                                      | Ref\<Product>     | `IDX`                                                                                                                       | <p>Product object reference </p><p></p><p>Example: "<code>{ "id": "PRD-1111-1111-1111", "href": "/catalog/products/PRD-1111-1111-1111", "name": "Microsoft Office 365 NCE", "icon": "/static/PRD-1111-1111-1111/logo.png" }"</code></p>                                                                                                   |
| **`externalIds`**                                  | ExternalIdsObject | <p><code>IDX</code> </p><p><code>OPTIONAL</code></p>                                                                        | <p>Set of external IDs identifiers </p><p></p><p>Example: "<code>{ "client": "12345678", "operations": "07bf766b-c767-4293-9ab3", "vendor": "ABC-2023-C07-dbeee0b302c0" }</code>"</p>                                                                                                                                                     |
| **`parameters``.order`**                           | ParameterValue\[] | `OPTIONAL`                                                                                                                  | <p>Request ordering parameters values </p><p></p><p>Example:</p><p> <code>[ { "id": "PRM-1234-1234-1234-1234", "name": "Tennant Id", "externalId": "tennant_id", "constraints": { ... }, "value": "69b73824-ce76-4866-ad47-b615ae9d8998", } ]</code></p>                                                                                  |
| <p><strong><code>error</code></strong><br><br></p> | ErrorObject       | `MARKDOWN`                                                                                                                  | <p>Error reported by validation procedure </p><p></p><p>Example </p><p><code>{ "id": "E001234", "message": "Agreement provisioning failed due to unavailability of the item" }</code></p>                                                                                                                                                 |
| **`audit`**                                        | AuditObject       | <p><code>READONLY</code> </p><p><code>IDX</code></p>                                                                        | <p>Audit object with possible entries: created, updated, activated, terminated, according to lifecycle of the object. Possible audit events: <strong>created</strong>, <strong>updated, querying</strong>. </p><p></p><p>Example </p><p><code>{ "created": { "at": "...", "by": { } }, "updated": { "at": "...", "by": { } } }</code></p> |

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
