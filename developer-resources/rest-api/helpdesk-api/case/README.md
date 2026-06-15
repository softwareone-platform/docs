# Case

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="154">Field</th><th width="174">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>A unique identifier for the case. </td></tr><tr><td><code>chat</code></td><td>object</td><td>The <a href="../chat/"><code>chat</code></a> object for the case.</td></tr><tr><td><code>revision</code></td><td>unit, core</td><td>The revision number used for platform-level versioning.</td></tr><tr><td><code>parameters</code></td><td>object</td><td><p>Represents the <code>parameter</code> object, which contains a set of parameter values. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
 {
   "id": "PAR-1344-4634",
   "name": "Priority",
   "scope": "Case",
   "phase": "request",
   "constraints":{
     "visibleToReporter": true,
   },
   "externalId": "ext-id-1234",
   "value": "Priority 1"
 }
]
</code></pre></td></tr><tr><td><code>status</code></td><td>enum, core</td><td><p>Represents the case status. Allowed values are:</p><ul><li><code>Processing</code></li><li><code>Querying</code></li><li><code>Completed</code></li></ul></td></tr><tr><td><code>awaiting</code></td><td>boolean</td><td>Allows an Operations user to mark the case as awaiting. This value is not visible to client or vendor account users. </td></tr><tr><td><code>queryPrompt</code></td><td>string</td><td>If a case is moved to <code>querying</code>, the participant, usually the operator, can provide an additional message to explain what is needed from the other side.</td></tr><tr><td><code>queue</code></td><td>object, core</td><td><p>The <a href="../queue/"><code>queue</code></a> that the case is currently in. This is not read-only, as the queue can change (the case can be transferred). </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "HQU-1234-1234",
  "name": "Business Onboarding",
  "workflow": "HWF-1234-4568"
}
</code></pre></td></tr><tr><td><code>assignee</code></td><td>object, core</td><td><p>Represents the actor responsible for managing the case. Usually, a user from the account that owns the queue. Any assigned actor is automatically added as a participant in the related case chat.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "USR-6375-2499",
  "email": "jane@doe.com",
  "firstName": "Jane",
  "lastName": "Doe"
}
</code></pre></td></tr><tr><td><code>account</code></td><td>object, core</td><td><p>Represents the <a href="../../accounts-api/account/"><code>account</code></a> from which the reporter opened the case. When a case is created by an operations account user on behalf of a client or vendor, this is the account chosen by the operator in the wizard. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "ACC-6685-9632",
  "name": "Stark Industries"
}
</code></pre></td></tr><tr><td><code>reporter</code></td><td>object, core</td><td><p>Represents the actor who is reporting the case. If not provided when the case is created, the reporter defaults to the identity from the request claim. When an operator creates a case on behalf of a client or vendor, that operator becomes the reporter. Any actor designated as the reporter is automatically added as a participant in the related case chat. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "USR-6375-2499",
  "name": "Jane Doe"
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
