# Extensions API

The **Extensions API** is a REST API used by the Marketplace Platform to manage extensions and everything around them. It lets you:

* Create, read, update, delete, review, publish and unpublish extensions.
* Create and maintain categories, then link extensions to them.
* Manage the documentation for the extension, including publish/unpublish documentation.
* Upload and manage images and videos.
* Manage terms and conditions and their variants.
* Track installations.

## Core Concepts

The Extensions API is built around the following core resources:

* **Category** - Enables the operator to add, view, or delete the `category` object.
* **Document** - Allows uploading supplementary documentation to an extension, either via a file upload or an online link.
* **Extension** - Represents a set of requirements (parameters) that vendors ask their clients to meet.&#x20;
* **Media** - Allows vendors to add, view, and delete `media` associated with an extension.
* **Terms** - Represents a collection of documents associated with an extension, including uploaded PDF or DOCX files or links to externally hosted documents.
* **Variant** - Represents a specific version of terms for an extension, provided as an uploaded PDF or DOCX file or a link to an externally hosted document.
* **Instance** - Represents a running instance in the database, such as a Kubernetes pod, with its current status, for example, running.
* **Installation** - Allows an operator to add, view, and delete installations.
* **Invitation** - Allows a vendor to create and send an `invitation`.

## Collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.&#x20;

Refer to the following capability matrix to see which roles are authorized to perform specific operations within each collection:

### Extension

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List all extensions</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get extension</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create extension</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update extension by ID</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Delete extension</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Publish extension</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Unpublish extension</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### Categories

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List categories</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get category</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create category</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Update category</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Delete category</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Activate category</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Deactivate category</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>

### Documents

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List documents</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get document</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create document</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update document</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete document</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Publish document</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Unpublish document</td><td>❌</td><td>✅</td><td>❌</td></tr></tbody></table>

### Media

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List extension media</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get extension media</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create extension media</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update media for an extension</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete media for an extension</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Publish media for an extension</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Unpublish media for an extension</td><td>❌</td><td>✅</td><td>❌</td></tr></tbody></table>

### Installation

<table><thead><tr><th width="284">Capability</th><th>Client</th><th>Vendor</th><th>Operation</th></tr></thead><tbody><tr><td>Create installation or invitation</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Update installation</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>List installation</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get installation</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Delete installation</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Get a list of installations</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get an item of installation</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Redeem invitation</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>

### Instance

<table><thead><tr><th width="284">Capability</th><th>Client</th><th>Vendor</th><th>Operation</th></tr></thead><tbody><tr><td>Create extension instance</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>List extension instance</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Get extension instance</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### Terms

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List terms</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get terms</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create terms</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update terms</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete terms</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Mark terms for review</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Publish terms</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Unpublish terms</td><td>❌</td><td>✅</td><td>❌</td></tr></tbody></table>

### Variant

<table><thead><tr><th width="328">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List all variants for terms</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get variant for terms</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create variant</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Update variant</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Delete variant</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Mark variant for review</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Publish variant</td><td>❌</td><td>✅</td><td>❌</td></tr><tr><td>Unpublish variant</td><td>❌</td><td>✅</td><td>❌</td></tr></tbody></table>
