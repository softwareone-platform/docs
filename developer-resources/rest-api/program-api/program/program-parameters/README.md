# Program Parameters

The Program Parameters object is a mechanism that enables vendors to specify additional information to be collected from and shared with a client, so that the client can get self-served within the SoftwareOne Marketplace.&#x20;

This object contains the following attributes:

<table><thead><tr><th width="148">Field</th><th width="170">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The business identifier of the Parameter object. </p><p>Example: PAR-1234-1234-0001</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>A reference to the resource. </p><p>Example: /v1/program/PGR-1234-1234/PAR-1234-1234-0001</p></td></tr><tr><td>scope</td><td><code>string</code></td><td>The scope in which the parameter will be used. The possible values are <code>Agreement</code>, <code>Item</code>, <code>Request</code>, or <code>Subscription</code>.</td></tr><tr><td>phase</td><td><code>string</code></td><td><p>The phase in which the process will be used. The</p><p>possible values are <code>Configuration</code>, <code>Order</code>, or <code>Fullfilment</code>.</p></td></tr><tr><td>type</td><td><code>string</code></td><td><p>Indicates the UI component that will be used to capture information. The possible values are</p><p><code>SingleLineText</code></p><p><code>MultiLineText</code></p><p><code>Address</code></p><p><code>Contact</code></p><p><code>Checkbox</code></p><p><code>Choice</code></p><p><code>Subdomain</code></p><p><code>Heading</code></p><p><code>DropDown</code></p><p><code>Email</code></p><p><code>DataObject</code></p><p><code>Date</code></p></td></tr><tr><td>options</td><td></td><td><p>These are specific to a selected type and allow customization of the UI component. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
    "label": "Client address",
    "hintText": "enter your email",
    "placeholderText": "someone@org.com",
    "defaultValue": "none"
}
</code></pre></td></tr><tr><td>constraints</td><td><code>constraintsObject</code></td><td>Specifies characteristics of the entire parameter, impacting value validation. For example, enabling 'Optional' overrides mandatory fields in UI components associated with the selected type.</td></tr><tr><td>group</td><td><a href="../program-parameter-groups/"><code>parameterGroup</code></a></td><td>Allows logical grouping of parameters. Used by the purchase wizard and represented as a step within the wizard.</td></tr><tr><td>externalId</td><td><code>string</code></td><td><p>Used for programmatic processing, for example, as a variable name within templates or a connector process.</p><p>Example: EXT-1234-1234</p></td></tr><tr><td>status</td><td><code>string</code></td><td><p>The status of the parameter. Only active parameters are returned.</p><p>Example: Active</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="PROGRAM PARAMETERS OBJECT" %}
{% code overflow="wrap" lineNumbers="true" %}
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
    "name": "Aggreement Id",
    "placeholderText": "AGR-xxx-xxx-xxx",
    "hintText": "Add agreement id",
    "minChar": 15,
    "maxChar": 15,
    "defaultValue": null
  },
  "group": { "id": PGR-7373-6782" },
  "status": "active"
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
