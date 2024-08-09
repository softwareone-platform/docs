# Key Concepts

Certain concepts and terms are central to the functionality and design of the Marketplace Platform. We recommend that you understand the terminology because it's often referred to in our platform and documentation. Understanding the terminology will make it easier for you to interact with the platform and maximize its use.&#x20;

{% hint style="info" %}
If you'd rather watch a getting started video, see our [Getting Started Guide ](https://youtu.be/LrMOMN8sjM4)which describes all concepts listed on this page in detail and provides insights into what makes our platform unique.&#x20;
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

**Users** - Users, as the name suggests, represent individuals or persons who can sign in to the platform using their credentials and perform all operations associated with permissions.&#x20;

**Accounts** - An account is an object that represents a company or an organization utilizing the Marketplace Platform. In our platform, an account can contain one or multiple users:

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Account containing multiple users</p></figcaption></figure>

Additionally, users are not restricted to a single account. They can belong to multiple accounts and [switch between those accounts](basics/switch-account.md) seamlessly through the interface, without signing out of the platform:

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption><p>Users belonging to multiple accounts</p></figcaption></figure>

**Groups** - A group is an object facilitating permissions in the scope of an account. Groups contain users and all users in the group have the same permissions. Note that in our platform, permissions are assigned at the group level, rather than the individual user level.&#x20;

Additionally, users can be a part of multiple groups, much like users can belong to multiple accounts.

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption><p>Multiple groups contaning multiple users</p></figcaption></figure>

## Sellers, Buyers, and Licensees <a href="#portals-accounts-and-users" id="portals-accounts-and-users"></a>

**Seller** - A seller is a SoftwareOne entity (for example, SoftwareOne Canada) that buys software solutions from vendors and sells those solutions to clients.&#x20;

In the Marketplace Platform, sellers are responsible for generating and issuing invoices to the buyer entities of clients, acting as the intermediary in the transaction process.

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption><p>Sellers in the Marketplace Platform</p></figcaption></figure>

**Buyer** - Buyers represent an entity that engages in commercial activities with the SoftwareOne reselling entity (known as Sellers).&#x20;

Buyers are the recipients of invoices issued by SoftwareOne, and they are central to the creation and context of orders, agreements, and subscriptions in the platform.

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption><p>Buyers in the Marketplace Platform</p></figcaption></figure>

**Licensee** - Licensees are the entities that consume the software products or services procured by the buyer. In our platform, licensees are critical in establishing agreements alongside buyers and sellers.

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption><p>Licensees in the Marketplace Platform</p></figcaption></figure>

## Agreement

An agreement is an object outlining the relationship between the seller, buyer, and licensee.&#x20;

Agreements establish the terms and conditions under which transactions occur. They are also the foundation for placing orders and creating subscriptions on the platform. Without an agreement, you cannot buy products on our platform.

<figure><img src="../../.gitbook/assets/image (24).png" alt=""><figcaption><p>Agreements in the Marketplace Platform</p></figcaption></figure>

## Orders and Subscriptions

**Order** - An order is an object that signifies a business transaction under the framework of an established agreement.&#x20;

The Marketplace Platform accommodates a variety of order types, distinguishing between new purchases, change orders, and termination orders, each tailored to support different operations and client needs:

* **Purchase order** - Purchase orders are created when you buy a new product or service by creating a new agreement.&#x20;
* **Change order** - Change orders are created when you modify your agreement or change the subscription quantity, such as downsizing the license quantity or buying additional resources.
* **Terminate order** - Terminate orders are created when you partially or fully terminate your agreement or subscription with SoftwareOne.&#x20;

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption><p>Different types of orders in the Marketplace Platform</p></figcaption></figure>

**Subscriptions** - Subscriptions are linked to an agreement and represent the provision of a service over a set period. One agreement can contain one or more subscriptions.&#x20;

If you need to change subscriptions, you can only do so through orders. For example, to terminate a subscription, you must place a termination order. Similarly, to add more licenses, a change order must be placed. It’s not possible to modify a subscription directly without placing an order.

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption><p>Subscriptions in the Marketplace Platform</p></figcaption></figure>
