# Subscriptions

The Subscriptions object represents a collection of product items within the agreement.

All items are connected to one product, one vendor, and one client (same as the agreement) and have a common billing frequency and commitment terms.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="202">Field</th><th width="126">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The identifier for the subscription object.</p><p>Example: SUB-2119-4550-8674-5962</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>Relative reference to the object in the API.</p><p>Example: /v1/commerce/subscriptions/SUB-2119-4550-8674-5962)</p></td></tr><tr><td>status</td><td><code>string</code></td><td><p>The key status of the object. Possible values are a by-product of the latest completed order that included this subscription. Possible statuses are a subset of all subscription statuses.</p><p>Example: Active</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the subscription.</p><p>Example: Subscription for Microsoft Office 365 NCE E1</p></td></tr><tr><td>agreement</td><td><a href="../agreements/"><code>agreement</code></a></td><td><p>The agreement that contains this particular subscription.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{   
    "id": "AGR-2119-4550-8674-5962",
    "name": "Microsoft Office 365 for My Company"
}
</code></pre></td></tr><tr><td>product</td><td><a href="../../catalog-api/product/"><code>product</code></a></td><td><p>Reference to the Product object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>startDate</td><td><code>string</code></td><td><p>The start date of the subscription.</p><p>Example: 2023-12-14T17:28:57Z</p></td></tr><tr><td>commitmentDate</td><td><code>string</code></td><td><p>The date when the subscription commitment ends and the subscription needs to be renewed.</p><p>Example: 2023-12-14T17:28:57Z</p></td></tr><tr><td>terminationDate</td><td><code>string</code></td><td><p>The date when the subscription is to be terminated.</p><p>Example: 2023-12-14T17:28:57Z</p></td></tr><tr><td>terms</td><td><a href="../../catalog-api/terms-and-conditions/"><code>terms</code></a></td><td><p>The subscription's billing terms.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "period": "1m",
  "commitment": "1y"
}
</code></pre></td></tr><tr><td>price</td><td><code>price</code></td><td><p>The price of the subscription.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "PPxY": 150,
  "PPxM": 12.50,
  "SPxY": 165,
  "SPxM": 13.75,
  "markup": 0.10,
  "margin": 0.11,
  "defaultMarkup": 0.15,
  "currency": "USD"
}
</code></pre></td></tr><tr><td>lines</td><td><code>lines</code></td><td><p>A list of all product items (lines) purchased in the scope of this subscription.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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
</code></pre></td></tr><tr><td>parameters</td><td><code>object</code></td><td><p>An object that groups separate lists of parameters. Only fulfillment parameters are available in this object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "fulfillment": [...]
}
</code></pre></td></tr><tr><td>parameters.fulfillment</td><td><code>object</code></td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "name": "New Subscription",
    "value": "Super_value_UPDATED",
    "constraints": {
        "readonly": false,
        "hidden": true,
        "required": true,
        "unique": false
    }
}
</code></pre></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>Audit object with possible entries: created, updated, activated, terminated, according to the object's lifecycle.</td></tr><tr><td>externalIDs</td><td><a href="../../common-api-objects/externalids.md"><code>externalIDs</code></a></td><td><p>Set of external IDs.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "client": "12345678",
  "vendor": "ABC-2023-C07-dbeee0b302c0"
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="SUBSCRIPTION OBJECT" %}
{% code lineNumbers="true" %}
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
{% endcode %}
{% endtab %}
{% endtabs %}
