---
description: >-
  You can generate reports for all quotes and orders, and schedule reports to
  run at a chosen time and frequency.
---

# Software Transaction Reports

The Client Portal reporting offers an easy way to create reports based on the stored data.

* **Report Wizard:** Use the wizard to create and update report configurations.
* **Scheduled Reports**: Use to access defined report configurations.
* **Reports History:** Use to view generated reports.
* **Quick Reports:** Use to quickly create new reports.
* **On-Page reporting**: Use to create and run reports.

You can create single-run reports (Run Once) and recurring (e.g. monthly) reports.&#x20;

Access to the Reporting components is restricted to authorized users and depends on their roles. In addition, each report type has its own specific permission.

Reports are generated with their creators’ permission.

{% hint style="info" %}
**NOTE**: We support the latest stable versions of the most popular browsers (desktop only): Chrome, Edge, and Firefox. On-Page reporting (together with old reporting) is supported for Punchout users.
{% endhint %}

### Scheduled reports <a href="#post-988-_ref38294240" id="post-988-_ref38294240"></a>

You can find Scheduled report configurations (for your company) on the Scheduled Reports view. You can edit, run, pause, resume, preview, and delete reports.

To open Scheduled Reports, navigate to **Analyze** > **Scheduled**. You must have the SCHEDULED\_REPORTING permission to access this component.

#### Column Descriptions <a href="#post-988-_toc51828558" id="post-988-_toc51828558"></a>

You can show, hide, and change the order of the columns.

