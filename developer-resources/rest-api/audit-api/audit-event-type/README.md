# Audit Event Type

Audit Event Type refers to an event that has occurred within the platform. These records are generated automatically and can be used to store supplementary information related to the specific event type.

<table><thead><tr><th width="136">Field</th><th width="145">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The ID of the item. </td></tr><tr><td><code>key</code></td><td>string, core</td><td>(Read-only) The event's key. </td></tr><tr><td><code>name</code></td><td>string, core</td><td>(Read-only) The name of the event. </td></tr><tr><td><code>description</code></td><td>string</td><td>(Read-only) (Optional) A description of the event. </td></tr></tbody></table>

## Example

{% code title="AUDIT EVENT TYPE OBJECT" lineNumbers="true" %}
```json
{
  "id": "AET-5699-2751",
  "Key": "platform.commerce.order.created",
  "Name": "Order created.",
  "Description": "A standard event that occurs upon the creation of an order."
},
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
