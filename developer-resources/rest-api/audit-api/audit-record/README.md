# Audit Record

The Audit object serves as a comprehensive record of a singular event that took place within the platform.

<table><thead><tr><th width="166">Field</th><th width="157">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Unique identifier for the audit record. Note that no nesting exists for this identifier. </p><p></p><p>Example: AUD-1671-0642-1234-1234</p></td></tr><tr><td>event</td><td>string</td><td><p>The event code. Format: {platform/extension}.{module/extension name}.{object}.{action} </p><p></p><p>Example: platform.commerce.order.created</p></td></tr><tr><td>summary</td><td>string</td><td><p>A summary of the audit record.</p><p></p><p>Example: Order created</p></td></tr><tr><td>details</td><td>string</td><td><p>The audit details template. Any document property may be used as a placeholder. </p><p></p><p>Example: The order {{order.id}} has been successfully created by {{actor.name}} and is now in the platform.</p></td></tr><tr><td>actor</td><td>Audit Record Actor</td><td><p>Information about the actor who has triggered an event. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "USR-2311-4038",
  "name": "Will Smith",
  "icon": "/public/users/usr-2311-4038.jpg",
  "account": {
    "id": "ACC-8989-32321",
    "name": "AdAstra Flex",
    "icon": "/public/accounts/acc-8989-32321.jpg",
  }
}
</code></pre></td></tr><tr><td>object</td><td>Audit Record Object</td><td><p>The API object for which an event has been triggered. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "ORD-3568-4038-2535",
  "type": "order",
  "icon": null,
  "objectType" : "Order"
}
</code></pre></td></tr><tr><td>timestamp</td><td>DateTime</td><td><p>The timestamp of the event. </p><p></p><p>Example: 2024-07-25T09:09:30.087Z</p></td></tr><tr><td>type</td><td>AuditRecordType Enum</td><td><p>The visibility of the audit record, which can be public or private. </p><p></p><p>Example: Public</p></td></tr><tr><td>request</td><td>Request</td><td><p>The request for technical data. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
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
}: null,
</code></pre></td></tr><tr><td>documents</td><td>JsonObject</td><td><p>JsonElement containing a collection of linked EventRecordObjects. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json"><strong>{
</strong>  "order_01": {
    "id": "ORD-3568-4038-2535",
    "href": "/commerce/orders/ORD-3568-4038-2535",
    "type": "Purchase",
    "status": "Completed" 
  }
  "extraData_01" {
    "extra_prop_01": "Some value that does not exist in order" 
  }
}
</code></pre></td></tr><tr><td>viewers</td><td>Viewer []</td><td><p>A list of accounts that have access to the audit records. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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
]
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="Audit Record" %}
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
{% endtab %}
{% endtabs %}
