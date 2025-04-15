---
hidden: true
---

# Notifications

Notifications Management allows account administrators to configure recipients and manage the notification categories for their account. These notifications are sent via email to alert recipients about the events in their account so they can keep up-to-date and take proactive actions as necessary.

The Marketplace Platform supports various categories that can be easily enabled or disabled from the interface. Administrators also have the flexibility to define recipients at the account level. They can specify individual users or a group of users as recipients of these emails. Individual users can manage notifications for their profiles through the **My profile** option in the account menu.&#x20;

## Notification categories <a href="#notification_types" id="notification_types"></a>

In the Marketplace Platform, all related notification emails are grouped together as categories.

Each category consolidates emails of a similar type, allowing you to manage preferences at the category level instead of handling each email individually. For example, when you disable the Orders category, you'll stop receiving all order-related emails.&#x20;

The following table lists the categories supported by email notifications:

| Category name       | Description                                                                                                                                                                   |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Account             | These notifications alert recipients to the changes in the account. For instance, when a new user is added or an existing one is removed.                                     |
| Billing and Invoice | These notifications relate to billing updates and invoices in your account. For instance, when a new statement is generated.                                                  |
| Catalog             | These notifications are sent when the catalog has been updated to change the product's status and pricing.                                                                    |
| News and updates    | These notifications alert recipients to the platform news and latest announcements, such as feature releases, upcoming maintenance, and more.                                 |
| Orders              | These notifications are sent when there's an order-related activity in your account. For instance, when you place a new order or the status of your existing order changes.   |
| Programs            | These notifications relate to enrollments and certificates. For instance, when your enrollment request has been approved by the vendor.                                       |
| Quotes              | These notifications relate to your requests for a quotation.                                                                                                                  |
| Requests            | These notifications alert you to the submitted requests in your account. For instance, when the status of your request changes, when you need to action a request, and so on. |
| Subscriptions       | The platform sends these notifications for subscription-related updates to your account. For instance, renewal updates or when a new subscription is created.                 |
| User updates        | These email notifications are sent when you update your profile. For instance, when you update your password. You cannot opt out of these notifications.                      |

You can manage these categories from the **Notifications** > **Subscribers** page. See [Enable or Disable Categories](enable-or-disable-categories.md) to learn more.

## Notifications interface <a href="#audit-trail-interface" id="audit-trail-interface"></a>

Account administrators can access notifications by selecting **Settings** > **Notifications** from the main menu.

<figure><img src="../../../.gitbook/assets/notifications_interface.png" alt=""><figcaption><p>Notifications page</p></figcaption></figure>

The **Notifications** page contains these three tabs: **Subscribers**, **Messages**, and **Settings**.&#x20;

### Subscribers

The **Subscribers** tab displays all [notification categories](./#notification_types) configured for your account. For each notification, you can view the following details:

* **Subscribers** - Displays the category name. Clicking the name opens the [subscriber details page ](./#subscriber-details-page)to manage the notification's configuration. &#x20;
* **Short description** - Displays a short description of the category.
* **Recipients** - Shows the total number of users and groups who are the recipients of the notifications.
* **Updated** - Shows the date and time the notification's configuration was updated.&#x20;
* **Last used** - Shows the date and time the platform sent the notification in that category.&#x20;
* **Updated by** - Displays the name and ID of the individual who updated the notification's configuration.&#x20;
* **Status** - Indicates whether the category is enabled or disabled.&#x20;

#### Subscriber details page

From the **Subscriber** details page, you can manage recipients and groups for a notification category. You can also enable or disable a category. See [Configure Recipients](configure-recipients.md) and [Enable or Disable Categories](enable-or-disable-categories.md) for details.

<figure><img src="../../../.gitbook/assets/notifications_subscribers_details.png" alt=""><figcaption><p>Subscribers details page</p></figcaption></figure>

### Messages

The **Messages** tab contains all messages sent to the users in your account.&#x20;

<figure><img src="../../../.gitbook/assets/notifications_message.png" alt=""><figcaption><p>Messages tab</p></figcaption></figure>

For each message, you can view the following details:

* **Message ID** - Displays the message ID.
* **Contact** - Displays the recipient's email address.&#x20;
* **User** - Displays the name and ID of the individual linked to the contact. If the field is empty, it means the recipient doesn't have a Marketplace Platform account.
* **Subject** - Displays the subject line of the email.
* **Category** - Displays the category of the notification. See [Notification categories](./#notification_types) for details.
* **Account** - <mark style="color:red;">Description required</mark>
* **Created** - <mark style="color:red;">Description required</mark>
* **Created by** - <mark style="color:red;">Description required</mark>
* **Status** - Displays the status of the message. To learn about the possible statuses, see [Notification States](notification-states.md).
* **Actions** - Includes the **View details** option, which opens the **Message details** page.

#### Message details page

The **Message details** page displays detailed information for the message. You can also view the content of the email, the files attached to the message, the time and date when the message was triggered, and so on.&#x20;

<figure><img src="../../../.gitbook/assets/notifications_message_detail.png" alt=""><figcaption><p>Message details page</p></figcaption></figure>

### Settings

The **Settings** tab allows you to view and edit your account-level notification settings, such as the sender name, the default language you wish to use for all emails, and the email's footer. See [Customize Notification Settings](edit-notification-settings.md) for information on how to edit these details.&#x20;

<figure><img src="../../../.gitbook/assets/notifications_settings.png" alt=""><figcaption><p>Edit notification settings</p></figcaption></figure>
