# Audit Record

The Audit Record object provides a detailed record of a specific event that occurred within the platform. This object contains the following properties:

<table><thead><tr><th width="166">Field</th><th width="217">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>A unique identifier for the audit record. Note that no nesting exists for this identifier.</p><p>Example: AUD-1671-0642-1234-1234</p></td></tr><tr><td>event</td><td><code>string</code></td><td><p>The event code. Format: {platform/extension}.{module/extension name}.{object}.{action}</p><p>Example: platform.commerce.order.created</p></td></tr><tr><td>summary</td><td><code>string</code></td><td><p>A summary of the audit record.</p><p>Example: Order created</p></td></tr><tr><td>details</td><td><code>string</code></td><td><p>The audit details template. Any document property may be used as a placeholder.</p><p>Example: The order {{order.id}} has been successfully created by {{actor.name}} and is now in the platform.</p></td></tr><tr><td>actor</td><td><a href="./#audit-record-actor"><code>auditRecordActor</code></a></td><td><p>Information about the actor who has triggered an event.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "USR-2311-4038",
  "name": "Will Smith",
  "icon": "/public/users/usr-2311-4038.jpg",
  "account": {
    "id": "ACC-8989-32321",
    "name": "AdAstra Flex",
    "icon": "/public/accounts/acc-8989-32321.jpg",
  }
}
</code></pre></td></tr><tr><td>object</td><td><a href="./#heading-title-text"><code>auditRecordObject</code></a></td><td><p>The API object for which an event has been triggered.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "ORD-3568-4038-2535",
  "type": "order",
  "icon": null,
  "objectType" : "Order"
}
</code></pre></td></tr><tr><td>timestamp</td><td><code>dateTime</code></td><td><p>The timestamp of the event.</p><p>Example: 2024-07-25T09:09:30.087Z</p></td></tr><tr><td>type</td><td><code>enum</code></td><td>The visibility of the audit record. The possible values are  <code>Public</code> or <code>Private</code>.</td></tr><tr><td>request</td><td><a href="../../commerce-api/requests/"><code>request</code></a></td><td><p>The request for technical data.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
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
</code></pre></td></tr><tr><td>documents</td><td><a href="./#heading-title-text-2"><code>auditRecordDocuments</code></a></td><td><p>A JSON element containing a collection of linked Event Record objects.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "order_01": {
    "id": "ORD-3568-4038-2535",
    "type": "Purchase",
    "status": "Completed" 
  }
  "extraData_01" {
    "extra_prop_01": "Some value that does not exist in order" 
  }
}
</code></pre></td></tr><tr><td>viewers</td><td><a href="./#heading-title-text-1"><code>auditRecordViewer</code></a></td><td><p>The list of accounts that have access to the audit records.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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

## AuditRecord <a href="#heading-title-text" id="heading-title-text"></a>

The Audit record object signifies a specific entity within the platform for which an Audit object is generated. It is important to note that each Audit object can only be created for one platform object at a time.

<table><thead><tr><th width="153">Field</th><th width="149">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The object's identifier. </p><p>Example: ORD-1234-1234-5678</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the platform object. Contains the ID if the name doesn't exist. </p><p>Example: ORD-1234-1234-5678</p></td></tr><tr><td>icon</td><td><code>string</code></td><td>The URL of the object icon. </td></tr><tr><td>objectType</td><td><code>string</code></td><td><p>The type of object. </p><p>Example: Order</p></td></tr><tr><td>revision</td><td><code>integer</code></td><td><p>The revision of the object. </p><p>Example: 24</p></td></tr></tbody></table>

## AuditRecordActor

The Identity object signifies a user present within the platform, which is associated with the creation of an Audit object.

<table><thead><tr><th width="112">Field</th><th width="207">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The ID of the user. </p><p>Example: USR-0556-8733</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the user. </p><p>Example: John Doe</p></td></tr><tr><td>icon</td><td><code>string</code></td><td><p>The URL to the user's logo. </p><p>Example: /v1/accounts/users/USR-0556-8733/icon</p></td></tr><tr><td>account</td><td><a href="./#audit-record-actor-account"><code>auditRecordActorAccount</code></a></td><td><p>The user's account details.  </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "ACC-3408-7241",
    "name": "MPT_QA_STATIC Commerce e2e client",
    "icon": "/v1/accounts/accounts/ACC-3408-7241/icon",
    "accountType": "Client"
  }
</code></pre></td></tr></tbody></table>

## AuditRecordActorAccount <a href="#audit-record-actor-account" id="audit-record-actor-account"></a>

