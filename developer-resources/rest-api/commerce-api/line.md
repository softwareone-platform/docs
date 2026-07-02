# Line

A `Line` object represents one of the following: an **Order Line**, an **Agreement Line**, or a **Subscription Line**.

A `Line` object describes the quantity of product items being purchased within the scope of an order or subscription, along with the associated pricing.

Typically, a `Line` object is first introduced through a purchase order or a change order. After creation, the line is assigned either to a subscription (for recurring terms) or to an agreement (for one‑time terms). A line belonging to an active subscription may later appear in a change order to update its quantity or price. In some cases, a new `Line` object may be created directly within a subscription by the vendor—for example, during migration or synchronization scenarios.

The lifecycle of a `Line` object is tied to the lifecycle of the corresponding agreement.

`Line` objects are always returned or provided as part of a `lines` array within one of the following parent objects: an `agreement`, a `subscription`, or an `order`.

<table data-search="false"><thead><tr><th width="168">Field</th><th width="188">Type</th><th>Description</th><th data-hidden></th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>Line identifier, consisting of fixed prefix (same digits as in relevant agreement object), and a suffix, which is sequential number for all allocated lines in scope of the agreement (including failed or deleted orders).</td><td>ALI-1234-1234-1234-0001</td></tr><tr><td><code>item</code></td><td>object</td><td> Represents the <a href="../catalog-api/items/"><code>item</code></a> object.</td><td><code>{ "id": "ITM-1234-1234-1234-0021", "name": "Adobe Illustrator" }</code></td></tr><tr><td><code>oldQuantity</code></td><td>integer</td><td>In case of purchase orders, this value will always be unset. For change orders, this value reflects the agreement quantity at the time the change order was created.</td><td>7</td></tr><tr><td><code>quantity</code></td><td>integer</td><td>The quantity of items in a subscription.</td><td>10</td></tr><tr><td><code>price</code></td><td>object</td><td>The <a href="../../api-usage-and-reference/common-api-objects/price.md"><code>price</code></a> for the item in the subscription. Not all fields are visible to all actors. </td><td><code>{ "PPxY": 150, "PPxM": 12.50, "unitPP": 1.25 "SPxY": 165, "SPxM": 13.50, "unitSP": 1.35, "markup": 0.10, "margin": 0.11, "currency": "USD" }</code></td></tr><tr><td><code>subscription</code></td><td>object</td><td>A reference to <a href="subscriptions/"><code>subscription</code></a> where this line resides. The value is never returned in the context of a subscription. It is used only in orders.</td><td><code>{ "id": "SUB-1234-1234-1234" }</code></td></tr><tr><td><code>order</code></td><td>object</td><td>Last <a href="orders/"><code>order</code></a> where the Line was introduced/updated. The value is never returned in the context of an order. It can be used in the context of a subscription or agreement.</td><td><code>{ "id": "ORD-6869-4529-8975-9005" }</code></td></tr></tbody></table>

## Example

{% code title="LINE OBJECT" overflow="wrap" lineNumbers="true" %}
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
    "unitPP": 1.25,
    "SPxY": 165,
    "SPxM": 13.50,
    "unitSP": 1.35,
    "markup": 0.10,
    "margin": 0.11,
    "currency": "USD"
  },
  "subscription": {
    "id": "SUB-1234-1234-1234"
  }
}
```
{% endcode %}
