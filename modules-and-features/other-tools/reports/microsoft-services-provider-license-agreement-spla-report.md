---
description: Report on your monthly Microsoft Service Provider License Agreements (SPLA).
---

# Microsoft Services Provider License Agreement (SPLA) Report

The Microsoft Services Provider License Agreement (SPLA) is a license agreement for organizations that want to offer their customers hosted software services, including web services, database services, and applications. Microsoft issues a monthly invoice to the service provider that corresponds to the use of the software. Accordingly, the provider must provide adequate reporting so that monthly usage can be reliably recorded.

The SoftwareOne Client Portal has a custom Service Provider Reporting module that offers advanced management and allows you to create monthly reports for your Microsoft SPLA contract.&#x20;

You can access the module by navigating to the main menu of the Client Portal and selecting **Marketplace** > **Service Provider Reporting**.

## Service Provider Reporting interface

The **Service Provider Reporting** page contains options that allow you to edit product quantities and view your contracts. The page also displays products within each contract, along with the prices, item numbers, and pool. Clicking a product opens up its **Product Detail** page.

<figure><img src="../../../.gitbook/assets/image (282).png" alt=""><figcaption></figcaption></figure>

On the **Service Provider Reporting** page:

* The highlighted column represents the current month.&#x20;
* The **Open** status means that this report hasn't been transmitted yet.
* The **Deadline/Submit Date** represents the delivery date by which the report must be submitted. The reporting window opens on the 28th of the reporting month and closes on the 10th of the following month. Orders must be placed during that time and for the given period. If this date is exceeded, it will be highlighted in red. As a result, entries in future months can only be saved as a draft and cannot be transferred.
* A green star represents changes to quantities after importing an SPLA template.

On the **Service Provider Reporting**, you can also view details of the past reports that have already been submitted, for example, the date of the last order, the day of the last invoice, or the **PO reference**. To view such information, click **Details**.

## View your contracts

You can view your contracts using the **Contracts** option on the **Service Provider Reporting** page.&#x20;

After selecting a contact, click the magnifying glass icon to view the details associated with your selected contract. When you click the magnifying glass icon, the License Agreement Details page opens.&#x20;

## Edit contract quantities

You can edit the quantity of products using the **Edit All Contracts Quantities** option. Follow these steps to edit the quantity:

1. On the **Service Provider Reporting** page, click **Edit All Contracts Quantities**.
2. In **Edit All Contracts Quantities**, click **Download Template**. When you click this button, an Excel file is downloaded to your system.&#x20;
3. Open the downloaded file and provide the information in the **Open Quantities** and **Comment** columns.&#x20;
4. Save your file and upload it to the Client Portal. To upload the file, click **Import Template** in **Edit All Contracts Quantities**.&#x20;

The report view reloads automatically to display the updated data. All changes in the quantities after importing the SPLA template are marked with a green star and can also be checked in **Latest Import Changes Applied**.

{% hint style="info" %}
Downloading the template might take a few seconds. If any of your contracts are outdated, the template will include the oldest month still open. Ensure all previous months are updated and sent before performing this action for the current month.
{% endhint %}

## Adjust quantity

Follow these steps to adjust the quantity:

1. On the **Service Provider Reporting** page, click within a cell. The background color of the cell changes and a **Details** window containing details of the data set opens.&#x20;
2. Enter the new value in the cell and add your comments in the **Comments** field.
3. Click **Save** to update your changes.

When you save your changes, the yellow-colored fields will change to their original color. This creates or updates a draft for the revised month, which can be edited until it is transferred via **Create Order.**

{% hint style="info" %}
If you add your comments, the red marking in the cell will imply that a comment has been entered into this field. If you hover your mouse, the comment will be displayed. When you are finished, select another line, and the quantity will be accepted. The cell that has now been edited is highlighted in yellow as a sign that changes have been made but have not been saved yet.
{% endhint %}

## Add new products <a href="#htoc-adding-new-products" id="htoc-adding-new-products"></a>

You can add new products from the SPLA catalog using the **Add Product** option (available under the **Product** column).

Follow these steps to add a new product:

1. On the **Service Provider Reporting** page, click **Add Product**.&#x20;
2. Select a product from the list or type the product name. The product is added.

<figure><img src="../../../.gitbook/assets/image (283).png" alt=""><figcaption></figcaption></figure>

3. Click **Save**. The feature creates or updates a draft for the revised month, which can be edited until it is transferred via **Create Order**.

## Copy or clear quantities <a href="#htoc-copying-or-clearing-quantities" id="htoc-copying-or-clearing-quantities"></a>

The **Copy Quantities** option allows you to copy the values from the previous month.

* To copy the quantities, select the cell for the month to be filled out to select it and click **Copy Quantities**. After clicking the button, the values from the previous month are transferred.
* To clear the values, click **Clear Quantities**.

## Save changes <a href="#htoc-saving-changes-and-creating-an-order" id="htoc-saving-changes-and-creating-an-order"></a>

The **Save** option is enabled when you make any changes, for example, if you add comments or new products.

The action creates a draft that can still be edited. Draft numbers are always stored and can be changed until the final submission. The orders that are not submitted or completed are marked as **Draft** in the bottom line of the table as well.

## Create an order

The **Create Order** option allows you to move your changes to the shopping cart.&#x20;

Before clicking **Create Order**, make sure to review the address details and contact persons. Personal references or order numbers can also be stored, and related documents can be attached.

<figure><img src="../../../.gitbook/assets/image (709).png" alt=""><figcaption></figcaption></figure>

The **PO Number 1** field is blocked from editing because the SPLA month year is automatically displayed. The payment method and special instructions can be transmitted.

After checking the specified details and products in the shopping cart, the order can be submitted. Once you've placed the order, the color of the submitted month in the overview changes from green to gray, and the status changes to **Submitted.**&#x20;

It means that your request has been sent to the appropriate team. If there are inconsistencies, or if there is a better cost model that you could use, they will contact you.&#x20;

## Submit zero usage <a href="#htoc-submit-zero" id="htoc-submit-zero"></a>

The **Submit Zero** option allows you to confirm that no usage statement should be sent for a given month.

For security reasons, the page will open a new dialog window asking you to confirm the action. Then the column background of the submitted month in the overview changes from green to gray, and the status changes to Reported Zero.

## Related topics

{% content-ref url="https://app.gitbook.com/s/B8rr5E9BB4HBPts7pBng/modules/procurement/service-provider-dashboard" %}
[Service Provider Dashboard](https://app.gitbook.com/s/B8rr5E9BB4HBPts7pBng/modules/procurement/service-provider-dashboard)
{% endcontent-ref %}
