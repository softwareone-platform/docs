---
description: Learn about the access levels and settings, and create new chargebacks.
---

# Create Chargebacks

***

### Access levels <a href="#access-levels" id="access-levels"></a>

Chargebacks have two access levels:

* **User Level**: Users with this access level will only be able to see the Chargebacks tab. The Add New Chargebacks page will not be available to users who have “User Level Access”. User Level Access is for users who need to view chargebacks but do not have permission to create chargebacks. These users can then access the document details in order to analyze the charges using the Consumption module. This will give users detailed information on the relevant chargeback
* **Admin Level**: Users with this access level will be able to see both the Chargeback tab as well as the Add New Chargebacks tab. Admins can view, create, modify, and delete chargebacks.

{% hint style="info" %}
**NOTE:** If you need to get your access level changed, please contact your SoftwareONE Account Team.
{% endhint %}

***

### Document management <a href="#document-management" id="document-management"></a>

#### Issuing documents in a recurring manner <a href="#issuing-documents-in-recurring-manner" id="issuing-documents-in-recurring-manner"></a>

1. (Optional) Configure Custom Groups or Tenants & Subscriptions (Consumption module documentation).
2. Set bill-to details on the **Settings** page.
3. Configure scheduled report.
4. Adjust the generated document in the Chargeback section.
5. Send documents to the recipient.
6. Generate summary report of issued documents

#### Issue a one-time document <a href="#issue-one-time-document" id="issue-one-time-document"></a>

1. (Optional) Configure Custom Groups or Tenants & Subscriptions (Consumption module documentation).
2. Generate the document using the **Setup** page.
3. Adjust the generated documents (Chargebacks section).
4. Send documents to the recipient.

#### Document corrections <a href="#document-corrections" id="document-corrections"></a>

1. Open the generated document in Chargebacks by selecting the line item in the Chargabacks tab section.
2. Apply additional charges/discounts, change currency, bill-to, and other properties. If the document has been sent, a new version will be created.
3. Send the corrected document to the recipient.

***

### Chargebacks <a href="#chargebacks" id="chargebacks"></a>

#### Chargeback Tab <a href="#chargeback-tab" id="chargeback-tab"></a>

On the Chargeback tab, you can see all chargeback invoices including specific details about each invoice:

| **Document Name**        | Name of the document.                                                                                     |
| ------------------------ | --------------------------------------------------------------------------------------------------------- |
| **Chargeback No.**       | This is unique number for generated chargeback invoice. Column hidden by default.                         |
| **Providers**            | Publisher list taken into consideration for document                                                      |
| **Bill To**              | Company name which paying department belongs to                                                           |
| **Email**                | Recipient’s email. Column hidden by default.                                                              |
| **Document Date**        | Date of document generation                                                                               |
| **Amount**               | Amount of this Chargeback i.e. Total of all line items                                                    |
| **Billing/Usage period** | Consumption filter – start/end date or list of billing periods – it has been generated for                |
| **Status**               | <p>Status of the chargeback invoice.<br>Possible values: “Generating”, “Generated”, ”Sent”, “Failed”.</p> |

{% hint style="info" %}
**NOTE:** This module supports Azure EA, Azure CSP, AWS, and O365.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (115).png" alt=""><figcaption></figcaption></figure>

#### Invoice Details <a href="#invoice-details" id="invoice-details"></a>

You can select any row to open a detailed view of the respective chargeback invoice. The page shows all information related to the document and allows you to edit it.

**Document view** – consists of header, body, and footer. On the right side “Actions”, “Activity” and “Versions” panels are available.

**Header** – consists of the name and date the document was generated. Bill-to-address, company logo, customer number, consumption/billing period date range and field to store custom notes.

**Body** – lists the line items. Each line item is described with appropriate providers, total resources count, and amount. Line items are further divided into sub-lines, which display top Resource Types.

**Resource Type** – defines provider and type of resource. If the resource type is virtual machines or storage, you will also see SaaS-connected resource types like “User” or “License”. See the Consumption Module for details.

**Footer** – displays contacts, company information, and exchange rates applied during currency conversion. Additionally system-wide unique Chargeback Number is visible and should be used during contact with Support in case of issues with the document.

