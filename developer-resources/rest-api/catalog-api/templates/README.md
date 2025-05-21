# Templates

The Template object provides functionality for templates to be made and automatically delivered once a set of rules based on type is met. This enables the client to know what is happening with their order and if anything is needed of them.

The Template object contains the following properties:

<table><thead><tr><th width="120">Field</th><th width="129">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The template's ID.</p><p>Example: TPL-1234-5678</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>A relative reference to the object in the API.</p><p>Example: v1/products/PRD-1234-1234/templates/TPL-1234-5678-0001</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the template.</p><p>Example: Thank you for your interest.</p></td></tr><tr><td>type</td><td><code>string</code></td><td><p>The type of template.</p><p>Example: RequestProcessing</p></td></tr><tr><td>content</td><td><code>string</code></td><td><p>The content of the template.</p><p>Example:</p><pre class="language-html" data-overflow="wrap" data-line-numbers><code class="lang-html">&#x3C;p>We are delighted that you have contacted us at SoftwareOne. Your interest in the Microsoft 365 Online Services product is greatly valued, and we are here to provide all the support you need. Our dedicated team is actively working on your query, and we are committed to responding within 24 hours. \n Thank you!!!&#x3C;p>
</code></pre></td></tr><tr><td>default</td><td><code>boolean</code></td><td><ul><li>Each product has 4 defaults automatically generated upon product creation (against each status).</li><li>Each template automatically created has a default system message that the client account will need to update.</li><li>The default cannot be deleted, but non-default can be deleted.</li></ul><p>Example: true</p></td></tr><tr><td>product</td><td><a href="../product/"><code>product</code></a></td><td><p>A reference to the Product object.</p><p>Example:</p><pre class="language-json"><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
} 
</code></pre></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the Audit object.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="TEMPLATE OBJECT" %}
{% code lineNumbers="true" %}
```json
{
  "id": "TPL-1234-5678-0001",
  "name": "Thank you for your interest",
  "type": "RequestProcessing",
  "content": "We are delighted that you have contacted us at SoftwareOne. Your interest in Microsoft 365 Online Services product is greatly valued, and we are here to provide all the support you need. Our dedicated team is actively working on your query, and we are committed to responding within 24 hours. \n Thank you!!!",
  "isDefault": true,
  "product": {
    "id": "PRD-1234-5678-0001"
  }
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
