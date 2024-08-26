# Key Concepts

Certain concepts and terms are central to the functionality and design of the Marketplace Platform. We recommend that you understand the terminology because it's often referred to in our platform and documentation. Understanding the terminology will make it easier for you to interact with the platform and maximize its use.&#x20;

{% hint style="info" %}
You can also watch our [Getting Started Guide ](https://youtu.be/LrMOMN8sjM4)which describes all concepts listed on this page in detail and provides insights into what makes our platform unique for your enterprise software procurement.&#x20;
{% endhint %}

## Actors

The Marketplace Platform seamlessly brings together various actors to facilitate the buying, selling, provisioning, and billing of software products.&#x20;

Actors represent different entities that interact with the platform for procurement and fulfillment-related activities as well as other operations specific to the platform.&#x20;

<figure><img src="../../.gitbook/assets/image (21).png" alt=""><figcaption><p>Key actors in the Marketplace Platform</p></figcaption></figure>

The following are the key actors in our platform:

**Vendors** - A vendor is a company or a person from whom SoftwareOne buys software solutions. Vendors develop and sell their products and services. Examples include Microsoft, Dropbox, and more.

**Distributors** - A distributor is an entity that resells software solutions sourced from multiple vendors to resellers. Distributors facilitate software procurement in cases where direct relationships with vendors are not feasible.

**Associates** - Associates are the internal SoftwareOne associates who administer the business network. Our associates are involved in various processes throughout your journey with both SoftwareOne and the Marketplace Platform.

**Partners** - Partners represent entities or businesses that buy products or services from SoftwareOne for resale to other businesses. Partners assist us in serving specific clients better.

**Clients** - A client is a company or organization that utilizes our platform to buy software products for their own use or direct consumption.

**Developers and System Integrators** - Developers and system integrators represent entities involved in building integrations within the business network.

## Users, Accounts, and Groups <a href="#portals-accounts-and-users" id="portals-accounts-and-users"></a>

**Users** - Users, as the name suggests, represent individuals or persons who can sign in to the platform using their credentials and perform all operations associated with their permissions.&#x20;

**Account** - An account is an object that represents a company or an organization utilizing the Marketplace Platform. Three types of accounts exist in the platform: Client account, Vendor account, and Operations account.&#x20;

* **Client account** - A client account is used by our clients and partners to establish agreements and procure software solutions for their enterprises.
* **Vendor account** - A vendor account is used by vendors to define the product structure and make those products available for ordering through the marketplace.&#x20;
* **Operations account** - An operations account is used by SoftwareOne associates.

In the Marketplace Platform, an account can contain one or multiple users:

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Account containing multiple users</p></figcaption></figure>

Additionally, users are not restricted to a single account. They can belong to multiple accounts and [switch between those accounts](interface/switch-account.md) seamlessly through the interface, without signing out of the platform:

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption><p>Users belonging to multiple accounts</p></figcaption></figure>

**Group** - A group is an object facilitating permissions in the scope of an account. Groups contain users and all users in the group have the same permissions. Note that in our platform, permissions are assigned at the group level, rather than the individual user level.&#x20;

Additionally, users can be a part of multiple groups, much like users can belong to multiple accounts.

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption><p>Multiple groups containing multiple users</p></figcaption></figure>

## Sellers, Buyers, and Licensees <a href="#portals-accounts-and-users" id="portals-accounts-and-users"></a>

**Seller** - A seller is a SoftwareOne entity (for example, SoftwareOne Canada) that buys software solutions from vendors (like Microsoft) and sells those solutions to clients.&#x20;

In the Marketplace Platform, sellers are responsible for generating and issuing invoices to the buyer entities of clients, acting as the intermediary in the transaction process.

<figure><img src="../../.gitbook/assets/image (472).png" alt=""><figcaption><p>Sellers in the Marketplace Platform</p></figcaption></figure>

**Buyers** - Buyers represent an entity that engages in commercial activities with the SoftwareOne reselling entity (known as Sellers).&#x20;

Buyers are the recipients of invoices issued by SoftwareOne, and they are central to the creation and context of orders, agreements, and subscriptions in the platform.

<figure><img src="../../.gitbook/assets/image (473).png" alt=""><figcaption><p>Buyers in the Marketplace Platform</p></figcaption></figure>

**Licensees** - Licensees are the entities that consume the software products or services procured by the buyer. In our platform, licensees are critical in establishing agreements alongside buyers and sellers.

<figure><img src="../../.gitbook/assets/image (474).png" alt=""><figcaption><p>Licensees in the Marketplace Platform</p></figcaption></figure>

## Agreements&#x20;

An agreement is an object outlining the relationship between the seller, buyer, and licensee.&#x20;

Agreements establish the terms and conditions under which transactions occur. They are also the foundation for placing orders and creating subscriptions on the platform. Without an agreement, it's not possible to buy products on our platform.

<figure><img src="../../.gitbook/assets/image (476).png" alt=""><figcaption><p>Agreements in the Marketplace Platform</p></figcaption></figure>

## Orders and Subscriptions

**Orders** - An order is an object that signifies a business transaction under the framework of an established agreement.&#x20;

The Marketplace Platform accommodates a variety of order types, distinguishing between new purchases, change orders, and termination orders to support different operations and client needs. The following types of orders exist in our platform:

* **Purchase order** - Purchase orders are created when you buy a new product or service by creating a new agreement.&#x20;
* **Change order** - Change orders are created when you modify your agreement or change the subscription quantity, such as downsizing the license quantity or buying additional resources.
* **Terminate order** - Terminate orders are created when you terminate your agreement or subscription with SoftwareOne.&#x20;

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption><p>Different types of orders in the Marketplace Platform</p></figcaption></figure>

**Subscriptions** - Subscriptions are linked to an agreement and represent service provision over a set period. One agreement can contain one or more subscriptions.&#x20;

If you need to change subscriptions, you can only do so through orders. For example, to terminate a subscription, you must place a termination order. Similarly, to add more licenses, a change order must be placed. It’s not possible to modify a subscription directly without placing an order.

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption><p>Subscriptions in the Marketplace Platform</p></figcaption></figure>

## Products, Items, and Parameters

**Products** - Products are the solutions or services offered by vendors through the marketplace. They contain various items and parameters, which are also defined by vendors.&#x20;

* **Items** - Represent the individual stock-keeping units (SKUs). In our platform, a product can contain one or more items, each with its specific name and price.&#x20;
* **Parameters** - Parameters represent structured data used by vendors to collect information from clients during the ordering process. Examples of this information might include contact details, address information, domain name, and more. Parameters can also be used by vendors to pass information to clients during provisioning.&#x20;

<figure><img src="../../.gitbook/assets/image (479).png" alt=""><figcaption><p>Products in the Marketplace Platform</p></figcaption></figure>

## Price List

A Price List is an object that holds key pricing details of each item within the product.

Our platform allows vendors to define price lists for different regions. These price lists are linked to specific sellers and are organized through an object called Listing.&#x20;

The Listing object is established by SoftwareOne associates after reviewing products. It links the product price list with the seller, ultimately making the product available for our clients in the SoftwareOne Marketplace.

<figure><img src="../../.gitbook/assets/image (480).png" alt=""><figcaption><p>Price List in the Marketplace Platform</p></figcaption></figure>
