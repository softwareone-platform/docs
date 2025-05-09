# Agreements

The Agreement object represents an instance of a relationship between the seller, buyer, and licensee. It may refer to one-time purchases or a set of subscriptions.&#x20;

This object contains the following properties:

<table data-full-width="false"><thead><tr><th width="155">Field</th><th width="206">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Primary account identifier. </p><p></p><p>Example: AGR-2119-4550-8674</p></td></tr><tr><td>href</td><td>string</td><td><p>Relative reference to the object in the API. </p><p></p><p>Example: /v1/commerce/agreements/AGR-2119-4550-8674</p></td></tr><tr><td>status</td><td>string</td><td>The key status of the object. May only be specified on creation and cannot be updated with <code>PUT</code>.</td></tr><tr><td>name</td><td>string</td><td><p>The agreement name. The value is assigned automatically when the agreement is created, as {product.name} for {licensee.name}. The value can be changed later.</p><p></p><p>Example: Microsoft Office 365 NCE E1</p></td></tr><tr><td>vendor</td><td><a href="../../accounts-api/account/#account-object">Account</a></td><td><p>Reference to the vendor account object filled in upon creation, according to the product.</p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>client</td><td><a href="../../accounts-api/account/#account-object">Account</a></td><td><p>Reference to the client account object.</p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "ACC-1234-4444",
    "name": "Best LLC",
    "icon": "/static/ACC-1234-4444/account.png"
}
</code></pre></td></tr><tr><td>buyer</td><td><a href="../../accounts-api/buyer/#buyer-object">Buyer</a></td><td><p>Reference to the Buyer object.</p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "BUY-3731-7971",
    "name": "Adam Ruszczak",
    "icon": "/static/BUY-3731-7971/icon.png"
}
</code></pre></td></tr><tr><td>seller</td><td><a href="../../accounts-api/seller/#seller-object">Seller</a></td><td><p>Reference to the Seller object.</p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "SEL-9121-8944",
    "name": "Software LN",
    "icon": "/static/SEL-9121-8944/icon.png"
}
</code></pre></td></tr><tr><td>licensee</td><td><a href="../../accounts-api/licensee/#licensee-object">Licensee</a></td><td><p>Reference to the Licensee object.</p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "LCE-9625-9634",
    "name": "John Smith",
    "icon": "/static/LCE-9625-9634/icon.png"
}
</code></pre></td></tr><tr><td>product</td><td><a href="../../catalog-api/product/">Product</a></td><td><p>Reference to the Product object.</p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>listing</td><td>Listing</td><td><p>Reference to the listing that allows this agreement.</p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "LST-1234-1234"
}
</code></pre></td></tr><tr><td>authorization</td><td>Authorization</td><td><p>Reference to the Authorization object used for the agreement.</p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "AUT-1234-4567",
    "name": "Salesforce Enterprise License"
}
</code></pre></td></tr><tr><td>price</td><td>Price</td><td><p>The agreement's pricing details including the monthly and yearly costs, excluding one-time charges. </p><p></p><p>Different aspects of the price object are visible to different actors, as indicated in the Price Object.</p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "PPxY": 150,
  "PPxM": 12.50,
  "SPxY": 165,
  "SPxM": 13.75,
  "currency": "USD"
}
</code></pre></td></tr><tr><td>template</td><td>Template</td><td><p>Reference to Template object. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "TPL-1234-4444",
    "name": "Succesful Activation"
}
</code></pre></td></tr><tr><td>error</td><td>ErrorObject</td><td><p>Markup text string explaining the reason for provisioning failure. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
     "id": "E001234",
     "message": "Agreement provisioning failed due to unavailability of the item"
}
</code></pre></td></tr><tr><td>lines</td><td>Lines</td><td><p>List of items in the agreement. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "ALI-1234-1234-1234-0127",
    "item": {
      "id": "ITM-1234-1234-1234-0992",
      "name": "Adobe Migration"
    },
    "quantity": 10,
    "price": {
      "PPx1": 12.50,
      "unitPP": 1.25
      "SPx1": 13.50,
      "unitSP": 1.35,
      "currency": "USD"
    },
    "order": { "id": "ORD-6869-4529-8975-9005" }
  }
]
</code></pre></td></tr><tr><td>subscriptions</td><td>Subscription</td><td><p>List of subscriptions in the agreement.</p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
    {
      "id": "SUB-0792-5000-2253",
    }
]
</code></pre></td></tr><tr><td>parameters.fulfillment</td><td>OrderParameterValue</td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
      "id": "PRM-1234-1234-1234",
      "name": "Tennant Id",
      "externalId": "tennant_id",
      "constraints": {
          "readonly": false,
          "hidden": true,
          "required": true,
          "unique": false
      },
      "value": "69b73824-ce76-4866-ad47-b615ae9d8998",
      "error": {
          "id": "E001234",
          "message": "Incorrect parameter value"
      }
  }
]
</code></pre></td></tr><tr><td>parameters.ordering</td><td>Order Parameter Object</td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
      "id": "PRM-1234-1234-1234",
      "name": "Tennant Id",
      "externalId": "tennant_id",
      "constraints": {
          "readonly": false,
          "hidden": true,
          "required": true,
          "unique": false
      },
      "value": "69b73824-ce76-4866-ad47-b615ae9d8998",
      "error": {
          "id": "E001234",
          "message": "Incorrect parameter value"
      }
  }
]
</code></pre></td></tr><tr><td>audit</td><td>AuditObject</td><td><p>Audit object with possible entries: created, updated, activated, terminated, according to the object's lifecycle. </p><p></p><p>Possible audit events include Created, Updated, Activated, Terminated, and Failed.</p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } },
  "activated": { "at": "...", "by": { } },
  "terminated": { "at": "...", "by": { } }
}
</code></pre></td></tr><tr><td>externalIds</td><td>ExternalIdsObject</td><td><p>Set of external IDs. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "client": "12345678",
  "operations":	"07bf766b-c767-4293-9ab3",
  "vendor": "ABC-2023-C07-dbeee0b302c0"
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="SHORT FORM" %}
```json
{
  "id": "AGR-2119-4550-8674",
  "status": "Draft",
  "name": "Microsoft Office 365 NCE E1", 
  "vendor": { "id": "ACC-1234-1234" },
  "client": { "id": "ACC-1234-4444" },
  "seller": { "id": "SEL-9121-8944" },
  "buyer": { "id": "BUY-3731-7971" },
  "licensee": { "id": "LCE-9625-9634" },
  "product": {
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
  },
  "price": {
    "PPxY": 150,
    "PPxM": 12.50,
    "SPxY": 165,
    "SPxM": 13.75,
    "currency": "USD"
  },
  "startDate": "2023-12-14T17:28:57.667Z",
  "endDate": "2023-12-14T17:28:57.667Z",
  "template": {
    "id": "TPL-1234-4444",
    "name": "Succesful Activation"
  },
  "audit": {
    "created": { "at": "...", "by": { } },
    "updated": { "at": "...", "by": { } }
  },
  "lines": [
    {
      "id": "ALI-1234-1234-1234-0127",
      "item": {
        "id": "ITM-1234-1234-1234-0992",
        "name": "Adobe Migration"
      },
      "quantity": 10,
      "price": {
        "PPx1": 12.50,
        "unitPP": 1.25
        "SPx1": 13.50,
        "unitSP": 1.35,
        "currency": "USD"
      },
      "order": { "id": "ORD-6869-4529-8975-9005" }
    }
  ],
  "subscriptions": [
    { "id": "SUB-0792-5000-2253" }
  ],
  "parameters": {
    "ordering": [ ],
    "fulfillment": [ ]
  },
  "externalIDs": {
    "client": "12345678",
    "operations":	"07bf766b-c767-4293-9ab3",
    "vendor": "ABC-2023-C07-dbeee0b302c0"
  }
}
```
{% endtab %}

