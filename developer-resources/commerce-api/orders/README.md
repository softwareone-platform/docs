# Orders

An order is a request made by a buyer to create/update an agreement with a one-time purchase or/and set of subscriptions. There are three types of Orders.

* Purchase - A purchase order is the first order created in the lifecycle of an agreement. The purchase order is always the first order and there is only one within an agreement.
* Change - A change order is a request to update the agreement. There can be multiple change orders in an agreement.
* Termination - A termination order is a request to terminate the agreement or terminate a specific subscription within the agreement. There can be multiple termination orders.

<table><thead><tr><th>Field</th><th>Type</th><th width="173">Constraints</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p><code>READONLY</code> </p><p><code>IDX</code></p></td><td><p>Primary order identifier </p><p></p><p>Example: "ORD-5542-1187-3130-0991"</p></td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td><code>READONLY</code></td><td><p>Relative reference to object on API (always /commerce/orders/{id}) </p><p></p><p>Example: "/commerce/orders/ORD-5542-1187-3130-0991"</p></td></tr><tr><td><strong><code>type</code></strong></td><td>string</td><td><p><code>FINAL</code> </p><p><code>IDX</code></p><p><code>enum</code></p></td><td><p>Specified on creation of order, cannot be updated. </p><p></p><p>Example: "Purchase"</p></td></tr><tr><td><strong><code>status</code></strong></td><td>string</td><td><p><code>READONLY</code></p><p> <code>IDX</code></p><p><code>enum</code></p></td><td>Example: "Processing"</td></tr><tr><td><strong><code>externalIds</code></strong></td><td>ExternalIds</td><td><p><code>OPTIONAL</code> </p><p><code>IDX</code></p></td><td><p>External IDs for either client/vendor/distributor.</p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "client": "abc-123",
  "operations": "SO-1234-1234-1111"
}
</code></pre></td></tr><tr><td><strong><code>notes</code></strong></td><td>string</td><td><code>OPTIONAL</code></td><td><p>Contains initial customer notes added by Buyer during purchase process. Buyer can edit and add notes at any time for all order statuses. Managed by client. Not used by vendor extensions. </p><p></p><p></p><p>Example: "Order of 2 subs for 2 ppl from accounting dept."</p></td></tr><tr><td><strong><code>statusNotes</code></strong></td><td>Message Object</td><td><code>OPTIONAL</code></td><td><p>Notes added during status change by vendor or vendor extensions to indicate reason of order failure or status change. Should be shown on order screen (as part of template or standalone). </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "E001234",
    "message": "Adobe cannot provision your subscription"
}
</code></pre></td></tr><tr><td><strong><code>error</code></strong></td><td>Message Object</td><td><p><code>OPTIONAL</code></p><p><code>MARKUP</code></p></td><td><p>Standard error object. Means some error appeared on parameters validation, which can include markup.<br>Used to indicate validation error by vendor or vendor extension during order validation.<br>Should be reflected in purchase wizard while parameters validation and on the parameters and the items screens of order.<br>Should behave like errors in parametes, i.e. reset on order status changes.</p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "E001234",
    "message": "Order has incompatible items - eductation and goverment"
}
</code></pre></td></tr><tr><td><strong><code>agreement</code></strong></td><td>Agreement</td><td><p><code>FINAL</code> </p><p><code>IDX</code></p></td><td><p>The agreement represents an instance of a relationship between Seller, Buyer, and Licensee. </p><p></p><p>It may refer to one-time purchases or/and set of subscriptions. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "AGR-2119-4550-8674-5962",
    "href": "/commerce/agreements/AGR-2119-4550-8674-5962",
    "name": "Microsoft Office 365 NCE E1",
    "icon": null
}
</code></pre></td></tr><tr><td><strong><code>authorization</code></strong></td><td>Authorization</td><td><p><code>READONLY</code><br><code>FINAL</code> </p><p><code>IDX</code></p></td><td><p>Reference to Authorization object which was used for ther order. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "AUT-1234-4567",
    "href": "/authorization/ATH-1234-45678",
    "name": "Salesforce Enterprise License"
}
</code></pre></td></tr><tr><td><strong><code>listing</code></strong></td><td>Listing</td><td><p><code>READONLY</code><br><code>FINAL</code> </p><p><code>IDX</code></p></td><td><p>Reference to Listing which was used for the order.</p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "LST-1234-1234"
}
</code></pre></td></tr><tr><td><strong><code>template</code></strong></td><td>Template</td><td></td><td><p> Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "TPL-1234-4444",
    "href": "/products/product/PRD-1234-1234-1234/templates/TPL-1234-4444",
    "name": "Succesful Activation"
}
</code></pre></td></tr><tr><td><strong><code>assignee</code></strong></td><td>User</td><td><code>OPTIONAL</code></td><td><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "TPL-1234-4444",
    "href": "/products/product/PRD-1234-1234-1234/templates/TPL-1234-4444",
    "name": "Succesful Activation"
}
</code></pre></td></tr><tr><td><strong><code>audit</code></strong></td><td>AuditObject</td><td><p><code>READONLY</code> </p><p><code>IDX</code></p></td><td><p>AuditObject is a dictionary with events that happened with the object, every event has “at<strong>”</strong> part which specifies the last time the event occurred, and “by” part which specifies who the actor executed the event. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } },
  "activated": { "at": "...", "by": { } },
  "terminated": { "at": "...", "by": { } }
}
</code></pre></td></tr><tr><td><strong><code>lines[]</code></strong></td><td>Line[]</td><td><code>OPTIONAL</code></td><td><p>An Order Lines contains the information about the specific item the Buyer is purchasing/updating.  </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">[
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
</code></pre></td></tr><tr><td><strong><code>parameters.fulfillment</code></strong></td><td>Order Parameter Object []</td><td><code>OPTIONAL</code></td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors.  </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">[
  {
      "id": "PRM-1234-1234-1234-1234",
      "name": "Tennant Id",
      "externalId": "tennant_id",
      "value": "69b73824-ce76-4866-ad47-b615ae9d8998"
  }
]
</code></pre></td></tr><tr><td><strong><code>parameters.ordering</code></strong></td><td>Order Parameter Object []</td><td><code>OPTIONAL</code></td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">[
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
</code></pre></td></tr><tr><td><strong><code>subscriptions</code></strong></td><td>Subscription</td><td><code>IDX</code></td><td><p>List of subscription references, for these subscriptions that going to be added/updated by the order. On POST or PUT, lines property of subscription can be provided to reflect these changes. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">[
  { "id": "SUB-5374-9558-1697-7777" },
  { "id": "SUB-5374-9558-1697-8888" },
  { "id": "SUB-5374-9558-1697-9999" }
]  
</code></pre></td></tr><tr><td><code>price</code></td><td>Price</td><td> </td><td><p>This represents the total price for an Order and is displayed to the various actors. Object is READONLY</p><p> </p><p>Please note not all fields are visible to all actors.  </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{  
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
