---
description: >-
  Find information on how to access the Pricelist Center and view or add prices
  from the IaaS/PaaS cloud providers.
---

# View and Manage Prices

***

### Accessing the Pricelist Center <a href="#navigating-to-the-pricelist-center" id="navigating-to-the-pricelist-center"></a>

**To access the Pricelist Center**

* From the main menu, go to **Setup** and select **Pricelist Center**.

The Pricelist Center page contains several sections.

<figure><img src="../../.gitbook/assets/image (42) (1).png" alt=""><figcaption></figcaption></figure>

| Number | Field/Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1      | <p>Pricelist Views – Three options exist which were designed to help users quickly find products of interest.</p><ul><li>All – Shows all pricelists</li><li>Missing Prices – This view is very important and all products under this view should be addressed. Any missing prices means that a Consumption Report may not be accurate. Go to this view to add any missing prices. This view is empty if all products are having a price.</li><li>Customer Set Prices – shows all products, which are having a customer-defined price. Here you can maintain the configured prices.</li></ul> |
| 2      | Filters – This section is used to quickly find products by Price List Type, Product Name, Region, or Currency.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 3      | More Options – In addition to the Filters, we have provided additional filter options to quickly find products of interested.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 4      | Product – This is the name of the product, provided by the Cloud Provider and Pricelist                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 5      | Agreement – If you are having multiple agreements for the same product you will see the agreement ID here.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 6      | Date – The date field is used to indicate when the price for this product was last applied by the user or updated by the provider.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 7      | Region – Some products are having different prices per region.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 8      | Currency – The currency field is used to show the currently set price or the prices per currency. For SaaS Prices, users will only see one currency. For IaaS/PaaS prices, users will see multiple currencies to pick from, to understand those product costs in the currency of choice.                                                                                                                                                                                                                                                                                                     |
| 9      | Unit Price – The unit price is either the price set by the user or the price being provided by the Provider.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 10     | Actions – With “View” we will show the details of this product. When a price can be added to an individual product, users will see the “+ Add new price” option in this column.                                                                                                                                                                                                                                                                                                                                                                                                              |
| 11     | Customize – As more columns are added to this table, not all the available properties of the prices may be displayed. “Customize” can be used to show additional columns or hide existing ones.                                                                                                                                                                                                                                                                                                                                                                                              |
| 12     | Export – To export the data from the grid                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

***

### Finding a provider price list <a href="#finding-a-provider-price-list" id="finding-a-provider-price-list"></a>

**To open a provider price list**

1. Go to the **Pricelist Center** and choose a “Price List Type” and for some providers the “Region”.
2. Select **Search** to display the results of that provider’s prices.

***

### Filtering the Price List results <a href="#filtering-the-price-list-results" id="filtering-the-price-list-results"></a>

IaaS/PaaS Price Lists often have specific prices for certain Regions. For instance, Microsoft may charge a different price for an A3 Cloud Service or Virtual Machine, between a US and UK region.

Use the **Product Name** text input field and the **Region** field to help narrow down the prices. Here is an example:

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

As a result, many A3 options will be displayed, but only based on those two regions. Here is an example:

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

SaaS Price Lists are different from IaaS/PaaS Pricelists from Cloud Providers. SaaS Price lists are based on what Subscriptions or Licenses are active for that SaaS Provider. To search for a specific Price for an Office 365 product, be sure to select the Office 365 Pricelist and type in a product name or select from an Active Tenant attached to PyraCloud.

***

### Adding missing SaaS prices <a href="#adding-missing-saas-prices" id="adding-missing-saas-prices"></a>

It’s important to add any missing price to the Pricelist Center, to ensure accurate Consumption reports as generated as users analyze their spend over time with the Consumption Overview page. To determine what SaaS Subscriptions/Licenses require prices, go to the Pricelist Center and select **Missing Prices** tab.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

If this is the first time entering prices, users may notice several Subscriptions/Licenses with missing prices.

Add the proper pricing to each Subscription/License by selecting **+ Add new price** button.

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

|   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| - | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1 | <p>The <strong>Effective Date</strong> field is used as the starting date for the price entered. </p><p></p><p>PyraCloud only collects SaaS data based on when the SaaS Subscription was added to PyraCloud. </p><p>So dates can either be the date the SaaS Subscription was added to PyraCloud or the date in which users purchased these subscriptions/licenses (for their own accounting purposes). </p><p></p><p>Anything before the integration with PyraCloud will be ignored. If users don’t know the prices for their SaaS license they will need to refer to the individual who purchased the SaaS service for their organization.</p> |
| 2 | This is where users input the price for your SaaS subscription/license. Once complete, click on “Add” to the add this price to the subscription/ license in question.                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 3 | The Currency is set based on the contract information stored in PyraCloud. If a change of currency is required, contact our Support team or your SoftwareOne Account team.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |

Adding prices requires a recalculation of the historical spend information within our system. This may take up to 24 hours to complete.

***

### Managing SaaS prices <a href="#managing-saas-prices" id="managing-saas-prices"></a>

After the SaaS prices are added, users may want to update them in the future or remove them if they are not accurate.&#x20;

To do so, find the SaaS prices in the Pricelist Center. Navigate to the Pricelist Center and select the **Customer Set Prices** 1 tab.

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

On this page, users will see all the current prices that have been set for all of their SaaS products. If users would like to refine this list to a specific Price List or Product name, use the filters above to find the specific Price Lists or products.

By selecting **View**, you can review the history of prices and their start dates, for example, if users are renewing a contract with a different price or would like to see how far back prices are applied. Within this Product Details view the user can view the historical prices, change them, or add new ones.

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

If you're unable to Edit Price or Add Price, it might be due to your permissions. Contact your administrator to change permissions.
