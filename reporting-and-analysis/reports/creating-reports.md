---
description: You can create various types of reports using the Reports module.
---

# Creating reports

Using the Reports module, you can create single-run as well as recurring scheduled reports. You can also edit the existing Scheduled report configurations.&#x20;

Access to the Reports module depends on your user permissions and job role. In addition, each report type has its own specific permission. Reports are generated with their creators’ permission.

The Reports module supports the latest stable versions of the most popular browsers (desktop only), including Chrome, Edge, and Firefox. On Page reporting (together with old reporting) are supported for Punchout users.

***

### Creating a new report  <a href="#post-4285-_ref38442975" id="post-4285-_ref38442975"></a>

**To create a new report**

1. From the main menu, navigate to **Analyze** and select **Reports**.
2. Select **Create New Report**.
3. Select the type and output format of the report. Available report types depend on your permissions. There are a large number of report types, which are grouped into business areas. To select a report type, first select **Group** and then **Type**.

<div align="left">

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/11/41-1.png" alt=""><figcaption></figcaption></figure>

</div>

4. Choose the filters. Filters allow you to restrict the data that appear in a report (the date range for data can be set in the Date Range step). Available filters depend on the selected report type. Common filters:
   * SoftwareONE Company – allows you to restrict data in a report to only selected SoftwareONE companies. This is a multi-select field. If none are selected, then data for all SoftwareONE companies will be included.
   * Also include countries added in the future – if checked, then any new countries added in the future will be automatically added to the report.
   * **Companies** – allows you to restrict data in a report to selected companies. Users can select multiple companies. If none are selected, then data for all companies will be included.
   * Also include companies added in the future – if checked, then any new companies added in the future will be automatically added to the report

To set additional filters (related to dates and number formatting, and also whether empty reports shall be generated) click **Show more formatting options** (only available for some report types).

* **Date Format** – You can select your preferred date format for reports generated. By default, the regional format settings defined in **My Profile** are selected (not applicable to PDF reports)
* **Decimal Separator** – Allows you to select a separator for decimal numbers (not applicable to PDF nor JSON reports)
* **Report Contains No Data** – If a generated report is empty, you can decide if the report should be delivered or not

5. Choose the report schedule.
6. Select the date range for the data in the report.
7. Create a new template or select an existing one (if the report type supports templates). If no template is selected, a default template with all visible columns for that given report type will be applied. If there are existing templates for the report type, you can find them under **Saved Templates.**&#x20;
8. Provide a unique **Report Name** and choose the report delivery method.
9. Select **Finish**.&#x20;

You will be redirected to Scheduled Reports (if a Scheduled report was created) or to Reports History (if a Run Once report was created). Run Once reports are triggered immediately.

***

### Creating a template

Click **Edit Default Columns** to start creating a template (if there are already existing templates for the report type, the option is under **Saved Templates**).

You can apply all required modifications and click **Save as new template** to save it. In the opened dialog window, enter the **Template Name** and select whether the template shall be **Personal** (only the user can see or edit it) or **Shared** (anyone in user’s entire company can see or edit it), and click **Save as new template.**

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/11/131-1.png" alt=""><figcaption></figcaption></figure>

Columns and their default grouping depend on the selected report type (not all templates utilize grouping of columns). Column grouping is applied in the template editor to facilitate its creation (column grouping is not visible in generated reports). To unfold or fold a group, click on the group name.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/11/141-1-1024x301.png" alt=""><figcaption></figcaption></figure>

**Column Descriptions**

* Order – position of the column in the report
* Name – default name of the column (as it will be shown in the generated report if Name override is empty)
* Name override – column name that will be visible in a report (if blank, then column name from Name will be used)
* Override value – value that will be visible in a report for the column. If left blank, then generated data will be used
* Value when blank – value that will be visible in a report if there is no data for the column
* Max text length – the maximum number of characters for the field. Blank means no limitation
* **Actions** – list of actions for a column

**Find in Columns**

To search columns, start typing in the **Search Columns** field (a list of matching column names will be suggested). Matches will be highlighted and you will also see the number of results calculated. To navigate to the first match, click **Go to first match**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/11/152-1024x449.png" alt=""><figcaption></figcaption></figure>

**Change the Order of Columns (and groups)**

To change a column position, drag and drop the column name into the desired position. Columns can be moved between groups. To move all columns from one group to another, drag and drop a folded group into an unfolded one.

You can re-order groups in the same way (only if they are folded). It is also possible to enter a new index for a column – the column will be automatically located in the new position.

**Change a Column Name**

By default, the name from the **Name** column will be visible in the generated report.

To override a column’s name, type a new name in **Name override.**

**Override Value**

By default, data generated by the reporting engine will be visible in the generated report.

To override a column’s value, enter a new value in the **Override value.**

**Set Value when Blank**

To override a blank value column in a generated report, enter a new value in the **Override value.**

**Limit Length of Column**

To limit the maximum length of characters in a column, you can type a number in **Max text length**.

**Duplicating a Column**

You can duplicate an existing column, and then, for example, change its name or override values.

* To duplicate a column click (**…**) in the **Actions** column and then click **Duplicate**. A new column will be added just below the original one.
* To delete a duplicated column, click (**…**) in the **Actions** column and click **Delete**.

**Automatically include or exclude new columns**

In the future, additional columns may be added to the report type. You can decide if these columns should be automatically added to the template (and thus to generated reports). New columns will be added at the end. This option is switched on for the default template.

To automatically include new columns, check **Yes, automatically include new columns**.

<div align="left">

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/11/171-5.png" alt=""><figcaption><p><strong>Figure 16 – Automatically include new columns</strong></p></figcaption></figure>

</div>

#### Updating a template <a href="#post-4285-_toc51828553" id="post-4285-_toc51828553"></a>

To update a template, first select it, then click on the template name and click **Edit**. Note that you cannot edit the default and universal templates.

#### Deleting a template <a href="#post-4285-_toc51828554" id="post-4285-_toc51828554"></a>

To delete a template, select it and click **Delete.**&#x20;

In confirmation dialog, click **Delete template** (templates that are being used in other reports’ configurations can’t be deleted). Deleted templates can’t be recovered. Removing a template doesn’t impact already generated reports.

#### Request additional fields <a href="#post-4285-_toc51828555" id="post-4285-_toc51828555"></a>

You can request additional fields for a report type. To send a request for additional fields, start editing or creating a new template, then click (**…**) next to **Cancel** and then click **Request Additional Fields**.

<div align="left">

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/11/181-3.png" alt="" height="130" width="566"><figcaption></figcaption></figure>

</div>

Fill in the fields and select **Request Additional Fields**.
