# Category

The Category object represents a category for notifications. Emails are sent within specific categories. Operation administrators can disable email sending for certain categories, and user-level opt-outs are also managed through these categories.&#x20;

This object contains the following attributes:

<table><thead><tr><th width="183">Field</th><th width="135">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The primary identifier for the category. </p><p>Example: NTC-1234-9876</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>A relative reference to the object. </p><p>Example: /v1/notifications/categories/NTC-1234-9876</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the category. </p><p>Example: Orders</p></td></tr><tr><td>shortDescription</td><td><code>string</code></td><td><p>The short description, shown in the notification settings view for contacts. </p><p>Example: Includes updates about order confirmations, order status updates, and related communications.</p></td></tr><tr><td>description</td><td><code>string</code></td><td>Detailed description of the category to be shown on the platform. The description describes the overall purpose of this category. It can be used to include the links to our documentation for more information. </td></tr><tr><td>status</td><td><code>enum</code></td><td>The status of the category. Only published categories are visible to clients and vendors.</td></tr><tr><td>note</td><td><code>string</code></td><td>Notes that must be added to unpublish a category.</td></tr><tr><td>optOutAllowed</td><td><code>bool</code></td><td><p>Indicates if a contact can disable a notification category. </p><p>Example: true</p></td></tr><tr><td>statistics</td><td><code>object</code></td><td><p>Statistics indicating how many messages of a given category were sent today, this week, and this month. </p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
  "messagesSent": 
  {
    "today": 22,
    "currentWeek": 244,
    "currentMonth": 668
  }
}
</code></pre></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td><p>A reference to the Audit object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">"created": { 
  "at": "2023-12-14T17:28:57Z", 
  "by": {
    "id": "UR-1234-1234-1234",
    "name": "John Smith",
    "icon": "/static/users/UR-1234-1234-1234.icon.svg"
  },
  "of": {
    "id": "ACC-1234-1234",
    "href": "/accounts/accounts/ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
  }
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="CATEGORY OBJECT" %}
{% code lineNumbers="true" %}
```json
{
  "id": "NTC-1234-9876",
  "href": "/v1/notifications/categories/NTC-1234-9876",
  "name": "Orders",
  "shortDescription": "Includes updates about order confirmations, order status updates, and related communications.",
  "description": "This category is used by the platform to provide notifications regarding\nOrders updates when a new Order is created, an existing\nOrder is updated or validation failed.",
  "status": "Published",
  "optOutAllowed": "true",
  "statistics": {
    "messagesSent": 
    {
      "today": 22,
      "currentWeek": 244,
      "currentMonth": 668
    }
  },
  "audit": {
    "created": { 
      "at": "2023-12-14T17:28:57Z", 
      "by": {
        "id": "UR-1234-1234-1234",
        "name": "John Smith",
        "icon": "/static/users/UR-1234-1234-1234.icon.svg"
      },
      "of": {
        "id": "ACC-1234-1234",
        "href": "/accounts/accounts/ACC-1234-1234",
        "name": "Microsoft",
        "icon": "/static/ACC-1234-1234/account.png"
      }
    }
  }
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