{% hint style="info" %}
**Note:** Subgroups structure is only available using Custom Group split. It is not possible to display both group structure and Resource Types at the same time. It is possible to switch between Subgroups and Resource types in the Customize menu which can be found in the middle section of the document **Volume** column is hidden by default. It can be adjusted in the Customize menu.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>

**Software-as-a-Service Licenses**

Office 365 licenses are classified by their assignment status. On the chargeback document, assigned licenses are visible as a “User” subline with resource count matching active users. On the other hand, unassigned licenses are gathered under the “License” subline with resource count matching the number of license types (like Office365 E3 or E5).

<figure><img src="../../.gitbook/assets/image (117).png" alt=""><figcaption></figcaption></figure>

**Additional charges**

Additional charges represent new line items added by hand to the generated document. Costs associated with such lines may represent various invoice corrections or items not associated with consumption data. Support fees, discounts, and credits are typical examples of such charges.

Functionality is available through the **Add Charge or Credit** button.

<figure><img src="../../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure>

Additional charges may be fixed or percentage-based. The percentage amount is calculated based on consumption data only, therefore other lines (e.g. markup) are not taken into consideration. Negative values are calculated as discounts. Additional charges can be removed with the **Delete** button.

<figure><img src="../../.gitbook/assets/image (119).png" alt=""><figcaption></figcaption></figure>

**Subgroups structure**

Documents based on Custom Groups can display nested group sublines. The whole purpose of sublines is to add more transparency to the cost of the line item. It is an alternative to displaying top Resource Types.

<figure><img src="../../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>

Subgroups are organized in the tree structure. Visibility and depth of presented sublines can be selected in the Customize menu. Please note that the cost of the subline is not calculated into the total cost of the document. In other words, it provides justification for line costs.

<figure><img src="../../.gitbook/assets/image (121).png" alt=""><figcaption></figcaption></figure>

The name of the given subgroup (and therefore line name) can be properly adjusted on the Settings page.

**Notes**

Generated documents often miss crucial information needed to justify the amount associated with line items. Moreover, documents often require appending internal tracking numbers. Notes address both of these needs and have the capability to store text and append it to the generated PDF. The field is accessible near the top of the document.

<figure><img src="../../.gitbook/assets/image (122).png" alt=""><figcaption></figcaption></figure>

**Versions**

Chargeback documents are “read-only” after being sent. Further edits of sent documents are treated as separate versions. New versions are marked with the date and person making the edits. All changes are collated as long as the new version is not sent to the recipient again.

Previous versions are accessible through the panel on the right side of the document. Previous versions cannot be changed or deleted.

<figure><img src="../../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>

**Actions and Activity Panel**

The Chargebacks page has an “Actions” panel on the right side, which will allow users to perform actions with selected invoices as outlined below:

* Export with Charts as a PDF or Export as a PDF.
* Analyze Consumption Report.
* Export resource data to CSV.
* Delete Chargeback. The document is permanently removed from the system.
* Activity – Send the document to the recipient. After sending the document, the status is changed to **Sent**.

<figure><img src="../../.gitbook/assets/image (125).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**NOTE:** Delete Chargeback option is only available for users with an “Admin Access Level”. In most cases, it is the owner of the chargeback invoice i.e. the user who has generated the invoice. Analyze Spend Report is a drop-down wherein users can select the required providers. This will redirect users to the Consumption Module for the selected provider.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (126).png" alt=""><figcaption></figcaption></figure>

**Document delivery**

Sent documents are delivered to the recipient by email. Recipients receive a PDF with the chargeback document along with a link to the detailed report (CSV file).

The detailed file describes every line of the document with the Meter Name, Volume, and Resource Name. Data provided in CSV files are input to calculations performed to generate the chargeback document. The attached details can be imported to external systems for reference or further analysis. Diagnosis of miscalculations is also feasible.

The links to the detailed files expire after 5 days from the time the message is received. Regeneration of links is possible by sending documents once again – using the **Send** button in Chargeback Manager.

***

### Adding new chargebacks <a href="#adding-new-chargebacks" id="adding-new-chargebacks"></a>

Select A**dd New Chargebacks.** This will open the New Chargebacks page. There is an intro paragraph explaining what chargebacks are that can be hidden by clicking on the \[x].

<figure><img src="../../.gitbook/assets/image (127).png" alt=""><figcaption></figcaption></figure>

