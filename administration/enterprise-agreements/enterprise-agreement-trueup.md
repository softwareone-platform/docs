---
description: >-
  Optimize and simplify the Enterprise Agreement True-Up process at a local or
  global scale from collection to license allocation.
---

# Enterprise Agreement TrueUp

***

This section of the document will guide you through the Enterprise Agreement Setup Wizard. Running through the Wizard and enabling reporting is the first step in the EA module onboarding process.

The onboarding process consists of 2 phases:

1. Wizard Setup
2. Asset Allocation

The purpose of the Wizard Setup is to gather data around agreement structure, company structure, and customer price sheet information.

The following prerequisites are required to run through the Setup Wizard :

* Enterprise Agreement
* Company structure information
* Customer Price Sheet

***

### Accessing EA Setup <a href="#post-3370-_toc513023077" id="post-3370-_toc513023077"></a>

Only EA Admins can access the wizard. If you do not see this option, it may be a permissions issue.&#x20;

* From the navigation menu, go to **Setup** and select **EA Setup Wizard**.

***

### Setup Wizard <a href="#post-3370-_toc513023078" id="post-3370-_toc513023078"></a>

* Select **Add data in our wizard** to start the setup process. The Wizard will run you through 7 steps. All of the steps need to be followed in sequence. You can only move on to the next step once the current step has been completed.
* Only one agreement can be set up at a time. It is currently not possible to fill in data for two different agreements simultaneously.

The Wizard automatically saves the data you have added after every change. The data input process may be interrupted at any time and resumed when convenient. The Wizard remembers which step you were actively working on.

To reset the Wizard click on the “Discard all progress” button visible on the bottom of every step.

### Step 1 – Select Agreement <a href="#post-3370-_toc513023079" id="post-3370-_toc513023079"></a>

Select your EA Agreement from the drop-down. The following license model agreements are supported:

* Direct Enterprise Agreement
* Indirect Enterprise Agreement
* Server Cloud Enrolment
* Enrolment for Core Infrastructure

Users need to have permission to inspect agreements.

Agreements that have already been set i.e. moved to Asset Allocation or Reporting, are not displayed on the list.

{% hint style="info" %}
In cases where either:

* The user does not have proper permission
* All agreements have already been set up
* No agreement exists in the system

Then only the form for registering a new agreement will be available. If you can see your target agreement on the License Agreements page (i.e. Manage>Contracts), and no setup has been completed but you still do not find it on this page, submit a support request.
{% endhint %}

If you do not find your EA Agreement in the list, click on the **Register New Agreement** tile to create a new agreement. Your SoftwareOne Account Manager will receive a notification and will need to set up the agreement in our backend system in order to get the process completed. Refer to the **Register New Agreement** section for more information.&#x20;

Once selected, click on **Next** to move on to the next step – **Structure.**

### Step 2 – Structure <a href="#post-3370-_toc513023080" id="post-3370-_toc513023080"></a>

This is to define the structure of the agreement. From this step onwards, you need to have the Customer Price Sheet (CPS) available to proceed.

This page **allows you to set tenants and products profiles** (as available in your CPS), however both of these fields are not mandatory, so you can have these disabled.

**Profiles**

Typically profiles and tenants can be found as a subsection in CPS. Profiles can be found in both “SECTION 1. Licenses and Software Assurance” and “Future Pricing”. Please note that the “Enterprise” subsection should not be treated as a profile and will be automatically added in the Wizard. Please inspect the below screenshot from a sample CPS with “Industry Device II” and “Manufacturing” profiles.

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

The screenshot below shows the “Enterprise” subsection which should not be counted as a profile:

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

**Tenants**

Tenants represent the domain of subscription products. They can be found in “SECTION 2: Monthly Subscriptions” as well as the proper “Future Pricing” subsection. The screenshot below shows two tenants have been identified. Subsections should not be treated as tenants and will be automatically added by default.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

**Adding Profiles and Tenants**

If you want to add tenants or product profiles, you can enable these by clicking on the “switch buttons”. It is also possible to delete existing profiles and tenants.

Once you have inserted the details, click on the “Next” button to move on to next step i.e. **Reporting Location**.

{% hint style="info" %}
**NOTE**: If you do not have tenant or product profile information in your price sheet, you do not need to add this information to the Wizard. Both of these are optional so you can simply click on the next button to move on to Step 3.
{% endhint %}

### Step 3 – Reporting Location <a href="#post-3370-_toc513023081" id="post-3370-_toc513023081"></a>

