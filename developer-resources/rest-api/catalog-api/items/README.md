# Item

The Item object represents a “product item” as a transactable element of a product that, for example, in a created order, is represented as a “line item” of that order.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="224">Field Name</th><th width="159">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>A unique identifier for the item.</p><p>Example: ITM-0690-0539-0001</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>The resource URI of the Item.</p><p>Example: /product-items/ITM-0690-0539-0001</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the item.</p><p>Example: Microsoft 365 Apps for Business</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the item.</p><p>Example: Best for businesses that need Office apps across devices and cloud file storage. </p></td></tr><tr><td><code>externalIds</code></td><td>object</td><td><p>A reference to the <a href="./#externalids"><code>externalIds</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "vendor": "ven-1233-3222",
  "operations": "op-322-322",
}
</code></pre></td></tr><tr><td><code>terms</code></td><td>object</td><td><p>Terms for the items, as defined in the <code>terms</code> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "period": "1m",
  "commitment": "1y"
}
</code></pre></td></tr><tr><td><code>quantityNotApplicable</code></td><td>boolean</td><td><p>Indicates if the quantity isn't applicable or relevant to the product item being sold.</p><p>Example: true</p></td></tr><tr><td><code>status</code></td><td>string</td><td><p>The status of the item.</p><p>Example: Draft</p></td></tr><tr><td><code>parameters</code></td><td><a href="./#parameter">parameterValue</a></td><td><p>Captures any additional information required for a product item and is defined by item configuration parameters.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ 
  "id": "PRM-1234-1234-1234",
  "externalId": "SKU",
  "value": "65272478BB01A12"
}
</code></pre></td></tr><tr><td><code>group</code></td><td>object</td><td>The <a href="../item-group/"><code>itemGroup</code></a> to which the item has been assigned.</td></tr><tr><td><code>unit</code></td><td>object</td><td>The <a href="../units-of-measure/"><code>unitOfMeasure</code></a> assigned to item.</td></tr><tr><td><code>product</code></td><td>object</td><td>The <a href="../product/"><code>product</code></a> to which item is assigned.</td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. Allowed values: <code>created</code>, <code>updated</code>, <code>activated</code>, or <code>terminated</code>.</td></tr></tbody></table>

## Parameter object <a href="#parameter" id="parameter"></a>

The parameter object contains the given parameter's value and additional information, like Constraints.

<table><thead><tr><th width="188">Field Name</th><th width="164">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The identifier of the parameter definition this value refers to.</p><p>Example: PDF-1234-1234-1234</p></td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>The ID of the parameter in the external system.</p><p>Example: SKU</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The display name for the parameter.</p><p>Example: Stock keeping unit</p></td></tr><tr><td><code>value</code></td><td>string</td><td><p>The value of the parameter.</p><p>Example: 65272478BB01A12</p></td></tr></tbody></table>

## ExternalIds object <a href="#externalids" id="externalids"></a>

<table><thead><tr><th width="195">Field Name</th><th width="175">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>vendor</code></td><td>string</td><td>A vendor-recognizable item identifier used to ensure the correct item is supplied when an order is placed.</td></tr></tbody></table>

## Example response

{% code lineNumbers="true" %}
```json
{
    "id": "ITM-0690-0539-0001",
    "name": "Microsoft 365 Online Services for Charity",
    "description": "TestTeam",
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