#### Providers <a href="#providers" id="providers"></a>

The first section is “Providers”. This represents a list of all available and supported provider groups.

<figure><img src="../../.gitbook/assets/image (129).png" alt=""><figcaption></figcaption></figure>

Admins need to select all of the providers they want to create chargeback invoices for. By selecting a provider, the system fetches consumption data for every tenant that is enabled under that provider.

{% hint style="info" %}
**NOTE**: We currently support five providers (AWS, Azure EA, Azure, CSP, Office 365, and Adobe). This section will only show those providers that the customer has subscriptions with, and are supported. Customers must be migrated to the new consumption module as the data is pulled from this module. Customers using the Old Azure EA Module must first upgrade to the new consumption module. Your Account Team can help you with this request. At least one provider has to be selected to create a chargeback invoice
{% endhint %}

Once providers have been selected, select **Done** to navigate to the next section **Date Range.**

#### Date Range <a href="#date-range" id="date-range"></a>

The “Date Range” section allows Admin to narrow down the date range of consumption data. The date range is specified in two modes:

* Usage Dates – described with start/end dates
* Billing Period – list of periods connected to bill cycles

<figure><img src="../../.gitbook/assets/image (130).png" alt=""><figcaption></figcaption></figure>

Once the date range has been selected, click on “Done” to navigate to the next section “Create”.

**Note**: Start and End usage dates are inclusive i.e. consumption would be fetched for these dates as well. Billing Periods are available only for Azure EA and Azure CSP.

#### Create <a href="#create" id="create"></a>

Newly selected consumption spend (by selecting providers and date range) may be optionally divided in two ways:

* Using a Custom Group structure
* Using Tenants & Subscriptions hierarchy

**Split by Custom Groups**

The Custom Groups section shows the group structure as defined in Custom Groups. This allows Admins to select departments/groups they would like chargebacks for.

<figure><img src="../../.gitbook/assets/image (131).png" alt=""><figcaption></figcaption></figure>

Selecting each group allows Admins to split chargeback invoices for selected groups. If none of the groups are selected, one global chargeback invoice is created for complete consumption of selected providers.

Costs displayed against each group is the estimated consumption by that group. Consumption for all ungrouped resources is reflected as “Untracked” in this section.

Click on “Done” to navigate to the next section “Review Chargeback”

**Note:** Invoice will be created for first selected group. Lines will correspond to closest selected groups under document group. Consumption will show only for selected groups in the invoice.

<figure><img src="../../.gitbook/assets/image (132).png" alt=""><figcaption></figcaption></figure>

**Split by Tenants & Subscriptions**

Tenants & Subscriptions are the foundation of the Consumption module. Chargebacks use the existing structure to create documents. No further configuration is required. Convention based approach is applied: every Tenant is documented with lines derived from its Subscriptions.

**Note:** Document/line options can be set on Settings page. Scheduled generation is supported. Please consult Original Document subsection in Reporting section.

<figure><img src="../../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure>

#### Review Chargeback <a href="#review-chargeback" id="review-chargeback"></a>

Review Chargeback is the last section that summarizes the selections Admin user has made and provides the following capabilities to Admins:

* Admins can preview the document that will be generated
* Admins can edit the Bill To details
* Admins can change the name of the document i.e. chargeback invoice – This allows users to name the invoice appropriately within the organization

<figure><img src="../../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

Selecting “Preview” will open a preview of the invoice so that Admins can see how it will be displayed on chargeback tab.

**Note:** There will be no costs displayed on the preview tab because the document is not yet generated, however costs will be available once the document has been generated.

Selecting “Edit Bill To” will allow Admin to edit the Bill-To details if required. Admins can change the address and contact details for the chargeback.

<figure><img src="../../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>

#### Create Chargebacks <a href="#create-chargebacks" id="create-chargebacks"></a>

