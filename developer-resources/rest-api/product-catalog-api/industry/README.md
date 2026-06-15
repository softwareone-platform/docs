# Industry

Industries refer to specific business sectors or markets that products are designed to serve.&#x20;

This classification helps users identify solutions tailored to the unique challenges and requirements of their field. Examples of industries include healthcare, finance, education, retail, manufacturing, and technology. By categorizing products by industry, we enable users to quickly find software that understands and addresses their sector-specific needs, compliance requirements, and best practices.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="165">Field</th><th width="149">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) An identifier for the industry.</td></tr><tr><td><code>externalId</code></td><td>string</td><td>The identifier in the external system.</td></tr><tr><td><code>name</code></td><td>string, core</td><td>A user-friendly name for the industry.</td></tr><tr><td><code>description</code></td><td>string</td><td>A short description of the industry.</td></tr><tr><td><code>status</code></td><td>string, core</td><td><p>The status of the industry. Allowed values are: </p><ul><li><code>Draft</code></li><li><code>Published</code></li><li><code>Unpublished</code></li><li><code>Deleted</code></li></ul></td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>revision</code></td><td>integer, core</td><td>The entity's revision number.</td></tr></tbody></table>

## Example

{% code title="INDUSTRY OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "IND-1671-3887",
  "externalId": "arK9uX45",
  "name": "Education",
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
