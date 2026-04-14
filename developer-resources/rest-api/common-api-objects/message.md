# Message

The `Message` object indicates an error or reason for order failure.

<table><thead><tr><th width="169">Field Name</th><th width="122">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>The message identifier to be used for the localization process.</td></tr><tr><td><code>message</code></td><td>string</td><td>The content of the message.</td></tr><tr><td><code>parameters</code></td><td>string</td><td>The parameters used within the message.</td></tr></tbody></table>

### Examples

{% tabs %}
{% tab title="WITHOUT PARAMETERS" %}
{% code lineNumbers="true" %}
```json
{
     "id": "E001234",
     "message": "Agreement provisioning failed due to unavailability of the item"
}
```
{% endcode %}
{% endtab %}

{% tab title="WITH PARAMETERS" %}
{% code lineNumbers="true" %}
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
