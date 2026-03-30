# Orders

An order is a request to create a new agreement or update an agreement to include a one-time purchase or set of subscriptions. There are different types of orders in the SoftwareOne Marketplace:

* **Purchase orders** - An order to buy a new product or service by establishing a new agreement.
* **Change orders** - An order to change the quantity, such as downsizing the quantity of licenses or ordering additional licenses.
* **Terminate order** - An order to terminate an active subscription or an agreement.
* **Configuration order** - An order to enable or disable the auto-renewal of a subscription.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="184">Field Name</th><th width="164">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary identifier for the order.</p><p>Example: ORD-5542-1187-3130-0991</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>A relative reference to the object in the API.</p><p>Example: /commerce/orders/ORD-5542-1187-3130-0991</p></td></tr><tr><td><code>type</code></td><td>string</td><td><p>The type of order. The value is specified when the order is created and cannot be updated.</p><p>Example: Purchase</p></td></tr><tr><td><code>status</code></td><td>string</td><td><p>The status of the order.</p><p>Example: Processing</p></td></tr><tr><td><code>externalIds</code></td><td>externalIds</td><td><p><a href="../../common-api-objects/externalids.md"><code>externalIds</code></a> for client/vendor/distributor.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "client": "abc-123",
  "operations": "SO-1234-1234-1111"
}
</code></pre></td></tr><tr><td><code>notes</code></td><td>string</td><td><p>Contains initial customer notes added by the buyer during the purchase process. Buyers can edit and add notes at any time for all order statuses.</p><p>Example: Order of 2 subs for 2 ppl from the accounting dept.</p></td></tr><tr><td><code>statusNotes</code></td><td>object (<a href="../../notifications-api/messages/"><code>messageObject</code></a>)</td><td><p>Notes added during status change by the vendor or vendor extensions to indicate the reason for order failure or status change. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "E001234",
    "message": "Adobe cannot provision your subscription"
}
</code></pre></td></tr><tr><td><code>error</code></td><td>object (<a href="../../notifications-api/messages/"><code>messageObject</code></a></td><td><p>Standard error object. Means some error appeared on the parameters validation, which can include markup.<br></p><p>Used to indicate a validation error by the vendor or vendor extension during order validation.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "E001234",
    "message": "Order has incompatible items - education and government"
}
</code></pre></td></tr><tr><td><code>agreement</code></td><td>object</td><td><p>A reference to the <a href="../agreements/"><code>agreement</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "AGR-2119-4550-8674-5962",
    "name": "Microsoft Office 365 NCE E1",
    "icon": null
}
</code></pre></td></tr><tr><td><code>authorization</code></td><td>object</td><td><p>A reference to the <a href="../../catalog-api/authorization/"><code>authorization</code></a> object, which was used for the order.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "AUT-1234-4567",
    "name": "Salesforce Enterprise License"
}
</code></pre></td></tr><tr><td><code>listing</code></td><td>object</td><td><p>A reference to the <a href="../../catalog-api/listing/"><code>listing</code></a> that was used for the order.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "LST-1234-1234"
}
</code></pre></td></tr><tr><td><code>template</code></td><td>object</td><td><p>A reference to the <a href="../../catalog-api/templates/"><code>template</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "TPL-1234-4444",
    "name": "Successful Activation"
}
</code></pre></td></tr><tr><td><code>assignee</code></td><td>object</td><td><p>A reference to the <a href="../../accounts-api/users/"><code>user</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "TPL-1234-4444",
    "name": "Successful Activation"
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>lines</code></td><td>object</td><td><p>Contains information about the specific item that the buyer is purchasing/updating.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
   {
      "id": "ALI-1234-1234-1234-0001",
      "item": {
        "id": "ITM-1234-1234-1234-0021",
        "name": "Adobe Illustrator"
      },
      "quantity": 10,
      "price": { ... },
      "subscription": { "id": "SUB-1234-1234-1234" }
    },
    {
      "id": "ALI-1234-1234-1234-0002",
      "item": {
        "id": "ITM-4444-4444-4444-0031",
        "name": "Adobe Photoshop"
      },
      "quantity": 1,
      "price": { ... }
    }
]
</code></pre></td></tr><tr><td><code>parameters.fulfillment</code></td><td>object</td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
      "id": "PRM-1234-1234-1234-1234",
      "name": "Tennant Id",
      "externalId": "tenant_id",
      "value": "69b73824-ce76-4866-ad47-b615ae9d8998"
  }
]
</code></pre></td></tr><tr><td><code>parameters.ordering</code></td><td>object</td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
      "id": "PRM-1234-1234-1234-0001",
      "name": "Microsoft Partner ID",
      "externalId": "msPartnerId",
      "constraints": {
          "readonly": false,
          "hidden": false,
          "required": true
      },
      "value": "123456",
      "error": {
          "id": "E001234",
          "message": "Unknown MS Partner ID"
      }
  }
]
</code></pre></td></tr><tr><td><code>subscriptions</code></td><td>object</td><td><p>A list of references for <a href="../subscriptions/"><code>subscription</code></a> to be added or updated by the order.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  { "id": "SUB-5374-9558-1697-7777" },
  { "id": "SUB-5374-9558-1697-8888" },
  { "id": "SUB-5374-9558-1697-9999" }
]  
</code></pre></td></tr><tr><td><code>price</code></td><td>object</td><td><p>Represents the total <a href="../../catalog-api/pricelists/"><code>price</code></a> for the order and is displayed to the various actors. The object is <code>READONLY</code>.</p><p>Not all fields are visible to all actors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{  
  "PPxY": 150,  
  "PPxM": 12.50,  
  "SPxY": 165,  
  "SPxM": 13.75,  
  "markup": 0.10,  
  "margin": 0.11,  
  "defaultMarkup": 0.15,  
  "currency": "USD"
}  
</code></pre></td></tr><tr><td><code>termsAndConditions</code></td><td>object</td><td><p>Represents the terms and conditions in <code>published</code> state of the product being accepted as a part of the order. The terms are accepted on an order at the point of order creation and also at the point when the order is set to the processing state.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "TCS-3159-1891-0980-8679",    
    "accepted": "2024-04-29T15:37:16.071Z",
    "acceptedBy": {
       "id": "USR-0000-0001",
       "href": "/accounts/users/USR-0000-0001",
       "name": "Will Smith"
    },
    "name": "Microsoft 365 Terms of Service"
  }
]
</code></pre></td></tr></tbody></table>

