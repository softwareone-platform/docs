# Orders

An order is a request made by a buyer to create/update an agreement with a one-time purchase or/and set of subscriptions. There are three types of Orders.

* Purchase - A purchase order is the first order created in the lifecycle of an agreement. The purchase order is always the first order, and there is only one within an agreement.
* Change - A change order is a request to update the agreement. There can be multiple change orders in an agreement.
* Termination - A termination order is a request to terminate the agreement or terminate a specific subscription within the agreement. There can be multiple termination orders.

The Order object contains the following properties:

<table><thead><tr><th width="144">Field</th><th width="164">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Primary identifier for the order. </p><p></p><p>Example: ORD-5542-1187-3130-0991</p></td></tr><tr><td>href</td><td>string</td><td><p>Relative reference to the object in the API.</p><p></p><p>Example: /commerce/orders/ORD-5542-1187-3130-0991</p></td></tr><tr><td>type</td><td>string</td><td><p>The type of order. Specified when the order is created and cannot be updated. </p><p></p><p>Example: Purchase</p></td></tr><tr><td>status</td><td>string</td><td><p>Status of the order. </p><p></p><p>Example: Processing</p></td></tr><tr><td>externalIds</td><td>ExternalIds</td><td><p>External IDs for either client/vendor/distributor.</p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "client": "abc-123",
  "operations": "SO-1234-1234-1111"
}
</code></pre></td></tr><tr><td>notes</td><td>string</td><td><p>Contains initial customer notes added by the buyer during the purchase process. Buyers can edit and add notes at any time for all order statuses.</p><p></p><p>Example: Order of 2 subs for 2 ppl from the accounting dept.</p></td></tr><tr><td>statusNotes</td><td>Message Object</td><td><p>Notes added during status change by the vendor or vendor extensions to indicate the reason for order failure or status change. </p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "E001234",
    "message": "Adobe cannot provision your subscription"
}
</code></pre></td></tr><tr><td>error</td><td>Message Object</td><td><p>Standard error object. Means some error appeared on the parameters validation, which can include markup.<br></p><p>Used to indicate a validation error by the vendor or vendor extension during order validation.</p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "E001234",
    "message": "Order has incompatible items - education and government"
}
</code></pre></td></tr><tr><td>agreement</td><td>Agreement</td><td><p>The agreement represents an instance of a relationship between the seller, buyer, and the licensee. </p><p></p><p>It may refer to one-time purchases or/and set of subscriptions. </p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "AGR-2119-4550-8674-5962",
    "name": "Microsoft Office 365 NCE E1",
    "icon": null
}
</code></pre></td></tr><tr><td>authorization</td><td>Authorization</td><td><p>Reference to the Authorization object which was used for the order. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "AUT-1234-4567",
    "name": "Salesforce Enterprise License"
}
</code></pre></td></tr><tr><td>listing</td><td>Listing</td><td><p>Reference to the listing that was used for the order.</p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "LST-1234-1234"
}
</code></pre></td></tr><tr><td>template</td><td>Template</td><td><p>Reference to the Template object.</p><p> </p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "TPL-1234-4444",
    "name": "Succesful Activation"
}
</code></pre></td></tr><tr><td>assignee</td><td>User</td><td><p>Reference to the User object.</p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "TPL-1234-4444",
    "name": "Succesful Activation"
}
</code></pre></td></tr><tr><td>audit</td><td>AuditObject</td><td><p>Reference to the Audit object.</p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } },
  "activated": { "at": "...", "by": { } },
  "terminated": { "at": "...", "by": { } }
}
</code></pre></td></tr><tr><td>lines</td><td>Line</td><td><p>Order lines contain the information about the specific item the buyer is purchasing/updating.  </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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
</code></pre></td></tr><tr><td>parameters.fulfillment</td><td>Order Parameter Object</td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors.  </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
      "id": "PRM-1234-1234-1234-1234",
      "name": "Tennant Id",
      "externalId": "tenant_id",
      "value": "69b73824-ce76-4866-ad47-b615ae9d8998"
  }
]
</code></pre></td></tr><tr><td>parameters.ordering</td><td>Order Parameter Object</td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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
</code></pre></td></tr><tr><td>subscriptions</td><td>Subscription</td><td><p>List of subscription references for subscriptions to be added or updated by the order. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  { "id": "SUB-5374-9558-1697-7777" },
  { "id": "SUB-5374-9558-1697-8888" },
  { "id": "SUB-5374-9558-1697-9999" }
]  
</code></pre></td></tr><tr><td>price</td><td>Price</td><td><p>Represents the total price for the order and is displayed to the various actors. The object is <code>READONLY</code>.</p><p> </p><p>Not all fields are visible to all actors.  </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{  
  "PPxY": 150,  
  "PPxM": 12.50,  
  "SPxY": 165,  
  "SPxM": 13.75,  
  "markup": 0.10,  
  "margin": 0.11,  
  "defaultMarkup": 0.15,  
  "currency": "USD"
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="ORDER OBJECT" %}
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
        "externalId": "tennant_id",
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
  "audit": {
    "created": { "at": "...", "by": { } },
    "updated": { "at": "...", "by": { } },
    "activated": { "at": "...", "by": { } },
    "terminated": { "at": "...", "by": { } }
  }
}
```
{% endtab %}
{% endtabs %}
