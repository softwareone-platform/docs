# Reports

## About Reports

The Client Portal offers a large number of reports, allowing you to gain valuable insights into your software asset inventory, resource utilization, cloud consumption, renewals, and more.

You can set up a report using the **Quick Reports** feature or create a customized report using the available report options. You can also:&#x20;

* Export your reports to any of the available formats.
* Run and publish reports only once, daily, weekly, or monthly.
* Modify report configuration and existing schedule.&#x20;
* Delete reports.
* Pause or resume scheduled reports.
* View, search, and share reports.
* Create report templates.

## How to access the Reports page

You can access the **Reports** page by navigating to the main menu and selecting **Other tools** > **Reports**.

{% hint style="info" %}
Access to the **Reports** feature depends on your user permissions and role. Additionally, each report type has specific permissions, and reports are generated with their owner's permission
{% endhint %}

## Quick Reports <a href="#post-4285-_ref38442975" id="post-4285-_ref38442975"></a>

The **Quick Reports** tab displays all report options that are available to you and allows you to create a new report based on predefined filters quickly. Note that by default, all quick reports are created as Run Once only.

### Create a quick report <a href="#post-4285-_ref38442975" id="post-4285-_ref38442975"></a>

Follow these steps to create a quick report:

1. From the main menu, navigate to **Other tools** > **Reports**.
2. On the **Quick Reports** tab, navigate to the report group and choose the reporting template from the menu.&#x20;
3. Select **Create**. The **Create Quick Report** page opens.&#x20;
4. Review the report summary, name, and delivery method. Note that you can adjust the details and apply filters as needed.
5. Select **Finish**. Your report is created and a confirmation message is displayed.

Watch the following video tutorial on how to create a Software Asset Inventory quick report:

{% embed url="https://vimeo.com/889172885" %}

## Scheduled Reports

The **Scheduled** tab displays the scheduled report configurations and allows you to edit, run, pause, resume, preview, and delete reports.&#x20;

Note that you must have the `SCHEDULED_REPORTING` permission to access this tab.&#x20;

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Scheduled tab</p></figcaption></figure>

On this tab, you can view the following details:

* **Name** - The name of the report.
* **Frequency** - Indicates if this is a **Daily**, **Weekly,** or **Monthly** report. **Off** means that recurrence for the report is not yet defined (this is only possible when the report has been created using old reporting).
* **Status** - Indicates whether the report is being generated or paused.
* **Delivery** - The delivery format for the report.
* **Last Report** - The time when the report was last generated.
* **Created** - The date and time when the report was created.
* **Next Report** - The time when the next report will be generated.
* **Group** - The type of the report group.
* **Recipients**­ - The email address of the recipient.
* **Render type** - The format of the report.
* **Type** - The type of report.
* **Template** - Indicates whether any template has been selected for the report.
* **Last Modified** - The date and time of the last update of the report configuration (in the local time zone).
* **Actions** - The list of actions for the report.

### Create a scheduled report <a href="#post-4285-_ref38442975" id="post-4285-_ref38442975"></a>

Follow these steps to create a new report:

{% hint style="info" %}
When creating a new report, the available options vary based on the type of report. Some reports can be run once only, whereas others can be run once or scheduled periodically. Similarly, some reports support report templates, while others don't. For each report type, you can view the available options when you are creating the report.
{% endhint %}

1. Navigate to the Reports page (**Other tools** > **Reports**) and click **Create New Report**.
2. Select the report group and the type of report, and then choose the format in which you wish to generate the report. Note that the format varies depending on the report.&#x20;
3. Choose the filters and select **Next**. To set additional filters (related to dates and number formatting), select **Show more formatting options**.

<details>

<summary>Learn about report filters</summary>

Filters allow you to restrict the data that appears in a report. The list of available filters depends on the selected report type. The following are the common filters:

* **SoftwareOne Company**: Allows you to restrict data in a report to only selected SoftwareOne companies. This is a multi-select field. If none is selected, the data for all SoftwareOne companies is included.
* **Also include countries added in the future**: When selected, any new countries added in the future will be automatically added to the report.
* **Companies**: Allows you to restrict data in a report to selected companies. Users can select multiple companies. If none are selected, then data for all companies will be included.
* **Also include companies added in the future**: When selected, any new companies added in the future will be automatically added to the report.

