---
hidden: true
---

# Product and Vendor Profiles API

The **Product and Vendor Profiles API** allows you to manage vendor and product profiles within the SoftwareOne Marketplace platform.

It allows you to programmatically:

* Create and manage vendor profiles.
* Create and manage product profiles.
* Publish and unpublish catalog entries.
* Manage categories, industries, and segments used to organize the catalog.

Access to this API is role-based. Clients can view published items only, vendors can manage their own vendor and product profiles, and SoftwareOne Operations have full access to all entities and states.

## Core Concepts

The Program API is built around the following core resources:

* **Vendor profile** - Represents a `vendor` in the public catalog.
* **Product profile** - Represents a `product` in the public catalog.
* **Category** - Represents a software category or sub-category, used to classify software in the public catalog.
* **Industry** - Represents specific business sectors or markets that products are designed to serve.&#x20;
* **Segment** - Categorizes `products` based on the size and type of organizations for which they are most suitable.&#x20;

## Collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.&#x20;

Refer to the following capability matrix to see which roles are authorized to perform specific operations within each collection:

### Vendor Profile

<table><thead><tr><th width="231">Capability</th><th width="132">Public</th><th width="120">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List vendor profiles</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get vendor profile details</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create vendor profile</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Publish vendor profile</td><td>❌</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Modify vendor profile</td><td>❌</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Delete vendor profile</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>

### Product Profile

<table><thead><tr><th width="233">Capability</th><th>Public</th><th>Client</th><th>Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List product profiles</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get product profile details</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create product profile</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Publish product profile</td><td>❌</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Unpublish product profile</td><td>❌</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Modify product profile</td><td>❌</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>Delete product profile</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>

### Categories&#x20;

<table><thead><tr><th width="215">Capability</th><th>Public</th><th>Client</th><th>Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List categories</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get a specific category</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create category</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Publish category</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Unpublish category</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Modify category</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Delete category</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>

### Industries

<table><thead><tr><th width="219">Capability</th><th>Public</th><th>Client</th><th>Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List industries</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get a specific industry</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create industry</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Publish industry</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Unpublish industry</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Modify industry</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Delete industry</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>

### Segments

<table><thead><tr><th width="221">Capability</th><th>Public</th><th>Client</th><th>Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List segments</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Get a specific segment</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create segment</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Publish segment</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Unpublish segment</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Modify segment</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>Delete segment</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr></tbody></table>
