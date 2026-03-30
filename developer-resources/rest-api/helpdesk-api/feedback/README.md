# Feedback

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="142">Field Name</th><th width="145">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary identifier for the feedback. </p><p>Example: FDB-1234-5678</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>Represents the feedback. </p><p>Example: "Great product!"</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A long description of the feedback. </p><p>Example: "This is the best Marketplace to buy and manage subscriptions."</p></td></tr><tr><td><code>requester</code></td><td>object</td><td><p>The <a href="../../accounts-api/users/"><code>user</code></a> who submitted the feedback. </p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{ 
  "id": "USR-1234-4444",
  "name": "John Smith"
}
</code></pre></td></tr><tr><td><code>account</code></td><td>object</td><td><p>A reference to the <a href="../../accounts-api/account/"><code>account</code></a> object. </p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1234",   
    "name": "SatisfactionMicrosoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the feedback. Allowed values are <code>submitted</code>, <code>reviewed</code>, or <code>deleted</code>. </td></tr><tr><td><code>rating</code></td><td>integer</td><td>Represents the feedback rating provided by the user, ranging from -2 (strongly dissatisfied) to 2 (very satisfied).</td></tr><tr><td><code>notes</code></td><td>string</td><td><p>An optional message provided by Operations to share feedback or updates with the requester. </p><p>This field is visible to the associated vendor and client based on the requester’s account. Editable by Operations users only. </p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">Thank you for your feedback. We will look to add it as a future roadmap item. 
</code></pre></td></tr><tr><td><code>internalNotes</code></td><td>string</td><td><p>Internal notes related to the feedback. Only Operations users can view and edit the notes. </p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">The feature has been added to our roadmap.
</code></pre></td></tr><tr><td><code>metadata</code></td><td> </td><td><p>The metadata captured at the time of feedback, including:</p><ul><li>Timestamp</li><li>Browser and operating system</li><li>Device type</li><li>Screen resolution</li><li>Language settings</li><li>Current page URL</li><li>Location (based on IP address)</li></ul><p>This field is read-only.</p></td></tr><tr><td><code>externalIds</code></td><td><a href="../../common-api-objects/externalids.md">externalIds</a></td><td><p>A set of external IDs. </p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "operations":	"07bf766b-c767-4293-9ab3",
}
</code></pre></td></tr><tr><td><code>attachments</code></td><td>object</td><td><p>A reference to the <code>attachment</code> object. </p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{ 
"id": "FDA-1234-5678-0001",
"name": "Invoice",
"type": "file",
"filename": "invoice_001.pdf",
"size": 204800,
"contentType": "application/pdf",
"id": "USR-1234-4444",
"name": "John Smith"
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. Allowed values:  <code>created</code>, <code>updated</code>, <code>completed</code>, or <code>deleted</code>.</td></tr></tbody></table>

### Feedback Attachments object <a href="#feedback-attachments-object" id="feedback-attachments-object"></a>

<table><thead><tr><th width="139">Field</th><th width="149">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>Unique identifier for the feedback attachment. </p><p>Example: FDA-1234-5678-0001</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the feedback attachment. </p><p>Example: Comments</p></td></tr><tr><td><code>type</code></td><td>string</td><td>The type of the attachment object. Allowed values are <code>image</code>, <code>video</code>, or <code>file</code></td></tr><tr><td><code>filename</code></td><td>string</td><td><p>The name of the file. </p><p>Example: Comments.pdf</p></td></tr><tr><td><code>size</code></td><td>integer</td><td><p>The file size. </p><p>Example: 30</p></td></tr><tr><td><code>contentType</code></td><td>string</td><td>The type of the attached content, indicating its format. Example: application/pdf</td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. Allowed values: <code>created</code>, <code>updated</code>, or <code>deleted</code>.</td></tr></tbody></table>
