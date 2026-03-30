# Webhook API

The Webhook object represents an endpoint of an external system that should be invoked for specific events within the Marketplace Platform.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="153">Field Name</th><th width="171">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The webhook's unique identifier.</p><p>Example: WBH-5433-8787</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>The relative reference to the object within the API. </p><p>Example: /notifications/webhooks/WBH-5433-8787</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the webhook.  </p><p>Example: Webhook for purchase order draft validation for Microsoft Office 365.</p></td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the webhook. Allowed values: <code>enabled</code> or <code>disabled</code>.</td></tr><tr><td><code>type</code></td><td>enum</td><td><p>Defines what the webhook is designed for. Allowed values: <code>validatePurchaseOrderDraft</code>, <code>validatePurchaseOrderQuerying</code>, <code>validateChangeOrderDraft</code>,</p><p><code>validateTerminateOrder</code>,</p><p><code>validateRequest</code>,</p><p><code>validateAccount</code>,</p><p><code>selectOrderLines</code>.</p></td></tr><tr><td><code>objectType</code></td><td>enum</td><td><p>An object that triggers the webhook event. </p><p>Allowed values:  <code>order</code>, <code>request</code>, or <code>account</code>.</p></td></tr><tr><td><code>url</code></td><td>string</td><td><p>The webhook endpoint URL. Only <code>https://</code> endpoints are allowed.</p><p>Example: https://some-api.vendor.com/order-validation</p></td></tr><tr><td><code>criteria</code></td><td>object</td><td><p>A set of key-value objects required in the webhook payload to trigger the webhook call. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ "product.id": "PRD-6233-9657-3232" }
</code></pre></td></tr><tr><td><code>statistics</code></td><td>object (<a href="./#statistics"><code>statistics</code></a>)</td><td><p>The statistical and debug information regarding webhook executions. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "total": 1234,
  "successes": 1132,
  "failures": 101,
  "failuresSinceLastSuccess": 2
}
</code></pre></td></tr><tr><td><code>lastSuccess</code></td><td>object (<a href="./#call"><code>call</code></a>)</td><td><p>The last successful call to webhook URL. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
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
}
</code></pre></td></tr><tr><td><code>lastFailure</code></td><td>object (<a href="./#call"><code>call</code></a>)</td><td><p>Last failed call to webhook URL. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ 
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
}
</code></pre></td></tr><tr><td><code>lastCall</code></td><td>object (<a href="./#call"><code>call</code></a>)</td><td><p>THe last call to webhook URL. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
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
}
</code></pre></td></tr><tr><td><code>secret</code></td><td>string</td><td><p>The secret used for authorization in the third-party systems. It's returned only once in response to the <a href="create-webhook.md">Create Webhook</a> endpoint.</p><p>Example: 3ct^6NoryQN22V</p></td></tr><tr><td><code>account</code></td><td>object</td><td><p>A reference to the vendor <a href="../../accounts-api/"><code>account</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "ACC-1234-1234",
  "href": "/accounts/accounts/ACC-1234-1234",
  "name": "Microsoft",
  "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Statistics  object <a href="#statistics" id="statistics"></a>

<table><thead><tr><th width="228.22216796875">Field Name</th><th width="127">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>total</code></td><td>number</td><td><p>The total number of calls made from the Marketplace Platform to the external system represented by the Webhook object. </p><p>Example: 77</p></td></tr><tr><td><code>successes</code></td><td>number</td><td><p>The total number of successful calls made from the Marketplace Platform to an external system represented by the Webhook object. </p><p>Example: 70</p></td></tr><tr><td><code>failures</code></td><td>number</td><td><p>The total number of failed calls made from the Marketplace Platform to an external system represented by the Webhook object. </p><p>Example: 7</p></td></tr><tr><td><code>failuresSinceLastSuccess</code></td><td>number</td><td><p>The total number of failed calls since the last successful call made by the Marketplace Platform to an external system, represented by the Webhook object. </p><p>Example: 3</p></td></tr></tbody></table>

## Call object <a href="#call" id="call"></a>

<table><thead><tr><th width="223">Field Name</th><th width="118">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>total</code></td><td>number</td><td><p>The total number of calls made from the Marketplace Platform to the external system represented by the webhook object. </p><p>Example: 77</p></td></tr><tr><td><code>successes</code></td><td>number</td><td><p>The total number of successful calls made from the Marketplace Platform to an external system represented by the webhook object. </p><p>Example: 70</p></td></tr><tr><td><code>failures</code></td><td>number</td><td><p>The total number of failed calls made from the Marketplace Platform to an external system represented by the webhook object. </p><p>Example: 7</p></td></tr><tr><td><code>failuresSinceLastSuccess</code></td><td>number</td><td><p>The total number of failed calls since the last successful call made by the Marketplace Platform to an external system, represented by the webhook object. </p><p>Example: 3</p></td></tr></tbody></table>
