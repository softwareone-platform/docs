# Agreement

The Agreement object represents an instance of a relationship between the seller, buyer, and licensee. It may refer to one-time purchases or a set of subscriptions.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="218">Field</th><th width="120">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The primary identifier for the account.</td></tr><tr><td><code>status</code></td><td>string</td><td>The key status of the object. May only be specified on creation and cannot be updated with <code>PUT</code>.</td></tr><tr><td><code>name</code></td><td>string</td><td>The agreement name. The value is assigned automatically when the agreement is created, as {product.name} for {licensee.name}. The value can be changed later.</td></tr><tr><td><code>vendor</code></td><td>object </td><td>(Read-only) Represents the vendor <a href="../../accounts-api/account/#account-object"><code>account</code></a> object filled in upon creation, according to the product.</td></tr><tr><td><code>client</code></td><td>object</td><td>Represents the client <a href="../../accounts-api/account/#account-object"><code>account</code></a> object.</td></tr><tr><td><code>buyer</code></td><td>object</td><td>(Read-only) Represents the <a href="../../accounts-api/buyer/#buyer-object"><code>buyer</code></a> object.</td></tr><tr><td><code>seller</code></td><td>object</td><td>(Read-only) Represents the <a href="../../accounts-api/seller/#seller-object"><code>seller</code></a> object.</td></tr><tr><td><code>licensee</code></td><td>object</td><td>Represents the <a href="../../accounts-api/licensee/#licensee-object"><code>licensee</code></a> object.</td></tr><tr><td><code>product</code></td><td>object</td><td><p>Represents the <a href="../../catalog-api/product/"><code>product</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td><code>listing</code></td><td>listing</td><td><p>Represents the <a href="../../catalog-api/listing/"><code>listing</code></a> that allows this agreement.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "LST-1234-1234"
}
</code></pre></td></tr><tr><td><code>authorization</code></td><td>object </td><td>(Read-only) Represents the <a href="../../catalog-api/authorization/"><code>authorization</code></a> object used for the agreement.</td></tr><tr><td><code>price</code></td><td>object</td><td><p>(Read-only) Represents the agreement’s pricing details. Monthly and yearly prices exclude one‑time charges. Visibility of specific price fields varies by actor, as defined within the <a href="../../../api-usage-and-reference/common-api-objects/price.md"><code>price</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "PPxY": 150,
  "PPxM": 12.50,
  "SPxY": 165,
  "SPxM": 13.75,
  "currency": "USD"
}
</code></pre></td></tr><tr><td><code>template</code></td><td>object</td><td><p>Represents the <a href="../../catalog-api/templates/"><code>template</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "TPL-1234-4444",
    "name": "Succesful Activation"
}
</code></pre></td></tr><tr><td><code>error</code></td><td>object</td><td><p>Represents the <a href="../../../api-usage-and-reference/common-api-objects/error.md"><code>error</code></a> object,containing a markup‑formatted text string that explains the reason for provisioning failure.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
     "id": "E001234",
     "message": "Agreement provisioning failed due to unavailability of the item"
}
</code></pre></td></tr><tr><td><code>lines</code></td><td>object</td><td><p>Represents the <a href="../line.md"><code>line</code></a> object, containing a list of items in the agreement.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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
</code></pre></td></tr><tr><td><code>subscriptions</code></td><td>object</td><td>Represents the <a href="../subscriptions/"><code>subscription</code></a> within the agreement.</td></tr><tr><td><code>parameters.fulfillment</code></td><td>object </td><td><p>(Optional) Represents the <a href="../../../api-usage-and-reference/common-api-objects/order-parameter.md"><code>orderParameter</code></a> object containing a concise definition of a parameter, its value, and any associated errors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
      "id": "PRM-1234-1234-1234",
      "name": "Tennant Id",
      "externalId": "tenant_id",
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
</code></pre></td></tr><tr><td><code>parameters.ordering</code></td><td>object </td><td><p>(Optional) Represents the <a href="../../../api-usage-and-reference/common-api-objects/order-parameter.md"><code>orderParameter</code></a> object containing a concise definition of a parameter, its value, and any associated errors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
      "id": "PRM-1234-1234-1234",
      "name": "Tennant Id",
      "externalId": "tenant_id",
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
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>externalIds</code></td><td>object</td><td>(Optional) Represents a set of <a href="../../../api-usage-and-reference/common-api-objects/externalids.md"><code>externalIds</code></a>.</td></tr><tr><td><code>termsAndConditions</code></td><td>object</td><td>(Read‑only) Represents the terms and conditions of the product that were accepted as part of the order. These values are then copied from the order into the agreement when the order is completed.</td></tr></tbody></table>

## Examples

{% tabs %}
{% tab title="MINIMAL EXAMPLE" %}
<pre class="language-json" data-title="AGREEMENT OBJECT" data-overflow="wrap" data-line-numbers><code class="lang-json">{
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
    { "id": "SUB-0792-5000-2253" }
  ],
  "parameters": {
    "ordering": [ ],
    "fulfillment": [ ]
<strong>  },
</strong>  "externalIDs": {
    "client": "12345678",
    "operations":	"07bf766b-c767-4293-9ab3",
    "vendor": "ABC-2023-C07-dbeee0b302c0"
  },
  "termsAndConditions":[
  {
     "id": "TCS-3159-1891-0980-8679",    
     "accepted": "2024-04-29T15:37:16.071Z",
     "acceptedBy": {
        "id": "USR-0000-0001",        
        "name": "Will Smith"
      },
      "name": "Microsoft 365 Terms of Service"
    }
  ]
}
</code></pre>
{% endtab %}

{% tab title="COMPLETE EXAMPLE" %}
{% code title="AGREEMENT OBJECT" overflow="wrap" lineNumbers="true" %}
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
      "id": "SUB-0792-5000-2253"      
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
  },
  "termsAndConditions":[
  {
     "id": "TCS-3159-1891-0980-8679",    
     "accepted": "2024-04-29T15:37:16.071Z",
     "acceptedBy": {
        "id": "USR-0000-0001",       
        "name": "Will Smith"
      },
      "name": "Microsoft 365 Terms of Service"
    }
  ]
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
