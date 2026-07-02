# Category

The Category object represents a category for notifications. Emails are sent within specific categories. Operations administrators can disable email sending for certain categories. User-level opt-outs are also managed through these categories.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-search="false"><thead><tr><th width="183">Field</th><th width="153">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The primary identifier for the category. </td></tr><tr><td><code>href</code></td><td>string, core</td><td>(Read-only) A relative reference to the object. </td></tr><tr><td><code>name</code></td><td>string, core</td><td>The name of the category. </td></tr><tr><td><code>shortDescription</code></td><td>string, core</td><td>A short description of the category. The description is displayed in the notification settings view for contacts. </td></tr><tr><td><code>description</code></td><td>string</td><td>A detailed description of the category. It describes the overall purpose of this category and can be used to include links to the documentation. </td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the category. Only published categories are visible to clients and vendors.</td></tr><tr><td><code>note</code></td><td>string</td><td>Notes to unpublish a category.</td></tr><tr><td><code>optOutAllowed</code></td><td>bool</td><td>Indicates if a contact can disable a notification category. </td></tr><tr><td><code>statistics</code></td><td>object</td><td><p>(Read-only) Statistics indicating how many messages of a given category were sent today, this week, and this month. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "messagesSent": 
  {
    "today": 22,
    "currentWeek": 244,
    "currentMonth": 668
  }
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Example

{% code title="CATEGORY OBJECT" overflow="wrap" lineNumbers="true" %}
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