## Example response

{% code lineNumbers="true" %}
```json
{
  "id": "ORD-6869-4529-8975-9005", 
  "agreement": {
    "id": "AGR-2119-4550-8674-5962",
    "name": "Microsoft Office 365 NCE E1"
  },
  "type": "Purchase",
  "status": "Processing",
  "statusNotes": {
    "id": "ERR-123-123",
    "message": "Vendor API is not responding. Try later"
  },
  "template": {
    "id": "TPL-1234-4444",
    "name": "Activation in Progress"
  },
  "assignee": {
    "id": "USR-1234-1234-1234",
    "name": "John Smith",
    "icon": "/static/users/USR-1234-1234-1234.icon.svg"
  },
  "lines": [
      {  // Upsize
        "id": "ALI-1234-1234-1234-0001",
        "item": {
          "id": "ITM-1234-1234-1234-0021",
          "name": "Adobe Illustrator"
        },
        "quantity": 10,
        "price": { ... },
        "subscription": { "id": "SUB-1234-1234-1234" }
      },
      {   // New purchase
        "id": "ALI-1234-1234-1234-0002",
        "item": {
          "id": "ITM-4444-4444-4444-0031",
          "name": "Adobe Photoshop"
        },
        "quantity": 1,
        "price": { ... }
      }
  ],
  "notes": "Order for accounting team",
  "parameters": {
    "fulfillment": [
      {
        "id": "PRM-1234-1234-1234-1234",
        "name": "Tennant Id",
        "externalId": "tenant_id",
        "value": "69b73824-ce76-4866-ad47-b615ae9d8998"
      }
    ],
    "ordering": [
      {
        "id": "PRM-1234-1234-1234-0001",
        "name": "Microsoft Partner ID",
        "externalId": "msPartnerId",
        "constraints": {
            "readonly": false,
            "hidden": false,
            "required": true
        },
        "value": "123456",
        "error": {
            "id": "E001234",
            "message": "Unknown MS Partner ID"
        }
      }
    ]
  },
  "externalIDs": {
    "client": "abc-123",
    "operations": "SO-1234-1234-1111"
  },
  "termsAndConditions":[
  {
     "id": "TCS-3159-1891-0980-8679",   
     "accepted": "2024-04-29T15:37:16.071Z",
     "acceptedBy": {
        "id": "USR-0000-0001",
        "href": "/accounts/users/USR-0000-0001",
        "name": "Will Smith"
      },
      "name": "Microsoft 365 Terms of Service"
    }
  ],
  "audit": {
    "created": { "at": "...", "by": { } },
    "updated": { "at": "...", "by": { } }
  }
}
```
{% endcode %}
