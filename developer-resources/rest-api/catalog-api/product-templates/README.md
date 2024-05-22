# Product Templates

## Template object

The Template Object provides functionality for templates to be made and automatically delivered once a set of rules based on type is achieved. This enables the client to know what is happening with their order and if anything is needed of them.

| Field         | Type                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ------------- | ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **`id`**      | string                 | <p>Template ID. </p><p></p><p>Example: "TPL-1234-5678"</p>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **`href`**    | string                 | <p>Relative reference to object on API (always <code>products/{id}/templates/{id}</code>) </p><p></p><p>Example: "v1/products/PRD-1234-1234/templates/TPL-1234-5678-0001"</p>                                                                                                                                                                                                                                                                                                  |
| **`name`**    | string                 | <p>Template name </p><p></p><p>Example: "Thank you for your interest"</p>                                                                                                                                                                                                                                                                                                                                                                                                      |
| **`type`**    | string                 | Example: "RequestProcessing"                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **`content`** | string                 | <p>Content for the template. </p><p></p><p>Example:</p><pre class="language-html" data-line-numbers><code class="lang-html">&#x3C;p>We are delighted that you have contacted us at SoftwareOne. Your interest in Microsoft 365 Online Services product is greatly valued, and we are here to provide all the support you need. Our dedicated team is actively working on your query, and we are committed to responding within 24 hours. \n Thank you!!!&#x3C;p>
</code></pre> |
| **`default`** | boolean                | <ul><li>Each product will have 4 defaults automatically generated upon product creation (against each status)</li><li>Each template automatically created will have a default system message client account will need to update these</li><li>Default cannot be deleted</li><li>Non default can be deleted</li></ul><p>Example: "true"</p>                                                                                                                                     |
| **`product`** | [Product](../product/) | <p> </p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
} 
</code></pre>                                                                                                                                                                                                                                       |
| **`audit`**   | Audit Object           | <p> </p><p></p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

## Example

{% tabs %}
{% tab title="TEMPLATE OBJECT" %}
```json
{
  "id": "TPL-1234-5678-0001",
  "href": "v1/products/PRD-1234-1234/templates/TPL-1234-5678-0001",
  "name": "Thank you for your interest",
  "type": "RequestProcessing",
  "content": "We are delighted that you have contacted us at SoftwareOne. Your interest in Microsoft 365 Online Services product is greatly valued, and we are here to provide all the support you need. Our dedicated team is actively working on your query, and we are committed to responding within 24 hours. \n Thank you!!!",
  "isDefault": true,
  "product": {
    "id": "PRD-1234-5678-0001"
  }
}
```
{% endtab %}
{% endtabs %}
