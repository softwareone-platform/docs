# Order

An order is a request to create a new agreement or update an agreement to include a one-time purchase or set of subscriptions. There are different types of orders in the SoftwareOne Marketplace:

* **Purchase orders** – An order to buy a new product or service by establishing a new agreement.
* **Change orders** – An order to change the quantity, such as downsizing the quantity of licenses or ordering additional licenses.
* **Terminate order** – An order to terminate an active subscription or an agreement.
* **Configuration order** – An order to enable or disable the auto-renewal of a subscription.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="223">Field</th><th width="119">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The primary identifier for the order.</td></tr><tr><td><code>type</code></td><td>string</td><td>The type of order. The value is specified when the order is created and cannot be updated.</td></tr><tr><td><code>status</code></td><td>string</td><td>(Read-only) The status of the order.</td></tr><tr><td><code>externalIds</code></td><td>object</td><td>(Optional) Represents the <a href="../../../api-usage-and-reference/common-api-objects/externalids.md"><code>externalIds</code></a> object.</td></tr><tr><td><code>notes</code></td><td>string</td><td>(Optional) Contains initial customer notes added by the buyer during the purchase process. Buyers can edit and add notes at any time for all order statuses.</td></tr><tr><td><code>statusNotes</code></td><td>object</td><td>(Optional) Represents the <a href="../../notifications-api/messages/"><code>message</code></a> object containing notes added during a status change by the vendor or vendor extensions, indicating the reason for an order failure or status change.</td></tr><tr><td><code>error</code></td><td>object</td><td>(Optional) Represents the <a href="../../notifications-api/messages/"><code>message</code></a> object indicating a validation error returned by the vendor or vendor extension during order validation. The message may include markup.</td></tr><tr><td><code>agreement</code></td><td>object</td><td>Represents the <a href="../agreements/"><code>agreement</code></a> object.</td></tr><tr><td><code>authorization</code></td><td>object</td><td>(Read-only) Represents the <a href="../../catalog-api/authorization/"><code>authorization</code></a> object, which was used for the order.</td></tr><tr><td><code>listing</code></td><td>object</td><td>(Read-only) Represents the <a href="../../catalog-api/listing/"><code>listing</code></a> used for the order.</td></tr><tr><td><code>template</code></td><td>object</td><td>Represents the <a href="../../catalog-api/templates/"><code>template</code></a> object</td></tr><tr><td><code>assignee</code></td><td>object</td><td>(Optional) Represents the <a href="../../accounts-api/users/"><code>user</code></a> object</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>lines</code></td><td>object</td><td>(Optional) Contains information about the specific item that the buyer is purchasing/updating.</td></tr><tr><td><code>parameters.fulfillment</code></td><td>object</td><td>(Optional) An object that holds a concise definition of a parameter, its value, and any associated errors.</td></tr><tr><td><code>parameters.ordering</code></td><td>object</td><td>(Optional) An object that holds a concise definition of a parameter, its value, and any associated errors.</td></tr><tr><td><code>subscriptions</code></td><td>object</td><td>A list of references for <a href="../subscriptions/"><code>subscription</code></a> to be added or updated by the order.</td></tr><tr><td><code>price</code></td><td>object</td><td><p>(Read-only) Represents the total <a href="../../catalog-api/pricelists/"><code>price</code></a> for the order and is displayed to the various actors. </p><p>Not all fields are visible to all actors.</p></td></tr><tr><td><code>termsAndConditions</code></td><td>object</td><td>(Read-only) Represents the published terms and conditions of the product that are accepted as part of the order. The terms are accepted when the order is created and again when the order enters the processing state.</td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% code title="ORDER OBJECT" overflow="wrap" lineNumbers="true" %}
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
