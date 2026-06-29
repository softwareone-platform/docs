---
description: Manage your products programmatically using the Catalog API.
---

# Catalog API

The **Catalog API** enables you to create, retrieve, and manage products. You can also configure individual items and item groups through the API.

Additionally, you can define parameters and parameter groups, and manage pricing with price lists. You can also create custom templates and product variants. The API also includes endpoints for managing product media, documents, listings, and terms and conditions.

## Before you start

Review the shared API docs before you work with catalog resources.

* [Authentication](../)
* [URL structure](../../api-usage-and-reference/url-structure.md)
* [Error handling](../../api-usage-and-reference/errors-handling.md)

## Core resources

The Catalog API is built around the following core resources:

* **Authorization** – Represents the permissions and credentials that are required for interactions between sellers and vendors in the scope of a product.
* **Document** – Used to upload product documentation (via an online link or file) to the `product` object.
* **Item** – Represents the individual stock-keeping units (SKUs) or transactable element of a product. Items are shown as a line item in an order.
* **Item group** – Represents a group of items.
* **Listing** – Represents a business entity that aligns a product with a specific SoftwareOne `seller`.
* **Media** – Enables vendors to add, view, or delete media from the `product` object.
* **Product** – Represents a collection of `items` and their associated parameters organized into a unified group.
* **Parameter** – Allows vendors to define additional information that must be collected from and shared with the client, enabling the client to self-serve within the SoftwareOne Marketplace.
* **Parameter group** – Represents a group of `parameters`.
* **Pricelist** – Includes key pricing details such as sales and purchase prices, enabling vendors and operations to effectively manage and apply different price points for product items.
* **Pricing policy** – Defines client-specific markup and pricing rules based on negotiated terms and special agreements.

## Browse collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.

Use the following links to jump to the collection you need:

