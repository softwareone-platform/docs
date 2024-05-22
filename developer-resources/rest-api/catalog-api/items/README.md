# Items

## Item object

The Item Object represents a “product item” as a transactable element of a product that, for example, in a created order, is represented as a “line item” of that order.

<table><thead><tr><th>Field</th><th width="249">Type</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p>Platform generated Id. </p><p></p><p>Example: "ITM-0690-0539-0001"</p></td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td><p>The resource URI of the Item. </p><p></p><p>Example: "/product-items/ITM-0690-0539-0001"</p></td></tr><tr><td><strong><code>name</code></strong></td><td>string</td><td><p>Name of the item. </p><p></p><p>Example: "Microsoft 365 Apps for Business"</p></td></tr><tr><td><strong><code>description</code></strong></td><td>string</td><td><p>Item description. </p><p></p><p>Example: "Best for businesses that need Office apps across devices and cloud file storage. For businesses with up to 300 employees."</p></td></tr><tr><td><strong><code>externalIds</code></strong></td><td><a href="./#externalids">ExternalIds</a></td><td><p> Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "vendor": "ven-1233-3222",
  "operations": "op-322-322",
}
</code></pre></td></tr><tr><td><strong><code>terms</code></strong></td><td>Terms</td><td><p>Terms for the Items, as defined in Terms object. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "period": "1m",
  "commitment": "1y"
}
</code></pre></td></tr><tr><td><strong><code>quantityNotApplicable</code></strong></td><td>boolean</td><td><p>Is quantity is not applicable or relevant to the product item being sold. </p><p></p><p>Example: "true"</p></td></tr><tr><td><strong><code>status</code></strong></td><td>Draft, Published, or Upublished</td><td><p>Status of the item. </p><p></p><p>Example: "Draft"</p></td></tr><tr><td><strong><code>parameters</code></strong></td><td><a href="./#parameter">ParameterValue</a></td><td><p>Captures any additional information required for a product item and is defined by item configuration parameters.</p><p><br>Only item configuration parameters are available on this list. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{ 
  "id": "PRM-1234-1234-1234",
  "externalId": "SKU",
  "value": "65272478BB01A12"
}
</code></pre></td></tr><tr><td><strong><code>group</code></strong></td><td><a href="../item-groups/">ItemGroup</a></td><td>Item group to wich item is assigned.</td></tr><tr><td><strong><code>unit</code></strong></td><td><a href="../unit-of-measure/">UnitOfMeasure</a></td><td>Unit of measure assigned to item.</td></tr><tr><td><strong><code>product</code></strong></td><td><a href="../product/">Product</a></td><td>Product to which item is assigned.</td></tr><tr><td><strong><code>audit</code></strong></td><td>AuditObject</td><td><p>Audit object with possible entries: created, updated, activated, terminated, according to lifecycle of the object. Possible audit events: <strong>created</strong>, <strong>updated</strong>. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Parameter <a href="#parameter" id="parameter"></a>

The parameter object contains the value of the given parameter along with additional information like constraints.

| Field            | Parameter | Description                                                                                                 |
| ---------------- | --------- | ----------------------------------------------------------------------------------------------------------- |
| **`id`**         | string    | <p>Identifier of parameter definition this value refers to. </p><p></p><p>Example: "PDF-1234-1234-1234"</p> |
| **`externalId`** | string    | <p>Id of the parameter in external system. </p><p></p><p>Example: "SKU"</p>                                 |
| **`name`**       | string    | <p>Parameter display name. </p><p></p><p>Example: "Stock keeping unit"</p>                                  |
| **`value`**      | string    | <p>Value of the parameter. </p><p></p><p>Example: "65272478BB01A12"</p>                                     |

## ExternalIds <a href="#externalids" id="externalids"></a>

ExternalIds contain any external identifier

| Field        | Type   | Description                                                                                                                                            |
| ------------ | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **`vendor`** | string | A vendor identifier is item identifier recognizable by vendor, so when an order is placed they will easily understand which item is to be provisioned. |

## Example

{% tabs %}
{% tab title="ITEM OBJECT" %}
```json
{
    "id": "ITM-0690-0539-0001",
    "href": "/product-items/ITM-0690-0539-0001",
    "name": "Microsoft 365 Online Services for Charity",
    "description": "mashaTestTajfunTeam",
    "state": "Draft",
    "parameters": [
      {
        "id": "PRM-0690-0539-0001",
        "externalId": "SKU",
        "name": "Stock keeping unit",
        "value": "65272478BB01A12"
      },
      {
        "id": "PRM-0690-0539-0004",
        "externalId": "countries",
        "name": "Countries (checkboxes)",
        "value": [
          "us",
          "eu",
          "jp"
        ]
      },
      {
        "id": "PRM-0690-0539-0004",
        "externalId": "countries",
        "name": "Countries (checkboxes)",
        "value": {
          "addressLine1": "123 Main Street",
          "addressLine2": "Apt 4B",
          "postCode": "12345",
          "city": "Cityville",
          "state": "S",
          "country": "ST"
        }
      },            
      {
        "id": "PRM-0690-0539-0002",
        "externalId": "JSON_data",
        "name": "Information stored by vendor integration",      
        "value": { ...data... }
      }    
    ],
    "group": {
        "id": "IGR-0690-0539-0001",
    },
    "unit": {
        "id": "UNT-7362",
    },
    "product": {
        "id": "PRD-0690-0539",
    },
    "audit": {
        "created": { "at": "...", "by": { } },
        "updated": { "at": "...", "by": { } }
    }
}

```
{% endtab %}
{% endtabs %}
