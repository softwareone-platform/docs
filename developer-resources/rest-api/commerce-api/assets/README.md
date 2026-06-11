# Asset

An asset is a one-time purchase item or a perpetual license within the Marketplace Platform. Assets assist vendors and SoftwareOne in differentiating each one-time item in the agreement.

The Asset object stores the fulfillment parameters provided by the vendor for these one-time items. This enables vendors to effectively identify and manage their one-time items by utilizing the parameters stored during the fulfillment phase.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="218">Field</th><th width="124">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>The primary identifier for the asset.</td></tr><tr><td><code>name</code></td><td>string</td><td>The name of the asset.</td></tr><tr><td><code>status</code></td><td>string</td><td>(Read-only) The status of the asset. </td></tr><tr><td><code>lines</code></td><td>object</td><td>(Optional) Represents the <a href="../line.md"><code>lines</code></a> object.</td></tr><tr><td><code>price</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/price.md"><code>price</code></a> object. </td></tr><tr><td><code>externalIDs</code></td><td>object</td><td>(Optional) Represents the <a href="../../../api-usage-and-reference/common-api-objects/externalids.md"><code>externalIDs</code></a> object.</td></tr><tr><td><code>template</code></td><td>object</td><td>(Optional) Represents the <a href="../../catalog-api/templates/"><code>template</code></a> object.</td></tr><tr><td><code>parameters.fulfillment</code></td><td>object</td><td>(Optional) Represents the <a href="../../../api-usage-and-reference/common-api-objects/order-parameter.md"><code>parameter</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>agreement</code></td><td>object</td><td>Represents the <a href="../agreements/"><code>agreement</code></a> object.</td></tr><tr><td><code>product</code></td><td>object</td><td>Represents the <a href="../../catalog-api/product/"><code>product</code></a> object.</td></tr><tr><td><code>licensee</code></td><td>object</td><td>Represents the <a href="../../accounts-api/licensee/"><code>licensee</code></a> object.</td></tr><tr><td><code>listing</code></td><td>object</td><td>Represents the <a href="../../catalog-api/listing/"><code>listing</code></a> object.</td></tr><tr><td><code>priceList</code></td><td>object</td><td>Represents the <a href="../../catalog-api/pricelists/"><code>priceList</code></a> object.</td></tr></tbody></table>

## Example

{% code title="ASSET OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "AST-2876-9782-1823", 
  "name": "Access LTSC 2024 for Stark",
  "status": "Active",
  "lines": [
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
  ],
  "price": {  
    "PPx1": 150,
    "SPx1": 165,
    "markup": 0.10,  
    "margin": 0.11,
    "defaultMarkup": 5.0,
    "currency": "USD"
  },
  "externalIDs": {
    "client": "12345678",
    "vendor": "ABC-2023-C07-dbeee0b302c0"
  },
  "template": {
      "id": "TPL-2434-7545",    
      "name": "Successful Deployment"
  },
  "parameters": {
    "fulfillment": {
        "name": "Order ID",
        "value": "ORD-2378-8237-9182",
        "constraints": {
            "readonly": false,
            "hidden": false,
            "required": true,
            "unique": false
        }
    }
  },
  "agreement": {
    "id": "AGR-2634-1298-0221",
    "name": "Microsoft Agr for Stark Industries"
  },
  "product": {
    "id": "PRD-7562-8393-0192",
    "name": "Microsoft Perpetual"
  },
  "licensee": {
    "id": "LCE-7562-8393-0192",
    "name": "Stark Industries"
  },
  "listing": {
    "id": "LST-1234-1234"
  },
  "priceList": {
    "id": "PRC-1234-5678-9012"
  },
  "audit": {
    "created": { "at": "...", "by": { } },
    "updated": { "at": "...", "by": { } }
  }
}
```
{% endcode %}