This step is to add locations that will be used for reporting purposes. The customer Price Sheet is oriented around “Usage Countries”. Each country aggregates license quantities from all locations (e.g. companies) within that country. However, to provide accurate reports we suggest using a more detailed location structure.

Location is the extension of the company which should exist in backend systems. If it does not exist then both “Company” and “extended Location” can be added in the form below. It is advised to have permissions for all companies in the address tree relevant to the agreement being set up. Only one location can be added per company.

The location form consists of:

* **Company-** You can select a company from the drop-down list as it will show you all the companies available in the address tree. The company is required to add a location. If you think a company is missing, you can **Create New Company** by following the steps in the “Add New Company” section.
* **Location Group** – This is a user-defined grouping, you can group the companies based on your requirements. One group may have multiple locations, however, one location may only exist in one group.
* **Product Profile** – is a drop-down that has profiles from Step 2. Multiple values can be selected.
* **Company identifier** – is a user-defined identifier for each location. There are no strict rules around identifiers but it is recommended to use a number that does not change frequently. (like internal subsidiary identifier).

Once all the details are provided, **click on the “Add”** button.

Clicking on the “Add” button would bring the reporting location record down and a new form would be available to add more locations.

You can also delete or edit already added reporting locations by using the “Edit” or “Delete” options.

You have to add at least one reporting location in order to proceed to the next step.

When all the reporting locations are added, click on the “**Next**” button.

### Step 4 – License and Software Assurance <a href="#post-3370-_toc513023082" id="post-3370-_toc513023082"></a>

The purpose of this step is to add License and Software Assurance details i.e. product and price details from Customer Price Sheet.

Data required in this step can be found in CPS table under the header “Section 1 – License and Software Assurance” as shown below. Products for every year should be added (please inspect the note regarding auto auto-populate feature below).

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Pricing information for all products across every year is required. However, due to the structure of agreements only data for the first year need to be added. Subsequent years are auto-populated and only need to be adjusted in singular cases (please see note below).

The screenshot below shows the tabs representing each year relating to your agreement. Pricing for 3 years is available by default. Additional years can be added if needed in alignment with the agreement duration and details available in the CPS. When selecting a year tab it will display all the data for that selected year.

Each year tab has a grid available with two main sections i.e. **“Enterprise Products” and “Additional Products”.**

In case you have added any product profiles in Step 2, those would also be available under the Enterprise Products section. Products with the same part number but different pricing can be added to multiple profiles.

The order of columns in the Wizard and CPS is different. More importantly, the “Part Number” of the product is the first column and should be inserted before other data. This is due to the fact that “Product Description” and “License Type” are auto-filled based on the product part number. In case that part number can not be found and auto-filled then data should be added manually.

After providing base product information the “Net Unit Price” and “License Quantity” should be filled out. As a result “Extended Amount” will be calculated. The “Calculated Extended Amount” value should match the corresponding value in CPS.

The “Usage Country” field is optional. It may be used for the review process after the list is completed. Especially when “Total Year Payment” (seen at the bottom of the screen) in the Wizard does not match the corresponding value in CPS.

Following the same process, you need to fill in all the products from CPS. You should see the total payment for that year at the bottom of the screen and this amount should match with the total year payment on CPS for the corresponding year.

* **“Total Year Payment”:** Total Year Payment presented in Step 4 should be compared to Total Year Payment contained in “Section 1 – Licenses and Software Assurance” for a particular year table in CPS. Fill in the details for each year and once done, click on” Next” to proceed to the next step i.e. Subscription.
* **Products auto-population across years”:** Data from Year 1 is auto-populated to subsequent years. Typically year-to-year data in CPS does not change. However, if it is required, products every year can be altered manually. Please note that auto-populate propagates changes from a given year to the next ones. **Example:** For a 3-year agreement. After adding data to Year 1, the user decides to add one new product to Year 2. The auto-populate feature will copy the new product to Year 3, but will not touch Year 1. After that, change from Year 1 will not be propagated to Year 2 and Year 3.

**Note:** In the screenshot below, details for a few of the products are inserted. However, you still need to fill in the details for each product in the price sheet and under all relevant years.

### Step 5 – Subscriptions <a href="#post-3370-_toc513023083" id="post-3370-_toc513023083"></a>

This step lets you fill in details for subscriptions.

Data required in this step can be found in CPS table under the header “Section 2 – Monthly Subscriptions” as shown below. There are a few columns in CPS that you do not have to take into consideration from now on: “Usage indicator”, “Usage Start Date” and “Unit of Measure”. Those columns should be omitted when inputting pricing information.

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Step 5 has a similar grid to Step 4, the only difference is the “Unit Quantity” field is added. “Unit Quantity” represents the number of months. It is set to 12 months by default, however, it can be changed if required.

