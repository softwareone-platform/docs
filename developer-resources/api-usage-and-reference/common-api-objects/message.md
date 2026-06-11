# Message

The Message object indicates the error or the reason for the order failure. This object contains the following attributes:

<table><thead><tr><th width="144">Field</th><th width="122">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Optional) The message identifier to be used for the localization process.</td></tr><tr><td><code>message</code></td><td>string</td><td>The content of the message.</td></tr><tr><td><code>parameters</code></td><td>string</td><td>(Optional) Parameters used within the message.</td></tr></tbody></table>

### Examples

{% tabs %}
{% tab title="EXAMPLE WITHOUT PARAMETERS" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
     "id": "E001234",
     "message": "Agreement provisioning failed due to unavailability of the item"
}
```
{% endcode %}
{% endtab %}

{% tab title="EXAMPLE WITH PARAMETERS" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
     "id": "E001234",
     "message": "Agreement provisioning failed due to unavailability of the item {{ item }}",
     "parameters": {
        "item": "ITM-1234-1234-1234"
     }
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
