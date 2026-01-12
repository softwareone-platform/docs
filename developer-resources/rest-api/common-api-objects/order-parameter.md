# Order Parameter

## Parameter <a href="#parameter" id="parameter"></a>

The `Parameter` object contains the value of the given parameter along with additional information, such as constraints and validation errors.

<table><thead><tr><th width="143">Field</th><th width="134">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td>The primary identifier for the parameter.</td></tr><tr><td>name</td><td><code>string</code></td><td>The display name for the parameter.</td></tr><tr><td>externalId</td><td><code>string</code></td><td>The ID of the parameter within the external system.</td></tr><tr><td>value</td><td><code>string</code></td><td>The parameter's updatable value.</td></tr><tr><td>displayValue</td><td><code>string</code></td><td>The read-only value for the parameter.</td></tr><tr><td>constraints</td><td></td><td><p>Parameter constraints.</p><ul><li>When specified, the value represents overridden parameter constraints.</li><li>When not specified, parameter constraints must be taken from the parameter definition.</li></ul></td></tr><tr><td>error</td><td><a href="../notifications-api/messages/"><code>message</code></a></td><td>A reference to the error object. When specified represents a parameter validation error.</td></tr></tbody></table>

### Example

{% tabs %}
{% tab title="PARAMETER" %}
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
{% endtab %}
{% endtabs %}

## Parameter Constraints <a href="#parameter-constraints" id="parameter-constraints"></a>

Parameter Constraints define the overridden behavior of a parameter.

<table><thead><tr><th width="141">Field</th><th width="141">Type</th><th>Description</th><th data-hidden></th></tr></thead><tbody><tr><td>readonly</td><td><code>bool</code></td><td>The parameter may be only viewed.</td><td>false</td></tr><tr><td>hidden</td><td><code>bool</code></td><td>The parameter must not be shown to user.</td><td>true</td></tr><tr><td>required</td><td><code>bool</code></td><td>The parameter value is required.</td><td>true</td></tr><tr><td>unique</td><td><code>bool</code></td><td>The parameter value is unique.</td><td>true</td></tr></tbody></table>

### Example

{% tabs %}
{% tab title="PARAMETER CONSTRAINTS" %}
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
{% endtab %}
{% endtabs %}

## Parameter Group <a href="#parameter-group" id="parameter-group"></a>

Parameter Group is used to visually split different types of parameters.

<table><thead><tr><th width="149">Field</th><th width="168">Type</th><th>Description</th></tr></thead><tbody><tr><td>ordering</td><td>Parameter []</td><td>Array of ordering parameters</td></tr><tr><td>fulfillment</td><td>Parameter []</td><td>Array of fulfillment parameters</td></tr></tbody></table>

### Example

{% tabs %}
{% tab title="PARAMETER GROUP" %}
{% code lineNumbers="true" %}
```json
{
    "ordering": [...],
    "fulfillment": [...]
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