The grid has two sections i.e. **“Enterprise Products”** and **“Additional Products”.** Both sections need to be mapped correctly from CPS.

Filling in “Part Number” will auto-populate “Product Description”..

Filling “Net Unit Price” / “Month and License Quantity” will auto-populate “Extended Amount”. Please note that the price is for one single month, therefore it should be the same as in CPS.

You can “Edit>Inserted Row” anytime. Adding a new product is achievable by clicking on the “Add Product” button.

**“Products auto-population across years”:** Data from Year 1 is auto-populated to subsequent years. Typically year-to-year data in CPS does not change. However, if it is required, products every year can be altered manually. Please note that auto-populate propagates changes from one given year to the next.

**Example:** For a 3-year agreement. After adding data to Year 1, the user decides to add one new product to Year 2. The auto-populate feature will copy the new product to Year 3, but will not touch Year 1. After that, changes from Year 1 will not be propagated to Year 2 and Year 3.

In this step, data inserted for Year 1 is copied for subsequent years. Please inspect the notes in Step 4 for more details.

Once completed, click on the “Next” button to move to the next step i.e. Future Pricing.

### Step 6 – Future Pricing <a href="#post-3370-_toc513023084" id="post-3370-_toc513023084"></a>

This step is to insert future pricing details that come from the “Future Pricing” section of the Customer Price Sheet. Rows in CPS represent products and columns with the right prices for the TrueUp process for that given year. The “Future Pricing” section in CPS looks similar to what is shown below:

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

The “Future Pricing” section in CPS typically consists of multiple subsections such as “TrueUps”, “Higher Editions”, “Step-Ups”, “Future Monthly – Enterprise Online Services”, “Future Monthly – Enterprise Online Services”, etc.

Even though these sections are not represented directly in the Wizard, they can be divided into subscriptions and non-subscription products. It is recommended to add all products from “Future Pricing” in the relevant section in the Wizard based on the following three questions:

1. Is the product a subscription? Yes/No
2. What is the product category? Enterprise/Additional
3. What is the product profile? – (Reference profiles added in Step 2 if applicable)

This step is designed around two sections(Related to Question 1 – Is the product a subscription?):

* “License and Software Assurance” – referencing products from Step 4
* “Subscriptions” – referencing products from Step 5

Both sections are divided into “Enterprise Products” and “Additional Products” (Question 2 – What is the product category?) and further down into profiles if applicable (Question 3 – What is the product profile?).

The following products will be automatically added from the previous steps:

* All products of type LicSA (License and Software Assurance Pack) without prices
* All products of type SASU (Software Assurance Step Up) without prices
* All products of type UpgSA (Upgrade and Software Assurance Pack)
* All subscriptions with prices

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

The number of years on Step 6 is equal to the number of years you have defined in Steps 4 and 5.

Fill in the prices for all products in Y1, Y2, Y3 until Yn (n = no. of years tab you have added in Step 4).

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

Prices for subscriptions are already populated from Step 5, however, you can add more if needed but existing subscriptions (added in Step 5) cannot be removed.

Once all the details are entered into the Wizard, click on the “Next” button to move on to the next step i.e. Review.

### Step 7 – Review <a href="#post-3370-_toc513023085" id="post-3370-_toc513023085"></a>

The review step summarizes all the information provided in the Wizard. It allows you to review important details and if something is not correct, you can navigate to the respective step to correct. This step allows you to:

* Review all the details.
* Go back to any of the steps to edit/amend the details.
* Submit all the entered details by clicking on the “Finish” button.
* Review the annual and total payment details for the reported agreement. The figures for all years should match with the figures in the summary section of CPS sheet for respective years.

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

If you feel that all the details are correct, submit by clicking on the “Finish” button. Clicking on “Finish” will submit the agreement for Asset Allocation as shown below:

All 7 steps have a “Discard all progress” button that allows you to reset the agreement and will remove all the details you have set in the Wizard against this agreement.

{% hint style="info" %}
**NOTE**: Once you have clicked on “Finish” in Step 7 and submitted the details, you cannot make any changes. If you want to make any changes you need to raise a support request.
{% endhint %}

***

### Register New Agreement <a href="#post-3370-_register_new_agreement" id="post-3370-_register_new_agreement"></a>

