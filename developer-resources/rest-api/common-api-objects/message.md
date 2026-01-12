# Message

The `Message` object indicates an error or reason for order failure.

<table><thead><tr><th width="169">Field</th><th width="115">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td>The message identifier to be used for the localization process.</td></tr><tr><td>message</td><td><code>string</code></td><td>The content of the message.</td></tr><tr><td>parameters</td><td><code>string</code></td><td>The parameters used within the message.</td></tr></tbody></table>

## Example

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