* [Authorization](./#authorization)
* [Documents](./#documents)
* [Items](./#items)
* [Item Groups](./#item-group)
* [Listings](./#listings)
* [Media](./#media)
* [Parameters](./#parameters)
* [Parameter Groups](./#parameter-groups)
* [Price Lists](./#price-lists)
* [Pricing Policies](./#pricing-policies)
* [Products](./#products)
* [Templates](./#templates)
* [Terms](./#terms)
* [Unit of Measure](./#unit-of-measure)
* [Variants](./#variants)

### Authorization

<details>

<summary>View Authorization operations</summary>

<table><thead><tr><th width="236">Operation</th><th width="102">Method</th><th>Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="authorization/create-authorization.md">Create authorization</a></td><td>POST</td><td>Creates a new authorization in the catalog.</td><td>ops</td></tr><tr><td><a href="authorization/list-authorizations.md">List authorizations</a></td><td>GET</td><td>Gets a list of authorizations.</td><td>vendor, client, ops</td></tr><tr><td><a href="authorization/get-authorization.md">Get authorization by id</a></td><td>GET</td><td>Retrieves an authorization by its id.</td><td>vendor, client, ops</td></tr><tr><td><a href="authorization/update-authorization.md">Update authorization</a></td><td>PUT</td><td>Updates an existing authorization.</td><td>ops</td></tr><tr><td><a href="authorization/delete-authorization.md">Delete authorization</a></td><td>DELETE</td><td>Deletes an authorization (used by vendors).</td><td>ops</td></tr></tbody></table>

</details>

### Documents

<details>

<summary>View Documents operations</summary>

| Operation                                                             | Method | Description                                   | Access              |
| --------------------------------------------------------------------- | ------ | --------------------------------------------- | ------------------- |
| [Create document](documentation/create-document.md)                   | POST   | Creates a new document in catalog management. | vendor              |
| [List documents](documentation/list-documents.md)                     | GET    | Lists all documents based on filter criteria. | vendor, client, ops |
| [Get document by id](documentation/get-document.md)                   | GET    | Gets a document by id.                        | vendor, client, ops |
| [Update document](documentation/update-document.md)                   | PUT    | Updates a document.                           | vendor, ops         |
| [Delete document](documentation/delete-document.md)                   | DELETE | Removes a document.                           | vendor, ops         |
| [Publish document](documentation/publish-document.md)                 | POST   | Publishes a document.                         | ops                 |
| [Mark document for review](documentation/mark-document-for-review.md) | POST   | Marks a document for review.                  | vendor              |
| [Unpublish document](documentation/unpublish-document.md)             | POST   | Unpublishes a document.                       | vendor, ops         |

</details>

### Items

<details>

<summary>View Items operations</summary>

| Operation                                             | Method | Description                                                   | Access              |
| ----------------------------------------------------- | ------ | ------------------------------------------------------------- | ------------------- |
| [Create item](items/create-item.md)                   | POST   | Creates a product item in the catalog.                        | vendor              |
| [List items](items/list-items.md)                     | GET    | Gets a list of items in the catalog based on filter criteria. | vendor, client, ops |
| [Get item by id](items/get-item.md)                   | GET    | Gets a product item by id.                                    | vendor, client, ops |
| [Update item](items/update-item.md)                   | PUT    | Updates a product item.                                       | vendor              |
| [Delete item](items/delete-item.md)                   | DELETE | Deletes a product item.                                       | vendor, ops         |
| [Mark item for review](items/mark-item-for-review.md) | POST   | Marks a product item as ready for review.                     | vendor              |
| [Publish item](items/publish-item.md)                 | POST   | Publishes a product item.                                     | ops                 |
| [Unpublish item](items/unpublish-item.md)             | POST   | Unpublishes a product item.                                   | vendor, ops         |
| List items by product                                 | GET    | Gets a list of items in the catalog based on filter criteria. | vendor, client, ops |
| Get item by product id                                | GET    | Gets a product item by id.                                    | vendor, client, ops |

</details>

### Item Groups

<details>

<summary>View Item Groups operations</summary>

| Operation                                            | Method | Description                                                         | Access              |
| ---------------------------------------------------- | ------ | ------------------------------------------------------------------- | ------------------- |
| [Create item group](item-group/create-item-group.md) | POST   | Creates a new item group for a given product in the catalog.        | vendor              |
| [List item groups](item-group/list-item-groups.md)   | GET    | Lists all item groups for a given product based on filter criteria. | vendor, client, ops |
| [Get item group by id](item-group/get-item-group.md) | GET    | Gets an item group by id for a given product.                       | vendor, client, ops |
| [Update item group](item-group/update-item-group.md) | PUT    | Updates an item group for a given product.                          | vendor              |
| [Delete item group](item-group/delete-item-group.md) | DELETE | Deletes an item group from a given product.                         | vendor              |

</details>

### Listings

<details>

<summary>View Listings operations</summary>

| Operation                                   | Method | Description                             | Access              |
| ------------------------------------------- | ------ | --------------------------------------- | ------------------- |
| [Create listing](listing/create-listing.md) | POST   | Creates a new listing in the catalog.   | ops                 |
| [List listings](listing/get-listings.md)    | GET    | Gets a list of listings in the catalog. | vendor, client, ops |
| [Get listing by id](listing/get-listing.md) | GET    | Gets a listing by id.                   | vendor, client, ops |
| [Update listing](listing/update-listing.md) | PUT    | Updates a listing in the catalog.       | ops                 |
| [Delete listing](listing/delete-listing.md) | DELETE | Deletes a listing.                      | ops                 |

</details>

### Media

<details>

<summary>View Media operations</summary>

| Operation                                               | Method | Description                                      | Access              |
| ------------------------------------------------------- | ------ | ------------------------------------------------ | ------------------- |
| [Create product media](media/create-product-media.md)   | POST   | Creates new media for a product.                 | vendor              |
| [List product media](media/list-product-media.md)       | GET    | Gets a list of media for a product.              | vendor, client, ops |
| [Get product media by id](media/get-product-media.md)   | GET    | Gets an item of media for a product.             | vendor, client, ops |
| [Update product media](media/update-media.md)           | PUT    | Updates an item of media for a product.          | vendor              |
| [Mark media for review](media/mark-media-for-review.md) | POST   | Marks an item of media for a product for review. | vendor              |
| [Publish media](media/publish-media.md)                 | POST   | Publishes an item of media for a product.        | ops                 |
| [Unpublish media](media/unpublish-media.md)             | POST   | Unpublishes an item of media for a product.      | vendor, ops         |
| [Delete product media](media/delete-media.md)           | DELETE | Deletes an item of media for a product.          | vendor, ops         |

</details>

### Parameters

<details>

<summary>View Parameters operations</summary>

| Operation                                                 | Method | Description                              | Access              |
| --------------------------------------------------------- | ------ | ---------------------------------------- | ------------------- |
| [Create parameter](parameter/create-product-parameter.md) | POST   | Creates a product parameter.             | vendor              |
| [List parameters](parameter/list-product-parameters.md)   | GET    | Gets a list of parameters for a product. | vendor, client, ops |
| [Get parameter by id](parameter/get-product-parameter.md) | GET    | Gets a product parameter definition.     | vendor, client, ops |
| [Update parameter](parameter/update-product-parameter.md) | PUT    | Updates a product parameter definition.  | vendor              |
| [Delete parameter](parameter/delete-product-parameter.md) | DELETE | Deletes a product parameter definition.  | vendor              |

</details>

### Parameter Groups

<details>

<summary>View Parameter Groups operations</summary>

| Operation                                                           | Method | Description                                                              | Access              |
| ------------------------------------------------------------------- | ------ | ------------------------------------------------------------------------ | ------------------- |
| [Create parameter group](parameter-group/create-parameter-group.md) | POST   | Creates a new parameter group for a given product in the catalog.        | vendor              |
| [List parameter groups](parameter-group/list-parameter-groups.md)   | GET    | Lists all parameter groups for a given product based on filter criteria. | vendor, client, ops |
| [Get parameter group by id](parameter-group/get-parameter-group.md) | GET    | Gets a parameter group by id for a given product.                        | vendor, client, ops |
| [Update parameter group](parameter-group/update-parameter-group.md) | PUT    | Updates a parameter group for a given product.                           | vendor              |
| [Delete parameter group](parameter-group/delete-parameter-group.md) | DELETE | Deletes a parameter group from a given product.                          | vendor              |

</details>

### Price Lists

<details>

<summary>View Price Lists operations</summary>

| Operation                                                         | Method | Description                               | Access              |
| ----------------------------------------------------------------- | ------ | ----------------------------------------- | ------------------- |
| [Create price list](pricelists/create-pricelist.md)               | POST   | Creates a price list.                     | ops, vendor         |
| [List price lists](pricelists/list-pricelists.md)                 | GET    | Gets a list of price lists.               | vendor, client, ops |
| [Get price list by id](pricelists/get-pricelist.md)               | GET    | Gets a price list.                        | vendor, client, ops |
| [Update price list](pricelists/update-pricelist.md)               | PUT    | Updates a price list.                     | ops, vendor         |
| [Delete price list](pricelists/delete-pricelist.md)               | DELETE | Deletes a price list.                     | ops, vendor         |
| [List price list items](pricelist-item/list-pricelist-items.md)   | GET    | Gets a list of items in a price list.     | vendor, client, ops |
| [Get price list item by id](pricelist-item/get-pricelist-item.md) | GET    | Gets a price item within a price list.    | vendor, client, ops |
| [Update price list item](pricelist-item/update-pricelist-item.md) | PUT    | Updates a price item within a price list. | ops, vendor         |

</details>

### Pricing Policies

<details>

<summary>View Pricing Policies operations</summary>

| Operation                                                                                | Method | Description                                    | Access      |
| ---------------------------------------------------------------------------------------- | ------ | ---------------------------------------------- | ----------- |
| [Create pricing policy](pricing-policies/create-pricing-policy.md)                       | POST   | Creates a new pricing policy.                  | ops         |
| [List pricing policies](pricing-policies/list-pricing-policies.md)                       | GET    | Gets a list of pricing policies.               | ops, client |
| [Get pricing policy by id](pricing-policies/get-pricing-policy.md)                       | GET    | Gets a pricing policy by id.                   | ops, client |
| [Update pricing policy](pricing-policies/update-pricing-policy.md)                       | PUT    | Updates an existing pricing policy.            | ops         |
| [Delete pricing policy](pricing-policies/delete-pricing-policy.md)                       | DELETE | Deletes an existing pricing policy.            | ops         |
| [Activate pricing policy](pricing-policies/activate-pricing-policy.md)                   | POST   | Activates an existing pricing policy.          | ops         |
| [Deactivate pricing policy](pricing-policies/deactivate-pricing-policy.md)               | POST   | Disables an existing pricing policy.           | ops         |
| [List pricing policy attachments](pricing-policies/list-pricing-policy-attachments.md)   | GET    | Gets a list of pricing policy attachments.     | ops         |
| [Get pricing policy attachment by id](pricing-policies/get-pricing-policy-attachment.md) | GET    | Gets a pricing policy attachment by id.        | ops         |
| [Create pricing policy attachment](pricing-policies/create-pricing-policy-attachment.md) | POST   | Creates a new pricing policy attachment.       | ops         |
| [Update pricing policy attachment](pricing-policies/update-pricing-policy-attachment.md) | PUT    | Updates an existing pricing policy attachment. | ops         |
| [Delete pricing policy attachment](pricing-policies/delete-pricing-policy-attachment.md) | DELETE | Deletes an existing pricing policy attachment. | ops         |

</details>

### Products

<details>

<summary>View Products operations</summary>

<table><thead><tr><th width="221">Operation</th><th width="110">Method</th><th width="239">Description</th><th>Access</th></tr></thead><tbody><tr><td><a href="product/create-product.md">Create product</a></td><td>POST</td><td>Creates a new product.</td><td>vendor</td></tr><tr><td><a href="product/list-products.md">List products</a></td><td>GET</td><td>Fetches a list of products.</td><td>vendor, client, ops</td></tr><tr><td><a href="product/get-product.md">Get product by id</a></td><td>GET</td><td>Gets a product by id.</td><td>vendor, client, ops</td></tr><tr><td><a href="product/update-product.md">Update product</a></td><td>PUT</td><td>Updates some properties of a product.</td><td>vendor</td></tr><tr><td><a href="product/delete-product.md">Delete product</a></td><td>DELETE</td><td>Deletes a product.</td><td>vendor, ops</td></tr><tr><td><a href="product/mark-product-for-review.md">Mark product for review</a></td><td>POST</td><td>Marks a product for review by operations.</td><td>vendor</td></tr><tr><td><a href="product/publish-product.md">Publish product</a></td><td>POST</td><td>Publishes a product.</td><td>ops</td></tr><tr><td><a href="product/unpublish-product.md">Unpublish product</a></td><td>POST</td><td>Unpublishes a product.</td><td>vendor, ops</td></tr><tr><td><a href="product/update-product-settings.md">Update product settings</a></td><td>PUT</td><td>Updates a product’s settings.</td><td>vendor</td></tr></tbody></table>

</details>

### Templates

<details>

<summary>View Templates operations</summary>

| Operation                                               | Method | Description                             | Access              |
| ------------------------------------------------------- | ------ | --------------------------------------- | ------------------- |
| [Create product template](templates/create-template.md) | POST   | Creates a template for a product.       | vendor              |
| [List product templates](templates/list-templates.md)   | GET    | Gets a list of templates for a product. | vendor, client, ops |
| [Get product template by id](templates/get-template.md) | GET    | Gets a template for a product.          | vendor, client, ops |
| [Update product template](templates/update-template.md) | PUT    | Updates a template for a product.       | vendor              |
| [Delete product template](templates/delete-template.md) | DELETE | Deletes a template for a product.       | vendor              |

</details>

### Terms

<details>

<summary>View Terms operations</summary>

| Operation                                                              | Method | Description                             | Access              |
| ---------------------------------------------------------------------- | ------ | --------------------------------------- | ------------------- |
| [Create terms](terms-and-conditions/create-terms.md)                   | POST   | Creates terms for a product.            | vendor, ops         |
| [List terms](terms-and-conditions/list-terms.md)                       | GET    | Gets a list of all terms for a product. | vendor, client, ops |
| [Get terms by id](terms-and-conditions/get-terms.md)                   | GET    | Gets terms for a product.               | vendor, client, ops |
| [Update terms](terms-and-conditions/update-terms.md)                   | PUT    | Updates terms for a product.            | vendor, ops         |
| Delete terms                                                           | DELETE | Deletes terms for a product.            | vendor, ops         |
| [Mark terms for review](terms-and-conditions/mark-terms-for-review.md) | POST   | Marks terms for a product for review.   | vendor              |
| [Publish terms](terms-and-conditions/publish-terms.md)                 | POST   | Publishes terms for a product.          | ops                 |
| [Unpublish terms](terms-and-conditions/unpublish-terms.md)             | POST   | Unpublishes terms for a product.        | vendor, ops         |

</details>

### Unit of Measure

<details>

<summary>View Unit of Measure operations</summary>

| Operation                                                            | Method | Description                      | Access      |
| -------------------------------------------------------------------- | ------ | -------------------------------- | ----------- |
| [Create unit of measure](units-of-measure/create-unit-of-measure.md) | POST   | Creates a new unit of measure.   | ops         |
| [List units of measure](units-of-measure/list-unit-of-measure.md)    | GET    | Gets a list of units of measure. | vendor, ops |
| [Get unit of measure by id](units-of-measure/get-unit-of-measure.md) | GET    | Gets a unit of measure by id.    | vendor, ops |
| [Update unit of measure](units-of-measure/update-unit-of-measure.md) | PUT    | Updates a unit of measure by id. | ops         |

</details>

### Variants

<details>

<summary>View Variants operations</summary>

| Operation                                                      | Method | Description                                | Access              |
| -------------------------------------------------------------- | ------ | ------------------------------------------ | ------------------- |
| [Create variant](variants/create-variant.md)                   | POST   | Creates a variant for terms.               | vendor, ops         |
| [List variants](variants/list-variants.md)                     | GET    | Gets a list of all variants for terms.     | vendor, client, ops |
| [Get variant by id](variants/get-variant-for-terms.md)         | GET    | Gets a variant for terms.                  | vendor, client, ops |
| [Update variant](../extensions-api/variant/update-variant.md)  | PUT    | Updates a variant for terms for a product. | vendor, ops         |
| [Delete variant](variants/delete-variant.md)                   | DELETE | Deletes a variant for terms.               | vendor, ops         |
| [Mark variant for review](variants/mark-variant-for-review.md) | POST   | Marks a variant for terms for review.      | vendor              |
| [Publish variant](variants/publish-variant.md)                 | POST   | Publishes a variant for terms.             | ops                 |
| [Unpublish variant](variants/unpublish-variant.md)             | POST   | Unpublishes a variant for terms.           | vendor, ops         |

</details>
