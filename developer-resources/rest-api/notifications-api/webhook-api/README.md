# Webhook API

The Webhook object represents an endpoint of an external system that should be invoked for specific events within the Marketplace Platform. The object contains the following attributes:

<table><thead><tr><th width="153">Field</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The webhook's unique identifier.</p><p>Example: WBH-5433-8787</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>The relative reference to the object within the API. </p><p>Example: /notifications/webhooks/WBH-5433-8787</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>A description of the webhook.  </p><p>Example: Webhook for purchase order draft validation for Microsoft Office 365.</p></td></tr><tr><td>status</td><td><code>enum</code></td><td><p>The status of the webhook. </p><p>Possible enum values: <code>Enabled</code> or <code>Disabled</code>.</p></td></tr><tr><td>type</td><td><code>enum</code></td><td><p>Defines what for webhook is designed for. </p><p>Possible enum values: </p><p><code>ValidatePurchaseOrderDraft</code></p><p><code>ValidatePurchaseOrderQuerying</code></p><p><code>ValidateChangeOrderDraft</code></p><p><code>ValidateTerminateOrder</code></p><p><code>ValidateRequest</code></p><p><code>ValidateAccount</code></p><p><code>SelectOrderLines</code></p></td></tr><tr><td>objectType</td><td><code>enum</code></td><td><p>An object that triggers the webhook event. </p><p>Possible enum values: <code>Order</code>, <code>Request</code>, or <code>Account</code>.</p></td></tr><tr><td>url</td><td><code>string</code></td><td><p>The webhook endpoint URL. Only https:// endpoints are allowed.</p><p>Example: https://some-api.vendor.com/order-validation</p></td></tr><tr><td>criteria</td><td><code>object</code></td><td><p>A set of key-value objects required in the webhook payload to trigger the webhook call. </p><p>Example:</p><pre class="language-json"><code class="lang-json">{ "product.id": "PRD-6233-9657-3232" }
</code></pre></td></tr><tr><td>statistics</td><td><a href="./#statistics"><code>statistics</code></a></td><td><p>The statistical and debug information regarding webhook executions. </p><p>Example:</p><pre class="language-json"><code class="lang-json">{
  "total": 1234,
  "successes": 1132,
  "failures": 101,
  "failuresSinceLastSuccess": 2
}
</code></pre></td></tr><tr><td>lastSuccess</td><td><a href="./#call"><code>call</code></a></td><td><p>The last successful call to webhook URL. </p><p>Example:</p><pre class="language-json"><code class="lang-json">{
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
</code></pre></td></tr><tr><td>lastFailure</td><td><a href="./#call"><code>call</code></a></td><td><p>Last failed call to webhook URL. </p><p>Example:</p><pre class="language-json"><code class="lang-json">{ 
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
</code></pre></td></tr><tr><td>lastCall</td><td><a href="./#call"><code>call</code></a></td><td><p>Last call to webhook URL. </p><p>Example:</p><pre class="language-json"><code class="lang-json">{
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
</code></pre></td></tr><tr><td>secret</td><td><code>string</code></td><td><p>The secret used for authorization in the third-party systems. It's returned only once in response to the <a href="create-webhook.md">Create Webhook</a> endpoint.</p><p>Example: 3ct^6NoryQN22V</p></td></tr><tr><td>account</td><td><code>account</code></td><td><p>A reference to the vendor Account object. </p><p>Example:</p><pre class="language-json"><code class="lang-json">{
  "id": "ACC-1234-1234",
  "href": "/accounts/accounts/ACC-1234-1234",
  "name": "Microsoft",
  "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>audit</td><td><code>auditObject</code></td><td><p>The audit object. Possible values: <code>Created</code>, <code>Updated</code>, <code>Enabled</code>, <code>Disabled</code>.</p><p>Example:</p><pre class="language-json"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } },
  "enabled": { "at": "...", "by": { } },
  "disabled": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Statistics <a href="#statistics" id="statistics"></a>

<table><thead><tr><th width="216">Field</th><th width="107">Type</th><th>Description</th></tr></thead><tbody><tr><td>total</td><td><code>number</code></td><td><p>The total number of calls made from the Marketplace Platform to the external system represented by the Webhook object. </p><p>Example: 77</p></td></tr><tr><td>successes</td><td><code>number</code></td><td><p>The total number of successful calls made from the Marketplace Platform to an external system represented by the Webhook object. </p><p>Example: 70</p></td></tr><tr><td>failures</td><td><code>number</code></td><td><p>The total number of failed calls made from the Marketplace Platform to an external system represented by the Webhook object. </p><p>Example: 7</p></td></tr><tr><td>failuresSinceLastSuccess</td><td><code>number</code></td><td><p>The total number of failed calls since the last successful call made by the Marketplace Platform to an external system, represented by the Webhook object. </p><p>Example: 3</p></td></tr></tbody></table>

## Call <a href="#call" id="call"></a>

<table><thead><tr><th width="223">Field</th><th width="103">Type</th><th>Description</th></tr></thead><tbody><tr><td>total</td><td><code>number</code></td><td><p>The total number of calls made from the Marketplace Platform to the external system represented by the Webhook object. </p><p>Example: 77</p></td></tr><tr><td>successes</td><td><code>number</code></td><td><p>The total number of successful calls made from the Marketplace Platform to an external system represented by the Webhook object. </p><p>Example: 70</p></td></tr><tr><td>failures</td><td><code>number</code></td><td><p>The total number of failed calls made from the Marketplace Platform to an external system represented by the Webhook object. </p><p>Example: 7</p></td></tr><tr><td>failuresSinceLastSuccess</td><td><code>number</code></td><td><p>The total number of failed calls since the last successful call made by the Marketplace Platform to an external system, represented by the Webhook object. </p><p>Example: 3</p></td></tr></tbody></table>
