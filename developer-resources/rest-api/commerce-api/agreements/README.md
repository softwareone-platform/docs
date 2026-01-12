# Agreements

The `Agreement` object represents an instance of a relationship between the seller, buyer, and licensee. It may refer to one-time purchases or a set of subscriptions.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="155">Field</th><th width="144">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>Primary account identifier.</p><p>Example: AGR-2119-4550-8674</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>Relative reference to the object in the API.</p><p>Example: /v1/commerce/agreements/AGR-2119-4550-8674</p></td></tr><tr><td>status</td><td><code>string</code></td><td>The key status of the object. May only be specified on creation and cannot be updated with <code>PUT</code>.</td></tr><tr><td>name</td><td><code>string</code></td><td><p>The agreement name. The value is assigned automatically when the agreement is created, as {product.name} for {licensee.name}. The value can be changed later.</p><p>Example: Microsoft Office 365 NCE E1</p></td></tr><tr><td>vendor</td><td><a href="../../accounts-api/account/#account-object"><code>account</code></a></td><td><p>A reference to the vendor account object filled in upon creation, according to the product.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>client</td><td><a href="../../accounts-api/account/#account-object"><code>account</code></a></td><td><p>A reference to the client account object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "ACC-1234-4444",
    "name": "Best LLC",
    "icon": "/static/ACC-1234-4444/account.png"
}
</code></pre></td></tr><tr><td>buyer</td><td><a href="../../accounts-api/buyer/#buyer-object"><code>buyer</code></a></td><td><p>A reference to the Buyer object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "BUY-3731-7971",
    "name": "Adam Ruszczak",
    "icon": "/static/BUY-3731-7971/icon.png"
}
</code></pre></td></tr><tr><td>seller</td><td><a href="../../accounts-api/seller/#seller-object"><code>seller</code></a></td><td><p>A reference to the Seller object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "SEL-9121-8944",
    "name": "Software LN",
    "icon": "/static/SEL-9121-8944/icon.png"
}
</code></pre></td></tr><tr><td>licensee</td><td><a href="../../accounts-api/licensee/#licensee-object"><code>licensee</code></a></td><td><p>A reference to the Licensee object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "LCE-9625-9634",
    "name": "John Smith",
    "icon": "/static/LCE-9625-9634/icon.png"
}
</code></pre></td></tr><tr><td>product</td><td><a href="../../catalog-api/product/"><code>product</code></a></td><td><p>A reference to the Product object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>listing</td><td><a href="../../catalog-api/listing/"><code>listing</code></a></td><td><p>A reference to the listing that allows this agreement.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "LST-1234-1234"
}
</code></pre></td></tr><tr><td>authorization</td><td><a href="../../catalog-api/authorization/"><code>authorization</code></a></td><td><p>A reference to the Authorization object used for the agreement.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "AUT-1234-4567",
    "name": "Salesforce Enterprise License"
}
</code></pre></td></tr><tr><td>price</td><td><a href="../../common-api-objects/price.md"><code>price</code></a></td><td><p>The agreement's pricing details, including the monthly and yearly costs, exclude one-time charges.</p><p>Different aspects of the price object are visible to actors, as indicated in the Price object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "PPxY": 150,
  "PPxM": 12.50,
  "SPxY": 165,
  "SPxM": 13.75,
  "currency": "USD"
}
</code></pre></td></tr><tr><td>template</td><td><a href="../../catalog-api/templates/"><code>template</code></a></td><td><p>A reference to the Template object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "TPL-1234-4444",
    "name": "Succesful Activation"
}
</code></pre></td></tr><tr><td>error</td><td><a href="../../common-api-objects/error.md"><code>error</code></a></td><td><p>Markup text string explaining the reason for provisioning failure.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
     "id": "E001234",
     "message": "Agreement provisioning failed due to unavailability of the item"
}
</code></pre></td></tr><tr><td>lines</td><td><code>lines</code></td><td><p>A list of items in the agreement.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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
      "currency": "USD"
    },
    "order": { "id": "ORD-6869-4529-8975-9005" }
  }
]
</code></pre></td></tr><tr><td>subscriptions</td><td><a href="../subscriptions/"><code>subscription</code></a></td><td><p>A list of subscriptions in the agreement.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
    {
      "id": "SUB-0792-5000-2253",
    }
]
</code></pre></td></tr><tr><td>parameters.fulfillment</td><td><a href="../../common-api-objects/order-parameter.md"><code>orderParameter</code></a></td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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
</code></pre></td></tr><tr><td>parameters.ordering</td><td><a href="../../common-api-objects/order-parameter.md"><code>orderParameter</code></a></td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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
</code></pre></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td><p>A reference to the Audit object.</p><p>Possible audit events include <code>Created</code>, <code>Updated</code>, <code>Activated</code>, <code>Terminated</code>, or <code>Failed</code>.</p></td></tr><tr><td>externalIds</td><td><a href="../../common-api-objects/externalids.md"><code>externalIds</code></a></td><td><p>A set of external IDs.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "client": "12345678",
  "operations":	"07bf766b-c767-4293-9ab3",
  "vendor": "ABC-2023-C07-dbeee0b302c0"
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="SHORT FORM" %}
{% code lineNumbers="true" %}
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
{% endcode %}
{% endtab %}

{% tab title="LONG EXAMPLE" %}
{% code lineNumbers="true" %}
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
{% endcode %}
{% endtab %}
{% endtabs %}