{% tab title="LONG EXAMPLE" %}
```json
{
  "id": "AGR-2119-4550-8674",
  "status": "Draft",
  "name": "Microsoft Office 365 NCE E1", 
  "vendor": {
    "id": "ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
  },
  "client": {
    "id": "ACC-1234-4444",
    "name": "Best LLC",
    "icon": "/static/ACC-1234-4444/account.png"
  },
  "seller": {
    "id": "SEL-9121-8944",
    "name": "Software LN",
    "icon": "/static/SEL-9121-8944/icon.png"
  },
  "buyer": {
    "id": "BUY-3731-7971",
    "name": "Adam Ruszczak",
    "icon": "/static/BUY-3731-7971/icon.png"
  },
  "licensee": {
    "id": "LCE-9625-9634",
    "name": "John Smith",
    "icon": "/static/LCE-9625-9634/icon.png"
  },
  "product": {
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
  },
  "price": {
    "PPxY": 150,
    "PPxM": 12.50,
    "SPxY": 165,
    "SPxM": 13.75,
    "markup": 0.10,
    "margin": 0.11,
    "currency": "USD"
  },
  "startDate": "2023-12-14T17:28:57.667Z",
  "endDate": "2023-12-14T17:28:57.667Z",
  "template": {
    "id": "TPL-1234-4444",
    "name": "Succesful Activation"
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
  },
  "lines": [
    {
      "id": "ALI-1234-1234-1234-0127",
      "item": {
        "id": "ITM-1234-1234-1234-0992",
        "name": "Adobe Migration"
      },
      "quantity": 10,
      "price": {
        "PPx1": 12.50,
        "unitPP": 1.25,
        "SPx1": 13.50,
        "unitSP": 1.35,
        "markup": 0.10,
        "margin": 0.11,
        "currency": "USD"
      },
      "order": { "id": "ORD-6869-4529-8975-9005" }
    }
  ],
  "subscriptions": [
    {
      "id": "SUB-0792-5000-2253",
    }
  ],
  "parameters": {
    "ordering": [
      {
        "id": "string",
        "name": "string",
        "value": "string",
        "hasError": true,
        "description": {
          "type": "SingleLine",
          "phase": "Configuration",
          "isRequired": true,
          "isHidden": true,
          "isReadOnly": true,
          "error": "string"
        }
      }
    ],
    "fulfillment": [
      {
        "id": "string",
        "name": "string",
        "value": "string",
        "hasError": true,
        "description": {
          "type": "SingleLine",
          "phase": "Configuration",
          "isRequired": true,
          "isHidden": true,
          "isReadOnly": true,
          "error": "string"
        }
      }
    ]
  },
  "externalIDs": {
    "client": "12345678",
    "operations":	"07bf766b-c767-4293-9ab3",
    "vendor": "ABC-2023-C07-dbeee0b302c0"
  }
}
```
{% endtab %}
{% endtabs %}
