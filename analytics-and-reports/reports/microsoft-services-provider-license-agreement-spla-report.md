---
description: Report on your monthly Microsoft Service Provider License Agreements (SPLA).
---

# Microsoft Services Provider License Agreement (SPLA) report

The Microsoft Services Provider License Agreement (SPLA) is a license agreement for organizations that want to offer their customers hosted software services, including web services, database services, and applications.

Microsoft issues a monthly invoice to the service provider that corresponds to the use of the software. Accordingly, the provider must provide adequate reporting so that monthly usage can be reliably recorded.

The SoftwareOne Client Portal has a custom Service Provider Reporting module that offers advanced management and allows you to create monthly reports for your Microsoft SPLA contract.

***

## Accessing the Service Provider reporting

**To access the Service Provider Reporting module**

* From the main menu, navigate to **Marketplace** and select **Service Provider Reporting**.

***

### Editing contract quantities

**To edit contract quantities**

1\. On the **Service Provider Reporting** page, select **Edit All Contracts Quantities**.

2\. Select **Download Template** to download the Excel template. Provide the information in the **Open Quantitie**s and **Comment** columns. Entries in other fields mean that the edited template cannot be imported.

3\. Upload the file using the **Import Template** option.

The report view reloads automatically to display the updated data. All changes in the quantities after importing the SPLA template are marked with a green star in the grid and can also be checked in the **Latest Import Changes Applied** area.

{% hint style="info" %}
**NOTE**: It might take a few seconds for the template to download. Additionally, if some of your contracts are not updated, this template contains the oldest month that is still open. To perform this action for the current month, first update and send all old months.
{% endhint %}

***

### Viewing contracts

**To view a contract**

1. Selecting the contract from the list.
2. View the associated contract details by selecting the magnifying glass icon.

If there are different invoices within the selected enrollment, you can switch between them in the **Reports** area.

#### Table overview <a href="#htoc-understanding-the-data" id="htoc-understanding-the-data"></a>

The table displays the current reported products with their prices, item numbers, and pool. If you click on a single product, you'll be redirected to the product details page.

If a column is highlighted in green, it indicates that it's the current active month. The **Open** status means that this report hasn't been transmitted yet.

<figure><img src="../../.gitbook/assets/image (15) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The **Deadline/Submit Date** is the delivery date by which the report must be submitted. The reporting window opens on the 28th of the reporting month and closes on the 10th of the following month. Orders must be placed during that time and for the given period. If this date is exceeded, it will be highlighted in red.

As a result, entries in future months can only be saved as a draft and cannot be transferred.

All changes to quantities after importing an **SPLA template** are marked with a green star.

***

### Viewing details

You can view details of the past reports that have already been submitted, for example, the date of the last order, the day of the last invoice, or the **PO reference**.

To view the details, select **Details**.

***

### Adjusting quantities

**To adjust quantities**

1. Select the cell. The **Details** window will open containing details of the data set.&#x20;
2. Enter the new value in the cell and optionally add your comments to the details window.
3. Select **Save** to update the changes.

When you save your changes, the yellow-colored fields will change to their original color. This creates or updates a draft for the revised month, which can be edited until it is finally transferred via **Create Order.**

{% hint style="info" %}
**NOTE**: If you choose to add your comments, the red marking in the cell will imply that a comment has been entered into this field. If you hover your mouse, the comment will be displayed. When you are finished, select another line, and the quantity will be accepted. The cell that has now been edited is highlighted in yellow as a sign that changes have been made but have not been saved yet.
{% endhint %}

***

### Adding new products <a href="#htoc-adding-new-products" id="htoc-adding-new-products"></a>

You can add new products from the SPLA catalog using the **Add Product** option.

**To add a new product**

* Enter the product name or article number. The list will be filtered automatically.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

If an incorrect list is selected, you can remove the products from the list. To do this, remove the product with the displayed '**X**' next to the product name before saving.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

To save these changes, click **Save**. The feature creates or updates a draft for the revised month, which can be edited until it is finally transferred via **Create Order**.

***

### Copying or clearing quantities <a href="#htoc-copying-or-clearing-quantities" id="htoc-copying-or-clearing-quantities"></a>

The **Copy Quantities** option allows you to copy the values from the previous month.

To copy the quantities, select the cell for the month to be filled out to select it and select **Copy Quantities**. After clicking the button, the values from the previous month are transferred.

To clear the values, select **Clear Quantities**.

To save your changes, click **Save**. The yellow colored fields will turn back to their original color and all values are saved. This creates or updates a draft for the revised month, which can be edited until it is finally transferred via **Create Order**.

***

### Saving changes and creating an order <a href="#htoc-saving-changes-and-creating-an-order" id="htoc-saving-changes-and-creating-an-order"></a>

The **Save** option is enabled when you make any changes, for example, if you add comments, adjust the values, or add new products.

The action creates a draft that can still be edited. Draft Numbers are always stored and can be changed until the final submission. The orders that are not submitted or completed are marked as ‘Draft’ on the bottom line of the table as well.

***

### **Create an order**

The entered values are moved to the shopping cart by clicking **Create Order**. Make sure to review the address details and contact persons. Personal references or order numbers can also be stored, and related documents can be attached.

<figure><img src="../../.gitbook/assets/image (199).png" alt=""><figcaption></figcaption></figure>

The **PO Number 1** field is blocked from editing because the reference 'SPLA month year' is automatically displayed. The payment method and special instructions can be transmitted.

After checking the specified details and products in the shopping cart, the order can be submitted.

After placing the order, the column background of the submitted month in the overview changes from green to gray, and the status changes to **Submitted.** Now the request is checked by the local hosting team. If there are inconsistencies, or if there is a better cost model that you could use, they will contact you. You will finally receive an order confirmation by email.

***

### Submit zero usage <a href="#htoc-submit-zero" id="htoc-submit-zero"></a>

The **Submit zero** option allows you to confirm that no usage statement should be sent in the given month.

For security reasons, the page will open a new dialog window asking you to confirm it before the transmission of the data. Then the column background of the submitted month in the overview changes from green to gray, and the status changes to Reported Zero.

***

## Accessing the Service Provider dashboard <a href="#htoc-accessing-the-service-provider-dashboard" id="htoc-accessing-the-service-provider-dashboard"></a>

**To access the Service Provider Dashboard**

* From the main menu, navigate to **Analyze** and select **Service Provider Dashboard**.

The dashboard displays the cost of the monthly usage by the pool, distribution of the costs by product as well as pool, and monthly costs by country.

You can filter the areas by a certain period, certain agreements, contracts, or reports. You can also determine which products to display - all or just a few. You can also filter by product, country, or pool using the advanced filter options or by selecting the legend.