In Step 1, if the user does not find the agreement listed in the drop-down, they can go ahead and register the new agreement by clicking on “Register New Agreement “:

Clicking this tile will take you to the next form as shown below:

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

Fill in the details and click on “Next” to proceed with this agreement.

{% hint style="info" %}
**NOTE:** You can proceed to the next step after registering a new agreement. Creation of the agreement via Wizard will trigger an email to inside sales. Finishing agreement onboarding (via asset allocation) **can only be done when the agreement is created in the backend database** (i.e. Navision) by inside sales.
{% endhint %}

***

### Add New Company <a href="#post-3370-_add_new_company" id="post-3370-_add_new_company"></a>

In Step 3 the user configures the reporting locations. If the target company is not available in the drop-down, then a new company may be requested.

Click on “Add New Company” under the company name drop-down. It will take you to the below form where you can provide the details and click on “**Save**”.

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**NOTE:** You can proceed to the next step after requesting the New Company, however, the creation of the new company via the Wizard will trigger an email to inside sales. Finishing new company onboarding can only be done when the company is created in the backend database (i.e. Navision) by inside sales.
{% endhint %}

***

### EA Asset Allocation <a href="#post-3370-_toc513023088" id="post-3370-_toc513023088"></a>

This section will guide you on how to do asset allocations once the Setup Wizard step is completed and the specific agreement has been submitted. The purpose of asset allocation is to link the products with the reporting locations, i.e. distributing the licenses across all companies. After completion, the chosen Agreement will be accessible from the EA Reporting module.

Below are the prerequisites to proceed with the asset allocation process.

* “Wizard Setup” for the required agreement is completed
* EA Admin (who would follow this document) should have allocation data available

#### Where to find Asset Allocation <a href="#post-3370-_toc513023089" id="post-3370-_toc513023089"></a>

Asset Allocation can be found in PyraCloud under the “Manage” menu option as shown below:

Users can also be taken to the Asset Allocation page when they complete the Setup Wizard by clicking on the “**Finish**” button in Step 7.

{% hint style="info" %}
**NOTE:** Only EA Admins will have access to the Asset Allocation page in PyraCloud. If you do not see this option available, it may be a permissions issue, in which case please get in touch with your Account Manager.
{% endhint %}

#### Asset Allocation <a href="#post-3370-_toc513023090" id="post-3370-_toc513023090"></a>

Clicking on “Asset Allocation” takes you to the below page where you can select the specific agreement you want to do asset allocation for.

**Note:** Only Agreements for which Wizard setup is completed will be shown in this drop-down.

Once the agreement is selected, you are taken to the Asset Allocation page for the selected agreement as shown below:

**Note**: If you submit the details in the Wizard in Step 7, then you are taken to the below page for the contract you have submitted the details. You do not need to find and select your contract from drop-down.

This page is an overview page and you can navigate to the details page for each product by clicking on the “Edit” option under the “Actions” column. The details page is shown below:

#### Overview Page <a href="#post-3370-_toc513023091" id="post-3370-_toc513023091"></a>

This is a read-only page and you cannot make any changes to this page. The grid on this page has data grouped by Product Profiles which you have created during the Wizard setup in Step 2 i.e. Structure.

The grid on this page contains below details:

**Part number and Product Description** – Fetching data from the details provided in Steps 4 and 5 in the Wizard setup.

**Remaining Licenses –** shows the number of licenses that have been allocated and the quantity remaining. For the given product, the license pool is equal to the sum of its licenses across all Usage Countries in the Customer Price Sheet.

For Example 0 of 100 – would mean that none of the licenses are allocated yet.

**Total Cost –** shows the total cost of allocated Licenses

**Status** – Status has three possible values as defined below:

* Complete – When all the available licenses are allocated
* Incomplete – When all the available licenses are not allocated, i.e. few/all licenses are still left to be allocated
* Overallocated – When too many licenses are allocated

Asset Allocation overview page also has a drop-down to select the products based on the required status (as shown below). If nothing is selected from this drop down list, all the products irrespective of their status will be shown in the grid.

**Action** – This column has an “**Edit**” option which can be used to navigate to the details page for the respective product

There is a “Submit” button on the overview page to submit the final asset allocation. However, this button is greyed out and would only be enabled when all the assets are allocated properly i.e. status of all the assets changes to complete.

#### Product Details Page <a href="#post-3370-_toc513023092" id="post-3370-_toc513023092"></a>

When you click on the “Edit” option under the actions column on the overview page, you are taken to the details page for the respective product. This is the place where you can allocate the assets across the companies.

