---
description: Manage programs, certificates, and enrollments with the Program API.
---

# Program API

The **Program API** provides secure endpoints for creating, retrieving, updating, and managing programs, certificates, and enrollments within the Marketplace Platform.&#x20;

With this API, you can also perform additional operations, including:

* Publish and unpublish programs.
* Update program settings.
* Manage program groups and parameters.
* Create and manage program documents, media, and terms & conditions.
* Create and manage program templates.
* Submit and retrieve enrollment requests.
* Validate enrollments in the draft and querying states.
* Manage attachments associated with enrollments.
* Process or fail enrollment requests.
* Retrieve an enrollment's template.

<a href="https://editor-next.swagger.io/?url=https://api.platform.softwareone.com/public/v1/program/openapi.json" class="button primary">Try API</a><a href="https://api.platform.softwareone.com/public/v1/program/openapi.json" class="button secondary">Download API</a>

## Core Concepts

The Program API is built around the following core resources:

* **Certificate** - Issued to a client or partner as confirmation that they meet a specific program's requirements.
* **Enrollment** - Process through which a client formally registers or signs up to participate in a vendor program.&#x20;
* **Program** - Represents a set of requirements (parameters) that vendors ask their clients to meet.&#x20;

## Collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.&#x20;

Refer to the following capability matrix to see which roles are authorized to perform specific operations within each collection:

### Certificates

<table><thead><tr><th width="277">Capability</th><th width="152">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List certificates</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get certificate</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create certificate</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Update certificate</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Terminate certificate</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Expire certificate</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Get certificate template</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### Enrollments

<table><thead><tr><th width="321">Capability</th><th width="152">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List enrollments</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get enrollment</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update enrollment</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create enrollment</td><td>✅</td><td>❌</td><td>❌</td></tr><tr><td>Validates draft enrollment</td><td></td><td></td><td></td></tr><tr><td>Validates querying enrollment</td><td>✅</td><td>✅</td><td>❌</td></tr><tr><td>Process enrollment</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Query enrollment</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Complete enrollment</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Fail enrollment</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Assign enrollment</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete enrollment</td><td>✅</td><td>❌</td><td>❌</td></tr><tr><td>Render enrollment template</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>List of enrollment attachments</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Get single enrollment attachment by id</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Create new enrollment attachment</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Update enrollment attachment</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>Delete enrollment attachment</td><td>✅</td><td>❌</td><td>✅</td></tr></tbody></table>

### Programs

<table><thead><tr><th width="277">Capability</th><th width="152">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List programs</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get program</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create program</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update program by ID</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete program</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Publish program</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Unpublish program</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update program settings</td><td>❌</td><td>✅</td><td>❌</td></tr></tbody></table>

### Program Parameters

<table><thead><tr><th width="277">Capability</th><th width="152">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List parameters for a program</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get program parameter</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create parameter</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update parameter</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete program parameter</td><td>❌</td><td>✅</td><td>❌</td></tr></tbody></table>

### Program Parameter Groups

<table><thead><tr><th width="277">Capability</th><th width="152">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List parameter groups</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get parameter group</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create parameter group</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update parameter group</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete parameter group</td><td>❌</td><td>✅</td><td>❌</td></tr></tbody></table>

### Program Documents

<table><thead><tr><th width="277">Capability</th><th width="152">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List documents</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get document</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create document</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update document</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete document</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Publish document</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Unpublish document</td><td>❌</td><td>✅</td><td>❌</td></tr></tbody></table>

### Program Media

<table><thead><tr><th width="277">Capability</th><th width="152">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List program media</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get program media</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create program media</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update program media</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete program media</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Publish program media</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Unpublish program media</td><td>❌</td><td>✅</td><td>❌</td></tr></tbody></table>

### Program Terms

<table><thead><tr><th width="277">Capability</th><th width="152">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List all terms</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get terms</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create terms</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update terms</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete terms</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Publish terms</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Unpublish terms</td><td>❌</td><td>✅</td><td>❌</td></tr></tbody></table>

### Program Terms Variants

<table><thead><tr><th width="277">Capability</th><th width="152">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List all terms</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get terms</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create terms</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update terms</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete terms</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Publish terms</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Unpublish terms</td><td>❌</td><td>✅</td><td>❌</td></tr></tbody></table>

### Program Templates

<table><thead><tr><th width="277">Capability</th><th width="152">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List program template </td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get program template </td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create program template </td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update program template </td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete program template </td><td>❌</td><td>✅</td><td>❌</td></tr></tbody></table>

### Program Webhooks

<table><thead><tr><th width="277">Capability</th><th width="152">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List program webhook</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get program webhook</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create program webhook</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update program webhook</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete program webhook</td><td>❌</td><td>✅</td><td>❌</td></tr></tbody></table>
