# Chat

The Chat object contains the following attributes:

<table><thead><tr><th width="167">Field</th><th width="159">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>A unique identifier for the chat. </td></tr><tr><td><code>revision</code></td><td>uint</td><td>(Read-only) The revision number of the chat. </td></tr><tr><td><code>icon</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The icon for the <code>group</code> and <code>channel</code> chat types.</td></tr><tr><td><code>name</code></td><td>string, core</td><td><p>(Optional) The chat's name. Required for <code>channel</code> chats, optional for <code>group</code> chats.</p><p>For <code>case</code> chats, the name is automatically generated from a truncated version of the first message in the support conversation.<br>This field is invalid for <code>direct</code> chats. </p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>(Optional) The chat's description. </p><p>Required for <code>channel</code> chats and optional for <code>group</code> chats. This field is invalid for any other chat type.</p></td></tr><tr><td><code>type</code></td><td>string, core</td><td><p> The type of chat. Allowed values are:</p><ul><li><code>Direct</code></li><li><code>Group</code></li><li><code>Case</code></li><li><code>Channel</code></li></ul></td></tr><tr><td><code>participants</code></td><td>object</td><td><p>The chat <a href="./#participant"><code>participant</code></a>. This field can be used to set the participants when creating a chat. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "CPT-1234-5678-9999",
    "role": "Admin",
    "status": "Active",
    "audit": {
      "created": {
        "at": "timestamp",
        "by": "{ IdentityQueryModel }"
     }
  }
]
</code></pre></td></tr><tr><td><code>lastMessage</code></td><td>object</td><td><p>The latest <a href="./#message-object"><code>message</code></a> in the chat sent by any participant. This field can be used to create an opening message when creating a chat. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "CMG-1234-5678-9999-XXXXX",
  "content": "string",
  "audit": {
    "created": {
      "at": "timestamp",
      "by": "{ IdentityQueryModel }"
  }
}
</code></pre></td></tr><tr><td><code>links</code></td><td>object</td><td>Represents the <a href="./#link-object"><code>link</code></a> for this chat.</td></tr><tr><td><code>attachments</code></td><td>object</td><td>Represents the <a href="./#attachment-object"><code>attachment</code></a> for this chat</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Participant object <a href="#participant-object" id="participant-object"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="184">Field</th><th width="141">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>The ID of the participant. </td></tr><tr><td><code>chat</code></td><td>chat</td><td><p>Chat parent object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "CHT-1111-2222-3333",
  "status": "Active|Archived",
  "type": "Private|Group|Case|Channel"
},
</code></pre></td></tr><tr><td><code>status</code></td><td>string</td><td>Can only be set  <code>exited</code> in chats that are not <code>direct</code>. <code>deactivated</code> is a special state for exited participants where the user is no longer active on the platform, to ensure their participant state is never transitioned back to <code>active</code>. </td></tr><tr><td><code>contact</code></td><td>object</td><td>The <a href="../../notifications-api/contacts/"><code>contact</code></a> entity from the notifications API forms the primary mechanism for identifying chat participants. </td></tr><tr><td><code>identity</code></td><td>identity</td><td><p>Platform identity model. The property exists on the <code>participant</code> object only as a convenience and is calculated from the identity property of the referenced <code>contact</code> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "USR-0000-0001",
  "name": "string",
  "icon": "optional string",
  "type": "User|ApiToken|Extension|Service"
}
</code></pre></td></tr><tr><td><code>account</code></td><td>object</td><td><p>Platform <a href="../../accounts-api/account/"><code>account</code></a> model. It is only provided during participant creation when a provided contact has multiple account contexts. In most circumstances, it is derived automatically from <code>contact</code>. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "ACC-0000-0000-0001",
  "status": "Active|Enabled|Disabled",
  "type": "Client|Vendor|Operations"
}
</code></pre></td></tr><tr><td><code>lastReadMessage</code></td><td><a href="./#message-object">message</a></td><td><p>If set, this field represents the last message seen by this user. It can be the same as latest message if user is up to date with chat. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "CMG-1234-5678-9999-XXXXX",
  "content": "string",
  "audit": {
    "created": {
      "at": "timestamp",
      "by": "{ IdentityQueryModel }"
  }
}
</code></pre></td></tr><tr><td><code>unread</code></td><td>integer</td><td><p>(Read-only) Calculated field. It represents the count of messages appended to the chat since the <code>lastReadMessage</code>. When a participant performs an action that changes any chat state, this will be reset to zero for that participant. It can also be reset by a put operation that changes the <code>lastReadMessage</code> reference. </p><p>Example: 27</p></td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>muted</code></td><td>boolean, core</td><td>(Optional) Flag indicating whether the participant should be notified of new messages in the chat. Example: true</td></tr></tbody></table>