| Column                 | Description                                                                                                                                                                                                                                                                            |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**               | Name of the report.                                                                                                                                                                                                                                                                    |
| **Frequency**          | Shows if this is a **Daily**, **Weekly,** or **Monthly** report, see [Schedule](software-transaction-reports.md#post-988-\_ref38374532). **Off** means that recurrence for the report is not yet defined (this is only possible when the report has been created using old reporting). |
| **Status**             | Shows whether the report generation is turned on (**Running**) or generation has been paused (**Paused**).                                                                                                                                                                             |
| **Delivery Method**    | Shows how generated reports will be delivered, see also Report delivery method.                                                                                                                                                                                                        |
| **Next Report**        | Shows the time of next report generation.                                                                                                                                                                                                                                              |
| **Last Report**        | Shows the last report generation time (in the local time zone).                                                                                                                                                                                                                        |
| **Last Modified**      | Shows the date and time of the last update of the report configuration (in the local time zone).                                                                                                                                                                                       |
| **Created**            | Shows the date and time of the report configuration creation (in the local time zone).                                                                                                                                                                                                 |
| **Group** and **Type** | The group and type of the report.                                                                                                                                                                                                                                                      |
| **Render type**        | For information about the output format of the report, see [Report Output Formats](software-transaction-reports.md#post-988-\_toc51828576).                                                                                                                                            |
| **Recipients­**        | List of email recipients (for **Email** delivery method only)                                                                                                                                                                                                                          |
| **Template**           | Shows which template (if any) has been selected for the report                                                                                                                                                                                                                         |
| **Actions**            | List of actions for a report.                                                                                                                                                                                                                                                          |

For more information about grid functionality (like sorting, filtering, grouping, or showing/hiding columns) see the [Grid Functionality](software-transaction-reports.md#post-988-\_ref38437292) section.

#### Update a report <a href="#post-988-_ref38824725" id="post-988-_ref38824725"></a>

You can update the scheduled report configuration (except its group and type) in the Report Wizard.

To start updating a report click (**…**) in the **Actions** column, and click **Edit**.

#### Run a report <a href="#post-988-_toc51828560" id="post-988-_toc51828560"></a>

You can trigger scheduled reports at any time. After the report is generated, it will automatically download. Like any other generated report, it will also be available in Reports History. Triggering reports manually doesn’t impact its next generation time (nor will it update its last execution time in the **Last Report**).

To run a report click **Download** in the **Actions** column.

#### Pause or resume a report <a href="#post-988-_ref38458440" id="post-988-_ref38458440"></a>

You can pause (or resume) a generating report. The status of a report (whether it is **Running** or **Paused**) is visible in **Status**.

To pause or resume a report click (**…**) in the **Actions** column and click **Pause** (to pause the generating report) or **Resume** (to re-activate the paused report).

![](<../../.gitbook/assets/image (200).png>)

#### Delete a report <a href="#post-988-_toc51828562" id="post-988-_toc51828562"></a>

You can delete a scheduled report configuration. Deleted reports can’t be recovered. Removing the scheduled report configuration does not remove reports that have already been generated (which can be found in Reports History).

To delete a report configuration, click (**…**) in the **Actions** column and click **Delete.** Then click **Delete scheduled report** in the confirmation dialog.

### Reports history <a href="#post-988-_toc51828563" id="post-988-_toc51828563"></a>

In the Reports History view, you can find generated reports (Scheduled and Run Once). You can download, send, delete, or edit the name of a report.

To open Reports History, navigate to **Analyze** -> **History**. On pages supporting “On Page” reporting you can also click **Exports** and click **Go to My Reports**.

<figure><img src="../../.gitbook/assets/image (201).png" alt=""><figcaption></figcaption></figure>

#### Column Descriptions <a href="#post-988-_toc51828564" id="post-988-_toc51828564"></a>

You can show, hide and change the order of the columns.

|                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Report Name**     | Name of the report.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Report Type**     | Output format of the report                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Time Requested**  | Approximate time when the report has been requested                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Scheduled**       | Information whether it is Scheduled or Run Once report.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Status**          | <p>status of the report:</p><ul><li><strong>Queued</strong> – the report is queued for creation.</li><li><strong>Processing</strong> – the report is being generated.</li><li><strong>Ready</strong> – the report has been generated and can be downloaded (see Download a report).</li><li><strong>Report Ready – SFTP Failed</strong> – The report has been generated but there was an issue when sending it to the configured sFTP server. The report can be manually downloaded or resend to an SFTP.</li><li><strong>No Data</strong> – The generated report contains no data.</li><li><strong>Error</strong> – There was an unexpected error during the report generation.</li><li><strong>Error – Bad Configuration</strong> – There was an error in the report configuration at the time of running it. The user shall check the report configuration and fix the issue.</li><li><strong>No permissions</strong> – the report couldn’t be generated because a user has no longer permission to data.</li></ul> |
| **File Name**       | File name of the report (visible only for generated reports).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **File Size**       | The size of the generated report file (visible only for generated reports).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Recipients**      | List of recipients of the report (for **Email** delivery method only, see Report delivery method).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Actions**         | List of actions for reports.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |

For more information about grid functionalities (like sorting, filtering, grouping, or showing/hiding columns) see the [Grid Functionally](software-transaction-reports.md#post-988-\_ref38437292) section.

You can also perform certain actions on multiple reports at once. To select reports, click on the checkboxes in the first column (information about a number of selected reports can be found just above the grid), To select all reports click **Select All**, to clear selection click **Clear Selection**. When at least one report is selected, **Actions** (located above the grid) will be enabled.

<figure><img src="../../.gitbook/assets/image (202).png" alt=""><figcaption></figcaption></figure>

#### Download a report <a href="#post-988-_ref39076953" id="post-988-_ref39076953"></a>

To download a generated report, select **Download** in the **Actions** column.

To download multiple reports at once, select up to ten reports, select **Actions** (above the grid), and click **Download**.

#### Send a report via email <a href="#post-988-_toc51828566" id="post-988-_toc51828566"></a>

To send a report via email, click (**…**) in the **Actions** column and click **Email**. In the opened dialog, enter email addresses (separated by semicolon), select whether the report shall be send as an **Attachment** or **Link,** and click **Send**.

{% hint style="info" %}
**Note**: If a report’s size is bigger than 25 MB, it will be always sent as a link only. To be able to download a report from the link, the email recipients need to have access to the report in PyraCloud.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (203).png" alt=""><figcaption></figcaption></figure>

#### Send a report to secure FTP server <a href="#post-988-_ref51684117" id="post-988-_ref51684117"></a>

You can send a report directly to a secure FTP server.

To send a report to sFTP, click (**…**) in the **Actions** column and click **sFTP**. Select an sFTP server from the list and click **Use Selected Server**.

<figure><img src="../../.gitbook/assets/image (204).png" alt=""><figcaption></figcaption></figure>

If needed, you can add a new SFTP configuration or edit an existing one. See the [sFTP Configuration](software-transaction-reports.md#post-988-\_ref38826088) section for more details.

#### Copy or move reports to Zip File <a href="#post-988-_toc51828568" id="post-988-_toc51828568"></a>

To copy or move reports to a zip archive (e.g. to download or send them later), select up to ten reports, click **Actions** (above the grid) and click **Copy to zip File** or **Move to zip File**.&#x20;

If **Move to zip File** has been selected, the moved reports will be automatically deleted (only zip file with the reports will still be available).

#### Delete a report <a href="#post-988-_toc51828569" id="post-988-_toc51828569"></a>

You can delete a generated report. Deleted reports can’t be recovered.

To delete a report click (**…**) in the **Actions** column and click **Delete**. In the opened dialog, click **Delete report**.

To delete multiple reports, select them all, click **Actions** (above the grid) and click **Delete.**

#### Update a report and file names <a href="#post-988-_toc51828570" id="post-988-_toc51828570"></a>

You can update a generated report name and file name. Updating a generated report name does not change the scheduled report name based on which the report has been generated.

To update a report or file name click (**…**) in the **Actions** column and click **Edit**. Update the values and click **Update**.

<figure><img src="../../.gitbook/assets/image (205).png" alt=""><figcaption></figcaption></figure>

#### Report an issue <a href="#post-988-_ref38609555" id="post-988-_ref38609555"></a>

To report an issue with a report click **Report the problem** in the **Actions** column, enter a description, and click **Submit**.

### Quick reports <a href="#post-988-_ref38740623" id="post-988-_ref38740623"></a>

Quick Reports allow you to quickly create new reports using the Report Wizard, which will be opened with predefined filters (by default, Quick Reports are Run Once reports).

To open Quick Reports, navigate to **Analyze** > **Quick Reports**.

To create a Quick Report, select a report type and click **Create** – this will open the Report Wizard at the Delivery step. You can go back to any of the previous steps to make modifications or just click **Finish**.

### On-Page reporting <a href="#post-988-_toc51828573" id="post-988-_toc51828573"></a>

On some PyraCloud pages, it is possible to create new reports (Run Once and Scheduled) directly from the page. You can find **Exports** (top right) on pages that support On Page reporting.

To create a report using “**On-Page**” reporting, select **Exports** and select the report type you require, or click on the **Create / Schedule Report** option.

On Page reporting offers a simplified editor for defining new report configurations. If needed, you can easily continue to report configuration in the Report Wizard.

All users have permission to this component.

On the On-Page reporting form, you can select **Format** (see [Report Output Format](software-transaction-reports.md#post-988-\_toc51828576)), schedule (see [Schedule](software-transaction-reports.md#post-988-\_ref38374532)) and data date range (see [Date Range](software-transaction-reports.md#post-988-\_toc51828583)), select a **Template,** update the default name and set delivery method (see [Report Delivery Method](software-transaction-reports.md#post-988-\_toc51828584)).

<figure><img src="../../.gitbook/assets/image (206).png" alt=""><figcaption></figcaption></figure>

**Note**: The filters applied on a page will also be visible in the opened on-page reporting form.

<figure><img src="../../.gitbook/assets/image (207).png" alt=""><figcaption></figcaption></figure>

To create a report, click **Run**.

#### Continue report creation in the report wizard <a href="#post-988-_toc51828574" id="post-988-_toc51828574"></a>

If more advanced settings are needed, you can continue report creation in Report Wizard.

To open the Wizard click **Go to Advanced Reporting** (at the bottom of the form), and you will be transferred to the Wizard. Report creation in the Report Wizard is only available for some report types.

### Format, schedule, date range, and delivery <a href="#post-988-_toc51828575" id="post-988-_toc51828575"></a>

The following report configuration options are common for Report Wizard and On Page reporting.

#### Report Output Formats <a href="#post-988-_toc51828576" id="post-988-_toc51828576"></a>

Most of the reports can be generated in various formats (available formats depend on the report type).

<figure><img src="../../.gitbook/assets/image (208).png" alt=""><figcaption></figcaption></figure>

Additional options are available for some formats:

* **CSV - CSV Delimiter:** You can select a delimiter that will be used for CSV files
* **ZIP - Max Files per Archive:** You can select the maximum number of files per archive (if there are more files, multiple zip files will be created)
* **CIF - CIF Headers:** The headers can be configured in the “Type” step in the Report Wizard.

**Add CIF Header**

To add a CIF Header click **Add New CIF Header** (the new header will be added at the top).

**Update CIF Header**

To update the **Key** or **Value** of a CIF Header, click on the cell and update the value.

**Delete CIF Header**

To delete a CIF Header, click **Delete** in **Actions** column.

#### Schedule <a href="#post-988-_ref38374532" id="post-988-_ref38374532"></a>

You can create a Run Once report (that will be executed only once, and its configuration won’t be saved in Scheduled Reports), or a Scheduled report (with a recurrence type like daily or monthly, and its configuration will be saved in Scheduled Reports). Available recurrence types depend on the selected report type.

**Note**: You need to have permission to create Scheduled reports (Run Once are available to everyone).

**Run once reports**

The Run Once option is for reports that you want to run only once (no new report definition will be created, so you will not be able to open or edit the configuration later).

**Scheduled reports (Daily/Weekly/Monthly)**

For Scheduled reports, you can select how many days/weeks/months the report should be run (available options depend on the selected report type), as well as what time, and the duration.

To help to validate if the selected recurrence configuration is correct, information about the report’s next run time will be displayed.

**Select how often a report shall be generated**

To select how often a report shall be generated, first select one of the recurrence types, e.g. **Daily**, **Weekly** or **Monthly,** and then enter a number of how often you want the report to run in the **Every** field e.g. to run a report every two weeks.

Additional options for selected recurrence types:

* **Daily:** You can select whether reports should also be generated on weekends, by checking **Include weekends**
* **Weekly:** You can select on which days of the week the report should be generated. To select a day, click on **Days of the week**. The example below shows a report that will be generated each Monday and Thursday
* **Monthly** – You can select a specific day of the month or e.g. **First** **Weekday**

**Select at what time of day a report will be generated**

To choose the time of day a report should be generated, select the **Time** and **Time Zone**. Your local time zone is selected by default (except on IE11 due to the browser’s limitations).

**Select duration**

To set when the report generation should start, enter a date in **Starting from**.

By default, a report will have no end date and will be set to Run forever. To set an end date, click on the button next to **Run forever** to switch it to a date field and enter a date in the **until** field.

#### Date Range <a href="#post-988-_toc51828583" id="post-988-_toc51828583"></a>

Some report types allow you to select the data’s date range(s) for the report (Scheduled and Run Once).

For Scheduled reports, the data’s date range would be set to the same as the report’s run dates.

To help validate if the selected date range(s) are correct, information about the report’s next run time, with date range, will be displayed.

You can select one of the pre-defined values from **Date Range**, like **Last Month** (which means last calendar month) or **Current Year**, or you can set a period of time manually by selecting **Choose Date Range**.

* **2 Weeks(s)** – means last 14 days counting from the date of a report execution
* **1 Day(s)** – means one day before the date of the report execution

For Run Once reports, you can select one of the predefined ranges or select the dates manually.

#### Report Delivery Method <a href="#post-988-_toc51828584" id="post-988-_toc51828584"></a>

Allows you to select a delivery method for generated reports. Only one method can be selected, but all generated reports are also available in Reports History.

**Download**

This is the default delivery method. The generated report will be available to download from Reports History.

**Email**

The option allows you to send generated reports to an e-mail address.

To set email as the delivery method, click **Email**, and enter the email address in **To** and **CC** (separated by semicolon).

You can also select the maximum attachment size and select whether the report should be sent as an attachment, or if only a link to it shall be added to a message.

**SFTP**

To send the report to an sFTP (secure FTP), click on **sFTP** and select one of the existing configurations or create a new one.&#x20;

### SFTP configuration <a href="#post-988-_ref38826088" id="post-988-_ref38826088"></a>

#### Add a new SFTP configuration <a href="#post-988-_toc51828589" id="post-988-_toc51828589"></a>

To add a new sFTP configuration click **Add New SFTP**. In the opened dialog, fill in the fields and click **Create.**

#### Edit an SFTP configuration <a href="#post-988-_toc51828590" id="post-988-_toc51828590"></a>

To update an sFTP configuration, click **Edit** in **Actions** column. In opened dialog update fields and click **Update.**

#### Delete an SFTP configuration <a href="#post-988-_toc51828591" id="post-988-_toc51828591"></a>

You can delete an sFTP configuration if it is not used in any of the Scheduled reports.

To delete an sFTP configuration, click **Delete** in the **Actions** column and then click **OK** in the confirmation dialog.

### Grid functionality <a href="#post-988-_ref38437292" id="post-988-_ref38437292"></a>

PyraCloud grids allow you to select which columns should be displayed, and in what order. Filtering and grouping data or selecting how many rows should be visible on a single page.

#### Show and hide columns <a href="#post-988-_toc51828593" id="post-988-_toc51828593"></a>

To show or hide a column, click **Customize** (just above the grid, on the right), and click on a column name.

#### Reorder columns <a href="#post-988-_toc51828594" id="post-988-_toc51828594"></a>

To reorder columns, drag a column header and drop it into its new position.

#### Sort data <a href="#post-988-_toc51828595" id="post-988-_toc51828595"></a>

To sort data by column values, click on a column’s header. To change the order click on the columns header again. The third click turns off sorting. An arrow (up or down) next to the column’s header name indicates if and what sorting is applied. It is only possible to sort by one column at a time.

#### Filter data <a href="#post-988-_toc51828596" id="post-988-_toc51828596"></a>

You can set up to two filters for a single column. To filter data in a column, click on a filter icon in the column’s header.

#### Group data <a href="#post-988-_toc51828597" id="post-988-_toc51828597"></a>

To group data in the grid, drag a column header and drop it just above the columns’ headers. You can group data using multiple columns and can change the order of grouping by changing the order of labels (using drag & drop). To change the sorting of a group, click on the label – a small arrow will indicate the direction of sorting. To remove grouping, click **x** next to the group name.

#### Show more or fewer rows <a href="#post-988-_toc51828598" id="post-988-_toc51828598"></a>

To change the number of rows visible on a page, select one of the values in **Show** (just above the grid).
