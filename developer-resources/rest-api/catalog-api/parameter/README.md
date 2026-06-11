# Parameter

The Parameter object contains the following properties:

<table><thead><tr><th width="161">Field</th><th width="144">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) Platform-generated ID of the parameter. </td></tr><tr><td><code>scope</code></td><td>string</td><td>(Read-only) The context in which the parameter will be used. </td></tr><tr><td><code>phase</code></td><td>string</td><td>(Read-only) The process during which the parameter will be used. </td></tr><tr><td><code>context</code></td><td>string</td><td><p>(Read-only) Used only in the <code>Order</code> scope and during the Order phase. If the scope is not set to <code>Order</code>, the context value is assigned as <code>None</code>. Allowed values are: </p><ul><li><code>Change</code></li><li><code>Configuration</code></li><li><code>Purchase</code></li><li><code>Termination</code></li><li><code>None</code></li></ul></td></tr><tr><td><code>type</code></td><td>string</td><td>(Read-only) Indicates the UI component that will be used to capture information. </td></tr><tr><td><code>options</code></td><td>object</td><td><p>Are specific to the selected field type and allow customization of the UI component. One of the following option‑object types: </p><ul><li>AddressOptions</li><li>CheckboxOptions</li><li>SingleLineTextOptions</li><li>MultiLineTextOptions</li><li>ChoiceOptions</li><li>ContactOptions</li><li>SubdomainOptions</li><li>HeadingOptions</li><li>DropDownOptions</li><li>EmailOptions</li><li>DataObjectOptions</li><li>DateOptions</li></ul></td></tr><tr><td><code>multiple</code></td><td>boolean</td><td>(Optional) Multiple values type.</td></tr><tr><td><code>constraints</code></td><td>object</td><td>(Optional) Represents the <code>constraints</code> object, which defines characteristics that apply to the entire parameter and may influence value validation. For example, enabling <code>optional</code> overrides any mandatory fields within the UI components associated with the selected type.</td></tr><tr><td><code>group</code></td><td>object</td><td>Represents the <a href="../parameter-group/"><code>parameterGroup</code></a> object that allows logical grouping of parameters. They are used by the purchase wizard and represented as a wizard step. </td></tr><tr><td><code>externalId</code></td><td>object</td><td>(Optional)  Represents the <a href="../../../api-usage-and-reference/common-api-objects/externalids.md"><code>externalIds</code></a> object, which is used for programmatic processing, for example, as a variable name within embedding templates or a “connector” process. </td></tr><tr><td><code>status</code></td><td>string</td><td><p>Represents the current status of the parameter. Only active parameters are returned. Allowed values are</p><ul><li><code>Draft</code></li><li><code>Active</code></li><li><code>Unpublished</code></li></ul></td></tr></tbody></table>

## Example

{% code title="PARAMETER OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "scope": "Order",
  "phase": "Order",
  "description": "Agreement identifier of the reseller",
  "externalId": "RES-233-33-xx3",
  "displayOrder": 100,
  "context": "Purchase",
  "multiple": true,
  "constraints": {
    "hidden": true,
    "readonly": true,
    "required": false,
    "capacity": {
      "min": 2,
      "max": 3
    }
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
