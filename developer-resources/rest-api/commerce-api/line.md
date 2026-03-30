# Line

A Line object represents either an Order Line object an Agreement Line object or a Subscription Line object.

A Line object represents the amount (quantity) of product items being purchased in the scope of order and/or subscription as well as a price for them.

Usually, a Line object first appears in some purchase or change order. Later on, the line should be assigned to some subscription for recurrent terms, or to agreement for one-time terms. Also, a Line of active subscriptions can be used in a change order to update the quantity or/and price of the subscription Line. Also, a new Line object can be introduced just directly in the subscription by the vendor (migration or synchronization scenario).

The lifecycle of the Line object is bound to the lifecycle of the relevant agreement object.

Lines are always returned or provided as part of a `lines` array of either one of the Agreement object, the Subscription object, or the Order object.

<table><thead><tr><th width="168">Field</th><th width="188">Type</th><th>Description</th><th data-hidden></th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>Line identifier, consisting of fixed prefix (same digits as in relevant agreement object), and a suffix, which is sequential number for all allocated lines in scope of the agreement (including failed or deleted orders).</td><td>ALI-1234-1234-1234-0001</td></tr><tr><td><code>item</code></td><td><a href="../catalog-api/items/">item</a></td><td> </td><td><code>{ "id": "ITM-1234-1234-1234-0021", "name": "Adobe Illustrator" }</code></td></tr><tr><td><code>oldQuantity</code></td><td>integer</td><td>In case of purchase orders, this value will always be unset. For change orders, this value reflects the agreement quantity at the time the change order was created.</td><td>7</td></tr><tr><td><code>quantity</code></td><td>integer</td><td>The quantity of items in a <code>subscription</code>.</td><td>10</td></tr><tr><td><code>price</code></td><td>object</td><td>The <a href="../common-api-objects/price.md"><code>price</code></a> for the item in the subscription. Not all fields are visible to all actors. </td><td><code>{ "PPxY": 150, "PPxM": 12.50, "unitPP": 1.25 "SPxY": 165, "SPxM": 13.50, "unitSP": 1.35, "markup": 0.10, "margin": 0.11, "currency": "USD" }</code></td></tr><tr><td><code>subscription</code></td><td>object</td><td>A reference to <a href="subscriptions/"><code>subscription</code></a> where this line is resides. The value is never returned in context of <code>subscription</code>, it is used only in <code>orders</code>.</td><td><code>{ "id": "SUB-1234-1234-1234" }</code></td></tr><tr><td><code>order</code></td><td>object</td><td>Last <a href="orders/"><code>order</code></a> where the Line was introduced/updated. The value is never returned in context of an order. It can be used in context of a <code>subscription</code> or <code>agreement</code>.</td><td><code>{ "id": "ORD-6869-4529-8975-9005" }</code></td></tr></tbody></table>

### Example

{% code lineNumbers="true" %}
```json
{
  "id": "ALI-1234-1234-1234-0001",
  "item": {
    "id": "ITM-1234-1234-1234-0021",
    "name": "Adobe Illustrator"
  },
  "oldQuantity": 7,
  "quantity": 10,
  "price": {
    "PPxY": 150,
    "PPxM": 12.50,
    "unitPP": 1.25
    "SPxY": 165,
    "SPxM": 13.50,
    "unitSP": 1.35,
    "markup": 0.10,
    "margin": 0.11,
    "currency": "USD"
  },
  "subscription": { "id": "SUB-1234-1234-1234" }
}
```
{% endcode %}
