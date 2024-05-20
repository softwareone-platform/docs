# Parameter

## Parameter object

<table><thead><tr><th>Field</th><th width="270">Type</th><th>Description</th></tr></thead><tbody><tr><td><strong><code>id</code></strong></td><td>string</td><td><p>Platform generated ID. </p><p></p><p>Example: "PRD-1234-1234-1234"</p></td></tr><tr><td><strong><code>href</code></strong></td><td>string</td><td><p>Resource reference. </p><p></p><p>Example: "/v1/products/PRD-1234-1234-1234"</p></td></tr><tr><td><strong><code>scope</code></strong></td><td>string</td><td><p>Describes in which context parameter will be used. </p><p></p><p>Example: "Agreement"</p></td></tr><tr><td><strong><code>phase</code></strong></td><td>string</td><td><p>Described in which process it will be used. </p><p></p><p>Example: "Order"</p></td></tr><tr><td><strong><code>type</code></strong></td><td>string</td><td><p>Indicates which UI component will be used to capture information. </p><p></p><p>Example: "Email"</p></td></tr><tr><td>options</td><td><p>One of: </p><p></p><p>AddressOptions<br>CheckboxOptions<br>SingleLineTextOptions<br>MultiLineTextOptions<br>ChoiceOptions<br>AddressOptions<br>ContactOptions<br>SubdomainOptions<br>HeadingOptions<br>DropDownOptions<br>EmailOptions<br>DataObjectOptions<br>DateOptions<br></p></td><td><p>Are specific to a selected type and allow customization of UI component. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "label": "Client address",
    "hintText": "please add your email",
    "placeholderText": "someone@org.com",
    "defaultValue": "none"
}
</code></pre></td></tr><tr><td>constraints</td><td>ConstraintsObject</td><td>Used to specify characteristics of entire parameter, though it can have an impact of the validation of values too (i.e. turning on “Optional” will override any mandatory field within the UI components associated to the selected type.</td></tr><tr><td>group</td><td><a href="../parameter-group/">ParameterGroup</a></td><td>Groups allow logical grouping of parameters, used by purchase wizard and represented as wizard step. </td></tr><tr><td>externalId</td><td>string</td><td><p>Used for programmatic processing, for example as a variable name within embedding templates or within a “connector” process. </p><p></p><p>Example: "EXT-1234-1234"</p></td></tr></tbody></table>

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
