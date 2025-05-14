# Object Diagrams

The Marketplace Platform enables transactions among different actors, such as clients, partners, and vendors, in countries where SoftwareOne operates.&#x20;

The platform includes objects such as orders, subscriptions, and agreements, which represent a relationship between these actors and SoftwareOne. Each object contains workflows that are essential for different scenarios. These workflows are illustrated as state diagrams. These diagrams show the status transitions of all objects within the platform, allowing you to understand each status and its transition. For instance, the initial status of a subscription is always **New**, and it can go through multiple statuses during its lifecycle within the platform. With the help of these diagrams, you can visualize each transition easily.

The following tabs feature objects that undergo various states and transitions within the platform. Objects without any statuses, for example, audit records, spotlight, and more, are not included. &#x20;

{% tabs %}
{% tab title="Accounts" %}
* [Account](accounts-api/account/state-diagram.md)
* [API Token](accounts-api/api-tokens/token-state-diagram.md)
* [Buyer](accounts-api/buyer/buyer-state-diagram.md)
* [Group](accounts-api/user-groups/group-state-diagram.md)
* [Licensee](accounts-api/licensee/licensee-state-diagram.md)
* [Seller](accounts-api/seller/seller-state-diagram.md)
* [User](accounts-api/users/users-state-diagram.md)
{% endtab %}

{% tab title="Catalog" %}
* [Product](catalog-api/product/product-states.md)
* [Item](catalog-api/items/item-states.md)
* [Media](catalog-api/media/media-states.md)
* [Documentation](catalog-api/documentation/documentation-states.md)
* [Terms and Conditions](catalog-api/terms-and-conditions/terms-and-conditions-states.md)
* [Authorization](catalog-api/authorization/state-diagram.md)
* [Pricelist](catalog-api/pricelists/pricelist-states.md)
* [Pricelist Item](catalog-api/pricelist-item/pricelist-states.md)
* [Listing](catalog-api/listing/state-diagram.md)
{% endtab %}

{% tab title=" Commerce" %}
* [Agreement](../../modules-and-features/marketplace/agreements/agreement-states.md)
* [Order](../../modules-and-features/marketplace/orders/order-states.md)
* [Subscription](../../modules-and-features/marketplace/subscriptions/subscription-states.md)
* [Request](../../modules-and-features/marketplace/requests/request-states.md)
{% endtab %}

{% tab title="Notifications" %}
* [Category](notifications-api/categories/state-diagram.md)
* [Contact](notifications-api/contacts/state-diagram.md)
* [Message](notifications-api/messages/notification-state-diagram.md)
* [Subscriber](notifications-api/subscribers/state-diagram.md)
{% endtab %}

{% tab title="Program" %}
* [Program](program-api/program/program-state-diagram.md)
* [Certificates](../../modules-and-features/marketplace/certificates/certificate-states.md)
* [Enrollment](../../modules-and-features/marketplace/enrollments/enrollment-states.md)
{% endtab %}
{% endtabs %}