</details>

4. Select the schedule type. You can run the report once, daily, weekly, or monthly. Note that for the reports that can be run once only, the **Run Once** option is selected by default and you cannot change it. All other options are unavailable.
5. Select the date range for the data you want to include in the report.
6. Select an existing template from **Saved Templates** or create a new template. Note that the **Saved Templates** option is displayed only if the report supports templates. If the report does support templates, but you choose not to apply the template, the system will use the default template.
7. Provide a unique **Report Name** and choose the report delivery method.
8. Select **Finish**. A confirmation message is displayed.&#x20;

Depending on your chosen report schedule, the **Scheduled Reports** page or the **Reports History** page is displayed. Note that all Run Once reports are triggered immediately.

### Update a scheduled report <a href="#post-988-_ref38824725" id="post-988-_ref38824725"></a>

You can update the configuration of a scheduled report, except the report group and the type of report.&#x20;

To update a report, select the actions icon (•••) and choose **Edit**. When the Edit Scheduled Report page opens, make changes as necessary and then click **Finish** to save your changes.

### Run a scheduled report <a href="#post-988-_toc51828560" id="post-988-_toc51828560"></a>

You can trigger scheduled reports at any time. After a report is generated, it downloads automatically and is available on the **History** tab. To run a report, select **Download** in the **Actions** column.

Note that triggering a report manually doesn’t impact its next generation time or the last execution time in the **Last Report**.

### Pause or resume a scheduled report <a href="#post-988-_ref38458440" id="post-988-_ref38458440"></a>

To pause or resume a report, select the actions icon (•••) and select **Pause** to pause the report or select **Resume** to reactivate the paused report.

### Delete a scheduled report <a href="#post-988-_toc51828562" id="post-988-_toc51828562"></a>

To delete a scheduled report, select the actions icon (•••) and choose **Delete**.&#x20;

Next, confirm that you want to delete the report. Note that deleted reports cannot be recovered.&#x20;

## Report History <a href="#post-988-_toc51828563" id="post-988-_toc51828563"></a>

The **History** tab displays all reports that you've generated. The list includes scheduled and run-once reports. From the **Reports History** page, you can download, send, delete, or edit a report.

<figure><img src="../../../.gitbook/assets/image (276).png" alt=""><figcaption><p>History tab</p></figcaption></figure>

On this tab, you can view the following details:

* **File Name** - The file name of the report (visible only for generated reports).
* **Report Type** - The output format of the report.
* **Time Requested** - The approximate time when the report has been requested.
* Status - The status of the report. Possible values include:
  * **Queued** - The report is queued for creation.
  * **Processing** - The report is being generated.
  * **Ready** - The report has been generated and can be downloaded.
  * **Report Ready - SFTP Failed** - The report has been generated but there was an issue when sending it to the configured SFTP server. You can manually download the report and send it to an SFTP.
  * **No Data** - The generated report contains no data.
  * **Error** - There was an unexpected error during the report generation.
  * **Error – Bad Configuration** - There was an error in the report configuration.&#x20;
  * **No permissions** - The report couldn’t be generated because the user no longer has permissions.
* **Report Name** - The name of the report.
* **Recipients** - The list of recipients for the **Email** delivery method only.
* **File Size** - The size of the generated report file (visible only for generated reports).
* **Scheduled -** The information whether it is **Scheduled** or **Run Once** report.
* **Actions** - The list of actions for reports.

### Download reports <a href="#post-988-_toc51828570" id="post-988-_toc51828570"></a>

You can download a single or multiple reports from the **History** tab.

Follow these steps to download a report:

1. Locate the report or select the checkbox for the report you wish to download. You can select multiple checkboxes.
2. Do one of the following:
   * In the **Actions** column, click **Download**.
   * From the **Actions** menu above the table, choose **Download**, **Copy to ZIP file**, or **Move to Zip File**. Note that this menu is enabled only after you select a checkbox.