On this page, all details are shown for the respective product. i.e. if the same product has been added to two product profiles, both profiles would show up on this page.

**Product Selection**

Even though you have come to this page via a specific product record on the overview page, you can still select any other product directly from top dropdown. There is no need to go back to the overview page.

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

**Reporting Location**

For the selected product, the reporting location drop-down will only contain those options that belong to the available “Product Profile” for the selected product. Depending on the profile setup, different allocation rows may be displayed. Therefore, no invalid allocation can be added.

For example, if a product is set up under the “Industry Device” product profile, only those reporting locations would be available in the drop-down which belongs to this profile.

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

If nothing is selected in the “Reporting Locations” drop-down, all the available reporting locations are shown in the grid and are grouped by Location Group, as defined in Step 3 of the Wizard setup process.

At this step, you need to have the allocation data for the selected product. Numbers representing quantities should be added to the “Quantity” column:

Once you have defined the quantity, the amount will get calculated automatically based on the unit price you have set up in the Wizard (Year 1 of Steps 4 and 5) using CPS.

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

**Total Cost** – shows the total cost of all the allocated assets/licenses. i.e. if only 40 assets are allocated out of 90, the total cost will show the amount for 40 assets.

At the bottom of the reporting location column, you can see if all the available assets are allocated or not. Three possible values can be displayed here:

&#x20;![](<../../.gitbook/assets/image (17).png>) ![](<../../.gitbook/assets/image (18).png>) Depicts that all the assets are allocated properly and status field is set to “Complete”

Depicts that too many licenses have been allocated and the status field is set to “over-allocated”

