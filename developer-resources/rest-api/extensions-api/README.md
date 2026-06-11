# Extensions API

The **Extensions API** is a REST API used by the Marketplace Platform to manage extensions and everything around them. It lets you:

* Create, read, update, delete, review, publish and unpublish extensions.
* Create and maintain categories, then link extensions to them.
* Manage the documentation for the extension, including publish/unpublish documentation.
* Upload and manage images and videos.
* Manage terms and conditions and their variants.
* Track installations.

## Before you start

Review the shared API docs before you work with audit resources.

* [Authentication](../#authentication)
* [URL structure](../../api-usage-and-reference/url-structure.md)
* [Error handling](../../api-usage-and-reference/errors-handling.md)

## Core resources

The Extensions API is built around the following core resources:

* **Category** – Enables the operator to add, view, or delete the `category` object.
* **Document** – Allows uploading supplementary documentation to an extension, either via a file upload or an online link.
* **Extension** – Represents a set of requirements (parameters) that vendors ask their clients to meet.&#x20;
* **Media** – Allows vendors to add, view, and delete `media` associated with an extension.
* **Terms** – Represents a collection of documents associated with an extension, including uploaded PDF or DOCX files or links to externally hosted documents.
* **Variant** – Represents a specific version of terms for an extension, provided as an uploaded PDF or DOCX file or a link to an externally hosted document.
* **Instance** – Represents a running instance in the database, such as a Kubernetes pod, with its current status, for example, running.
* **Installation** – Allows an operator to add, view, and delete installations.
* **Invitation** – Allows a vendor to create and send an `invitation`.

## Browse collections <a href="#browse-collections" id="browse-collections"></a>

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.&#x20;

Use the following links to jump to the collection you need:

* [Extension](./#extension)
* [Categories](./#categories)
* [Documents](./#document)
* [Media](./#media)
* [Installation](./#installation)
* [Instance](./#instance)
* [Terms](./#terms)
* [Variants](./#variants)

### Extension

<details>

<summary>View Extension operations</summary>

<table><thead><tr><th width="216">Operation</th><th width="115">Method</th><th width="221">Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="extension/create-extension.md">Create extension</a></td><td>POST</td><td>Creates a new extension.</td><td>vendor</td></tr><tr><td><a href="extension/list-extensions.md">List extensions</a></td><td>GET</td><td>Fetches a list of extensions.</td><td>vendor, client, ops</td></tr><tr><td><a href="extension/get-extension.md">Get extension by id</a></td><td>GET</td><td>Gets an extension by id.</td><td>vendor, client, ops</td></tr><tr><td><a href="extension/update-extension.md">Update extension</a></td><td>PUT</td><td>Updates some properties of an extension.</td><td>vendor, ops</td></tr><tr><td><a href="extension/delete-extension.md">Delete extension</a></td><td>DELETE</td><td>Deletes an extension.</td><td>vendor, ops</td></tr><tr><td><a href="extension/publish-extension.md">Publish extension</a></td><td>POST</td><td>Publishes an extension.</td><td>ops</td></tr><tr><td><a href="extension/unpublish-extension.md">Unpublish extension</a></td><td>POST</td><td>Unpublishes an extension.</td><td>vendor, ops</td></tr></tbody></table>

</details>

### Categories

<details>

<summary>View Category operations</summary>

<table><thead><tr><th width="214">Operation</th><th width="122">Method</th><th width="226">Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="category/create-category.md">Create category</a></td><td>POST</td><td>Creates a new category.</td><td>ops</td></tr><tr><td><a href="category/get-categories.md">Get categories</a></td><td>GET</td><td>Fetches a list of categories.</td><td>vendor, client, ops</td></tr><tr><td><a href="category/get-category.md">Get category by id</a></td><td>GET</td><td>Gets a category by id.</td><td>vendor, client, ops</td></tr><tr><td><a href="category/update-category.md">Update category</a></td><td>PUT</td><td>Updates some properties of a category.</td><td>ops</td></tr><tr><td><a href="category/activate-category.md">Activate category</a></td><td>POST</td><td>Activates a category.</td><td>ops</td></tr><tr><td><a href="category/deactivate-category.md">Deactivate category</a></td><td>POST</td><td>Deactivates a category.</td><td>ops</td></tr></tbody></table>

</details>

### Documents

<details>

<summary>View Document operations</summary>

| Operation                                                          | Method | Description                                     | Access              |
| ------------------------------------------------------------------ | ------ | ----------------------------------------------- | ------------------- |
| [Create document](../catalog-api/documentation/create-document.md) | POST   | Creates a new document in extension management. | vendor              |
| [List documents](../catalog-api/documentation/list-documents.md)   | GET    | Lists all documents based on filter criteria.   | vendor, client, ops |
| [Get document by id](document/get-document.md)                     | GET    | Gets a document by id.                          | vendor, client, ops |
| [Update document](document/update-document.md)                     | PUT    | Updates a document.                             | vendor              |
| [Delete document](document/delete-document.md)                     | DELETE | Deletes a document.                             | vendor              |
| [Publish document](document/publish-document.md)                   | POST   | Publishes a document.                           | vendor              |
| [Unpublish document](document/unpublish-document.md)               | POST   | Unpublishes a document.                         | vendor              |

</details>

### Media

<details>

<summary>View Media operations</summary>

<table><thead><tr><th width="197">Operation</th><th width="135">Method</th><th width="262">Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="media/create-extension-media.md">Create media</a></td><td>POST</td><td>Creates new media for an extension.</td><td>vendor</td></tr><tr><td><a href="media/list-extension-media.md">List media</a></td><td>GET</td><td>Gets a list of media for an extension.</td><td>vendor, client, ops</td></tr><tr><td><a href="media/get-extension-media.md">Get media by id</a></td><td>GET</td><td>Gets an item of media for an extension.</td><td>vendor, client, ops</td></tr><tr><td><a href="media/update-media-for-extension.md">Update media</a></td><td>PUT</td><td>Updates an item of media for an extension.</td><td>vendor</td></tr><tr><td><a href="media/publish-media-for-extension.md">Publish media</a></td><td>POST</td><td>Publishes an item of media for an extension.</td><td>vendor</td></tr><tr><td><a href="media/unpublish-media-for-extension.md">Unpublish media</a></td><td>POST</td><td>Unpublishes an item of media for an extension.</td><td>vendor</td></tr><tr><td><a href="media/delete-media-for-extension.md">Delete media</a></td><td>DELETE</td><td>Deletes an item of media for an extension.</td><td>vendor</td></tr></tbody></table>

</details>

### Installation

<details>

<summary>View Installation operations</summary>

<table><thead><tr><th width="223">Operation</th><th width="124">Method</th><th width="209">Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="installation/create-installation-or-invitation.md">Create installation or invitation</a></td><td>POST</td><td>Creates a new installation or invitation.</td><td>vendor, client, ops</td></tr><tr><td><a href="installation/update-installation.md">Update installation</a></td><td>PUT</td><td>Updates the configuration of an installation.</td><td>vendor-owner</td></tr><tr><td><a href="installation/list-installation.md">List installations</a></td><td>GET</td><td>Gets a list of installations.</td><td>vendor, client, ops</td></tr><tr><td><a href="installation/get-installation.md">Get installation by id</a></td><td>GET</td><td>Gets an installation by id.</td><td>vendor, client, ops</td></tr><tr><td><a href="installation/delete-installation.md">Delete installation</a></td><td>DELETE</td><td>Deletes an installation.</td><td>vendor, ops</td></tr><tr><td><a href="installation/list-installation.md">List installations for extension</a></td><td>GET</td><td>Gets a list of installations for an extension.</td><td>vendor, client, ops</td></tr><tr><td><a href="installation/get-installation.md">Get installation for extension by id</a></td><td>GET</td><td>Gets an installation for an extension by id.</td><td>vendor, client, ops</td></tr><tr><td><a href="installation/redeem-invitation.md">Redeem invitation</a></td><td>POST</td><td>Creates a redeemed invitation.</td><td>client, vendor, ops</td></tr></tbody></table>

</details>

### Instance

<details>

<summary>View Instance operations</summary>

| Operation                                                          | Method | Description                                | Access       |
| ------------------------------------------------------------------ | ------ | ------------------------------------------ | ------------ |
| [Create extension instance](instance/create-extension-instance.md) | POST   | Creates an instance for an extension.      | vendor-owner |
| [List extension instances](instance/list-extension-instance.md)    | GET    | Gets a list of instances for an extension. | vendor, ops  |
| [Get extension instance by id](instance/get-extension-instance.md) | GET    | Gets an instance for an extension by id.   | vendor, ops  |

</details>

### Terms

<details>

<summary>View Terms operations</summary>

| Operation                                   | Method | Description                                | Access              |
| ------------------------------------------- | ------ | ------------------------------------------ | ------------------- |
| [Create terms](terms/create-terms.md)       | POST   | Creates terms for an extension.            | vendor              |
| [List terms](terms/list-terms.md)           | GET    | Gets a list of all terms for an extension. | vendor, client, ops |
| [Get terms by id](terms/get-terms.md)       | GET    | Gets terms for an extension by id.         | vendor, client, ops |
| [Update terms](terms/update-terms.md)       | PUT    | Updates terms for an extension.            | vendor              |
| [Delete terms](terms/delete-terms.md)       | DELETE | Deletes terms for an extension.            | vendor              |
| Mark terms for review                       | POST   | Marks terms for an extension for review.   | vendor              |
| [Publish terms](terms/publish-terms.md)     | POST   | Publishes terms for an extension.          | vendor              |
| [Unpublish terms](terms/unpublish-terms.md) | POST   | Unpublishes terms for an extension.        | vendor              |

</details>

### Variants

<details>

<summary>View Variantd operations</summary>

| Operation                                         | Method | Description                                   | Access              |
| ------------------------------------------------- | ------ | --------------------------------------------- | ------------------- |
| [Create variant](variant/create-variant.md)       | POST   | Creates a variant for terms.                  | vendor              |
| [List variants](variant/list-variants.md)         | GET    | Gets a list of all variants for terms.        | vendor, client, ops |
| [Get variant by id](variant/get-variant.md)       | GET    | Gets a variant for terms by id.               | vendor, client, ops |
| [Update variant](variant/update-variant.md)       | PUT    | Updates a variant for terms for an extension. | vendor              |
| [Delete variant](variant/delete-variant.md)       | DELETE | Deletes a variant for terms.                  | vendor              |
| Mark variant for review                           | POST   | Marks a variant for terms for review.         | vendor              |
| [Publish variant](variant/publish-variant.md)     | POST   | Publishes a variant for terms.                | vendor              |
| [Unpublish variant](variant/unpublish-variant.md) | POST   | Unpublishes a variant for terms.              | vendor              |

</details>
