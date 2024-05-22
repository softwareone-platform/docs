# Authorizations

## Authorization object <a href="#overview" id="overview"></a>

The `Authorization` object represents a business object that positions a Product within the purview of a particular SoftwareOne seller, characterized by a specific Authorization and an assigned Price List. Listings play a crucial role in controlling the visibility and availability of Products in various markets and managing their lifecycle in a scalable and efficient manner.

| Field             | Type                                                  | Description                                                                                                                                                                                                                                                                                                            |
| ----------------- | ----------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`id`**          | string                                                | <p>Authorization identifier. </p><p></p><p>Example: "AUT-1234-4678"</p>                                                                                                                                                                                                                                                |
| **`href`**        | string                                                | <p>Relative reference to object on API (always <code>/authorization/{id}</code>) </p><p></p><p>Example: "/v1/authorizations/AUT-1234-4678"</p>                                                                                                                                                                         |
| **`name`**        | string                                                | <p>Name of the authorization. </p><p></p><p>Example: "Salesforce Enterprise License"</p>                                                                                                                                                                                                                               |
| **`externalIds`** | [ExternalIds](./#externalids)                         | <p> Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "vendor": "ven-1233-3222",
  "operations": "op-322-322",
}
</code></pre>                                                                                                                                                      |
| **`currency`**    | string                                                | <p>Authorization currency. </p><p></p><p>Example: "EUR"</p>                                                                                                                                                                                                                                                            |
| **`notes`**       | string                                                | Optional notes                                                                                                                                                                                                                                                                                                         |
| **`product`**     | [Product](../product/)                                | <p>The Product that the Authorization belongs to.  </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{    
  "id": "PRD-1111-1111",
  "href": "/products/PRD-1111-1111",
  "name": "Microsoft Office 365 NCE",
  "icon": "/static/PRD-1111-1111/logo.png"
}
</code></pre> |
| **`vendor`**      | [Account](../../accounts-api/account/)                | <p>The Vendor that the Authorization belongs to. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "id": "ACC-1234-1234",
  "href": "/accounts/accounts/ACC-1234-1234",
  "name": "Microsoft",
  "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre>          |
| **`owner`**       | [Seller](../../accounts-api/seller/)                  | <p>SoftwareOne seller entity. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "id": "SEL-1234-4567",
  "href": "/seller/SEL-1234-4567",
  "name": "SoftwareOne, Inc."
}
</code></pre>                                                                               |
| **`statistics`**  | [AuthorizationStatistics](./#authorizationstatistics) | <p>Statistics about authorization. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "subscriptions": 5,
  "agreements": 10,
  "listings": 3,
  "sellers": 2
}
</code></pre>                                                                                          |
| **`audit`**       | Audit                                                 | <p>Authorization last audit events. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { 
    "at": "2023-12-14T17:28:57Z", 
    "by": { ... }
  },
  "updated": { 
    "at": "2023-12-14T17:28:57Z", 
    "by": { ... }
  }
}
</code></pre>                |

## ExternalIds <a href="#externalids" id="externalids"></a>

ExternalIds contain any external identifier

| Field            | Type   | Description                                                                    |
| ---------------- | ------ | ------------------------------------------------------------------------------ |
| **`operations`** | string | This external ID will be the unique identifier between vendor and SoftwareOne. |

## AuthorizationStatistics <a href="#authorizationstatistics" id="authorizationstatistics"></a>

| Field               | Type    | Description                                                                                   |
| ------------------- | ------- | --------------------------------------------------------------------------------------------- |
| **`subscriptions`** | integer | <p>Number of Subscriptions that are assigned to Authorization. </p><p></p><p>Example: "5"</p> |
| **`agreements`**    | integer | <p>Number of Agreements that are assigned to Authorization. </p><p></p><p>Example: "10"</p>   |
| **`listings`**      | integer | <p>Number of Listings that are referring to Authorization. </p><p></p><p>Example: "3"</p>     |
| **`sellers`**       | integer | <p>Number of Sellers that are referring to Authorization. </p><p></p><p>Example: "1"</p>      |

## Example

{% tabs %}
{% tab title="AUTHORIZATION OBJECT" %}
```json
{
  "id": "AUT-1234-4678",
  "href": "/v1/authorization/AUT-1234-4678",
  "name": "Salesforce Enterprise License",
  "externalId": "WW-1001111",
  "currency": "EUR",
  "notes": "Notes about given authorization",
  "partnerProgram": true,
  "product": {
      "id": "PRD-1111-1111",
      "href": "/products/PRD-1111-1111",
      "name": "Microsoft Office 365 NCE",
      "icon": "/static/PRD-1111-1111/logo.png"
  },
  "vendor": {
    "id": "ACC-1234-1234",
    "href": "/accounts/accounts/ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
  },
  "owner": {
      "id": "SEL-1234-4567",    
      "href": "/seller/SEL-1234-4567",    
      "name": "SoftwareOne, Inc."
  },
  "statistics": {
      "subscriptions" : 5,
      "agreements": 10,
      "listings": 4,
      "sellers": 1
  },
  "audit": {
    "created": { 
      "at": "2023-12-14T17:28:57Z", 
      "by": {
        "id": "UR-1234-1234-1234",
        "name": "John Smith",
        "icon": "/static/users/UR-1234-1234-1234.icon.svg"
      }
    },
    "updated": { 
      "at": "2023-12-14T17:28:57Z", 
      "by": {
        "id": "UR-1234-1234-1234",
        "name": "John Smith",
        "icon": "/static/users/UR-1234-1234-1234.icon.svg"
      }
    }
  }
}
```
{% endtab %}
{% endtabs %}
