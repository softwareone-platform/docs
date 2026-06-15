# Webhook API

The Webhook object represents an endpoint of an external system that should be invoked for specific events within the Marketplace Platform.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="153">Field</th><th width="128">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The webhook's unique identifier.</td></tr><tr><td><code>href</code></td><td>string</td><td>(Read-only) The relative reference to the object within the API. </td></tr><tr><td><code>description</code></td><td>string</td><td>A description of the webhook.  </td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the webhook. Allowed values are <code>enabled</code> or <code>disabled</code>.</td></tr><tr><td><code>type</code></td><td>enum</td><td><p>Defines what the webhook is designed for. Allowed values are: </p><ul><li><code>validatePurchaseOrderDraft</code></li><li><code>validatePurchaseOrderQuerying</code></li><li><code>validateChangeOrderDraft</code></li><li><code>validateTerminateOrder</code></li><li><code>validateRequest</code></li><li><code>validateAccount</code></li><li><code>selectOrderLines</code></li></ul></td></tr><tr><td><code>objectType</code></td><td>enum</td><td><p>Object that triggers the webhook event. Allowed values are:</p><ul><li><code>Order</code></li><li><code>Request</code></li><li><code>Account</code></li></ul></td></tr><tr><td><code>url</code></td><td>string</td><td>The webhook endpoint URL. Only <code>https://</code> endpoints are allowed.</td></tr><tr><td><code>criteria</code></td><td>object</td><td>(Read-only) A set of key-value objects required in the webhook payload to trigger the webhook call. </td></tr><tr><td><code>statistics</code></td><td>object</td><td>(Read-only) Represents the <a href="./#statistics"><code>statistics</code></a> object containing statistical and debug information regarding webhook executions. </td></tr><tr><td><code>lastSuccess</code></td><td>object</td><td>(Read-only) Represents the <a href="./#call"><code>call</code></a> object containing the last successful call to the webhook URL. </td></tr><tr><td><code>lastFailure</code></td><td>object</td><td>(Read-only) Represents the <a href="./#call"><code>call</code></a> object with details of the last failed call to the webhook URL. </td></tr><tr><td><code>lastCall</code></td><td>object</td><td>(Read-only) Represents the <a href="./#call"><code>call</code></a> object with details of the last call to the webhook URL. </td></tr><tr><td><code>secret</code></td><td>string</td><td>The secret used for authorization in the third-party systems. It's returned only once in response to the <a href="create-webhook.md">Create Webhook</a> endpoint.</td></tr><tr><td><code>account</code></td><td>object</td><td>(Read-only) Represents the vendor <a href="../../accounts-api/"><code>account</code></a> object. </td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Statistics object <a href="#statistics" id="statistics"></a>

<table><thead><tr><th width="233.22216796875">Field</th><th width="101">Data</th><th>Description</th></tr></thead><tbody><tr><td><code>total</code></td><td>number</td><td>(Read-only) Total number of calls made from the platform to the external system represented by the Webhook object. </td></tr><tr><td><code>successes</code></td><td>number</td><td>(Read-only) Total number of successful calls made from the platform to an external system represented by the Webhook object. </td></tr><tr><td><code>failures</code></td><td>number</td><td>(Read-only) Total number of failed calls made from the platform to an external system represented by the Webhook object. </td></tr><tr><td><code>failuresSinceLastSuccess</code></td><td>number</td><td>(Read-only) Total number of failed calls since the last successful call made by the platform to an external system, represented by the Webhook object. </td></tr></tbody></table>

## Call object <a href="#call" id="call"></a>

<table><thead><tr><th width="245">Field</th><th width="118">Data</th><th>Description</th></tr></thead><tbody><tr><td><code>total</code></td><td>number</td><td>(Read-only) Total number of calls made from the platform to the external system represented by the webhook object. </td></tr><tr><td><code>successes</code></td><td>number</td><td>(Read-only) Total number of successful calls made from the platform to an external system represented by the webhook object. </td></tr><tr><td><code>failures</code></td><td>number</td><td>(Read-only) Total number of failed calls made from the platform to an external system represented by the webhook object. </td></tr><tr><td><code>failuresSinceLastSuccess</code></td><td>number</td><td>(Read-only) Total number of failed calls since the last successful call made by the platform to an external system, represented by the webhook object. </td></tr></tbody></table>

## Example

<pre class="language-json" data-title="WEBHOOK API OBJECT" data-overflow="wrap" data-line-numbers><code class="lang-json"><strong>{
</strong>  "id": "WBH-5433-8787",
  "href": "/notifications/webhooks/WBH-5433-8787",
  "description": "Webhook for some products"
  "account": {
    "id": "ACC-7362-0233",
    "href": "/accounts/accounts/ACC-7362-0233",
    "name": "Adobe",
    "icon": "/static/ACC-7362-0233/account.png"
  },
  "objectType": "order",
  "type": "validatePurchaseOrderDraft",
  "params": {
    "product.id": "PRD-6233-9657"
  },
  "status": "enabled",
  "url": "https://my-webhook.endpoint.com/validation",
  "secret": "*******************",
  "statistics": {
    "total": 1234,
    "successes": 1132,
    "failures": 101,
    "failuresSinceLastSuccess": 2
  },
  "lastSuccess": {
    "success": true,
    "callTime": "2024-12-12T11:11:11",
    "responseTime": "2024-12-12T11:12:03",
    "httpStatusCode": "200",
    "reasonPhrase": "OK",
    "headers": {
      "Date": "Wed, 15 May 2024 10:16:56 GMT",
    },
    "error": null,
    "response": { ... }
  },
  "lastFailure": {
    "success": true,
    "callTime": "2024-12-12T11:11:11",
    "responseTime": "2024-12-12T11:12:03",
    "status": "401",
    "reasonPhrase": "Auth Error",
    "response": "Unauthenticated",
    "headers": {
      "Date": "Wed, 15 May 2024 10:16:56 GMT",
    },
    "error": "JWT Token was invalid",
    "response": null,
  },
  "lastCall": {
    "success": true,
    "callTime": "2024-12-12T11:11:11",
    "responseTime": "2024-12-12T11:12:03",
    "httpStatusCode": "200",
    "reasonPhrase": "OK",
    "headers": {
      "Date": "Wed, 15 May 2024 10:16:56 GMT",
    },
    "error": null,
    "response": { ... }
  },
  "audit": {
    "created": { "at": "...", "by": { } },
    "updated": { "at": "...", "by": { } }
  },
}
</code></pre>

