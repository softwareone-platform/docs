# Order Parameter

### Parameter object <a href="#parameter" id="parameter"></a>

The Parameter object contains the value of the given parameter along with additional information, such as constraints and validation errors.

<table><thead><tr><th width="143">Field</th><th width="134">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) Primary identifier for the parameter.</td></tr><tr><td><code>name</code></td><td>string</td><td>(Read-only) Display name for the parameter.</td></tr><tr><td><code>externalId</code></td><td>string</td><td>(Read-only) The ID of the parameter within the external system.</td></tr><tr><td><code>value</code></td><td>string</td><td>(Optional) The parameter's value that can be updated.</td></tr><tr><td><code>displayValue</code></td><td>string</td><td>(Read-only) (Optional) Read-only value for the parameter.</td></tr><tr><td><code>constraints</code></td><td>object</td><td><p>(Optional) Represents the parameter <code>constraints</code> object.</p><ul><li>If specified, the value represents overridden parameter constraints.</li><li>If unspecified, parameter constraints must be taken from the parameter definition.</li></ul></td></tr><tr><td><code>error</code></td><td>object</td><td>(Optional) Represents the <code>error</code> object. </td></tr></tbody></table>

{% code title="PARAMETER OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
    "id": "PRM-1234-1234-1234-1234",
    "name": "Tenant Id",
    "externalId": "tenant_id",
    "constraints": {
        "readonly": false,
        "hidden": true,
        "required": true,
        "unique": false
    },
    "value": "69b73824-ce76-4866-ad47-b615ae9d8998",
    "error": {
        "id": "E001234",
        "message": "Incorrect parameter value"
    }
}
```
{% endcode %}

### Parameter Constraints object <a href="#parameter-constraints" id="parameter-constraints"></a>

Parameter Constraints define the overridden behavior of a parameter.

<table><thead><tr><th width="141">Field</th><th width="92">Data</th><th>Description</th><th data-hidden></th></tr></thead><tbody><tr><td><code>readonly</code></td><td>bool</td><td>The parameter can only be viewed.</td><td>false</td></tr><tr><td><code>hidden</code></td><td>bool</td><td>The parameter is hidden and must not be shown to the user.</td><td>true</td></tr><tr><td><code>required</code></td><td>bool</td><td>The parameter value is required.</td><td>true</td></tr><tr><td><code>unique</code></td><td>bool</td><td>The parameter value is unique.</td><td>true</td></tr></tbody></table>

{% code title="PARAMETER CONSTRAINTS OBJECT" lineNumbers="true" %}
```json
{
    "readonly": false,
    "hidden": true,
    "required": true,
    "unique": false
}
```
{% endcode %}

### Parameter Group object <a href="#parameter-group" id="parameter-group"></a>

Parameter Group is used to visually split different types of parameters.

<table><thead><tr><th width="149">Field</th><th width="168">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>ordering</code></td><td>Parameter []</td><td>(Optional) Array of ordering parameters.</td></tr><tr><td><code>fulfillment</code></td><td>Parameter []</td><td>(Optional) Array of fulfillment parameters.</td></tr></tbody></table>

{% code title="PARAMETER GROUP OBJECT" lineNumbers="true" %}
```json
{
    "ordering": [...],
    "fulfillment": [...]
}
```
{% endcode %}