## Message object

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="132">Name</th><th width="161">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>The ID of the chat message. The first three sections are derived from the chat ID. The last section (length 5) supports up to 100,000 messages. For additional performance, this field could be separated from the clustered index in the database. </td></tr><tr><td><code>chat</code></td><td>object</td><td><p>Represents the <code>chat</code> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "CHT-1111-2222-3333",
  "status": "Active|Archived",
  "type": "Private|Group|Case|Channel"
}
</code></pre></td></tr><tr><td><code>sender</code></td><td>object</td><td><p>The <a href="./#participant-object"><code>participant</code></a> that sent this message. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "CPT-345-678",
  "status": "Active",
  "role": "Contributor"
}
</code></pre></td></tr><tr><td><code>content</code></td><td>string</td><td><p>The body of the message. Can contain any Markdown supported by the UI, as well as special markup for links to platform objects. </p><p>Example: <code>Please find attached &#x3C;form id=”FRm-1234-5678 display=”Order details”/></code></p></td></tr><tr><td><code>visibility</code></td><td>string, core</td><td>Allowed values:  <code>public</code> or <code>private</code>. <code>private</code> means that it's visible only to users within the same account. In the context of a <code>channel</code>, these statuses can be interpreted as <code>draft</code> (<code>private</code>) and <code>published</code> (<code>public</code>).</td></tr><tr><td><code>isDeleted</code></td><td>bool</td><td>Soft delete state. The message is hidden going forward but may have already been seen by users. Deleting a message does not delete associated attachments or links. Soft-deleted messages are still returned by the API but contain no content.</td></tr><tr><td><code>links</code></td><td>object</td><td><p>Represents the <a href="./#link-object"><code>link</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "LNK-0011-1233",
    "objectId": "HAT-345-678",
    "name": "certificate.pdf",
    "icon": "",
    "url": "/v1/helpdesk/chats/CHT-2601-7865-9618/attachments/HAT-1234-4567"
  },
  {
    "id": "LNK-1111-1233",
    "objectId": "AGR-345-678",
    "name": "E2E Seeded For Commerce",
    "type": "Agreement",
    "icon": "",
    "url": "/v1/commerce/agreements/AGR-345-678"
  },
  {
    "id": "LNK-2222-1233",
    "objectId": "HAN-345-678",
    "name": "",
    "icon": ""
  },
  {
    "id": "LNK-0123-1233",
    "objectId": "",
    "name": "Google",
    "icon": "",
    "url": "www.google.com"
  }
]

</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. For system messages, <code>created.by</code> is <code>null</code> whereas <code>created.at</code> contains a value.</td></tr></tbody></table>

## Link object

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="138">Field</th><th width="160">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>The ID of the link. </td></tr><tr><td><code>chat</code></td><td>object</td><td><p>Represents the linked <a href="./"><code>chat</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "CHT-1111-2222-3333",
  "status": "Active|Archived",
  "type": "Private|Group|Case|Channel"
}
</code></pre></td></tr><tr><td><code>message</code></td><td>object </td><td>The <a href="./#message-object"><code>message</code></a> object that this <code>link</code> object links to.</td></tr><tr><td><code>url</code></td><td>string, core</td><td>(Optional) The URL provided by the user.</td></tr><tr><td><code>objectId</code></td><td>string, core</td><td>(Optional) If <code>objectId</code> is present, the front end looks up the entity via the Audit API and builds a link using the returned <code>{ id, name, icon }</code>.</td></tr><tr><td><code>icon</code></td><td>string, core</td><td>Calculated by the front end when adding a link.</td></tr><tr><td><code>name</code></td><td>string, core</td><td>Calculated by the front end when not provided by the user.</td></tr><tr><td><code>isDeleted</code></td><td>boolean, core</td><td>Soft delete property.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Attachment object <a href="#attachment-object" id="attachment-object"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="150">Field</th><th width="178">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>The ID of the <code>attachment</code> object.</td></tr><tr><td><code>chat</code></td><td>object</td><td><p>The ID of the <a href="./"><code>chat</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "CHT-1111-2222-3333",
  "status": "Active|Archived",
  "type": "Private|Group|Case|Channel"
}
</code></pre></td></tr><tr><td><code>message</code></td><td>object </td><td>Represents the <a href="./#message-object"><code>message</code></a> object that this attachment links to.</td></tr><tr><td><code>isDeleted</code></td><td>bool, core</td><td>Indicates whether the message has been soft‑deleted. Soft deletion does not prevent users from having seen the message in the past. It only affects visibility going forward.</td></tr><tr><td><code>fileId</code></td><td>string, core</td><td>(Read-only) The ID of file metadata. </td></tr><tr><td><code>filename</code></td><td>string, core</td><td>The name of the file. </td></tr><tr><td><code>contentType</code></td><td>string</td><td>(Read‑only) The attachment MIME type. This value is set automatically when the attachment is uploaded.</td></tr><tr><td><code>size</code></td><td>integer</td><td>(Read-only) The size of the attachment in bytes. This value is set automatically when the attachment is uploaded. </td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. The <code>created</code> audit property is used to find the message sender and timestamp. For system messages,  <code>null</code> is used.</td></tr></tbody></table>

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
