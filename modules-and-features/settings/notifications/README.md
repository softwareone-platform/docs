# Notifications

The Notifications module in the Marketplace Platform lets account administrators configure and manage email notifications for their account.

Administrators can enable email notifications each time a certain event occurs within the account, such as when an order's status changes, a new agreement is created, platform maintenance is upcoming, and more. The Marketplace Platform supports various notification categories and sends emails to only those recipients defined by the administrator for each category.

While account administrators can manage notifications at the account level, individual users can also self-manage notifications for their profile. This can be done through the **My profile** option in the account menu. See [Manage Email Notifications](../../../marketplace-platform/getting-started/interface/manage-notification-preferences.md) to learn more.

## Notification categories <a href="#notification_types" id="notification_types"></a>

In the Marketplace Platform, all notifications are grouped into specific categories.&#x20;

Each category consolidates emails of a similar type, allowing you to manage your preferences at the category level instead of handling each email individually. For example, when you disable the Orders notification category, you'll stop receiving all order-related emails.&#x20;

The following table lists the supported notification categories:

| Notification categories | Description                                                                                                                                                                   |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Account                 | These notifications alert recipients to the changes in the account. For instance, when a new user is added or an existing one is removed.                                     |
| Agreements              | These notifications are sent when there are changes to an agreement. For instance, when an agreement is newly created or terminated.                                          |
| Billing and Invoice     | These notifications relate to billing updates and invoices in your account. For instance, when a new statement is generated.                                                  |
| News and updates        | These notifications alert recipients to the platform news and latest announcements, such as feature releases, upcoming maintenance, and more.                                 |
| Orders                  | These notifications are sent when there's an order-related activity in your account. For instance, when you place a new order or the status of your existing order changes.   |
| Quotes                  | These notifications relate to your requests for a quotation.                                                                                                                  |
| Requests                | These notifications alert you to the submitted requests in your account. For instance, when the status of your request changes, when you need to action a request, and so on. |
| Subscriptions           | The platform sends these notifications when there are subscription-related updates to your account. For instance, renewal updates or when a new subscription is created.      |
| User updates            | These email notifications are sent when you update your profile. For instance, when you update your password. You cannot opt out of these notifications.                      |

You can manage these categories from the **Notifications** > **Subscribers** page. See [Enable or Disable Categories](enable-or-disable-categories.md) to learn more.

## Notifications interface <a href="#audit-trail-interface" id="audit-trail-interface"></a>

Account administrators can access notifications by selecting **Settings** > **Notifications** from the main menu.

<figure><img src="../../../.gitbook/assets/notifications_interface.png" alt=""><figcaption><p>Notifications page</p></figcaption></figure>

The **Notifications** page contains these three tabs: **Subscribers**, **Messages**, and **Settings**.&#x20;

### Subscribers

The **Subscribers** tab displays all [notification categories](./#notification_types) configured for your account. For each notification, you can view the following details:

* **Subscribers** - Displays the category name. Clicking the name opens the [Subscribers details page ](./#subscriber-details-page)to manage the notification's configuration. &#x20;
* **Description** - Displays a short description of the category.
* **Recipients** - Shows the total number of users and groups who are the recipients of the notifications.
* **Updated** - Shows the date and time the notification's configuration was updated.&#x20;
* **Last used** - Shows the date and time the platform sent the notification in that category.&#x20;
* **Updated by** - Displays the name and ID of the individual who updated the notification's configuration.&#x20;
* **Status** - Indicates whether the category is enabled or disabled.&#x20;

#### Subscribers details page

The **Subscribers** details page is organized into tabs displaying general information about the category and an audit trail.&#x20;

From the details page, you can manage recipients and groups for a notification category and enable or disable a category. See [Configure Recipients](configure-recipients.md) and [Enable or Disable Categories](enable-or-disable-categories.md) for details.

<figure><img src="../../../.gitbook/assets/notifications_subscribers_details.png" alt=""><figcaption><p>Subscribers details page</p></figcaption></figure>

### Messages

The **Messages** tab contains all messages sent to the users in your account. For each message, you can view the following details:

* **ID** - Displays the ID assigned to the message by the platform.
* **Contact** - Displays the recipient's email address.&#x20;
* **User** - Displays the name and ID of the individual linked to the contact. If the field is empty, it means that the recipient doesn't have an account.
* **Subject** - Displays the subject line of the email.
* **Category** - Displays the category of the notification. See [Notification categories](./#notification_types) for details.
* **Created** -
* **Created by** -
* **Status** - Displays the status of the message. To learn about the possible statuses, see [Notification States](notification-states.md).
* **Actions** - Includes the **Details** option. Selecting this option displays the **Message details** page.

#### Message details page

The **Message details** page displays general information about the message, the content of the email, file attachments, and the time and date information for the message.&#x20;

<figure><img src="../../../.gitbook/assets/notifications_message_detail.png" alt=""><figcaption><p>Message details page</p></figcaption></figure>

### Settings

The **Settings** tab allows you to view and edit your account-level notification settings, such as the sender name, the default language to be used for all emails, and the email's footer. See [Edit Notification Settings](edit-notification-settings.md) for details.&#x20;

<figure><img src="../../../.gitbook/assets/notifications_settings.png" alt=""><figcaption><p>Edit notification settings</p></figcaption></figure>
