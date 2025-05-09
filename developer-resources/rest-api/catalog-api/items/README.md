# Items

The Item object represents a “product item” as a transactable element of a product that, for example, in a created order, is represented as a “line item” of that order.

This object contains the following properties:

<table><thead><tr><th width="194">Field</th><th width="159">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Identifier for the item.</p><p></p><p>Example: ITM-0690-0539-0001</p></td></tr><tr><td>href</td><td>string</td><td><p>The resource URI of the Item. </p><p></p><p>Example: /product-items/ITM-0690-0539-0001</p></td></tr><tr><td>name</td><td>string</td><td><p>Name of the item. </p><p></p><p>Example: Microsoft 365 Apps for Business</p></td></tr><tr><td>description</td><td>string</td><td><p>Item description. </p><p></p><p>Example: Best for businesses that need Office apps across devices and cloud file storage. For businesses with up to 300 employees.</p></td></tr><tr><td>externalIds</td><td><a href="./#externalids">ExternalIds</a></td><td><p> Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "vendor": "ven-1233-3222",
  "operations": "op-322-322",
}
</code></pre></td></tr><tr><td>terms</td><td>Terms</td><td><p>Terms for the Items, as defined in the Terms object. </p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "period": "1m",
  "commitment": "1y"
}
</code></pre></td></tr><tr><td>quantityNotApplicable</td><td>boolean</td><td><p>Indicates if the quantity is not applicable or relevant to the product item being sold. </p><p></p><p>Example: true</p></td></tr><tr><td>status</td><td><a href="item-states.md">Item States</a></td><td><p>Status of the item. </p><p></p><p>Example: Draft</p></td></tr><tr><td>parameters</td><td><a href="./#parameter">ParameterValue</a></td><td><p>Captures any additional information required for a product item and is defined by item configuration parameters.</p><p><br>Only item configuration parameters are available on this list. </p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ 
  "id": "PRM-1234-1234-1234",
  "externalId": "SKU",
  "value": "65272478BB01A12"
}
</code></pre></td></tr><tr><td>group</td><td><a href="../item-group/">ItemGroup</a></td><td>Item group to which the item has been assigned.</td></tr><tr><td>unit</td><td>UnitOfMeasure</td><td>Unit of measure assigned to item.</td></tr><tr><td>product</td><td><a href="../product/">Product</a></td><td>Product to which item is assigned.</td></tr><tr><td>audit</td><td>AuditObject</td><td><p>Audit object with possible entries: created, updated, activated, terminated, according to the lifecycle of the object. </p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Parameter <a href="#parameter" id="parameter"></a>

The parameter object contains the value of the given parameter along with additional information like constraints.

<table><thead><tr><th width="139">Field</th><th width="140">Parameter</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>The identifier of the parameter definition this value refers to. </p><p></p><p>Example: PDF-1234-1234-1234</p></td></tr><tr><td>externalId</td><td>string</td><td><p>ID of the parameter in the external system. </p><p></p><p>Example: SKU</p></td></tr><tr><td>name</td><td>string</td><td><p>Display name for the parameter. </p><p></p><p>Example: Stock keeping unit</p></td></tr><tr><td>value</td><td>string</td><td><p>Value of the parameter. </p><p></p><p>Example: 65272478BB01A12</p></td></tr></tbody></table>

## ExternalIds <a href="#externalids" id="externalids"></a>

<table><thead><tr><th width="139">Field</th><th width="175">Type</th><th>Description</th></tr></thead><tbody><tr><td>vendor</td><td>string</td><td>A vendor identifier is an item identifier that is recognizable by the vendor, ensuring that when an order is placed, they will easily understand which item needs to be provided.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="ITEM OBJECT" %}
```json
{
    "id": "ITM-0690-0539-0001",
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
