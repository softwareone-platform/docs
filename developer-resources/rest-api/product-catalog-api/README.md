# Product Catalog API

The Public Catalog API provides access to the SoftwareOne Marketplace product catalog.&#x20;

It exposes software product listings, vendor profiles, and classification data (categories, industries, and segments) through a RESTful interface, allowing you to:&#x20;

* Browse the full range of software products, vendors, and categories available on the SoftwareOne Marketplace.
* Create and manage vendor profiles.
* Create and manage product profiles.
* Publish and unpublish catalog entries.
* Manage categories, industries, and segments used to organize the catalog.

Access to this API is role-based. Clients can view published items, vendors can manage their own vendor and product profiles, and SoftwareOne Operations has full access to all entities and states.

## Before you start

Review the shared API docs before you work with public catalog resources.

* [Authentication](../)
* [URL structure](../../api-usage-and-reference/url-structure.md)
* [Error handling](../../api-usage-and-reference/errors-handling.md)

## Core resources

The Program API is built around the following core resources:

* **Vendor profile** – Represents a `vendor` in the public catalog.
* **Product profile** – Represents a `product` in the public catalog.
* **Category** – Represents a software category or sub-category, used to classify software in the public catalog.
* **Industry** – Represents specific business sectors or markets that products are designed to serve.&#x20;
* **Segment** – Categorizes `products` based on the size and type of organizations for which they are most suitable.&#x20;

## Browse collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.&#x20;

Use the following links to jump to the collection you need:

* [Vendor Profile](./#vendor-profile)
* [Product Profile](./#product-profile)
* [Category](./#category)
* [Industry](./#industry)
* [Segment](./#segment)

### Vendor Profile

<details>

<summary>View Vendor Profile operations</summary>

| Operation                                                              | Method | Description                                    | Access                      |
| ---------------------------------------------------------------------- | ------ | ---------------------------------------------- | --------------------------- |
| [Create vendor profile](vendor-profile/create-vendor-profile.md)       | POST   | Creates a new vendor profile in draft.         | ops                         |
| [List vendor profiles](vendor-profile/list-vendor-profiles.md)         | GET    | Gets vendor profiles collection.               | public, vendor, client, ops |
| [Get vendor profile by id](vendor-profile/get-vendor-profile.md)       | GET    | Gets vendor profile details.                   | public, vendor, client, ops |
| [Publish vendor profile](vendor-profile/publish-vendor-profile.md)     | POST   | Modifies vendor profile status to published.   | vendor, ops                 |
| [Unpublish vendor profile](vendor-profile/unpublish-vendor-profile.md) | POST   | Modifies vendor profile status to unpublished. | vendor, ops                 |
| [Update vendor profile](vendor-profile/update-vendor-profile.md)       | PUT    | Modifies an existing vendor profile.           | vendor, ops                 |
| [Delete vendor profile](vendor-profile/delete-vendor-profile.md)       | DELETE | Modifies vendor profile status to deleted.     | ops                         |

</details>

### Product Profile

<details>

<summary>View Product Profile operations</summary>

| Operation                                                                 | Method | Description                                     | Access                      |
| ------------------------------------------------------------------------- | ------ | ----------------------------------------------- | --------------------------- |
| [Create product profile](product-profile/create-product-profile.md)       | POST   | Creates a new product profile in draft status.  | ops                         |
| [List product profiles](product-profile/list-product-profiles.md)         | GET    | Gets product profiles collection.               | public, vendor, client, ops |
| [Get product profile by id](product-profile/get-product-profile.md)       | GET    | Gets product profile details.                   | public, vendor, client, ops |
| [Publish product profile](product-profile/publish-product-profile.md)     | POST   | Modifies product profile status to published.   | vendor, ops                 |
| [Unpublish product profile](product-profile/unpublish-product-profile.md) | POST   | Modifies product profile status to unpublished. | vendor, ops                 |
| [Update product profile](product-profile/update-product-profile.md)       | PUT    | Modifies an existing product profile.           | vendor, ops                 |
| [Delete product profile](product-profile/delete-product-profile.md)       | DELETE | Modifies product profile status to deleted.     | ops                         |

</details>

### Category

<details>

<summary>View Category operations</summary>

| Operation                                            | Method | Description                                                                              | Access                      |
| ---------------------------------------------------- | ------ | ---------------------------------------------------------------------------------------- | --------------------------- |
| [Create category](category/create-category.md)       | POST   | Creates a new category.                                                                  | ops                         |
| [List categories](category/list-categories.md)       | GET    | Gets list of categories.                                                                 | public, vendor, client, ops |
| [Get category by id](category/get-category.md)       | GET    | Gets category details.                                                                   | public, vendor, client, ops |
| [Publish category](category/publish-category.md)     | POST   | Publishes a category and updates it from draft to published (active).                    | ops                         |
| [Unpublish category](category/unpublish-category.md) | POST   | Unpublishes a category and updates it from published (active) to unpublished (disabled). | ops                         |
| [Update category](category/update-category.md)       | PUT    | Modifies a category.                                                                     | ops                         |
| [Delete category](category/delete-category.md)       | DELETE | Modifies the status of a category to deleted.                                            | ops                         |

</details>

### Industry

<details>

<summary>View Industry operations</summary>

| Operation                                            | Method | Description                                                                               | Access                      |
| ---------------------------------------------------- | ------ | ----------------------------------------------------------------------------------------- | --------------------------- |
| [Create industry](industry/create-industry.md)       | POST   | Creates a new industry.                                                                   | ops                         |
| [List industries](industry/list-industries.md)       | GET    | Gets a list of industries.                                                                | public, vendor, client, ops |
| [Get industry by id](industry/get-industry.md)       | GET    | Gets specific industry details.                                                           | public, vendor, client, ops |
| [Publish industry](industry/publish-industry.md)     | POST   | Publishes an industry and updates it from draft to published (active).                    | ops                         |
| [Unpublish industry](industry/unpublish-industry.md) | POST   | Unpublishes an industry and updates it from published (active) to unpublished (disabled). | ops                         |
| [Modify industry](industry/modify-industry.md)       | PUT    | Modifies an industry.                                                                     | ops                         |
| [Delete industry](industry/delete-industry.md)       | DELETE | Deletes an industry.                                                                      | ops                         |

</details>

### Segment

<details>

<summary>View Segment operations</summary>

| Operation                                         | Method | Description                                                                             | Access                      |
| ------------------------------------------------- | ------ | --------------------------------------------------------------------------------------- | --------------------------- |
| [Create segment](segment/create-segment.md)       | POST   | Creates a new segment.                                                                  | ops                         |
| [List segments](segment/list-segments.md)         | GET    | Gets a list of segments.                                                                | public, vendor, client, ops |
| [Get segment by id](segment/get-segment.md)       | GET    | Gets specific segment details.                                                          | public, vendor, client, ops |
| [Publish segment](segment/publish-segment.md)     | POST   | Publishes a segment and updates it from draft to published (active).                    | ops                         |
| [Unpublish segment](segment/unpublish-segment.md) | POST   | Unpublishes a segment and updates it from published (active) to unpublished (disabled). | ops                         |
| [Update segment](segment/update-segment.md)       | PUT    | Modifies a segment.                                                                     | ops                         |
| [Delete segment](segment/delete-segment.md)       | DELETE | Deletes a segment.                                                                      | ops                         |

</details>
