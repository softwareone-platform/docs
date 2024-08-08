# Key Concepts

Certain concepts and terms are central to the functionality and design of the Marketplace Platform. We recommend that you understand the terminology because it's often referred to in our platform and documentation. Understanding the terminology will make it easier for you to interact with the platform and maximize its use.&#x20;

{% hint style="info" %}
If you'd rather watch a video, see our [Getting Started Guide ](https://youtu.be/LrMOMN8sjM4)which describes all concepts listed on this page and provides valuable insights into what makes our platform unique.&#x20;
{% endhint %}

## Actors

The Marketplace Platform seamlessly brings together various actors to facilitate the buying, selling, provisioning, and billing of software products.&#x20;

Actors represent different entities that interact with the platform for procurement and fulfillment-related activities as well as other operations specific to the platform.&#x20;

<figure><img src="../../.gitbook/assets/image (21).png" alt=""><figcaption><p>Key actors in the Marketplace Platform</p></figcaption></figure>

The following are the key actors in our platform:

**Vendors** - A vendor is a company or an individual from which SoftwareOne procures software products.

**Distributors** - A distributor is an entity that resells software solutions sourced from multiple vendors to resellers. Distributors facilitate software procurement in cases where direct relationships with vendors are not feasible.

**Associates** - Associates are the SoftwareOne associates who administer the business network and are involved in various processes throughout your journey.

**Partners** - Represent entities or businesses that purchase software products from SoftwareOne for indirect consumption and then resell those products to other businesses. Partners assist us in serving specific clients better.

**Clients** - A client is a company or organization that utilizes our platform to buy software products for their direct consumption.

**Developers and System Integrators** - Developers and System integrators represent entities involved in building integrations within the business network.

## Accounts, Users, and Groups <a href="#portals-accounts-and-users" id="portals-accounts-and-users"></a>

**Accounts** - An account is an object that represents a company or an organization using our platform. An account can contain multiple users:

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Account with multiple users</p></figcaption></figure>

Additionally, users can be a part of multiple accounts:

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption><p>Users belonging to multiple accounts</p></figcaption></figure>

**Users** - Users represent individuals who can sign in to the platform and perform operations based on their permissions.&#x20;

**Groups** - A group is an object facilitating permissions in the scope of an account. Groups contain users and all users in the group have the same permissions. Our platform allows users to be a part of more than one group:

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption><p>Account containing multiple groups and users</p></figcaption></figure>

## Sellers, Buyers, and Licensees <a href="#portals-accounts-and-users" id="portals-accounts-and-users"></a>

**Seller** - A seller is a SoftwareOne entity that buys software solutions from vendors and sells those products to clients. For example, SoftwareOne USA. Sellers are responsible for generating and issuing invoices to the buyer entities of clients, acting as the intermediary in the transaction process.

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption><p>Sellers in the Marketplace Platform</p></figcaption></figure>

**Buyer** - An entity that engages in commercial activities with SoftwareOne sellers. Buyers are the recipients of invoices issued by SoftwareOne, and they are central to the creation and context of orders, agreements, and subscriptions.

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption><p>Buyers in the Marketplace Platform</p></figcaption></figure>

**Licensee** - An entity that consumes the services procured by the buyer. Licenses are critical in forming agreements alongside buyers and sellers.

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption><p>Licensees in the Marketplace Platform</p></figcaption></figure>

## Agreement

An agreement is an object outlining the relationship between the seller, buyer, and licensee. In our platform, agreements establish the terms and conditions under which transactions occur. They are also the foundation for placing orders and creating subscriptions on the platform.&#x20;

<figure><img src="../../.gitbook/assets/image (24).png" alt=""><figcaption><p>Agreements in the Marketplace Platform</p></figcaption></figure>

## Orders and Subscriptions

**Order** - An order is an object that signifies a business transaction under the framework of an established agreement. The Marketplace platform accommodates a variety of order types, distinguishing between new purchases, change orders, and other transactional categories, each tailored to support different commercial operations and client needs.

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption><p>Orders in the Marketplace Platform</p></figcaption></figure>

The following types of orders can be created on our platform:

* **Purchase order** - Used to establish a new agreement. Purchase orders are created when you buy a new product or service by creating a new agreement.
* **Change order** - Created when you modify the agreement or change the subscription quantity, such as downsizing the license quantity or buying additional resources.
* **Terminate order** - Created when you terminate the agreement or subscription.&#x20;

**Subscriptions** - A subscription is an object linked to an agreement. Subscriptions represent the provision of a service over a specific period of time.

In the Marketplace Platform, an agreement can contain multiple subscriptions. Additionally,  subscriptions can only be modified through orders:&#x20;

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption><p>Subscriptions in the Marketplace Platform</p></figcaption></figure>
