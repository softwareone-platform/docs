# Order Parameter

### Parameter object <a href="#parameter" id="parameter"></a>

The `Parameter` object contains the value of the given parameter along with additional information, such as constraints and validation errors.

<table><thead><tr><th width="143">Field</th><th width="134">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>The primary identifier for the parameter.</td></tr><tr><td><code>name</code></td><td>string</td><td>The display name for the parameter.</td></tr><tr><td><code>externalId</code></td><td>string</td><td>The ID of the parameter within the external system.</td></tr><tr><td><code>value</code></td><td>string</td><td>The parameter's value that can be updated.</td></tr><tr><td><code>displayValue</code></td><td>string</td><td>The read-only value for the parameter.</td></tr><tr><td><code>constraints</code></td><td></td><td><p>Parameter constraints.</p><ul><li>When specified, the value represents overridden parameter constraints.</li><li>When not specified, parameter constraints must be taken from the parameter definition.</li></ul></td></tr><tr><td><code>error</code></td><td><a href="../notifications-api/messages/">message</a></td><td>A reference to the error object. When specified represents a parameter validation error.</td></tr></tbody></table>

{% code lineNumbers="true" %}
```json
{
    "id": "PRM-1234-1234-1234-1234",
    "name": "Tennant Id",
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

<table><thead><tr><th width="141">Field Name</th><th width="141">Data Type</th><th>Description</th><th data-hidden></th></tr></thead><tbody><tr><td><code>readonly</code></td><td>bool</td><td>The parameter may be only viewed.</td><td>false</td></tr><tr><td><code>hidden</code></td><td>bool</td><td>The parameter must not be shown to user.</td><td>true</td></tr><tr><td><code>required</code></td><td>bool</td><td>The parameter value is required.</td><td>true</td></tr><tr><td><code>unique</code></td><td>bool</td><td>The parameter value is unique.</td><td>true</td></tr></tbody></table>

{% code lineNumbers="true" %}
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

<table><thead><tr><th width="149">Field Name</th><th width="168">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>ordering</code></td><td>Parameter []</td><td>Array of ordering parameters.</td></tr><tr><td><code>fulfillment</code></td><td>Parameter []</td><td>Array of fulfillment parameters.</td></tr></tbody></table>

{% code lineNumbers="true" %}
```json
{
    "ordering": [...],
    "fulfillment": [...]
}
```
{% endcode %}