Once all the selections are made and the preview looks good, Admins can go ahead and create the chargeback documents by clicking on “Finish & Create \[n] Chargebacks” (where \[n] is the number of Chargebacks as shown below

<figure><img src="../../.gitbook/assets/image (136).png" alt=""><figcaption></figcaption></figure>

Admins will be taken to the “Chargeback” page where they can see the invoices being generated. This is shown in the right-hand “Status” column as “Generating”.

<figure><img src="../../.gitbook/assets/image (137).png" alt=""><figcaption></figcaption></figure>

Once the invoices are ready, the status will be changed to “Generated”.

<figure><img src="../../.gitbook/assets/image (138).png" alt=""><figcaption></figcaption></figure>

### Settings <a href="#settings" id="settings"></a>

Invoice documents are issued many times throughout the year. Manually adjusting documents every time is unreasonable. Common information like bill-to details, margin, or contact information is typically recurring for a given document series.&#x20;

They can be bound to a single group or subscription. The settings page persists and allows editing most of the information stored in the document header.

Settings can be attached to either Custom Group, Tenant, or Subscription. All levels store the same set of settings. Stored settings are used twofold: as default values for manual generation (Setup) and base data during scheduled generation (Reporting).

The settings tab is divided into left pane and right pane.

* The left pane represents the tree structure of either Custom Groups or Tenants & Subscriptions. Clicking on a tree element selects a particular entity and the form is filled with appropriate data (by default form is empty).
* The right pane holds a set of information used during document generation. Data filled in the form are auto-saved.

***

### Reporting <a href="#reporting" id="reporting"></a>

Chargebacks support rich reporting capabilities. Reports allow ad-hoc and scheduled export of data. The granularity of the report extends from a basic overview to resource-level details. It is also possible to generate new documents with a selected cadence.

#### Where to find the reports? <a href="#where-to-find-reports" id="where-to-find-reports"></a>

If you are in Chargebacks, you have the option to “View Schedule Reports” Or “Add New Schedule” by clicking on the buttons on the top right.

You can also navigate to the main reports page by clicking on “Analyze” in the main navigation menu and then selecting “Reports” as shown below:

This will take you to the “Quick Reports” page. From here you can click on the dropdown under “Chargeback Manager” and select the report you want.

#### Types of Chargeback reports <a href="#chargeback-report-types" id="chargeback-report-types"></a>

The Chargeback module supports four report types.&#x20;

{% hint style="info" %}
**Note**: The top 4 reports in the table gather data about existing Chargeback documents. The last one, Original Document, creates new documents and sends them to the configured email address.
{% endhint %}

| Report                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| All Chargebacks Detailed | <p>This is an enriched version of the overview report with detailed line information. </p><p></p><p>Each row of the report stands for a single line in the document. Line cost, currency, list of providers, and resource count are available.</p>                                                                                                                                                                                                            |
| All Chargeback Overview  | <p>This report summarizes basic information about all documents generated within a target date range. </p><p></p><p>Each row represents a single document. Apart from the header information like document name, bill-to details; total amount, and currency are present.</p>                                                                                                                                                                                 |
| Chargeback Detail        | <p>This is a detailed report for chargeback line information. </p><p></p><p>Each row of the report stands for a single line in the document. Line cost, currency, list of providers, and resource count are available.</p>                                                                                                                                                                                                                                    |
| Provider Based           | <p>The report focuses on the provider’s shares analysis. </p><p></p><p>Line information is split across all contributing providers. </p><p></p><p>Further aggregation of data may answer questions regarding each provider's cost across all selected documents, trends in provider’s shares, etc.</p>                                                                                                                                                        |
| Original Document        | <p>This report enables the scheduled generation of documents – in contrast to the analysis of existing documents that previous types focus on. </p><p></p><p>The outcome of running the report is a set of new documents, which can further be adjusted in the Chargeback module (Additional Cost, etc.). </p><p></p><p>Rich configuration options of the report in cooperation with Settings allow achieving functionality similar to manual generation.</p> |

#### Scheduled Generation <a href="#scheduled-generation" id="scheduled-generation"></a>

Scheduled reports enable periodic reporting with automatic delivery capabilities. The scheduled report definition represents a “future report form” which will be filled with appropriate data. Both the data set and time of running the report can be customized to meet business requirements.

Reports are gathered under the **Scheduled** Tab.

<figure><img src="../../.gitbook/assets/image (139).png" alt=""><figcaption></figcaption></figure>

**New Scheduled Report**

**To create a new Scheduled Report**

* Select **Add New Schedule** in the top right corner of the Chargebacks page. This will open the Schedule Report page where you can follow the steps and fill in the required information for your report.

<figure><img src="../../.gitbook/assets/image (140).png" alt=""><figcaption></figcaption></figure>
