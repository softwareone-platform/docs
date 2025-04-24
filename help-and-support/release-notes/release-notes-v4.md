---
description: Discover our newest release.
hidden: true
---

# Release Notes v4

**Release Date: 15 May 2025**

Our latest release, Marketplace Platform v4, is here. This release introduces several new features to enhance our platform's capabilities and improve existing functionalities.

Watch the following video or continue reading to learn about this release:

## Billing Invoices and Statements&#x20;

In this release, we are introducing billing statements.&#x20;

In addition to invoices, you'll now receive statements containing a detailed record of charges for the subscriptions in your agreement. Billing statements are provided in the XLSX format. Unlike invoice PDFs, which only contain a summary of charges, statements include a comprehensive breakdown of all charges. See [Understand Your Billing Documents](../../modules-and-features/marketplace/billing/understand-your-billing-documents.md) to learn more.

We've also updated the platform's navigation menu to include the new **Billing** module. This module contains pages you can use to access your [Invoices ](../../modules-and-features/inventory/invoices.md)and [Statements](../../modules-and-features/marketplace/billing/statements.md).

## Deprecated Features

The following features have been deprecated and are no longer supported by the Marketplace Platform:

* 365EA + Unified Support
* Unified Support for Multivendor

## FinOps for Cloud

FinOps for Cloud is a new solution designed to help you optimize costs and manage your resources effectively.&#x20;

<div align="center" data-full-width="false"><figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption><p>FinOps for Cloud UI</p></figcaption></figure></div>

With FinOps for Cloud, you can explore and analyze your cloud expenses, monitor resource usage, and implement policies to ensure efficient and cost-effective cloud management. With a user-friendly interface and robust features, the solution provides greater visibility and control over cloud infrastructure. To learn more, see [FinOps for Cloud](../../extensions/finops-for-cloud/).

## New Order Status

Previously, the **Draft** status was used to identify orders that you intentionally saved for later.&#x20;

We have now introduced a new status called **Quoted**, which will apply to orders, including purchase, change, and termination orders, saved for later. The **Draft** status is now only used for orders that are created by the platform for validation purposes. To learn more, see [Order States](../../modules-and-features/marketplace/orders/order-states.md).

## Notifications Management

The new Notifications feature allows account administrators to configure and manage notification emails for their accounts.&#x20;

Admins can set recipients for these emails and manage categories to start or stop receiving notifications. This feature is accessible through the **Settings** menu. To learn more, see [Notifications](../../modules-and-features/settings/notifications/). Individual users can also customize notification settings through their profile to determine what notifications to receive. See [Manage Notification Preferences](../../marketplace-platform/getting-started/interface/manage-notification-preferences.md) for details.&#x20;

Additionally, developers and system integrators can use our new Notifications API to manage notification configurations for accounts.

## Object Spotlight

The new **Spotlight** feature simplifies task management by highlighting key business objects that require your attention. These objects include your agreements, invoices, subscriptions, and more.&#x20;

For instance, if there are saved orders in your account, those orders are spotlighted so you can manage them easily. Similarly, subscriptions that are nearing expiration are also shown so you can take timely action. To learn more, see [View Object Spotlight](../../marketplace-platform/getting-started/interface/view-pending-tasks.md).

You can find the **Spotlight** feature on the **Home** page, and it can also be accessed by selecting the spotlight icon <img src="../../.gitbook/assets/icon_pending_actions.png" alt="" data-size="line"> in the status bar. You can also access the feature programmatically using the Object Spotlight API.&#x20;

<figure><img src="../../.gitbook/assets/spotlight.png" alt=""><figcaption><p>Spotlight widget</p></figcaption></figure>

## Order Reminder Email

If there's an order in your account that has been created but not placed yet, you can now send an order reminder email to remind an individual about this order.&#x20;

Reminders can be sent to users within your account and to those who are not in your account but are registered users on the platform. Reminders can be sent for orders in the **Quoted** status only. To learn more, see [Send Order Reminder Email](../../modules-and-features/marketplace/orders/send-order-reminder-email.md).

## Public Catalog

We are excited to announce the launch of our public catalog, available at marketplace. softwareone.com.

Designed for intuitive navigation, our catalog ensures a seamless browsing experience and simplifies your software procurement journey.

The catalog is available to everyone and provides easy access to a wide range of software products and services. You can explore products from over 56,000 vendors across categories, including healthcare, finance, analytics, and more.&#x20;

<figure><img src="../../.gitbook/assets/release_notes_catalog.png" alt="" width="563"><figcaption><p>SoftwareOne public catalog</p></figcaption></figure>

## Search Query in Data Grids

As part of our ongoing effort to make our platform easier to work with, we've introduced a new filter condition called **Search Query**. You can find this condition within the <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGAAAABgCAYAAADimHc4AAAAAXNSR0IArs4c6QAAActJREFUeF7t2TFOQ0EQBFF8UgISjkRCwElBpASg0Y5VtnmOZ6e9Vb+Db1+efFIClzRd+BMB8UNAAAExgTheAwiICcTxGkBATCCO1wACYgJxvAYQEBOI4zWAgJhAHK8BBMQE4ngNICAmEMdrAAExgTheAwiICcTxGnBvAp5fXj/j73zT8R/vb6OHejT8fXMCfvdPQNwPAgiICcTxGkBATCCO14BHFxDf7+Hix+8BD0cgvhABBMQE4ngNICAmEMdrAAExgTheAwiICcTxGkBATCCOv3oD7v0vzOmvm1OfBPxBjIDpI7U8T8Ay0Ok6AqbElucJWAY6XUfAlNjyPAHLQKfr7l7A9ML/bf7q7wH/Dej0vgRMiS3PE7AMdLqOgCmx5XkCloFO1xEwJbY8T8Ay0Ok6AqbElucJWAY6XUfAlNjyPAHLQKfrbl7A6X/K1/4xbQr85zwBpwQPzxNwCPD0OAGnBA/PE3AI8PQ4AacED88TcAjw9DgBpwQPz9+8gMP73fxxAmJFBBAQE4jjNYCAmEAcrwEExATieA0gICYQx2sAATGBOF4DCIgJxPEaQEBMII7XAAJiAnG8BhAQE4jjNYCAmEAcrwEExATi+C97b2BhPsA2DAAAAABJRU5ErkJggg==" alt="<svg xmlns=&#x22;http://www.w3.org/2000/svg&#x22; height=&#x22;24px&#x22; viewBox=&#x22;0 -960 960 960&#x22; width=&#x22;24px&#x22; fill=&#x22;#5f6368&#x22;><path d=&#x22;M400-240v-80h160v80H400ZM240-440v-80h480v80H240ZM120-640v-80h720v80H120Z&#x22;/></svg>" data-size="line">**Filter** option in the data grid.&#x20;

This new condition allows you to enter a search term, which is then used to find matching records across other filter conditions, such as orders, agreements, and more.

<figure><img src="../../.gitbook/assets/search_query.png" alt=""><figcaption><p>Search query filter</p></figcaption></figure>

## Subscription Automatic Renewals

You can now easily manage the automatic renewal of your subscriptions through the platform's interface.&#x20;

If you prefer not to have your subscription renewed automatically, you can disable the auto-renewal. Additionally, if you previously disabled automatic renewal, you can re-enable it at any time. To learn more, see [Manage Automatic Renewals](../../modules-and-features/marketplace/subscriptions/manage-automatic-renewals.md).&#x20;
