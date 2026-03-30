# Constraints Object

Represents the parameter constraints object.

<table><thead><tr><th width="138">Field</th><th width="162">Type</th><th>Description</th></tr></thead><tbody><tr><td>hidden</td><td><code>bool</code></td><td><p>This constraint is very powerful as it allows vendors to conditionally request information from the client. Since it is about “collecting” information it is obvious that the <em>“hidden“ constraint is available only during the “order” phase</em>. </p><p>Example: true</p></td></tr><tr><td>required</td><td><code>bool</code></td><td><p>All defined parameters are mandatory by default, so to make the parameter optional we have to turn on this constraint. </p><p>Example: false</p></td></tr><tr><td>readonly</td><td><code>bool</code></td><td>If the requirement is to prevent the Client from modifying a value of some parameter, then this constraint can be turned on which will disable the UI components effectively making them not editable. Example: true</td></tr><tr><td>capacity</td><td><a href="constraints-object.md#capacity-object"><code>capacityObject</code></a></td><td><p>Min and Max number of parameter values. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  min: 1,
  max: 2
}
</code></pre></td></tr></tbody></table>

#### Capacity Object <a href="#capacity-object" id="capacity-object"></a>

<table><thead><tr><th width="128">Field</th><th width="122">Type</th><th>Description</th></tr></thead><tbody><tr><td>min</td><td><code>number</code></td><td>Minimum specifies how many values the user must provide.</td></tr><tr><td>max</td><td><code>number</code></td><td>Maximum value shows how many values the user can provide.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="CONSTRAINTS OBJECT" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
  "hidden": true,
  "readOnly": true,
  "required": false,
  "multiple": null
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
