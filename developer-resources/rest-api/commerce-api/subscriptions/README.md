# Subscriptions

The Subscriptions object represents a collection of product items within the agreement.&#x20;

All items are connected to one product, one vendor, and one client (same as the agreement) and have a common billing frequency and commitment terms. The Subscriptions object contains the following properties:

<table><thead><tr><th width="202">Field</th><th width="175">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Identifier for the subscription object. </p><p></p><p>Example: SUB-2119-4550-8674-5962</p></td></tr><tr><td>href</td><td>string</td><td><p>Relative reference to the object in the API.</p><p></p><p>Example: /v1/commerce/subscriptions/SUB-2119-4550-8674-5962)</p></td></tr><tr><td>status</td><td>string</td><td><p>The key status of the object. Possible values are a by-product of the latest completed order that included this subscription. Possible statuses are a subset of all subscription statuses. </p><p></p><p>Example: Active</p></td></tr><tr><td>name</td><td>string</td><td><p>Name of the subscription.</p><p></p><p>Example: Subscription for Microsoft Office 365 NCE E1</p></td></tr><tr><td>agreement</td><td>Agreement</td><td><p>The agreement that contains this particular subscription. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{   
    "id": "AGR-2119-4550-8674-5962",
    "name": "Microsoft Office 365 for My Company"
}
</code></pre></td></tr><tr><td>product</td><td>Product</td><td><p>Reference to the Product object.</p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>startDate</td><td>string</td><td><p>Start date of the subscription.</p><p></p><p>Example: 2023-12-14T17:28:57Z</p></td></tr><tr><td>commitmentDate</td><td>string</td><td><p>Date when the subscription commitment ends and the subscription needs to be renewed. </p><p></p><p>Example: 2023-12-14T17:28:57Z</p></td></tr><tr><td>terminationDate</td><td>string</td><td><p>Date when the subscription is to be terminated. </p><p></p><p>Example: 2023-12-14T17:28:57Z</p></td></tr><tr><td>terms</td><td>Terms</td><td><p>Subscription billing terms. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "period": "1m",
  "commitment": "1y"
}
</code></pre></td></tr><tr><td>price</td><td>Price</td><td><p>Price of the subscription.</p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "PPxY": 150,
  "PPxM": 12.50,
  "SPxY": 165,
  "SPxM": 13.75,
  "markup": 0.10,
  "margin": 0.11,
  "defaultMarkup": 0.15,
  "currency": "USD"
}
</code></pre></td></tr><tr><td>lines</td><td>Lines</td><td><p>List of all product items (lines) purchased in the scope of this subscription. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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
</code></pre></td></tr><tr><td>parameters</td><td>object</td><td><p>An object that groups separate lists of parameters. Only fulfillment parameters are available in this object.  </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "fulfillment": [...]
}
</code></pre></td></tr><tr><td>parameters.fulfillment</td><td>Order Parameter Object</td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "name": "New Subscription",
    "value": "Super_value_UPDATED",
    "constraints": {
        "readonly": false,
        "hidden": true,
        "required": true,
        "unique": false
    }
}
</code></pre></td></tr><tr><td>audit</td><td>AuditObject</td><td><p>Audit object with possible entries: created, updated, activated, terminated, according to the object's lifecycle. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } },
  "activated": { "at": "...", "by": { } },
  "terminated": { "at": "...", "by": { } }
}
</code></pre></td></tr><tr><td>externalIDs</td><td>ExternalIDsObject</td><td><p>Set of external IDs. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
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
  },
  "order": {
    "id": "ORD-8556-1262-1387-2499",
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
