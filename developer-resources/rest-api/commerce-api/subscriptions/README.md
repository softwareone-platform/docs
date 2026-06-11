# Subscription

The Subscription object represents a collection of product items within the agreement.

All items are connected to one product, one vendor, and one client (same as the agreement) and have a common billing frequency and commitment terms.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="228">Field</th><th width="126">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The identifier for the subscription.</td></tr><tr><td><code>status</code></td><td>string</td><td><p>The key status of the object. Allowed values are: </p><ul><li><code>Active</code></li><li><code>Updating</code></li><li><code>Terminating</code></li><li><code>Terminated</code></li></ul></td></tr><tr><td><code>name</code></td><td>string</td><td>The name of the subscription.</td></tr><tr><td><code>agreement</code></td><td>object</td><td>(Read-only) Represents the <a href="../agreements/"><code>agreement</code></a> that contains the subscription.</td></tr><tr><td><code>product</code></td><td>object</td><td>(Read-only) Represents the <a href="../../catalog-api/product/"><code>product</code></a> object.</td></tr><tr><td><code>startDate</code></td><td>string</td><td>(Optional) The start date of the subscription.</td></tr><tr><td><code>commitmentDate</code></td><td>string</td><td>(Optional) The date when the subscription commitment ends and must be renewed.</td></tr><tr><td><code>terminationDate</code></td><td>string</td><td>(Optional) The date by which the subscription must be terminated.</td></tr><tr><td><code>terms</code></td><td>object</td><td>(Read-only) Represents the <a href="../../catalog-api/terms-and-conditions/"><code>term</code></a> object containing the billing terms of the subscription.</td></tr><tr><td><code>price</code></td><td>object</td><td>The price of the subscription.</td></tr><tr><td><code>lines</code></td><td>object</td><td>A list of all product items (lines) purchased in the scope of this subscription.</td></tr><tr><td><code>parameters</code></td><td>object</td><td>(Optional) Represents the <code>parameters</code> object, which groups separate lists of parameters. Only fulfillment parameters are available in this object.</td></tr><tr><td><code>parameters.fulfillment</code></td><td>object</td><td>(Optional) Represents the <code>parameters.fulfillment</code> object that holds a concise definition of a parameter, its value, and any associated errors.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>externalIDs</code></td><td>object</td><td>(Optional) Represents the <a href="../../../api-usage-and-reference/common-api-objects/externalids.md"><code>externalIDs</code></a> object containing a set of IDs.</td></tr><tr><td><code>autoRenew</code></td><td>bool</td><td>(Optional) A flag that indicates whether the subscription is set to auto‑renew. The vendor can update this field. By default, it is set to <code>true</code>.</td></tr></tbody></table>

## Examples <a href="#example" id="example"></a>

{% tabs %}
{% tab title="MINIMAL EXAMPLE" %}
{% code title="SUBSCRIPTION OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "SUB-5374-9558-1697-7803",  
  "name": "Subscription for Adobe Creative Cloud",
  "status": "Updating",
  "startDate": "2023-06-05T19:08:42.3656851+02:00",
  "renewalDate": "2024-07-20T09:50:59.1139069+02:00",
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
  },
  "autoRenew": true,
  "lines": [
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
}
```
{% endcode %}
{% endtab %}

{% tab title="COMPLETE EXAMPLE" %}
{% code title="SUBSCRIPTION OBJECT" overflow="wrap" lineNumbers="true" %}
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
    "id": "AGR-8808-0693-9072-0018"    
  },
  "order": {
    "id": "ORD-8556-1262-1387-2499",
    "type": "Purchase",
    "status": "Draft",
    "clientReferenceNumber": null,
    "notes": null
  },
  "autoRenewalEnabled": true,
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
        "unitPP": 1.25,
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
        "unitPP": 12.50,
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
