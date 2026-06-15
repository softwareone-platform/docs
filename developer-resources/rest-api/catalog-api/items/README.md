# Item

The Item object represents a “product item” as a transactable element of a product that, for example, in a created order, is represented as a “line item” of that order.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="208">Field</th><th width="143">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) A unique identifier for the item.</td></tr><tr><td><code>name</code></td><td>string, core</td><td>The name of the item.</td></tr><tr><td><code>description</code></td><td>string</td><td>A description of the item.</td></tr><tr><td><code>externalIds</code></td><td>object</td><td><p>Represents the <a href="./#externalids"><code>externalIds</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "vendor": "ven-1233-3222",
  "operations": "op-322-322",
}
</code></pre></td></tr><tr><td><code>terms</code></td><td>object</td><td><p>Terms for the items, as defined in the <code>terms</code> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "period": "1m",
  "commitment": "1y"
}
</code></pre></td></tr><tr><td><code>quantityNotApplicable</code></td><td>boolean, core</td><td>Indicates if the quantity isn't applicable or relevant to the product item being sold.</td></tr><tr><td><code>status</code></td><td>string</td><td><p>The status of the item. Allowed values are:</p><ul><li><code>Draft</code></li><li><code>Published</code></li><li><code>Unpublished</code></li></ul></td></tr><tr><td><code>parameters</code></td><td>object</td><td><p>Captures any additional information required for a product item and is defined by item configuration parameters.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ 
  "id": "PRM-1234-1234-1234",
  "externalId": "SKU",
  "value": "65272478BB01A12"
}
</code></pre></td></tr><tr><td><code>group</code></td><td>object</td><td>The <a href="../item-group/"><code>itemGroup</code></a> to which the item has been assigned.</td></tr><tr><td><code>unit</code></td><td>object</td><td>The <a href="../units-of-measure/"><code>unitOfMeasure</code></a> assigned to item.</td></tr><tr><td><code>product</code></td><td>object</td><td>The <a href="../product/"><code>product</code></a> to which item is assigned.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Parameter object <a href="#parameter" id="parameter"></a>

The parameter object contains the given parameter's value and additional information, like Constraints.

<table><thead><tr><th width="148">Field</th><th width="135">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The identifier of the parameter definition this value refers to.</td></tr><tr><td><code>externalId</code></td><td>string</td><td>The ID of the parameter in the external system.</td></tr><tr><td><code>name</code></td><td>string</td><td>The display name for the parameter.</td></tr><tr><td><code>value</code></td><td>string</td><td>(Optional) The value of the parameter.</td></tr></tbody></table>

## External Ids object <a href="#externalids" id="externalids"></a>

<table><thead><tr><th width="145">Field</th><th width="154">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>vendor</code></td><td>string</td><td>A vendor-recognizable item identifier used to ensure the correct item is supplied when an order is placed.</td></tr></tbody></table>

## Example

{% code title="ITEM OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
    "id": "ITM-0690-0539-0001",    
    "name": "Microsoft 365 Online Services for Charity",
    "description": "Explore Microsoft 365 nonprofit solutions and technology to help your organization",
    "terms":{
      "model": "quantity",
      "period": "1m",
      "commitment": "1y"
    }, 
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
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
