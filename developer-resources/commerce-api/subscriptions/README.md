# Subscriptions

## Subscriptions object

The `subscriptions` object represents a collection of Product Items inside the Agreement. All items are connected to one Product, one vendor, and one client (the same as the agreement) and have common billing frequency and commitment terms.&#x20;

This object contains the following properties:

<table><thead><tr><th width="232">Field</th><th width="175">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Human Friendly identifier of Subscription object. </p><p></p><p>Example: "SUB-2119-4550-8674-5962"</p></td></tr><tr><td>href</td><td>string</td><td><p>Relative reference to object on API (always <code>/commerce/agreements/{id}</code>) </p><p></p><p>Example: "/v1/commerce/subscriptions/SUB-2119-4550-8674-5962)"</p></td></tr><tr><td>status</td><td>string</td><td><p>The key status of the object. </p><p>Possible values are a by-product of the latest completed order that touched this subscription. Possible statuses are a subset of all subscription statuses. </p><p></p><p>Example: "Active"</p></td></tr><tr><td>name</td><td>string</td><td><p>Subscription name. </p><p></p><p>Example: Subscription for Microsoft Office 365 NCE E1</p></td></tr><tr><td>agreement</td><td>Agreement</td><td><p>Agreement that holds this particular Subscription instance. </p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">{   
    "id": "AGR-2119-4550-8674-5962",
    "href": "/commerce/agreements/ACC-1234-1234",
    "name": "Microsoft Office 365 for My Company"
}
</code></pre></td></tr><tr><td>product</td><td>Product</td><td><p>Product reference </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "href": "/catalog/products/PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>startDate</td><td>string</td><td><p>Effective date of subscription start<br>may be not defined in sciope of order). </p><p></p><p>Example: "2023-12-14T17:28:57Z"</p></td></tr><tr><td>commitmentDate</td><td>string</td><td><p>Date when subscription commitment ends and subscription to be renewed. </p><p></p><p>Example: "2023-12-14T17:28:57Z"</p></td></tr><tr><td>terminationDate</td><td>string</td><td><p>Date when subscription to be terminated. </p><p></p><p>Example: "2023-12-14T17:28:57Z"</p></td></tr><tr><td>terms</td><td>Terms</td><td><p>Subscription billing terms. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "period": "1m",
  "commitment": "1y"
}
</code></pre></td></tr><tr><td>price</td><td>Price</td><td><p>Price for subscription, not all fields visible for everyone see details in Price, most of the object should be READONLY as it is calculated on orders completion, with only exception OPS can edit default markup for an active subscriptions. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "PPxY": 150,
  "PPxM": 12.50,
  "SPxY": 165,
  "SPxM": 13.75,
  "markup": 0.10,
  "margin": 0.11,
  "defaultMarkup": 0.15,
  "currency": "USD"
}
</code></pre></td></tr><tr><td>lines</td><td>Lines[]</td><td><p>List of all product items (lines) purchasedi n scope of this subscription. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">[
  { 
    "id": "ALI-1234-1234-1234-0001",
    "item": {
      "id": "ITM-1234-1234-1234-0021",
      "name": "Adobe Illustrator"
    },
    "quantity": 10,
    "price": { ... }
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
</code></pre></td></tr><tr><td>parameters</td><td>object</td><td><p>An object that groups together separate lists of parameters.<br>Only fulfillment parameters are available in this object.  </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "fulfillment": [...]
}
</code></pre></td></tr><tr><td>parameters.fulfillment</td><td>Order Parameter Object</td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "name": "New Subscription",
    "value": "Super_value_UPDATED",
    "constraints": {
        "readonly": false,
        "hidden": true,
        "required": true,
        "unique": false
    }
}
</code></pre></td></tr><tr><td>audit</td><td>AuditObject</td><td><p>Audit object with possible entries: created, updated, activated, terminated, according to the object's lifecycle. </p><p></p><p>Possible audit events: Created, Updated, Activated, Terminated, and Failed. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } },
  "activated": { "at": "...", "by": { } },
  "terminated": { "at": "...", "by": { } }
}
</code></pre></td></tr><tr><td>externalIDs</td><td>ExternalIDsObject</td><td><p>Set of external IDs. </p><p></p><p>Example: </p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "client": "12345678",
  "vendor": "ABC-2023-C07-dbeee0b302c0"
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="SUBSCRIPTION OBJECT" %}
```json
{
  "id": "SUB-5903-9370-1653-5455",
  "href": "/commerce/subscriptions/SUB-5903-9370-1653-5455",
  "name": "Subscription for Avast Pro",
  "status": "Updating",
  "startDate": "2025-10-05T04:46:24.0758413+02:00",
  "renewalDate": "2024-03-20T08:47:50.7092432+01:00",
  "terms": {
    "period": "1m",
    "commitment": "1y"
  },
  "price": {
    "margin": 0.01,
    "markup": 0.011,
    "SPxM": 1708.12,
    "SPxY": 20504.00,
    "PPxM": 7.12,
    "PPxY": 88.00,
    "defaultMarkup": 0.15,
    "currency": "USD"
  },
  "externalIDs": {
    "client": "12345678",
    "vendor": "ABC-2023-C07-dbeee0b302c0"
  },,
  "agreement": {
    "id": "AGR-8808-0693-9072-0018",
    "href": "/commerce/agreements/AGR-8808-0693-9072-0018"
  },
  "order": {
    "id": "ORD-8556-1262-1387-2499",
    "href": "/commerce/orders/ORD-8556-1262-1387-2499",
    "type": "Purchase",
    "status": "Draft",
    "clientReferenceNumber": null,
    "notes": null
  },
  "lines": [
    {
      "id": "ALI-1234-1234-1234-0001",
      "item": {
        "id": "ITM-1234-1234-1234-0021",
        "name": "Adobe Illustrator"
      },
      "quantity": 10,
      "price": {
        "PPxY": 150,
        "PPxM": 12.50,
        "unitPP": 1.25
        "SPxY": 165,
        "SPxM": 13.50,
        "unitSP": 1.35,
        "markup": 0.10,
        "margin": 0.11,
        "currency": "USD"
      }
    },
    {
      "id": "ALI-1234-1234-1234-0002",
      "item": {
        "id": "ITM-4444-4444-4444-0031",
        "name": "Adobe Photoshop"
      },
      "price": {
        "PPxY": 150,
        "PPxM": 12.50,
        "unitPP": 12.50
        "SPxY": 165,
        "SPxM": 13.50,
        "unitSP": 13.50,
        "markup": 0.10,
        "margin": 0.11,
        "currency": "USD"
      }
    }
  ]
}
```
{% endtab %}
{% endtabs %}
