# Agreements

## Agreements Object

The agreement represents an instance of a relationship between Seller, Buyer, and Licensee. It may refer to one-time purchases or/and set of subscriptions.

<table data-full-width="false"><thead><tr><th width="120">Field</th><th width="125">Type</th><th width="147">Constraints</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p><code>READONLY</code> </p><p><code>IDX</code> </p></td><td><p>Primary account identifier. </p><p></p><p>Example: "AGR-2119-4550-8674"</p></td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td><code>READONLY</code> </td><td><p>Relative reference to object on API (always /commerce/agreements/{id}). </p><p></p><p>Example: "/v1/commerce/agreements/AGR-2119-4550-8674"</p></td></tr><tr><td><strong><code>status</code></strong></td><td>string</td><td><code>IDX</code> </td><td>The key status of the object. May only be specified on creation - Draft or Provisioning, and cannot be updated with <code>PUT</code>.</td></tr><tr><td><strong><code>name</code></strong></td><td>string</td><td><code>IDX</code> </td><td><p>Agreement name, will be assigned automatically on creation, as <code>{product.name} for {licensee.name}</code> but can be changed later.</p><p></p><p>Example: "Microsoft Office 365 NCE E1"</p></td></tr><tr><td><strong><code>vendor</code></strong></td><td><a href="../../accounts-api/account/#account-object">Account</a></td><td><p><code>READONLY</code> </p><p><code>IDX</code> </p><p><code>OPTIONAL</code></p></td><td><p>Reference to the vendor <a href="../../accounts-api/account/#account-object">Account</a> object<br>filled-in on creation according product.</p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "href": "/accounts/accounts/ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td><strong><code>client</code></strong></td><td><a href="../../accounts-api/account/#account-object">Account</a></td><td><p><code>IDX</code> </p><p><code>FINAL</code></p></td><td><p>Reference to the Client <a href="../../accounts-api/account/#account-object">Account</a> object.</p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{
    "id": "ACC-1234-4444",
    "href": "/accounts/accounts/ACC-1234-4444",
    "name": "Best LLC",
    "icon": "/static/ACC-1234-4444/account.png"
}
</code></pre></td></tr><tr><td><strong><code>buyer</code></strong></td><td><a href="../../accounts-api/buyer/#buyer-object">Buyer</a></td><td><p><code>READONLY</code> </p><p><code>IDX</code> </p><p><code>OPTIONAL</code></p></td><td><p>Reference to <a href="../../accounts-api/buyer/#buyer-object">Buyer</a> object.</p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{
    "id": "BUY-3731-7971",
    "href": "/accounts/buyers/BUY-3731-7971",
    "name": "Adam Ruszczak",
    "icon": "/static/BUY-3731-7971/icon.png"
}
</code></pre></td></tr><tr><td><strong><code>seller</code></strong></td><td><a href="../../accounts-api/seller/#seller-object">Seller</a></td><td><p><code>READONLY</code> </p><p><code>IDX</code> </p><p><code>FINAL</code></p></td><td><p>Reference to the <a href="../../accounts-api/seller/#seller-object">Seller</a> object.</p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{
    "id": "SEL-9121-8944",
    "href": "/accounts/sellers/SEL-9121-8944",
    "name": "Software LN",
    "icon": "/static/SEL-9121-8944/icon.png"
}
</code></pre></td></tr><tr><td><strong><code>licensee</code></strong></td><td><a href="../../accounts-api/licensee/#licensee-object">Licensee</a></td><td><p><code>IDX</code> </p><p><code>FINAL</code></p></td><td><p>Reference to the <a href="../../accounts-api/licensee/#licensee-object">Licensee</a> object.</p><p></p><p>Example:</p><pre class="language-json"><code class="lang-json">{
    "id": "LCE-9625-9634",
    "href": "/accounts/licensees/LCE-9625-9634",
    "name": "John Smith",
    "icon": "/static/LCE-9625-9634/icon.png"
}
</code></pre></td></tr><tr><td><strong><code>product</code></strong></td><td><a href="../../catalog-api/product/">Product</a></td><td><p><code>IDX</code> </p><p><code>FINAL</code></p></td><td><p>Reference to the <a href="../../catalog-api/product/#product-object">Product</a> object.</p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "href": "/catalog/products/PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td><strong><code>listing</code></strong></td><td>Listing</td><td><code>IDX</code> </td><td><p>Reference to the listing which allows this agreement.</p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">{
    "id": "LST-1234-1234"
}
</code></pre></td></tr><tr><td><strong><code>authorization</code></strong></td><td>Authorization</td><td><p><code>READONLY</code> </p><p><code>IDX</code> </p><p><code>FINAL</code></p></td><td><p>Reference to the Authorization object used for the agreement.</p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">{
    "id": "AUT-1234-4567",
    "href": "/authorization/ATH-1234-45678",
    "name": "Salesforce Enterprise License"
}
</code></pre></td></tr><tr><td><strong><code>price</code></strong></td><td>Price</td><td><p><code>READONLY</code> </p><p><code>IDX</code> </p></td><td><p>The price for the agreement, explains the monthly and yearly prices for the whole agreement, one-time price tags are never included into it.<br>different parts of price object visible to different actors, see Price Object. </p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">{
  "PPxY": 150,
  "PPxM": 12.50,
  "SPxY": 165,
  "SPxM": 13.75,
  "markup": 0.10,
  "margin": 0.11,
  "currency": "USD"
}
</code></pre></td></tr><tr><td><strong><code>template</code></strong></td><td>Template</td><td><code>IDX</code></td><td><p>Reference to Template object. </p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">{
    "id": "TPL-1234-4444",
    "href": "/products/product/&#x3C;id>/templates/TPL-1234-4444",
    "name": "Succesful Activation"
}
</code></pre></td></tr><tr><td><strong><code>error</code></strong></td><td>ErrorObject</td><td><code>MARKDOWN</code></td><td><p>Markup text string explaining reason for provisining failure. Always set on moving status to Failed.</p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">{
     "id": "E001234",
     "message": "Agreement provisioning failed due to unavailability of the item"
}
</code></pre></td></tr><tr><td><strong><code>lines</code></strong></td><td>Lines[]</td><td><code>FINAL</code></td><td><p>List of items in Agreement. </p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">[
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
      "markup": 0.10,
      "margin": 0.11,
      "currency": "USD"
    },
    "order": { "id": "ORD-6869-4529-8975-9005" }
  }
]
</code></pre></td></tr><tr><td><strong><code>subscriptions</code></strong></td><td>Subscription[]</td><td><code>FINAL</code></td><td><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">[
    {
      "id": "SUB-0792-5000-2253",
      "href": "/commerce/agreements/AGR-2119-4550-8674-5962/subscriptions/SUB-0792-5000-2253"
    }
]
</code></pre></td></tr><tr><td><strong><code>parameters.fulfillment</code></strong></td><td>OrderParameterValue []</td><td><code>OPTIONAL</code></td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors. </p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">[
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
</code></pre></td></tr><tr><td><strong><code>parameters.ordering</code></strong></td><td>Order Parameter Object []</td><td><code>OPTIONAL</code></td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors. </p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">[
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
</code></pre></td></tr><tr><td><strong><code>audit</code></strong></td><td>AuditObject</td><td><p><code>READONLY</code> </p><p><code>IDX</code> </p></td><td><p>Audit object with possible entries: created, updated, activated, terminated, according to the object's lifecycle. </p><p></p><p>Possible audit events include Created, Updated, Activated, Terminated, and Failed.</p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } },
  "activated": { "at": "...", "by": { } },
  "terminated": { "at": "...", "by": { } }
}
</code></pre></td></tr><tr><td><strong><code>externalIds</code></strong></td><td>ExternalIdsObject</td><td><p><code>IDX</code> </p><p><code>OPTIONAL</code></p></td><td><p>Set of external IDs. </p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">{
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
  "href": "/commerce/agreements/AGR-2119-4550-8674",
  "status": "Draft",
  "name": "Microsoft Office 365 NCE E1", 
  "vendor": { "id": "ACC-1234-1234" },
  "client": { "id": "ACC-1234-4444" },
  "seller": { "id": "SEL-9121-8944" },
  "buyer": { "id": "BUY-3731-7971" },
  "licensee": { "id": "LCE-9625-9634" },
  "product": {
    "id": "PRD-1111-1111-1111",
    "href": "/catalog/products/PRD-1111-1111-1111",
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
    "href": "/products/product/<id>/templates/TPL-1234-4444",
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
        "markup": 0.10,
        "margin": 0.11,
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
  "href": "/commerce/agreements/AGR-2119-4550-8674",
  "status": "Draft",
  "name": "Microsoft Office 365 NCE E1", 
  "vendor": {
    "id": "ACC-1234-1234",
    "href": "/accounts/accounts/ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
  },
  "client": {
    "id": "ACC-1234-4444",
    "href": "/accounts/accounts/ACC-1234-4444",
    "name": "Best LLC",
    "icon": "/static/ACC-1234-4444/account.png"
  },
  "seller": {
    "id": "SEL-9121-8944",
    "href": "/accounts/sellers/SEL-9121-8944",
    "name": "Software LN",
    "icon": "/static/SEL-9121-8944/icon.png"
  },
  "buyer": {
    "id": "BUY-3731-7971",
    "href": "/accounts/buyers/BUY-3731-7971",
    "name": "Adam Ruszczak",
    "icon": "/static/BUY-3731-7971/icon.png"
  },
  "licensee": {
    "id": "LCE-9625-9634",
    "href": "/accounts/licensees/LCE-9625-9634",
    "name": "John Smith",
    "icon": "/static/LCE-9625-9634/icon.png"
  },
  "product": {
    "id": "PRD-1111-1111-1111",
    "href": "/catalog/products/PRD-1111-1111-1111",
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
    "href": "/products/product/<id>/templates/TPL-1234-4444",
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
      "href": "/commerce/agreements/AGR-2119-4550-8674-5962/subscriptions/SUB-0792-5000-2253"
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
