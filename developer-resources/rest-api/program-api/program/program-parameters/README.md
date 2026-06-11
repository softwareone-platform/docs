# Program Parameter

The Program Parameters object is a mechanism that enables vendors to specify additional information to be collected from and shared with a client, so that the client can get self-served within the SoftwareOne Marketplace.&#x20;

This object contains the following attributes:

<table><thead><tr><th width="148">Field</th><th width="153">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The business identifier of the Parameter object. </td></tr><tr><td><code>href</code></td><td>string</td><td>(Read-only) A reference to the resource. </td></tr><tr><td><code>scope</code></td><td>string</td><td>(Read-only) The scope in which the parameter will be used. Allowed values: <code>agreement</code>, <code>item</code>, <code>request</code>, or <code>subscription</code>.</td></tr><tr><td><code>phase</code></td><td>string</td><td>(Read-only) The phase in which the process will be used. Allowed values: <code>configuration</code>, <code>order</code>, or <code>fullfilment</code>.</td></tr><tr><td><code>type</code></td><td>string</td><td><p>(Read-only) Indicates the UI component that will be used to capture information. Allowed values:</p><ul><li><code>SingleLineText</code></li><li><code>MultiLineText</code></li><li><code>Address</code></li><li><code>Contact</code></li><li><code>Checkbox</code></li><li><code>Choice</code></li><li><code>Subdomain</code></li><li><code>Heading</code></li><li><code>DropDown</code></li><li><code>Email</code></li><li><code>DataObject</code></li><li><code>Date</code></li></ul></td></tr><tr><td><code>options</code></td><td>object</td><td><p>These are specific to a selected type and allow customization of the UI component. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
    "label": "Client address",
    "hintText": "enter your email",
    "placeholderText": "someone@org.com",
    "defaultValue": "none"
}
</code></pre></td></tr><tr><td><code>constraints</code></td><td>object</td><td>Represents the <code>constraints</code> object, which specifies characteristics of the entire parameter, impacting value validation. For example, enabling 'Optional' overrides mandatory fields in UI components associated with the selected type.</td></tr><tr><td><code>group</code></td><td>object</td><td>(Optional) Represents the <a href="../program-parameter-groups/"><code>parameterGroup</code></a> object, allowing logical grouping of parameters. It is used by the purchase wizard and represented as a step within the wizard.</td></tr><tr><td><code>externalId</code></td><td>string</td><td>(Optional) Used for programmatic processing, for example, as a variable name within templates or a connector process.</td></tr><tr><td><code>status</code></td><td>string</td><td>The status of the parameter. Only active parameters are returned.</td></tr></tbody></table>

## Example

{% code title="THE PROGRAM PARAMETERS OBJECT" overflow="wrap" lineNumbers="true" %}
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
    "required": false
  },
  "type": "SingleLineText",
  "options": {
    "name": "Agreement Id",
    "placeholderText": "AGR-xxx-xxx-xxx",
    "hintText": "Add agreement id",
    "minChar": 15,
    "maxChar": 15,
    "defaultValue": null
  },
  "group": { 
    "id": "PGR-7373-6782" 
  },
  "status": "active"
}
```
{% endcode %}