<table><thead><tr><th width="139">Field</th><th width="148">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The ID of the account.</p><p>Example: ACC-3408-7241</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the account. </p><p>Example: MPT Commerce e2e client</p></td></tr><tr><td>icon</td><td><code>string</code></td><td><p>The URL to the account's logo. </p><p>Example: /v1/accounts/accounts/ACC-3408-7241/icon</p></td></tr><tr><td>accountType</td><td><code>object</code></td><td><p>The type of account.</p><p>Example: Client</p></td></tr></tbody></table>

## AuditRecordViewer <a href="#heading-title-text" id="heading-title-text"></a>

The audit record viewer object signifies a platform account that grants access to specific audit records for its members.

<table><thead><tr><th width="139">Field</th><th width="148">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The ID of the account.</p><p>Example: ACC-3408-7241</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the account. </p><p>Example: MPT Commerce e2e client</p></td></tr><tr><td>icon</td><td><code>string</code></td><td><p>The URL to the account's logo. </p><p>Example: /v1/accounts/accounts/ACC-3408-7241/icon</p></td></tr><tr><td>accountType</td><td><code>object</code></td><td><p>The type of account.</p><p>Example: Client</p></td></tr></tbody></table>

## AuditRecordDocuments <a href="#heading-title-text" id="heading-title-text"></a>

The Documents object is a flexible JSON structure designed to hold essential information that characterizes an event. It can represent either a complete or partial depiction of the object related to the audit event, or it may consist of any arbitrary JSON data.

{% code overflow="wrap" lineNumbers="true" %}
```json
{
  "order": {
      "id": "ORD-1208-2301-8479",
      "href": "/commerce/orders/ORD-1208-2301-8479",
      "type": "Termination",
      "status": "Processing"
  },
  "actor": {
      "id": "TKN-8033-2484",
      "name": "Adobe Extension API",
      "icon": "",
      "account": {
          "id": "ACC-1675-9721",
          "name": "Adobe",
          "icon": "/v1/accounts/accounts/ACC-1675-9721/icon",
          "accountType": "Vendor"
      }
  }
}
```
{% endcode %}

## Examples

{% tabs %}
{% tab title="AUDIT RECORD" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
    "event": "platform.commerce.order.created",
    "summary": "Order Created",
    "details": "The order ORD-1208-2301-8479 has been successfully created by Jane Doe and is now in the platform.",
    "object": {
        "id": "ORD-1208-2301-8479",
        "name": "ORD-1208-2301-8479",
        "objectType": "Order"
    },
    "timestamp": "2024-10-21T10:03:00.800Z",
    "actor": {
        "id": "USR-0556-8733",
        "name": "JANE DOE",
        "icon": "/v1/accounts/users/USR-0556-8733/icon",
        "account": {
            "id": "ACC-3408-7241",
            "name": "MPT_QA Commerce e2e client",
            "icon": "/v1/accounts/accounts/ACC-3408-7241/icon",
            "accountType": "Client"
        }
    },
    "type": "Public",
    "request": {
        "api": {
            "ip": "00.00.00.00",
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
            "type": "Termination",
            "status": "Draft"
        },
        "actor": {
            "id": "USR-0556-8733",
            "name": "Jane Doe",
            "icon": "/v1/accounts/users/USR-0556-8733/icon",
            "account": {
                "id": "ACC-3408-7241",
                "name": "MPT_QA Commerce e2e client",
                "icon": "/v1/accounts/accounts/ACC-3408-7241/icon",
                "accountType": "Client"
            }
        }
    },
    "viewers": [
        {
            "id": "ACC-3408-7241",
            "name": "MPT_QA Commerce e2e client",
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
{% endtab %}

{% tab title="AUDIT RECORD ACTOR" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "USR-0556-8733",
  "name": "JOHN DOE",
  "icon": "/v1/accounts/users/USR-0556-8733/icon",
  "account": {
    "id": "ACC-3408-7241",
    "name": "MPT_QA_STATIC Commerce e2e client",
    "icon": "/v1/accounts/accounts/ACC-3408-7241/icon",
    "accountType": "Client"
  }
} 
```
{% endcode %}
{% endtab %}

{% tab title="AUDIT RECORD ACTOR ACCOUNT" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
    "id": "ACC-3408-7241",
    "name": "MPT Commerce e2e client",
    "icon": "/v1/accounts/accounts/ACC-3408-7241/icon",
    "accountType": "Client"
  }
```
{% endcode %}
{% endtab %}

{% tab title="AUDIT RECORD VIEWER" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "ACC-3408-7241",
  "name": "MPT_QA_STATIC Commerce e2e client",
  "type": "Client",
  "icon": "/v1/accounts/accounts/ACC-3408-7241/icon"
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

\
