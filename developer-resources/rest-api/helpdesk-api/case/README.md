# Case

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="140">Field Name</th><th width="165">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>A unique identifier for the case. </p><p>Example: CAS-1234-5678-9012</p></td></tr><tr><td><code>chat</code></td><td>object</td><td><p>The <a href="../chat/"><code>chat</code></a> object for the case. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "CHT-1111-2222-3333",
  "type": "case"
}
</code></pre></td></tr><tr><td><code>revision</code></td><td>unit</td><td>Revision number (used for platform-level versioning).</td></tr><tr><td><code>parameters</code></td><td>parameter</td><td><p>A set of parameter values. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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
</code></pre></td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the case. Allowed values: <code>processing</code>, <code>querying</code>, or <code>completed</code>.</td></tr><tr><td><code>awaiting</code></td><td>boolean</td><td><p>Allows an Operations user to mark the case as awaiting. This value is not visible to client or vendor account users. </p><p>Example: true</p></td></tr><tr><td><code>queryPrompt</code></td><td>string</td><td><p>If a case is moved to <code>querying</code>, the participant, usually the operator, can provide an additional message to explain what is needed from the other side.</p><p>Example: “Can you please fill in the form with the required information?”</p></td></tr><tr><td><code>queue</code></td><td>object</td><td><p>The <a href="../queue/"><code>queue</code></a> that the case is currently in. This is not read-only, as the queue can change (the case can be transferred). </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "HQU-1234-1234",
  "name": "Business Onboarding",
  "workflow": "HWF-1234-4568"
}
</code></pre></td></tr><tr><td><code>assignee</code></td><td>platformIdentity</td><td><p>Represents the actor responsible for managing the case. Typically, this is a user from the account that owns the queue. Any actor assigned will automatically be added as a participant in the related case chat. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "USR-6375-2499",
  "email": "will.smith@SWO1.com",
  "firstName": "Will",
  "lastName": "Smith"
}
</code></pre></td></tr><tr><td><code>account</code></td><td>object</td><td><p>Represents the <a href="../../accounts-api/account/">account</a> from which the reporter opened the case. When a case is created by an Operations account user on behalf of a client or vendor, this is the account chosen by the operator in the wizard. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "ACC-6685-9632",
  "name": "Stark Industries"
}
</code></pre></td></tr><tr><td><code>reporter</code></td><td>platformIdentity</td><td><p>Represents the actor who is reporting the case. If this information is not included in the payload when the case is created, the identity of the request claim serves as the default. When an operator creates a case on behalf of a client or vendor, that individual will be recognized as the identity associated with the case.</p><p> Any actor designated as the reporter will also be automatically included as a participant in the related case chat. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "USR-6375-2499",
  "name": "Jane Doe"
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>The <a href="../../common-api-objects/audit.md"><code>audit</code></a> trail of the case.</td></tr></tbody></table>
