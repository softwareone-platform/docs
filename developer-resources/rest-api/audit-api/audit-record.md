# Audit

The Audit object provides a detailed record of a specific event that occurred within the platform.&#x20;

{% include "../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="153">Field</th><th width="146">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) A unique identifier for the audit record. Note that no nesting exists for this identifier.</td></tr><tr><td><code>event</code></td><td>string, core</td><td>The event code. Format: {platform/extension}.{module/extension name}.{object}.{action}</td></tr><tr><td><code>summary</code></td><td>string, core</td><td>A summary of the audit record.</td></tr><tr><td><code>details</code></td><td>string, core</td><td>The audit details template. Any document property may be used as a placeholder.</td></tr><tr><td><code>actor</code></td><td>object, core</td><td><p>(Read-only) Represents the <a href="audit-record.md#auditrecordactor"><code>auditRecordActor</code></a> object containing information about the actor who has triggered an event. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "USR-2311-4038",
  "name": "Will Smith",
  "icon": "/public/users/usr-2311-4038.jpg",
  "account": {
    "id": "ACC-8989-32321",
    "name": "AdAstra Flex",
    "icon": "/public/accounts/acc-8989-32321.jpg",
  }
}
</code></pre></td></tr><tr><td><code>object</code></td><td>object, core</td><td><p>Represents the <a href="audit-record.md#heading-title-text-1"><code>auditRecord</code></a> object for which an event has been triggered.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "ORD-3568-4038-2535",
  "type": "order",
  "icon": null,
  "objectType": "Order"
}
</code></pre></td></tr><tr><td><code>timestamp</code></td><td>dateTime, core</td><td>(Read-only) The timestamp of the event.</td></tr><tr><td><code>type</code></td><td>enum, core</td><td>(Read-only) The visibility of the audit record. Allowed values are  <code>public</code> or <code>private</code>.</td></tr><tr><td><code>request</code></td><td>object, core</td><td><p>Represents the <a href="audit-record.md#audit-record-request"><code>auditRecordRequest</code></a> object, which defines the request for technical data.</p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "api": {
    "ip": "192.168.2.2",
    "geolocation": {
       "countryCode": "ES",
       "countryName": "Spain",
       "region": "Catalonia"
    },
    "userAgent": "Chrome" 
  }
  "worker": {
    "workerName": null }
  "log": {
    "correlationId": "some-app-insights-id" }
}
</code></pre></td></tr><tr><td><code>documents</code></td><td>object</td><td><p>Represents the <a href="audit-record.md#heading-title-text-2"><code>auditRecordDocument</code></a> containing a collection of linked <code>eventRecord</code> objects.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "order_01": {
    "id": "ORD-3568-4038-2535",
    "type": "Purchase",
    "status": "Completed" 
  }
  "extraData_01" {
    "extra_prop_01": "Some value that does not exist in order" 
  }
}
</code></pre></td></tr><tr><td><code>viewers</code></td><td>object, core</td><td><p>(Read-only) Represents the <a href="audit-record.md#heading-title-text-1"><code>auditRecordViewer</code></a> object containing the list of accounts with access to audit records.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
      "id": "ACC-3408-7241",
      "name": "MPT Commerce e2e client",
      "type": "Client",
      "icon": "/v1/accounts/accounts/ACC-3408-7241/icon"
  },
  {
      "id": "ACC-1675-9721",
      "name": "Adobe",
      "type": "Vendor",
      "icon": "/v1/accounts/accounts/ACC-1675-9721/icon"
  }
]
</code></pre></td></tr></tbody></table>

## Example

{% code title="AUDIT OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
    "event": "platform.commerce.order.created",
    "summary": "Order Created",
    "details": "The order ORD-1208-2301-8479 has been successfully created by Balint Polgar and is now in the platform.",
    "object": {
        "id": "ORD-1208-2301-8479",
        "name": "ORD-1208-2301-8479",
        "objectType": "Order"
    },
    "timestamp": "2024-10-21T10:03:00.800Z",
    "actor": {
        "id": "USR-0556-8733",
        "name": "Balint Polgar",
        "icon": "/v1/accounts/users/USR-0556-8733/icon",
        "account": {
            "id": "ACC-3408-7241",
            "name": "MPT_QA_STATIC Commerce e2e client",
            "icon": "/v1/accounts/accounts/ACC-3408-7241/icon",
            "accountType": "Client"
        }
    },
    "type": "Public",
    "request": {
        "api": {
            "ip": "92.26.0.92",
            "geolocation": {
                "countryCode": "GB",
                "countryName": "United Kingdom",
                "region": "Scotland"
            },
            "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:131.0) Gecko/20100101 Firefox/131.0"
        }
    },
    "documents": {
        "order": {
            "id": "ORD-1208-2301-8479",
            "href": "/commerce/orders/ORD-1208-2301-8479",
            "type": "Termination",
            "status": "Draft"
        },
        "actor": {
            "id": "USR-0556-8733",
            "name": "Balint Polgar",
            "icon": "/v1/accounts/users/USR-0556-8733/icon",
            "account": {
                "id": "ACC-3408-7241",
                "name": "MPT_QA_STATIC Commerce e2e client",
                "icon": "/v1/accounts/accounts/ACC-3408-7241/icon",
                "accountType": "Client"
            }
        }
    },
    "viewers": [
        {
            "id": "ACC-3408-7241",
            "name": "MPT_QA_STATIC Commerce e2e client",
            "type": "Client",
            "icon": "/v1/accounts/accounts/ACC-3408-7241/icon"
        },
        {
            "id": "ACC-1675-9721",
            "name": "Adobe",
            "type": "Vendor",
            "icon": "/v1/accounts/accounts/ACC-1675-9721/icon"
        }
    ],
    "id": "AUD-0391-8050-9033-9920"
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