### Edit the report name <a href="#post-988-_toc51828570" id="post-988-_toc51828570"></a>

You can only update the name of a generated report and file name. Updating a generated report name doesn't change the scheduled report name based on which the report has been generated.

Follow these steps to update a report or file name:

1. Select the actions icon (•••) and choose **Edit**. The edit mode is enabled.
2. Update the report name and file name as needed. Note that the file name must include an extension, Invoices.xlsx.
3. Update your changes.

### Email a report <a href="#post-988-_toc51828566" id="post-988-_toc51828566"></a>

If a report is bigger than 25 MB, it's always sent as a link only. Note that to download a report from the link, your email recipients must have access to the report in the Client Portal.

Follow these steps to send a report through email:

1. Select the actions icon (•••) and then choose **Email**.
2. Provide the email addresses (separated by a semicolon) and choose if you want to send the report as an **Attachment** or **Link**.&#x20;
3. Send your report.

### Send a report to an SFTP server <a href="#post-988-_ref51684117" id="post-988-_ref51684117"></a>

You can send a report directly to a secure FTP server. If needed, you can also add a new SFTP configuration or edit the existing configuration.&#x20;

Follow these steps to send a report to an SFTP:

1. Select the actions icon (•••) and select **SFTP**.&#x20;
2. Select an SFTP server from the list and choose **Use Selected Server**.

### Delete a report

You can delete reports that are no longer needed. You can delete a single report or multiple reports at once. Note that once you delete a report, it can't be recovered.

Follow these steps to delete a report:

1. Locate the report or select the checkbox for the report you wish to delete.
2. Do one of the following:
   * Select the actions icon (•••) and then select **Delete**.
   * From the **Actions** menu,  choose **Delete**.  Note that this menu is enabled only after you select a checkbox.
3. Confirm that you want to delete the report.

## Report Templates

### Create a report template

You can create a new template when you are creating a report. Note that only some reports support templates.&#x20;

Follow these steps to create a template:

1. On the **Reports** page, select **Create new report**.
2. On the Template page, select **Saved Templates** > **Edit Default Columns**.&#x20;
3. Make changes as needed and select **Save as new template**.&#x20;
   * To change a column position, drag the column to the desired position. You can move columns between groups.
   * To move all columns from one group to another, drag the entire group to an unfolded group.
   * To override a column’s value, enter a new value in the **Override value.**
   * To duplicate or delete a column, select the actions icon ( ••• ) and choose **Duplicate** or **Delete**.
4. Provide the **Template Name** and choose whether the template is **Personal** (only you can see or edit it) or **Shared** (anyone in your company can see or edit it).
5. Select **Save as new template**.

**Column Descriptions**

| Column           | Descriptions                                                                                                                                                                                                        |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Order            | The position of the column in the report.                                                                                                                                                                           |
| Name             | <p>The default name of the column (as it will be shown in the generated report if the Name override is empty). </p><p></p><p>To override a column’s name, provide a new name in <strong>Name override</strong>.</p> |
| Name override    | The column name that will be visible in a report. If blank, the column name from Name will be used.                                                                                                                 |
| Override value   | The value that will be visible in a report for the column. If blank, then generated data will be used.                                                                                                              |
| Value when blank | The value that will be visible in a report if there is no data for the column.                                                                                                                                      |
| Max text length  | The maximum number of characters for the field. Blank means no limitation.                                                                                                                                          |
| Actions          | The list of actions for a column.                                                                                                                                                                                   |

### Edit or delete a report template <a href="#post-4285-_toc51828553" id="post-4285-_toc51828553"></a>

{% hint style="info" %}
* You can edit all templates, except the default template.&#x20;
* You can only delete templates that are not used in other reports. Additionally, removing a template doesn’t impact already generated reports.
* Deleted templates cannot be recovered.&#x20;
{% endhint %}

To update or delete a template, select the template and choose **Edit or Delete**.

<figure><img src="../../../.gitbook/assets/image (173).png" alt=""><figcaption><p>Edit or delete a template</p></figcaption></figure>
