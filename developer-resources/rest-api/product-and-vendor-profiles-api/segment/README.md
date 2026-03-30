# Segment

Segments categorize products based on the size and type of organizations for which they are most suitable.&#x20;

This classification helps users identify solutions that align with their company's scale, complexity, and resource capabilities. Common segments include Small Business, Mid-Market, Enterprise, and Startups. By providing information about these segments, we assist users in finding software that not only meets their functional needs but also fits their organizational context. This ensures that the selected solutions have appropriate feature sets, pricing models, and scalability.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="135">Field Name</th><th width="170">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The identifier for the segment. </p><p>Example: SEG-1671-3887</p></td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>The identifier in an external system. </p><p>Example: arK9uX45</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>A user-friendly name for the industry.</p><p>Example: Development</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A short description of the segment. </p><p>Example: Software development tools</p></td></tr><tr><td><code>status</code></td><td>string</td><td>The status of the segment. Allowed values:  <code>draft</code>, <code>published</code>, <code>unpublished</code>, or <code>deleted</code>.</td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>revision</code></td><td>integer</td><td><p>The entity's revision number. </p><p>Example: 4</p></td></tr></tbody></table>

## Example response <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
{
  "id": "SEG-1671-3887",
  "externalId": "arK9uX45",
  "name": "Enterprise",
  "description": "Software development tools",
  "status": "Draft",
  "revision": 2,
  "audit": {
    "created": {
      "at": "2024-04-08T06:30:05.807Z",
      "by": {
        "id": "USR-2172-2499",
        "revision": 1,
        "name": "John User"
      }
    },
    "updated": {
      "at": "2024-05-16T09:17:36.406Z",
      "by": {
        "id": "TKN-3836-7769",
        "revision": 2,
        "name": "My token"
      },
    "deleted": {
      "at": "2024-05-17T09:17:36.406Z",
      "by": {
        "id": "TKN-3836-7769",
        "revision": 3,
        "name": "My token"
      }
    }
  }
}
```
{% endcode %}
