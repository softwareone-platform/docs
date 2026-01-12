# Assets

An asset is a one-time purchase item or a perpetual license within the Marketplace Platform. Assets assist vendors and SoftwareOne in differentiating each one-time item in the agreement.

The Asset object stores the fulfillment parameters provided by the vendor for these one-time items. This enables vendors to effectively identify and manage their one-time items by utilising the parameters stored during the fulfillment phase.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="112">Field</th><th width="146">Type </th><th>Example</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td>AST-2876-9782-1823</td></tr><tr><td>name</td><td><code>string</code></td><td>Access LTSC 2024 for Stark</td></tr><tr><td>status</td><td><code>string</code></td><td>Active</td></tr><tr><td>lines</td><td><code>lines</code></td><td><pre class="language-json" data-line-numbers><code class="lang-json">[
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
</code></pre></td></tr><tr><td>price</td><td><a href="../../common-api-objects/price.md"><code>price</code></a></td><td><pre class="language-json" data-line-numbers><code class="lang-json">{  
  "PPx1": 150,
  "SPx1": 165,
  "markup": 0.10,  
  "margin": 0.11,
  "defaultMarkup": 5.0,
  "currency": "USD"
}
</code></pre></td></tr><tr><td>externalIDs</td><td><a href="../../common-api-objects/externalids.md"><code>externalIDs</code></a></td><td><pre class="language-json" data-line-numbers><code class="lang-json">{
  "client": "12345678",
  "vendor": "ABC-2023-C07-dbeee0b302c0"
}
</code></pre></td></tr><tr><td>template</td><td><a href="../../catalog-api/templates/"><code>template</code></a></td><td><pre class="language-json" data-line-numbers><code class="lang-json">{
<strong>  "id": "TPL-2434-7545",    
</strong><strong>  "name": "Successful Deployment"
</strong>}
</code></pre></td></tr><tr><td>parameters.fulfillment</td><td><a href="../../common-api-objects/order-parameter.md"><code>orderParameter</code></a></td><td><pre class="language-json" data-line-numbers><code class="lang-json">{
    "name": "Order ID",
    "value": "ORD-2378-8237-9182",
    "constraints": {
        "readonly": false,
        "hidden": false,
        "required": true,
        "unique": false
    }
}
</code></pre></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td><p></p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } },
  "terminated": { "at": "...", "by": { } }
}
</code></pre></td></tr><tr><td>agreement</td><td><a href="../agreements/"><code>agreement</code></a></td><td><pre class="language-json" data-line-numbers><code class="lang-json">{
  "id": "AGR-2634-1298-0221",
  "name": "Microsoft Agr for Stark Industries"
}
</code></pre></td></tr><tr><td>product</td><td><a href="../../catalog-api/product/"><code>product</code></a></td><td><pre class="language-json" data-line-numbers><code class="lang-json">{
  "id": "PRD-7562-8393-0192",
  "name": "Microsoft Perpetual"
}
</code></pre></td></tr><tr><td>licensee</td><td><a href="../../accounts-api/licensee/"><code>licensee</code></a></td><td><pre class="language-json" data-line-numbers><code class="lang-json">{
  "id": "LCE-7562-8393-0192",
  "name": "Stark Industries"
}
</code></pre></td></tr><tr><td>listing</td><td><a href="../../catalog-api/listing/"><code>listing</code></a></td><td><pre class="language-json" data-line-numbers><code class="lang-json">{
  "id": "LST-1234-1234"
}
</code></pre></td></tr><tr><td>priceList</td><td><a href="../../catalog-api/pricelists/"><code>priceList</code></a></td><td><pre class="language-json" data-line-numbers><code class="lang-json">{
  "id": "PRC-1234-5678-9012"
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="ASSET OBJECT" %}
{% code lineNumbers="true" %}
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
{% endtab %}
{% endtabs %}
