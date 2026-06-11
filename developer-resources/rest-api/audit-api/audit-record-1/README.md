# Audit Record

The Audit record object signifies a specific entity within the platform for which an Audit object is generated. Each Audit object can only be created for one platform object at a time.

<table><thead><tr><th width="139">Field</th><th width="143">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The object's identifier. </td></tr><tr><td><code>name</code></td><td>string, core</td><td>(Read-only) The name of the object. If it  doesn't exist, the ID is included.</td></tr><tr><td><code>icon</code></td><td>string, core</td><td>(Read-only) The URL of the object icon. </td></tr><tr><td><code>objectType</code></td><td>string, core</td><td>(Read-only) The type of object. </td></tr><tr><td><code>revision</code></td><td>integer, core</td><td>(Read-only) The revision number of the object. </td></tr></tbody></table>

## Example

{% code title="AUDIT RECORD OBJECT" lineNumbers="true" %}
```json
{
  "id": "ORD-3568-4038-2535",
  "type": "order",
  "icon": null,
  "objectType": "Order",
  "revision": 24
}
```
{% endcode %}

## Audit Record Actor object

The Audit record object signifies a specific entity within the platform for which an Audit object is generated. Each Audit object can only be created for one platform object at a time.

<table><thead><tr><th width="115">Field</th><th width="144">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The ID of the user. </td></tr><tr><td><code>name</code></td><td>string, core</td><td>(Read-only) The name of the user. </td></tr><tr><td><code>icon</code></td><td>string, core</td><td>(Read-only) The URL to the user's logo. </td></tr><tr><td><code>account</code></td><td>object, core</td><td><p>(Read-only) Represents the <a href="./#audit-record-actor-account"><code>auditRecordActorAccount</code></a> object containing the user's account details.  </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "ACC-3408-7241",
    "name": "MPT Commerce e2e client",
    "icon": "/v1/accounts/accounts/ACC-3408-7241/icon",
    "accountType": "Client"
  }
</code></pre></td></tr></tbody></table>

### Example

{% code title="AUDIT RECORD ACTOR OBJECT" lineNumbers="true" %}
```json
 "name": "John Doe",
  "icon": "/v1/accounts/users/USR-0556-8733/icon",
  "account": {
    "id": "ACC-3408-7241",
    "name": "MPT_Commerce e2e client",
    "icon": "/v1/accounts/accounts/ACC-3408-7241/icon",
    "accountType": "Client"
  }
} 
```
{% endcode %}

## Audit Record Actor Account object <a href="#audit-record-actor-account" id="audit-record-actor-account"></a>

The Identity object represents a user account associated with the creation of an `audit` object.

<table><thead><tr><th width="181">Field</th><th width="166">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, core</td><td>(Read-only) (Optional) The account ID.</td></tr><tr><td><code>name</code></td><td>string, core</td><td>(Read-only) The account name. </td></tr><tr><td><code>icon</code></td><td>string, core</td><td>(Read-only) The URL of the account logo. </td></tr><tr><td><code>accountType</code></td><td>object, core</td><td>(Read-only) Represents the <a href="../../accounts-api/account/"><code>account</code></a> type.</td></tr></tbody></table>

### Example

{% code title="AUDIT RECORD ACTOR ACCOUNT OBJECT" lineNumbers="true" %}
```json
{
  "id": "ACC-3408-7241",
  "name": "MPT Commerce e2e client",
  "icon": "/v1/accounts/accounts/ACC-3408-7241/icon",
  "accountType": "Client"
}
```
{% endcode %}

## Audit Record Request object <a href="#audit-record-request" id="audit-record-request"></a>

The Request object captures request data that is useful to store as part of the Audit entry.

<table><thead><tr><th width="140">Field</th><th width="118">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>api</code></td><td>object</td><td><p>(Read-only) (Optional) Represents the <a href="./#api-request"><code>apiRequest</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "ip": "108.141.111.208",
  "geolocation": {
    "countryCode": "NL",
    "countryName": "Netherlands",
    "region": "North Holland"
  },
  "userAgent": "swo-extensions/1.0"
}
</code></pre></td></tr><tr><td><code>worker</code></td><td>object</td><td><p>(Read-only) (Optional) Represents the <a href="./#workerrequest"><code>workerRequest</code></a> object containing worker request details. </p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ 
    "workerName": "platformWorker"
}
</code></pre></td></tr><tr><td><code>log</code></td><td>object</td><td><p>(Read-only) (Optional) Represents the <a href="./#log-info"><code>logInfo</code></a> object containing the logging information or metadata. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "correlationId": "1233213215468"
}
</code></pre></td></tr></tbody></table>

### API Request object <a href="#api-request" id="api-request"></a>

This object captures metadata related to web-based requests, which is useful to include in the audit entry. It is populated only when the request is a web request.

<table><thead><tr><th width="137">Field</th><th width="120">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>ip</code></td><td>string</td><td>(Read-only) (Optional) A unique identifier of the IP address.</td></tr><tr><td><code>userAgent</code></td><td>string</td><td>(Read-only) (Optional) The user agent making the API request.</td></tr><tr><td><code>geolocation</code></td><td>object</td><td><p>(Read-only) The geolocation metadata for the request.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "countryCode": "NL",
  "countryName": "Netherlands",
  "region": "North Holland"
}
</code></pre></td></tr></tbody></table>

### Worker Request object

This object captures metadata for the request worker, which is useful to store as part of the Audit entry. It's populated only when the request is a worker request.

<table><thead><tr><th width="149">Field</th><th width="109">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>workerName</code></td><td>string</td><td>(Read-only) (Optional) The name of the request worker. </td></tr></tbody></table>

### Log Info object <a href="#log-info" id="log-info"></a>

This object captures request log metadata to be included in the audit entry.

<table><thead><tr><th width="154">Field</th><th width="102">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>corellationId</code></td><td>string</td><td>(Read-only) (Optional) The ID that can be used to track requests in the logging system.</td></tr></tbody></table>

## Audit Record Documents object <a href="#heading-title-text" id="heading-title-text"></a>

The Documents object is a flexible JSON structure designed to hold essential information that characterizes an event. It can represent either a complete or partial depiction of the object related to the audit event, or it may consist of any arbitrary JSON data.

{% code title="AUDIT RECORD DOCUMENTS OBJECT" overflow="wrap" lineNumbers="true" %}
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

## Audit Record Viewer object <a href="#heading-title-text" id="heading-title-text"></a>

The audit record viewer object signifies a platform account that grants access to specific audit records for its members.

<table><thead><tr><th width="144">Field</th><th width="129">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, core</td><td>(Read-only) The ID of the account.</td></tr><tr><td><code>name</code></td><td>string, core</td><td>(Read-only) The account name.</td></tr><tr><td><code>icon</code></td><td>string, core</td><td>(Read-only) The URL to the account logo. </td></tr><tr><td><code>accountType</code></td><td>object, core</td><td>(Read-only) The type of <a href="../../accounts-api/account/"><code>account</code></a>.</td></tr></tbody></table>

### Example

{% code title="AUDIT RECORD VIEWER OBJECT" lineNumbers="true" %}
```json
{
  "id": "ACC-3408-7241",
  "name": "e2e client",
  "type": "Client",
  "icon": "/v1/accounts/accounts/ACC-3408-7241/icon"
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
