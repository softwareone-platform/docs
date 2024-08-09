---
description: Learn how you can access and manage your software license agreements.
---

# License Agreements

A license agreement is a contract that outlines the conditions and terms under which an organization can use a specific software. Using the Client Portal's License Agreements module, you can easily view and manage your license agreements, and gain visibility into the entitlement data associated with those agreements. You can also create alerts for true-ups, renewals, and expiring contracts.

To access your license agreements, navigate to the main menu and select **Inventory** > **License agreements**.&#x20;

Watch the following video tutorial on how to access and use License Agreements:

{% embed url="https://vimeo.com/901511253" %}

## Searching for agreements

The License Agreements page contains filters to help you find the agreement you want to view or manage. You can search using:

* Agreement or Enrollment Number
* Publisher
* License Model
* Contract Category
* Start Date
* Expiration Date
* Status
* Reference
* Source

To find an agreement, specify the search parameters and then select **Search**. A list of agreements matching the criteria is displayed.

After you have found the agreement, you can view detailed information or export the agreement to any of the available formats.

## Using Grid and Timeline View options

By default, the License Agreements page displays the agreement data in a Grid View. You can customize the data to show selected columns and rearrange them in the order you wish.

You can also change the view and select **Timeline View** to view your agreements as a timeline. The timeline view allows you to track and visualize your expiring agreements.&#x20;

By selecting **Export to PDF**, you can export the timeline view to a PDF file. Note that you must have a PDF reader installed on your system to view the exported PDF document.

## Exporting license agreement reports

You can export an individual license agreement or all of your agreements.

Follow these steps to export an individual license agreement:

1. On the **License Agreements** page, find the contract you want to export.&#x20;
2. Select the actions icon (•••) and choose **Export to PDF**, **Export to CSV**, or **Export to Excel**. Your report is queued for processing and a confirmation message is displayed.&#x20;

Follow these steps to export all of your license agreements:

1. On the **License Agreements** page, hover over the **Exports** option and select **Contracts**. The **Create New Report - Contracts** page opens.
2. Choose the format for your report, and schedule frequency, and specify the start and the expiration date of your contract.&#x20;
3. Select a template and provide a name for your report. If you don't want to use any template, choose **None** from the list.&#x20;
4. Choose the delivery method and then select **Run** or **Create**, depending on whether you are creating a run once or a scheduled report.

Once your export is complete, you can view it by hovering over **Exports** and selecting **Go to My Reports**. This link will take you directly to your generated reports page.&#x20;

Alternatively, select the main menu of the Client Portal and navigate to **Analyze** > **Reports**. To learn more about reports and their features, see [Reports](../other-tools/reports/).

## **Exporting** expiration **date to Outlook**

You can export an agreement expiration date to Outlook to keep track of your expiring agreements.&#x20;

Note that Outlook reminders can only be set for contracts that have an end date specified. If the contract doesn't have an end date, a message is displayed.

Follow these steps to set up a reminder in Outlook:

1. On the License Agreements page, search for your agreement.
2. Do one of the following:
   * Select the actions icon and choose **Outlook Export**.&#x20;
   * Open the agreement and select **Outlook Export** in the upper right.&#x20;
3. When the download completes, open the downloaded file in Outlook.
4. Verify the agreement details and save the event in your calendar.

## Viewing agreement details

You can view the details of your agreement by selecting it from the License Agreements page. When the License Agreement Details page opens, the following information is displayed:

| Field                    | Description                                                                                                                                                                                                                                                                                 |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Description              | The name of the agreement.                                                                                                                                                                                                                                                                  |
| Publisher                | The publisher of the software for which the agreement is created.                                                                                                                                                                                                                           |
| SoftwareOne Contract No. | A unique number assigned to your agreement by SoftwareOne.                                                                                                                                                                                                                                  |
| Contract Duration        | <p>The start and expiration date of the agreement. The duration also shows the agreement status:</p><ul><li>Red indicates that your agreement has expired.</li><li>Yellow indicates that your agreement is expiring soon.</li><li>Green indicates that your agreement is active. </li></ul> |
| License Model            | The licensing model that applies to your contract.                                                                                                                                                                                                                                          |
| Agreement No.            | A unique number assigned to your agreement by the publisher.                                                                                                                                                                                                                                |
| Remaining Days           | The number of days remaining before your contract expires.                                                                                                                                                                                                                                  |
| Customer Name            | The name of the customer.                                                                                                                                                                                                                                                                   |
| Contract Type            | The type of contract.                                                                                                                                                                                                                                                                       |
| Enrollment No.           | The enrollment number assigned to your contract by the publisher.                                                                                                                                                                                                                           |
| Anniversary Date         | The renewal date of the agreement.                                                                                                                                                                                                                                                          |
| Currency                 | The currency of the agreement.                                                                                                                                                                                                                                                              |
| Level                    | The price level of the agreement.                                                                                                                                                                                                                                                           |
| Comments                 | Option to add and save your comments.                                                                                                                                                                                                                                                       |

The details page also contains tabs that you can use to view and manage specific details.

{% tabs %}
{% tab title="Keys" %}
Displays a list of products associated with the agreement and their license keys. You can also add new license keys or delete existing keys.

**Adding keys**

You can add a new license key by selecting **Add License Key** and providing the product name and the license key.

**Deleting keys**

You can delete a key by selecting **Delete** from the **Actions** column.&#x20;
{% endtab %}

{% tab title="Documents" %}
Displays a list of documents associated with the agreement, such as license certificates and purchase orders (if applicable)_._ You can add, download, and delete these documents.

**Adding new documents**

You can add new documents by selecting **Add a Document** and then uploading the document. To upload, select the file from your system or drag the file into the location.&#x20;

**Deleting documents**

You can delete a document by selecting **Delete** from the **Actions** column. Note that deleted documents cannot be recovered.

**Downloading documents**

You can download a document by either clicking the filename or by selecting **Open** from the **Actions** column.
{% endtab %}

{% tab title="Companies" %}
Displays the company/entity that is associated with the agreement. Note that you cannot modify any information on this tab.&#x20;
{% endtab %}

{% tab title="Alerts" %}
Displays all alerts for the agreement and allows you to create and delete alerts.&#x20;

**Adding new alerts**

You can add a new alert by selecting **Add Alert**. When the Add Alert page opens, add a subject line and then specify the email address to which the alert should be sent. Note that you can add three email addresses separated by a semicolon.&#x20;

Next, choose the alert type (**Agreement Expiration**, **True Up**, or **Renewal**) and specify how frequently you wish to be notified. You can select the frequency from the list or enter a date.&#x20;

**Delete alerts**

You can delete an alert by selecting **Delete** from the **Actions** column.
{% endtab %}

{% tab title="Related Documents" %}
Displays transactions, such as quotes, orders, invoices, and credit memos associated with the agreement. You can view the transaction details and export the information to PDF or Excel.

**Viewing details**

You can view the details by selecting the row or by selecting **View** from the **Actions** column.&#x20;

**Exporting files**

You can export the information by selecting the actions icon (•••) and choosing **Export to PDF**, **Export to Excel (CSV)**, or **Export to Excel (XLSX)**.
{% endtab %}
{% endtabs %}
