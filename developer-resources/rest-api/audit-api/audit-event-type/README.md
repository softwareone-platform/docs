# Audit Event Type

The Audit Event Type refers to an event that has occurred within the platform. These records are generated automatically and can be utilized to store supplementary information regarding the specific event type.

<table><thead><tr><th width="140">Field</th><th width="149">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>The ID of the event type. </p><p>Example: AET-7149-2212</p></td></tr><tr><td>key</td><td>string</td><td><p>The event's key. </p><p>Example: platform.commerce.order.created</p></td></tr><tr><td>name</td><td>string</td><td><p>The name of the event. </p><p>Example: Order created.</p></td></tr><tr><td>description</td><td>string</td><td><p>A description of the event. </p><p>Example: A standard event that occurs when the order is created. </p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="AUDIT EVENT TYPE" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "AET-5699-2751",
  "Key": "platform.commerce.order.created",
  "Name": "Order created.",
  "Description": "A standard event that occurs upon the creation of an order."
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
