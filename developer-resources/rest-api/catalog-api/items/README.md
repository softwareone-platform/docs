# Items

The Item object represents a “product item” as a transactable element of a product that, for example, in a created order, is represented as a “line item” of that order.

This object contains the following properties:

<table><thead><tr><th width="194">Field</th><th width="159">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>A unique identifier for the item.</p><p>Example: ITM-0690-0539-0001</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>The resource URI of the Item.</p><p>Example: /product-items/ITM-0690-0539-0001</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the item.</p><p>Example: Microsoft 365 Apps for Business</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>A description of the item.</p><p>Example: Best for businesses that need Office apps across devices and cloud file storage. For businesses with up to 300 employees.</p></td></tr><tr><td>externalIds</td><td><a href="./#externalids"><code>externalIds</code></a></td><td><p>A reference to the External Id object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "vendor": "ven-1233-3222",
  "operations": "op-322-322",
}
</code></pre></td></tr><tr><td>terms</td><td><a href="../../common-api-objects/terms.md"><code>terms</code></a></td><td><p>Terms for the items, as defined in the Terms object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "period": "1m",
  "commitment": "1y"
}
</code></pre></td></tr><tr><td>quantityNotApplicable</td><td><code>boolean</code></td><td><p>Indicates if the quantity isn't applicable or relevant to the product item being sold.</p><p>Example: true</p></td></tr><tr><td>status</td><td><a href="item-states.md"><code>Item States</code></a></td><td><p>The status of the item.</p><p>Example: Draft</p></td></tr><tr><td>parameters</td><td><a href="./#parameter"><code>parameterValue</code></a></td><td><p>Captures any additional information required for a product item and is defined by item configuration parameters.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ 
  "id": "PRM-1234-1234-1234",
  "externalId": "SKU",
  "value": "65272478BB01A12"
}
</code></pre></td></tr><tr><td>group</td><td><a href="item-group/"><code>itemGroup</code></a></td><td>The item group to which the item has been assigned.</td></tr><tr><td>unit</td><td><code>unitOfMeasure</code></td><td>The unit of measure assigned to item.</td></tr><tr><td>product</td><td><a href="../product/"><code>product</code></a></td><td>The product to which item is assigned.</td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the audit object. Possible entries include: Created, Updated, Activated, or Terminated.</td></tr></tbody></table>

## Parameter <a href="#parameter" id="parameter"></a>

The parameter object contains the given parameter's value and additional information, like Constraints.

<table><thead><tr><th width="188">Field</th><th width="164">Parameter</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The identifier of the parameter definition this value refers to.</p><p>Example: PDF-1234-1234-1234</p></td></tr><tr><td>externalId</td><td><code>string</code></td><td><p>The ID of the parameter in the external system.</p><p>Example: SKU</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The display name for the parameter.</p><p>Example: Stock keeping unit</p></td></tr><tr><td>value</td><td><code>string</code></td><td><p>The value of the parameter.</p><p>Example: 65272478BB01A12</p></td></tr></tbody></table>

## ExternalIds <a href="#externalids" id="externalids"></a>

<table><thead><tr><th width="184">Field</th><th width="175">Type</th><th>Description</th></tr></thead><tbody><tr><td>vendor</td><td><code>string</code></td><td>A vendor-recognizable item identifier used to ensure the correct item is supplied when an order is placed.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="ITEM OBJECT" %}
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
{% endtab %}
{% endtabs %}
