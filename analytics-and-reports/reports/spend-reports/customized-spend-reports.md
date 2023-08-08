---
description: >-
  Create multiple custom report views and combine them into one simple dashboard
  experience
---

# Customized Spend reports

With the new reporting capability, you can create multiple custom views and aggregate them into a simple dashboard experience.

***

### Building custom reports <a href="#building-custom-reports" id="building-custom-reports"></a>

**To create a custom executive report**

1. From the main menu, navigate to **Analyze** and select **Consumption Overview.**
2. Select **Executive Report** and then select **Add your Report** to create your custom report.
3. Enter a name for your new report. The name can be changed later if needed.

The report with aggregated Provider data will be added to your new Executive Report.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/09/image-12-1024x625.png" alt=""><figcaption></figcaption></figure>

You will also see spaces with a “plus icon” (4). Clicking on the plus icon allows you to quickly add new data that is of interest to you.

Each element has its own filters and grouping – including date range. You can override dates, grouping, and currency (_Figure 5_) in the report context to align all elements.

<div align="left">

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/09/image-13.png" alt=""><figcaption></figcaption></figure>

</div>

Dates, grouping, or currency overrides are not saved. So when you open the report again it will present data in the default state.

Only elements that are time-based will be affected by grouping changes. Elements with a custom “X” axis will ignore this setting.

You can delete a report by selecting the cog icon (3) and selecting **Delete report**. Once you confirm this action the report will disappear from the drop down.

Similarly, you can edit the report name by clicking on the pencil icon (2)

All changes made in the report are auto-saved.

***

### Reordering elements <a href="#reordering-elements" id="reordering-elements"></a>

**To rearrange the elements**

1. Hover over the element you want to move until you see the cross/arrow icon appear.&#x20;
2. Click on that icon and drag the element to the area you want to move it to.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/09/image-14-1024x538.png" alt=""><figcaption></figcaption></figure>

***

### Deleting Elements <a href="#deleting-elements" id="deleting-elements"></a>

You can remove elements by hovering over the element until you see the bin icon appear. Select the bin to delete the element.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/09/image-15.png" alt=""><figcaption></figcaption></figure>

***

### Using the edit mode <a href="#editing" id="editing"></a>

To enter the edit mode, click anywhere on the chart element.

***

### Configuring elements <a href="#configuring-elements" id="configuring-elements"></a>

In the configuration section, you can define your data and pick your preferred presentation option.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/09/image-16-1024x821.png" alt=""><figcaption></figcaption></figure>

You can control data displayed on the “X” axis in the “_Show By:_” drop-down (1). Available options are **Day**, **Month**, and **None**.

The **Day** and **Month** settings will make the “X” axis time-based. However, **None** will render the value selected in the “_Group by_” section (3).

***

### **Advanced filtering**

Reports support advanced filtering (2). This scans through all your data providers (e.g. _Azure_ / _Software Assets_ / _Virtual_) and provides you with a unified search experience.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/09/image-9-1024x555.png" alt=""><figcaption></figcaption></figure>

Search index breaks words by space or “-” character and uses “starts with operator” for each word. For example: for resource **my-test-vmineurope** if you type “test”, the index will find this resource. However, if you type “est” this resource will not be found.

By clicking the hierarchy icon (4) you can refine your custom group search using the tree structure. The changes made in the custom group selector are reflected in the filter control and vice-versa.

**Grouping Selector**

There are many grouping options. Availability depends on the providers you have activated (3).

**Chart Type Selector**

Depending on your business use case you can choose different presentation layers for your data (4), available options are:

* Line (perfect for daily time series)
* Bars (ideal for categories, for example, MeterCategory)
* Pie (the best for summaries, for example, Providers)
* Table (in all listings, for example, Resources)

**Currency Selector**

Each element can have a different currency. By default your budget currency is selected. However, you can change it at any time (5)

***

### Sharing executive reports <a href="#sharing-executive-reports" id="sharing-executive-reports"></a>

Executive Reports support quick share functionality. You can easily share your report with your colleagues by following the steps below.

#### Sharing a personal report <a href="#sharing-an-personal-report" id="sharing-an-personal-report"></a>

To share a personal report, select the report you would like to share from the report selection. Select **Share**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/03/image-2-1024x153.png" alt=""><figcaption></figcaption></figure>

Next, select members from your account. Allowed roles are **Can view** and **Can edit**. Users with the **Can Edit** role can also adjust the sharing list with limitations to the **Owner** role.

***

### Exporting executive reports <a href="#exporting-executive-report" id="exporting-executive-report"></a>

You can export an executive reports to a PDF.&#x20;

**To export a report**

1. Select your report from the report selector.
2. Select **Exports**.
