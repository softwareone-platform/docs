# Industry

Industries refer to specific business sectors or markets that products are designed to serve.&#x20;

This classification helps users identify solutions that are tailored to the unique challenges and requirements of their particular field. Examples of industries include healthcare, finance, education, retail, manufacturing, and technology. By categorizing products by industry, we enable users to quickly find software that understands and addresses their sector-specific needs, compliance requirements, and best practices.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="165">Field Name</th><th width="173">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>An identifier for the industry.</p><p>Example: IND-1671-3887</p></td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>The identifier in the external system.</p><p>Example: arK9uX45</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>A user-friendly name for the industry.</p><p>Example: Development</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A short description of the industry.</p><p>Example: Software development tools</p></td></tr><tr><td><code>status</code></td><td>string</td><td><p>The status of the industry. </p><p>Example: Draft</p></td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>revision</code></td><td>integer</td><td><p>The entity's revision number.</p><p>Example: 3</p></td></tr></tbody></table>

## Example response <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
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
