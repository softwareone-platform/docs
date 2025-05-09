# Parameter

The Parameter object contains the following properties:

<table><thead><tr><th width="171">Field</th><th width="226">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Platform-generated ID of the parameter. </p><p></p><p>Example: PRD-1234-1234-1234</p></td></tr><tr><td>href</td><td>string</td><td><p>Resource reference. </p><p></p><p>Example: /v1/products/PRD-1234-1234-1234</p></td></tr><tr><td>scope</td><td>string</td><td><p>Context in which the parameter will be used. </p><p></p><p>Example: Agreement</p></td></tr><tr><td>phase</td><td>string</td><td><p>Process during which the parameter will be used. </p><p></p><p>Example: Order</p></td></tr><tr><td>type</td><td>string</td><td><p>Indicates the UI component that will be used to capture information. </p><p></p><p>Example: Email</p></td></tr><tr><td>options</td><td><p>One of: </p><p></p><ul><li>AddressOptions</li><li>CheckboxOptions</li><li>SingleLineTextOptions</li><li>MultiLineTextOptions</li><li>ChoiceOptions</li><li>AddressOptions</li><li>ContactOptions</li><li>SubdomainOptions</li><li>HeadingOptions</li><li>DropDownOptions</li><li>EmailOptions</li><li>DataObjectOptions</li><li>DateOptions<br></li></ul></td><td><p>The options are specific to a selected type and allow customization of the UI component. </p><p></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "label": "Client address",
    "hintText": "please add your email",
    "placeholderText": "someone@org.com",
    "defaultValue": "none"
}
</code></pre></td></tr><tr><td>constraints</td><td>ConstraintsObject</td><td><p>Used to specify the characteristics of an entire parameter, which can also impact the validation of values. </p><p></p><p>For instance, enabling "Optional" overrides any mandatory fields within the UI components associated with the selected type.</p></td></tr><tr><td>group</td><td><a href="../parameter-group/">ParameterGroup</a></td><td>Groups allow logical grouping of parameters. They are used by the purchase wizard and represented as a wizard step. </td></tr><tr><td>externalId</td><td>string</td><td><p>Used for programmatic processing, for example, as a variable name within embedding templates or a “connector” process. </p><p></p><p>Example: EXT-1234-1234</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="PARAMETER OBJECT" %}
```json
{
  "scope": "Agreement",
  "phase": "Order",
  "description": "Agreement identifier of the reseller",
  "externalId": "RES-233-33-xx3",
  "displayOrder": 100,
  "constraints": {
    "hidden": true,
    "readonly": true,
    "optional": false
  },
  "type": "SingleLineText",
  "options": {
    "name": "Aggreement Id",
    "placeholderText": "AGR-xxx-xxx-xxx",
    "hintText": "Add agreement id",
    "minChar": 15,
    "maxChar": 15,
    "defaultValue": null
  },
  "group": { "id": PGR-7373-6782" }
}
```
{% endtab %}
{% endtabs %}
