# Subscription

The `subscription` object represents a collection of product items within the agreement.

All items are connected to one product, one vendor, and one client (same as the agreement) and have a common billing frequency and commitment terms.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="202">Field Name</th><th width="126">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The identifier for the <code>subscription</code> .</p><p>Example: SUB-2119-4550-8674-5962</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>Relative reference to the object in the API.</p><p>Example: /v1/commerce/subscriptions/SUB-2119-4550-8674-5962)</p></td></tr><tr><td><code>status</code></td><td>string</td><td><p>The key status of the object. Possible values are a by-product of the latest completed order that included this subscription. Possible statuses are a subset of all subscription statuses.</p><p>Example: Active</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the subscription.</p><p>Example: Subscription for Microsoft Office 365 NCE E1</p></td></tr><tr><td><code>agreement</code></td><td>object</td><td><p>The <a href="../agreements/"><code>agreement</code></a> that contains this particular subscription.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{   
    "id": "AGR-2119-4550-8674-5962",
    "name": "Microsoft Office 365 for My Company"
}
</code></pre></td></tr><tr><td><code>product</code></td><td>object</td><td><p>Reference to the <a href="../../catalog-api/product/"><code>product</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td><code>startDate</code></td><td>string</td><td><p>The start date of the subscription.</p><p>Example: 2023-12-14T17:28:57Z</p></td></tr><tr><td><code>commitmentDate</code></td><td>string</td><td><p>The date when the subscription commitment ends and the subscription needs to be renewed.</p><p>Example: 2023-12-14T17:28:57Z</p></td></tr><tr><td><code>terminationDate</code></td><td>string</td><td><p>The date when the subscription is to be terminated.</p><p>Example: 2023-12-14T17:28:57Z</p></td></tr><tr><td><code>terms</code></td><td>object</td><td><p>The subscription's billing <a href="../../catalog-api/terms-and-conditions/"><code>terms</code></a>.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "period": "1m",
  "commitment": "1y"
}
</code></pre></td></tr><tr><td><code>price</code></td><td>object</td><td><p>The price of the subscription.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "PPxY": 150,
  "PPxM": 12.50,
  "SPxY": 165,
  "SPxM": 13.75,
  "markup": 0.10,
  "margin": 0.11,
  "defaultMarkup": 0.15,
  "currency": "USD"
}
</code></pre></td></tr><tr><td><code>lines</code></td><td>object</td><td><p>A list of all product items (lines) purchased in the scope of this subscription.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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
</code></pre></td></tr><tr><td><code>parameters</code></td><td>object</td><td><p>An object that groups separate lists of parameters. Only fulfillment parameters are available in this object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "fulfillment": [...]
}
</code></pre></td></tr><tr><td><code>parameters.fulfillment</code></td><td>object</td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "name": "New Subscription",
    "value": "Super_value_UPDATED",
    "constraints": {
        "readonly": false,
        "hidden": true,
        "required": true,
        "unique": false
    }
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. Allowed values: <code>created</code>, <code>updated</code>, <code>activated</code>, or <code>terminated</code>.</td></tr><tr><td><code>externalIDs</code></td><td>externalIDs</td><td><p>A set of <a href="../../common-api-objects/externalids.md"><code>externalIDs</code></a>.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "client": "12345678",
  "vendor": "ABC-2023-C07-dbeee0b302c0"
}
</code></pre></td></tr></tbody></table>

## Example response

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
