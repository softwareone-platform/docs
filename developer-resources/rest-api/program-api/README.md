---
description: Manage programs, certificates, and enrollments with the Program API.
---

# Program API

The **Program API** provides secure endpoints for creating, retrieving, updating, and managing programs, certificates, and enrollments within the Marketplace Platform.

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

## Before you start

Review the shared API docs before you work with program resources.

* [Authentication](../)
* [URL structure](../../api-usage-and-reference/url-structure.md)
* [Error handling](../../api-usage-and-reference/errors-handling.md)

## Core resources

The Program API is built around the following core resources:

* **Certificate** – Issued to a client or partner as confirmation that they meet a specific program's requirements.
* **Enrollment** – Process through which a client formally registers or signs up to participate in a vendor program.
* **Program** – Represents a set of requirements (parameters) that vendors ask their clients to meet.

## Browse collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.

Use the following links to jump to the collection you need:

* [Certificate](./#certificate)
* [Enrollment](./#enrollment)
* [Program](./#program)
* [Program Parameter](./#program-parameter)
* [Program Parameter Group](./#program-parameter-group)
* [Program Document](./#program-document)
* [Program Media](./#program-media)
* [Program Terms](./#program-terms)
* [Program Terms Variant](./#program-terms-variant)
* [Program Template](./#program-template)

### Certificate

<details>

<summary>View Certificate operations</summary>

<table><thead><tr><th width="222">Operation</th><th width="113">Method</th><th>Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="certificate/create-certificate.md">Create certificate</a></td><td>POST</td><td>Migrates a certificate.</td><td>ops</td></tr><tr><td><a href="certificate/list-certificates.md">List certificates</a></td><td>GET</td><td>Returns a list of all certificates.</td><td>vendor, client, ops</td></tr><tr><td><a href="certificate/get-certificate.md">Get certificate by id</a></td><td>GET</td><td>Returns a certificate with the given id.</td><td>vendor, client, ops</td></tr><tr><td><a href="certificate/update-certificate.md">Update certificate</a></td><td>PUT</td><td>Updates an existing certificate.</td><td>vendor, client, ops</td></tr><tr><td><a href="certificate/terminate-certificate.md">Terminate certificate</a></td><td>POST</td><td>Terminates an active certificate.</td><td>vendor</td></tr><tr><td>Expire certificate</td><td>POST</td><td>Expires an active certificate.</td><td>vendor</td></tr><tr><td>Get certificate template</td><td>GET</td><td>Gets a template for a certificate.</td><td>vendor, client, ops</td></tr></tbody></table>

</details>

### Enrollment

<details>

<summary>View Enrollment operations</summary>

<table><thead><tr><th width="227">Operation</th><th width="133">Method</th><th width="235">Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="enrollment/create-enrollment.md">Create enrollment</a></td><td>POST</td><td>Creates a new enrollment and certificate.</td><td>client</td></tr><tr><td><a href="enrollment/validate-draft-enrollment.md">Validate draft enrollment</a></td><td>POST</td><td>Validates draft enrollment data.</td><td>client</td></tr><tr><td><a href="enrollment/validate-querying-enrollment.md">Validate enrollment</a></td><td>POST</td><td>Validates enrollment state.</td><td>vendor, client</td></tr><tr><td><a href="enrollment/process-enrollment.md">Process enrollment</a></td><td>POST</td><td>Changes enrollment status to processing.</td><td>vendor, client</td></tr><tr><td><a href="enrollment/query-enrollment.md">Query enrollment</a></td><td>POST</td><td>Changes enrollment status to querying.</td><td>vendor</td></tr><tr><td><a href="enrollment/complete-enrollment.md">Complete enrollment</a></td><td>POST</td><td>Changes enrollment status to complete.</td><td>vendor</td></tr><tr><td><a href="enrollment/fail-enrollment.md">Fail enrollment</a></td><td>POST</td><td>Changes enrollment status to failed.</td><td>vendor</td></tr><tr><td>Assign enrollment</td><td>POST</td><td>Assigns a user to an enrollment.</td><td>vendor</td></tr><tr><td><a href="enrollment/list-enrollments.md">List enrollments</a></td><td>GET</td><td>Lists enrollments visible to the user.</td><td>vendor, client, ops</td></tr><tr><td><a href="enrollment/get-enrollment.md">Get enrollment by id</a></td><td>GET</td><td>Gets an enrollment by id.</td><td>vendor, client, ops</td></tr><tr><td>Update enrollment</td><td>PUT</td><td>Updates some properties of an enrollment.</td><td>vendor, client, ops</td></tr><tr><td>Delete enrollment</td><td>DELETE</td><td>Deletes an enrollment.</td><td>client</td></tr><tr><td><a href="enrollment/render-enrollment-template.md">Render enrollment template</a></td><td>GET</td><td>Renders the template for the given enrollment id.</td><td>vendor, client, ops</td></tr><tr><td><a href="enrollment/enrollment-attachment/list-enrollment-attachments.md">List enrollment attachments</a></td><td>GET</td><td>Gets a list of enrollment attachments.</td><td>ops, client</td></tr><tr><td><a href="enrollment/enrollment-attachment/get-enrollment-attachment.md">Get enrollment attachment by id</a></td><td>GET</td><td>Gets an enrollment attachment by id.</td><td>ops, client</td></tr><tr><td><a href="enrollment/enrollment-attachment/create-enrollment-attachment.md">Create enrollment attachment</a></td><td>POST</td><td>Creates a new enrollment attachment.</td><td>ops, client</td></tr><tr><td><a href="enrollment/enrollment-attachment/update-enrollment-attachment.md">Update enrollment attachment</a></td><td>PUT</td><td>Updates an existing enrollment attachment.</td><td>ops, client</td></tr><tr><td><a href="enrollment/enrollment-attachment/delete-enrollment-attachment.md">Delete enrollment attachment</a></td><td>DELETE</td><td>Deletes an existing enrollment attachment.</td><td>ops, client</td></tr></tbody></table>

</details>

### Program

<details>

<summary>View Program operations</summary>

<table><thead><tr><th width="226">Operation</th><th width="124">Method</th><th width="203">Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="program/create-program.md">Create program</a></td><td>POST</td><td>Creates a new program.</td><td>vendor</td></tr><tr><td><a href="program/list-programs.md">List programs</a></td><td>GET</td><td>Fetches a list of programs.</td><td>vendor, client, ops</td></tr><tr><td><a href="program/get-program.md">Get program by id</a></td><td>GET</td><td>Gets a program by id.</td><td>vendor, client, ops</td></tr><tr><td><a href="program/update-program.md">Update program</a></td><td>PUT</td><td>Updates some properties of a program.</td><td>vendor</td></tr><tr><td><a href="program/delete-program.md">Delete program</a></td><td>DELETE</td><td>Deletes a program.</td><td>vendor</td></tr><tr><td><a href="program/publish-program.md">Publish program</a></td><td>POST</td><td>Publishes a program.</td><td>vendor</td></tr><tr><td><a href="program/unpublish-program.md">Unpublish program</a></td><td>POST</td><td>Unpublishes a program.</td><td>vendor</td></tr><tr><td><a href="program/update-program-settings.md">Update program settings</a></td><td>PUT</td><td>Updates a program’s settings.</td><td>vendor</td></tr></tbody></table>

</details>

### Program Parameter

<details>

<summary>View Program Parameter operations</summary>

<table><thead><tr><th width="211">Operation</th><th width="119">Method</th><th>Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="program/program-parameters/create-parameter.md">Create parameter</a></td><td>POST</td><td>Creates a program parameter.</td><td>vendor</td></tr><tr><td><a href="program/program-parameters/list-program-parameters.md">List parameters</a></td><td>GET</td><td>Gets a list of parameters for a program.</td><td>vendor, client, ops</td></tr><tr><td><a href="program/program-parameters/get-program-parameter.md">Get parameter by id</a></td><td>GET</td><td>Gets a program parameter definition.</td><td>vendor, client, ops</td></tr><tr><td><a href="program/program-parameters/update-program-parameter.md">Update parameter</a></td><td>PUT</td><td>Updates a program parameter definition.</td><td>vendor</td></tr><tr><td><a href="program/program-parameters/delete-program-parameter.md">Delete parameter</a></td><td>DELETE</td><td>Deletes a program parameter definition.</td><td>vendor</td></tr></tbody></table>

</details>

### Program Parameter Group

<details>

<summary>View Program Parameter Group operations</summary>

<table><thead><tr><th width="230">Operation</th><th width="102">Method</th><th width="227">Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="../catalog-api/parameter-group/create-parameter-group.md">Create parameter group</a></td><td>POST</td><td>Creates a new parameter group for a program.</td><td>vendor</td></tr><tr><td><a href="../catalog-api/parameter-group/list-parameter-groups.md">List parameter groups</a></td><td>GET</td><td>Lists all parameter groups for a program based on filter criteria.</td><td>vendor, client, ops</td></tr><tr><td><a href="program/program-parameter-groups/get-parameter-group.md">Get parameter group by id</a></td><td>GET</td><td>Gets a parameter group by id for a program.</td><td>vendor, client, ops</td></tr><tr><td><a href="program/program-parameter-groups/update-parameter-group.md">Update parameter group</a></td><td>PUT</td><td>Updates a parameter group for a program.</td><td>vendor</td></tr><tr><td><a href="program/program-parameter-groups/delete-parameter-group.md">Delete parameter group</a></td><td>DELETE</td><td>Deletes a parameter group from a program.</td><td>vendor</td></tr></tbody></table>

</details>

### Program Document

<details>

<summary>View Program Document operations</summary>

<table><thead><tr><th width="211">Operation</th><th width="125">Method</th><th>Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="program/program-documents/create-document.md">Create document</a></td><td>POST</td><td>Creates a new document.</td><td>vendor</td></tr><tr><td><a href="program/program-documents/list-documents.md">List documents</a></td><td>GET</td><td>Lists all documents based on filter criteria.</td><td>vendor, client, ops</td></tr><tr><td><a href="program/program-documents/get-document.md">Get document by id</a></td><td>GET</td><td>Gets a document by id.</td><td>vendor, client, ops</td></tr><tr><td><a href="program/program-documents/update-document.md">Update document</a></td><td>PUT</td><td>Updates a document.</td><td>vendor</td></tr><tr><td><a href="program/program-documents/delete-document.md">Delete document</a></td><td>DELETE</td><td>Removes a document.</td><td>vendor</td></tr><tr><td><a href="program/program-documents/publish-document.md">Publish document</a></td><td>POST</td><td>Publishes a document.</td><td>vendor</td></tr><tr><td><a href="program/program-documents/unpublish-document.md">Unpublish document</a></td><td>POST</td><td>Unpublishes a document.</td><td>vendor</td></tr></tbody></table>

</details>

### Program Media

<details>

<summary>View Program Media operations</summary>

<table><thead><tr><th width="224">Operation</th><th width="122">Method</th><th>Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="program/program-media/create-media.md">Create program media</a></td><td>POST</td><td>Creates new media for a program.</td><td>vendor</td></tr><tr><td><a href="program/program-media/list-media.md">List program media</a></td><td>GET</td><td>Gets a list of media for a program.</td><td>vendor, client, ops</td></tr><tr><td><a href="program/program-media/get-media.md">Get program media by id</a></td><td>GET</td><td>Gets an item of media for a program.</td><td>vendor, client, ops</td></tr><tr><td><a href="program/program-media/update-media.md">Update program media</a></td><td>PUT</td><td>Updates an item of media for a program.</td><td>vendor</td></tr><tr><td><a href="program/program-media/publish-media.md">Publish program media</a></td><td>POST</td><td>Publishes an item of media for a program.</td><td>vendor</td></tr><tr><td><a href="program/program-media/unpublish-media.md">Unpublish program media</a></td><td>POST</td><td>Unpublishes an item of media for a program.</td><td>vendor</td></tr><tr><td><a href="program/program-media/delete-media.md">Delete program media</a></td><td>DELETE</td><td>Deletes an item of media for a program.</td><td>vendor</td></tr></tbody></table>

</details>

### Program Terms

<details>

<summary>View Program Terms operations</summary>

<table><thead><tr><th width="192">Operation</th><th width="143">Method</th><th>Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="program/program-terms/create-terms.md">Create terms</a></td><td>POST</td><td>Creates terms for a program.</td><td>vendor</td></tr><tr><td><a href="program/program-terms/list-terms.md">List terms</a></td><td>GET</td><td>Gets a list of all terms for a program.</td><td>vendor, client, ops</td></tr><tr><td><a href="program/program-terms/get-terms.md">Get terms by id</a></td><td>GET</td><td>Gets terms for a program by id.</td><td>vendor, client, ops</td></tr><tr><td><a href="program/program-terms/update-terms.md">Update terms</a></td><td>PUT</td><td>Updates terms for a program.</td><td>vendor</td></tr><tr><td><a href="program/program-terms/delete-terms.md">Delete terms</a></td><td>DELETE</td><td>Deletes terms for a program.</td><td>vendor</td></tr><tr><td><a href="program/program-terms/publish-terms.md">Publish terms</a></td><td>POST</td><td>Publishes terms for a program.</td><td>vendor</td></tr><tr><td><a href="program/program-terms/unpublish-terms.md">Unpublish terms</a></td><td>POST</td><td>Unpublishes terms for a program.</td><td>vendor</td></tr></tbody></table>

</details>

### Program Terms Variant

<details>

<summary>View Program Terms Variant operations</summary>

<table><thead><tr><th width="191">Operation</th><th width="137">Method</th><th>Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="program/program-terms-variants/create-variant.md">Create variant</a></td><td>POST</td><td>Creates a variant for terms.</td><td>vendor</td></tr><tr><td><a href="program/program-terms-variants/list-variants.md">List variants</a></td><td>GET</td><td>Gets a list of all variants for terms.</td><td>vendor, client, ops</td></tr><tr><td><a href="program/program-terms-variants/get-variant-for-terms.md">Get variant by id</a></td><td>GET</td><td>Gets a variant for terms by id.</td><td>vendor, client, ops</td></tr><tr><td><a href="program/program-terms-variants/update-variant.md">Update variant</a></td><td>PUT</td><td>Updates a variant for terms for a program.</td><td>vendor</td></tr><tr><td><a href="program/program-terms-variants/delete-variant.md">Delete variant</a></td><td>DELETE</td><td>Deletes a variant for terms.</td><td>vendor</td></tr><tr><td><a href="program/program-terms-variants/publish-variant.md">Publish variant</a></td><td>POST</td><td>Publishes a variant for terms.</td><td>vendor</td></tr><tr><td><a href="program/program-terms-variants/unpublish-variant.md">Unpublish variant</a></td><td>POST</td><td>Unpublishes a variant for terms.</td><td>vendor</td></tr></tbody></table>

</details>

### Program Template

<details>

<summary>View Program Template operations</summary>

<table><thead><tr><th width="185">Operation</th><th width="143">Method</th><th>Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="program/program-templates/create-program-template.md">Create program template</a></td><td>POST</td><td>Creates a template for a program.</td><td>vendor</td></tr><tr><td><a href="program/program-templates/list-program-templates.md">List program templates</a></td><td>GET</td><td>Gets a list of templates for a program.</td><td>vendor, client, ops</td></tr><tr><td><a href="program/program-templates/get-program-template.md">Get program template by id</a></td><td>GET</td><td>Gets a template for a program.</td><td>vendor, client, ops</td></tr><tr><td><a href="program/program-templates/update-program-template.md">Update program template</a></td><td>PUT</td><td>Updates a template for a program.</td><td>vendor</td></tr><tr><td><a href="program/program-templates/delete-program-template.md">Delete program template</a></td><td>DELETE</td><td>Deletes a template for a program.</td><td>vendor</td></tr></tbody></table>

</details>
