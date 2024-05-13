---
description: Learn what's new in this release.
---

# Release notes v2

**Release Date: 22 May 2024**

We are happy to announce the v2 release of the Marketplace Platform. As part of this release, we’ve introduced several new modules, features, and improvements.

Watch the following video or continue reading to learn about this release:

{% embed url="https://vimeo.com/933735429" %}

## Accounts Management

We’ve redefined account management to offer new user and group management possibilities. Now, you can manage your account, view account settings, and manage users, groups, and other entities in a self-service way through the [Settings](../../platform-modules/settings/) module.

Here are some additional highlights:&#x20;

* **Invite new members** - Account administrators can invite new members to join the account on the Marketplace Platform. New members can be invited by email or by copying the invitation link from the interface and sharing it directly with the individual. Once invited, the individual must click the link to accept the invitation and set up their platform account. To learn more, see [Add new users](../../platform-modules/settings/users/add-new-users.md) and [Respond to invitations](../../platform-basics/respond-to-invitations.md).
* **Switch accounts** - The Marketplace Platform allows individuals to be a part of multiple accounts and switch between those accounts seamlessly, without signing out of the platform. To learn more, see [Switch accounts](../../platform-basics/profile-settings/switch-accounts.md).&#x20;
* **Manage users and permissions** - Account administrators can manage users and their permissions through the platform. However, permissions must be assigned at the group level, rather than the individual user level. Group-level permissions can be assigned by creating groups and then granting permissions that apply to all users in that group. To learn more, see [Groups](../../platform-modules/settings/groups/) and [Users](../../platform-modules/settings/users/).
* **Manage profile** - You can update your personal account settings (user details, display preferences, and communication settings) and change your password through the **My Profile** option in your user profile menu. To learn more, see [Manage your profile](../../platform-basics/profile-settings/manage-your-profile.md).

## Orders Management

We've introduced a new **Orders** module so you can view and manage your orders easily.

The new module displays a list of orders in your account, including purchase orders, change orders, and termination orders, and lets you complete order management tasks (such as adding notes to your order, downloading attachments, and more).

You can also find the items assigned to your order, pricing details, provisioning and ordering parameters, and other order-related attributes. To learn more, see [Orders](../../platform-modules/marketplace/orders/).

## Subscriptions and Agreements Management&#x20;

The new **Subscriptions** module is a centralized location to access your ordered subscriptions and manage those subscriptions in a self-service manner. For example, you can change the number of subscription items, terminate a subscription, and even rename your subscriptions. To learn more, see [Subscriptions](../../platform-modules/marketplace/subscriptions/).

The new **Agreements** module contains all your agreements with SoftwareOne and subscriptions within each agreement. You can also cancel all subscriptions and terminate the complete agreement, rename your agreement, and change the default ID assigned to your agreement. To learn more, see [Agreements](../../platform-modules/marketplace/agreements/).

## Requests Management

Requests Management enables you to create a presale request from within the platform and contact us for any product information you might need, for example, pricing details, product availability, or licensing details.&#x20;

You can also track all requests you’ve created, mark requests as complete after they’ve been answered, and send a message to our business experts from your account. To learn more, see [Requests](../../platform-modules/marketplace/requests/).

## Adobe VIP Marketplace and Microsoft 365

We’ve redesigned the **Products** page to improve usability and make it easier for you to discover Adobe VIP Marketplace and Microsoft 365 products, and purchase licenses. &#x20;

The new **Products** page has a cleaner look and feel so you can browse products in our catalog and easily select products you are interested in. You can also click a product to view its details page and see full product information. To learn more, see [Products interface](../../platform-modules/marketplace/products/products-interface.md)_._

Additionally, we’ve introduced a new **Purchase Wizard** that guides you step-by-step through the purchasing process for subscription-based products. The **Purchase Wizard** uses a consistent interface, regardless of the product you are buying. It guides you through each step and allows you to enter your data as required. To learn more, see [Buy products and services](../../platform-modules/marketplace/products/buy-products-and-services.md)_._

## New Navigation Structure&#x20;

With the addition of new modules to the Marketplace Platform, we’ve reorganized the main menu and added new categories to provide an intuitive layout. We’ve also removed certain sections from the menu and moved them to the other areas of the platform.

Here's a summary of the changes:

* The **Settings** module is new and provides access to all account management features and settings.
* The **Marketplace** module has been reorganized to include the new commerce and request management modules.&#x20;
* The **Cloud Tools**, **ITAM Tools**, **Other tools**, and **Procurement** modules have been created for features related to these categories.
* The **Help** module has been removed from the main menu. Now, you can [access documentation](../../platform-basics/view-documentation.md) and other content resources, and [view the help and support](../getting-support.md) page using the help icon in the header.&#x20;
* [Notifications](../../platform-basics/profile-settings/view-notifications.md) are now accessible through the notifications icon in the header, instead of the main menu.

## Other Updates

To provide a unified experience, we've implemented consistent styling and framework across the new modules and platform features:

* Where applicable, data grids have been used to display the different types of data, and advanced filtering and sorting options are implemented so you can control the table display. We’ve also introduced a view selector to switch between different preconfigured view options. To learn more, see [Table filters](../../platform-basics/platform-interface/table-filters/).&#x20;
* We’ve removed the footer, containing links to the knowledge resources and language selector. Now, you can access all resources using the question mark icon in the header and change your display language from the **Sign-in** page of the platform or through the [My Profile](../../platform-basics/profile-settings/manage-your-profile.md) option.

## APIs for Integration

Now, you can interact with the Marketplace Platform programmatically by generating API tokens from the platform's interface and then using those tokens to access different API endpoints. For more information, see [API tokens](../../platform-modules/settings/api-tokens/) and the **Developer Resources** section in the left navigation.

## Deprecated Features

With the v2 release, we've introduced notable changes to our platform and business processes. As a result, we've removed the following features and replaced them with self-service alternatives:

* **Cloud Subscriptions**, which enabled you to purchase Microsoft CSP products and manage subscriptions has been replaced with [Products](../../platform-modules/marketplace/products/) and [Subscriptions ](../../platform-modules/marketplace/subscriptions/)management.&#x20;
* **Guided Activation**, which enabled you to activate 365Simple and AzureSimple service has been replaced with the new [Orders](../../platform-modules/marketplace/orders/) and [Products](../../platform-modules/marketplace/products/) modules.&#x20;
* **Company Contacts**, which showed all contacts that existed for your company and allowed you to maintain your company structure has been removed. The concept of [Buyers](../../platform-modules/settings/buyers/) has been introduced as a replacement.
* **My account team**, which displayed the SoftwareOne sales contact for your account has also been removed.&#x20;