![](https://help.pyracloud.com/wp-content/uploads/2020/07/word-image-72.png) Depicts that licenses are still left unallocated and status field is set to “Incomplete”

You can select the products from the product drop-down and allocate the assets to bring the status of all products to “complete”.

If there is no value reported against any location it is considered as 0.

**Note**: All the changes made on this page are auto-saved.

You can navigate to the Overview page at any time by clicking on “Back to Asset Overview”.

<figure><img src="../../.gitbook/assets/image (37) (1) (1).png" alt=""><figcaption></figcaption></figure>

Your changes should be reflected here. You need to complete this process for all the products.

<figure><img src="../../.gitbook/assets/image (38) (1) (1).png" alt=""><figcaption></figcaption></figure>

Once this is completed for all the products, the “Submit” button on the Overview Page will be enabled.

<figure><img src="../../.gitbook/assets/image (39) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Note:** In order to enable the “Submit” button, all the products have to be in “Complete” status.

#### Submit the Form <a href="#post-3370-_toc513023093" id="post-3370-_toc513023093"></a>

Once the ”Submit” button is enabled you can go ahead and submit the form. You will then see apop message informing you that the data will be sent to the “EA Reporting Tool”, and this page will be locked i.e. no further changes can be made.

You can either “Cancel” or proceed to submit the data by clicking the “Yes, Send Data” button.

<figure><img src="../../.gitbook/assets/image (40) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Validating Details**

At this point, the agreement and company details are validated.

If the allocation data you are submitting belongs to a newly registered agreement, then it is verified in the backend system. After requesting the new agreement in the Setup Wizard, your SoftwareONE Account Manager receives an email with all of the agreement information. Propagating data across all systems may take up to 24 hours. If the agreement has not been set up yet, then an error message will be displayed. It is recommended that you try submitting the form again the next working day.

<figure><img src="../../.gitbook/assets/image (41) (1) (1).png" alt=""><figcaption></figcaption></figure>

If you continue to get the error message, please report this to your Account Manager to get this set up in the database. Once this has been done you will be able to submit the form.

**Note**: If you have created a company in the Wizard, it will follow the same process, i.e. your Account Manager needs to set it up in the database. If this has not been done you will get a similar error message.

***

### EA Reporting Module <a href="#post-3370-_toc513023094" id="post-3370-_toc513023094"></a>

The EA Reporting Module in PyraCloud simplifies the EA TrueUp reporting process for customers. Due to the individual agreement structure of the Microsoft EA, customers can report on the products they have added within their environment on an ad-hoc or annual basis.

When organizations are multinational or global it brings added complexity. The EA Reporting Module has been designed to allow organizations to determine which locations and users need to report on their current environments license usage. The local users may add in these license counts depending on how the organization determines their reporting cycle i.e monthly, quarterly or yearly.

The onboarding process for the EA Reporting module is outlined in this section of the document. EA Agreements are unique for each customer and this brings added complexity which is why it is important to ensure the TrueUp Module is onboarded correctly.

Below are key points to note whilst setting up the EA Reporting Module for a customer.

* All customer locations and users must be set within NAV, including Web shop access
* The tree and global NAV push (if needed) must also be set up
* Ensure the EA Setup Wizard and Asset Allocation steps have been completed in order to have reporting data available here.

***

### Where to find EA Reporting in PyraCloud <a href="#post-3370-_toc513023095" id="post-3370-_toc513023095"></a>

EA Reporting can be found in PyraCloud under the “Manage” menu option as shown below.

**Note:** If you do not see this option available it may be a permissions issue, in which case please get in touch with your Account Manager.

Once you click on “Enterprise Agreement” under the “Manage” menu you are taken to the “EA Reporting” page.

<figure><img src="../../.gitbook/assets/image (42) (1) (1).png" alt=""><figcaption></figcaption></figure>

There are two types of permissions for the EA module i.e. **EA Admin** and **EA User**. Based on those permissions, the UI and available options on this page might differ as explained later in this document.

***

### EA Reporting – User View <a href="#post-3370-_toc513023096" id="post-3370-_toc513023096"></a>

With the **EA User** permissions, the user has restricted access to information and can only perform certain tasks within EA portal. The major difference is that users can only report the usage for the subsidiary or group of subsidiaries that they are responsible for. Users cannot submit the final EA report.

A person with EA User permission would see the below user interface on the EA Reporting page.

<figure><img src="../../.gitbook/assets/image (43) (1).png" alt=""><figcaption></figcaption></figure>

At the top of the reporting page, filters are available which users can select to see required data as shown in the screenshot below:

<figure><img src="../../.gitbook/assets/image (44) (1).png" alt=""><figcaption></figcaption></figure>

Once you have selected the values for these filters, you need to click on the “Search” button to render the data of your search.

* **Agreement** – This is to select the agreement you are interested in.
* **Company** – This is to select data from a specific company **Product** – By default the user will see all the products associated with the contract, however using this drop-down filter they can select specific products they want to report on. The page will only show the data for that selected product.
* **Profile** – This is to select the product profile created during the Wizard setup.

Profile filter is available only if the selected agreement has product profiles created. If there are no product profiles in the selected agreement, this drop-down will be hidden.

On the right-hand side of filters, there are a few more options available:

<figure><img src="../../.gitbook/assets/image (45) (1).png" alt=""><figcaption></figcaption></figure>

* **Agreement Details** – This takes you to the “License Agreement Details” page for the selected contract in “Agreement”
* **Show Agreement Price Sheets** – This can be used to see the price sheet being used for this agreement. It is a reflection of the data submitted via the Wizard Setup

#### Page Views <a href="#post-3370-_toc513023097" id="post-3370-_toc513023097"></a>

**Overview Page**

By default, the user lands on the Overview page as shown below:

<figure><img src="../../.gitbook/assets/image (46) (1).png" alt=""><figcaption></figcaption></figure>

If the user clicks on any of the line items, they will be navigated to a detailed view for that particular product, as shown below. The product filter gets set to the value you clicked on.

**Detailed Page**

On the “Overview” page if the user clicks on any item in the grid, or selects a specific company/ product using the filters they are navigated to the ”Detailed” view (shown below) and quick filters are visible. Data available on the “Detailed” page represents possible report entities. If product profiles are used, then only locations bound to those product profiles will be displayed. The same applies to the “Location” view where only products available for a particular location will be displayed.

<figure><img src="../../.gitbook/assets/image (47) (1).png" alt=""><figcaption></figcaption></figure>

#### Quick Filters <a href="#post-3370-_toc513023098" id="post-3370-_toc513023098"></a>

Quick filters are only visible on the “Detailed” page view, and the user can switch them on/off to enable or disable them.

<figure><img src="../../.gitbook/assets/image (48) (1).png" alt=""><figcaption></figcaption></figure>

**Recent TrueUp**

Recent TrueUp is visible on both the “Overview” page and the “Details” page.

It reduces the number of results in the data grid i.e. if “Recent TrueUp” it is enabled, then the user will only see data for the most recently opened and last submitted EA TrueUp as shown in Figure 2 below.

<figure><img src="../../.gitbook/assets/image (49) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (50) (1).png" alt=""><figcaption></figcaption></figure>

**Only Changed**

Shows only those records where the user has made a change as shown in the screenshot below:

<figure><img src="../../.gitbook/assets/image (51) (1).png" alt=""><figcaption></figcaption></figure>

**Show Costs**

Enabling this filter will show the license cost instead of license quantities. If this is set to “Off”, the page will show the license quantities as shown below.

<figure><img src="../../.gitbook/assets/image (52) (1).png" alt=""><figcaption></figcaption></figure>

**Costs Share**

<figure><img src="../../.gitbook/assets/image (53) (1).png" alt=""><figcaption></figcaption></figure>

Enabling this will show the Software Assurance cost share for the selected product. If this is set to “Off”, these values will be hidden as shown below.

<figure><img src="../../.gitbook/assets/image (54) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (55) (1).png" alt=""><figcaption></figcaption></figure>

**Product Summary**

If this is set to “On”, the user will see the license summary for the selected.

<figure><img src="../../.gitbook/assets/image (56) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (57) (1).png" alt=""><figcaption></figcaption></figure>

#### Scenarios <a href="#post-3370-_toc513023099" id="post-3370-_toc513023099"></a>

Enables users to create different scenarios which is useful to simulate different allocations of assets.

<figure><img src="../../.gitbook/assets/image (58) (1).png" alt=""><figcaption></figcaption></figure>

Users can create a new scenario by clicking on the “New” button and providing the below information:

#### TrueUp Status Highlighters <a href="#post-3370-_toc513023100" id="post-3370-_toc513023100"></a>

If you see this icon against any record, it depicts that the total available licenses are lower than total required license count i.e. additional licenses are needed.

If you see this icon against any record, it depicts that the total number of available licenses is higher than the required licenses count i.e. extra licenses are available.

The desired state is not to have any such indicators.

![](<../../.gitbook/assets/image (59) (1).png>)

#### Action Column <a href="#post-3370-_toc513023101" id="post-3370-_toc513023101"></a>

On the detailed page, there is a column called “Actions” and this has two possible values:

* Change
* Details

<figure><img src="../../.gitbook/assets/image (60) (1).png" alt=""><figcaption></figcaption></figure>

**Change**

Clicking this option takes you to the below pop-up window.

<figure><img src="../../.gitbook/assets/image (61) (1).png" alt=""><figcaption></figcaption></figure>

This shows the current required quantity. Users can change this field and can also add comments to support the changes.

It also allows users to add additional information like PO number, Tenant, and Reference information. Information provided is tracked in the “Details” window.

If any record is updated using this feature, an email is sent to the Account Manager with the details of the changes.

**Details**

The “Details” option displays the history of the given report entity i.e. when a number of licenses have been changed within a given location. Additionally, it allows users to commit the current value set in the required quantity, with comments, which will be visible to the admin.

<figure><img src="../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

#### User Responsibilities – Reporting Usage <a href="#post-3370-_toc513023102" id="post-3370-_toc513023102"></a>

EA Users are responsible for reporting the required quantity of licenses for their subsidiary. They need to sync with local users to get this data for each company in their subsidiaries.

To report the required quantity, they should have the “EA Reporting” window open as show below. If this it is not present, it means that the EA admin has not opened it yet.

The “Up” arrow shows the quantity has been increased from the reported quantity and the “Down” arrow shows the required quantity has been decreased.

<figure><img src="../../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

In order to report the usage/required quantity, users’ needs to:

* Decide the product and company they want to report on
* Go to the open slice of the respective row
* Click the required quantity field
* Provide the required quantity
* Alternatively, change action can be used as described below.

These steps should be repeated, as long as all products and all locations have been updated. Then the “Commit Quantity” button should be used to confirm all values.

#### Actions Column <a href="#post-3370-_toc513023103" id="post-3370-_toc513023103"></a>

On the detailed page, there is a column in grid called “Actions” and this has two possible values:

* Change
* Details

<figure><img src="../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

**Change Window**

Clicking this option takes you to below pop-up window.

<figure><img src="../../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

This window shows the current required quantity. Users can change this field and they can add comments to support these changes.

Users can also add additional information like PO number, Tenant, and Reference information.

If any record is updated using this feature, an email is sent to the Account Manager with all the details of the changes.

**Details Window**

The “Details” option displays the history of the cells i.e. when a particular value was changed. Additionally, it allows the user to commit the current value set in the required quantity with comments which will be visible to the admin.

<figure><img src="../../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

Once it is committed, users will see a lock symbol in the grid.

<figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

The lock symbol means users cannot make any further changes. If any change is required, it has to be made using the “Change” option under the “Actions” column which will trigger an email to the Account Manager.

**Note**: You need to click on “Save” after making any changes or committing any individual quantities otherwise the changes will be lost when the page is refreshed or on the next login.

Users need to report all the products for the locations they are responsible for. Once the user is done with reporting the quantities, they can commit the report by clicking the “Commit Quantity” button on the “Overview” page as shown below. Once it is clicked, the report will be available for the EA Admin.

Users can also click ”Save” to save the changes they have made and can commit later.

Once the quantities are committed, they will be blocked and users will not be able to make any further changes.

If the user wants to make further changes, they need to follow the steps outlined below:

* Go to the entry you want to update and click the “Details” option under the “Actions” column
* Set the “Commit Quantity” flag to “Off”
* Go to the “Change” option under the “Action” column for the same entry
* Make the required change and click “Update”
* Save the changes
* Commit the report again

***

### EA Module – Admin View <a href="#post-3370-_toc513023104" id="post-3370-_toc513023104"></a>

EA Admin roles bring more responsibility. An EA Admin has all the features a User role has, with additional features and functionalities specific to the EA role as outlined below..

EA Admins can see the committed quantities from different companies as shown in the screenshot below:

**Note:** In this document, we are selecting a single product to explain it efficiently, however in real scenarios, Admins have to manage more than one product.

**Indicators help Admins to understand the reporting status.** When an Admin hovers over a value, an indicator will pop up telling the Admin what the color code is referring to i.e. if any extra licenses are available or extra licenses are required, etc.

**Indicators show changes in regard to the previous report**. The “Up” arrow signifies that there has been an increase in reported quantity and the “Down” arrow shows a decrease. If there is no change in the reported quantity then no indicator is present.

The EA Admin is the responsible person for TrueUp reporting. Before submitting the TrueUp, they need to perform the following tasks:

**Add:** If an extra quantity is needed, the Admin can add the additional quantity in the “TrueUp Quantity” row.

**Optimize** Every time an EA Admin inspects the reported usage, they can optimize the additional license count. For example, if the required quantity has decreased in one company but increased for another company, then the Admin can move spare licenses between locations, avoiding additional costs.

**Scenario 1 – Adding Licenses**

In this scenario, the EA Admin is reporting the TrueUp. First of all the EA Admin needs to look at the header.

In this case, the total required licenses are 15, whereas from previous purchases the Admin only has 7 licenses. This implies that 8 additional licenses are required in order to be compliant again.

<figure><img src="../../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

The next step would be for the Admin to check the details reported by all companies and look at any change in the usage. As explained above, the up and down arrow indicators displayed in the cells represent changes in usage. “Only changed” filter can preselect locations/products with changed license count.

The below screenshot shows the usage and the changes reported.

<figure><img src="../../.gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>

We can see that license usage in France has increased by 3 and in Great Britain it has increased by 4.

These locations would need more licenses.

Here the Admin can decide which location is appropriate to buy these additional licenses based on tax rates and other factors. The Admin can then add license quantity accordingly against “TrueUp Quantity” for those locations.

<figure><img src="../../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>

**Scenario 2 – Optimization**

In this scenario, the total required licenses equals 10, whereas from previous purchases the Admin only has 4 licenses. This implies that 6 additional licenses are required in order to be compliant again.

<figure><img src="../../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>

We can see that license usage in France has increased by 5 and in Great Britain it has increased by 3.

These locations would need 8 more licenses in total, however usage in Philadelphia has decreased by 2.

The two available licenses in Philadelphia can be used by France or Great Britain and thus only 6 more licenses would be necessary.

Here the Admin can decide which location is appropriate to buy these additional 6 licenses based on tax rates and other factors. The Admin can add license quantity accordingly against “TrueUp Quantity” for those locations.

<figure><img src="../../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

#### Additional Access <a href="#post-3370-_toc513023105" id="post-3370-_toc513023105"></a>

Apart from extra responsibilities, EA Admins have access to additional features that are available on the top and bottom of the EA Reporting page.

* **Reporting Summary**: Using this feature EA Admins can check the reporting summary to see how many products each subsidiary has committed. Based on this summary, they can reach out to the respective representatives of each country if any further information is required. EA Admins can track who reported which company. A responsible contact can be assigned to each company.
* **Create TrueUp:** Only an Admin can create a TrueUp, which means only an Admin can open a slice. Opened slice can be used by EA Users to report usage within locations they are responsible for.
* **Submit:** Used to submit the EA reporting. Once the reporting is completed by the EA Admin, they can submit the report by using the “Submit” button. Users do not have the required permissions to submit the report, they can only commit the usage. Once submitted, the Account Manager receives the report and they will import the TrueUp into the backend system.
