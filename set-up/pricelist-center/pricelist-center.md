# Pricelist Center

### Introduction <a href="#introduction" id="introduction"></a>

The Pricelist Center is a part of our Cloud Management experience. The Pricelist Center offers a way to either check on the latest prices from IaaS/PaaS Cloud Providers or set prices for SaaS Cloud Providers. We have consolidated all price lists, so users can easily search for, or sort by various prices that are of interest or that users may want to compare.

Many supported IaaS/PaaS Cloud Providers will publish a price list either based on current pricing levels or a list price for their service. In addition, those same providers will offer Reserved Instances as a separate price list. To ensure users are aware of the latest prices from these Providers, we have made them available for users to either filter/sort by.

SaaS Cloud Providers do not provide price lists, but prices have to be set either by the user or by SoftwareONE. If users are an Office 365 EA or Adobe customer, they will need to set the price for each of their subscriptions/licenses and update them by date, based on any changes on contract renewals. If users are Office 365 Simple customers, SoftwareONE will automatically update these prices.

This article will provide an overview of how the IaaS/PaaS Cloud Provider price lists work and how to input or view prices for SaaS Cloud Providers.

### Navigating to the Pricelist Center <a href="#navigating-to-the-pricelist-center" id="navigating-to-the-pricelist-center"></a>

From the main PyraCloud navigation menu, click on the “Setup” and select “Pricelist Center”.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/11/PLC_Navigation-1024x772.png" alt="" height="772" width="1024"><figcaption><p><strong>Figure 1 Navigating to the Pricelist Center</strong></p></figcaption></figure>

### Understanding the Main Pricelist Center Page <a href="#understanding-the-main-pricelist-center-page" id="understanding-the-main-pricelist-center-page"></a>

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/11/PLC_Overview-1024x535.png" alt="" height="535" width="1024"><figcaption><p><strong>Figure 2 – Main Pricelist Center Page</strong></p></figcaption></figure>

| 1  | <p>Pricelist Views – Three options exist which were designed to help users quickly find products of interests.<br>• All – shows all pricelists<br>• Missing Prices – this view is very important and all products under this view should be addressed. Any missing prices means that a Consumption Report may not be accurate. Go to this view to add any missing prices. This view is empty if all products are having a price.<br>• Customer Set Prices – shows all products, which are having a customer defined price. Here you can maintain the configured prices.</p> |
| -- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2  | Filters – This section is used to quickly find products by Price List Type, Product Name, Region or Currency.                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 3  | More Options – In addition to the Filters, we have provided additional filter options to quickly find products of interested.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 4  | Product – This is the name of the product, provided by the Cloud Provider and Pricelist                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 5  | Agreement – If you are having multiple agreements for the same product you will see the agreement ID here.                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 6  | Date – The date field is used to indicate when the price for this product was last applied by the user or updated by the provider.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 7  | Region – Some products are having different prices per region.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 8  | Currency – The currency field is used to show the currently set price or the prices per currency. For SaaS Prices, users will only see one currency. For IaaS/PaaS prices, users will see multiple currencies to pick from, to understand those product costs in the currency of choice.                                                                                                                                                                                                                                                                                    |
| 9  | Unit Price – The unit price is either the price set by the user or the price being provided by the Provider.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 10 | Actions – With “View” we will show the details of this product. When a price can be added to an individual product, users will see the “+ Add new price” option in this column.                                                                                                                                                                                                                                                                                                                                                                                             |
| 11 | Customize – As more columns are added to this table, not all the available properties of the prices may be displayed. “Customize” can be used to show additional columns or hide existing ones.                                                                                                                                                                                                                                                                                                                                                                             |
| 12 | Export – To export the data from the grid                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |

### Finding a Provider Price List <a href="#finding-a-provider-price-list" id="finding-a-provider-price-list"></a>

To open a Provider Price List, go to the Pricelist Center and choose a “Price List Type” and for some providers the “Region”.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/01/word-image-2.png" alt="" height="227" width="425"><figcaption><p><strong>Figure 3 – Finding a IaaS/PaaS Provider Price List</strong></p></figcaption></figure>

Now click “Search”, to display the results of that Provider’s prices in the table below.

### Filtering the Price List Results <a href="#filtering-the-price-list-results" id="filtering-the-price-list-results"></a>

IaaS/PaaS Price Lists often have specific prices for certain Regions. For instance, Microsoft may charge a different price for an A3 Cloud Service or Virtual Machine, between a US and UK region.

Use the “Product Name” text input field and the “Region” field to help narrow down the prices. Here is an example:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/01/word-image-3.png" alt="" height="416" width="1201"><figcaption><p><strong>Figure 4 – Filtering the Price List Results – Show More Options</strong></p></figcaption></figure>

As a result, see many A3 options will be displayed, but only based on those two regions. Here is an example:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/01/word-image-4.png" alt="" height="575" width="973"><figcaption><p><strong>Figure 5 – Filtering the Price List Results – Results Displayed for Regions</strong></p></figcaption></figure>

SaaS Price Lists are a different from IaaS/PaaS Pricelists from Cloud Providers. SaaS Price lists are based on what Subscriptions or Licenses are active for that SaaS Provider. To search for a specific Price for an Office 365 product, be sure to select the Office 365 Pricelist and type in a product name or select from an Active Tenant attached to PyraCloud.

### Adding Missing SaaS Prices <a href="#adding-missing-saas-prices" id="adding-missing-saas-prices"></a>

It’s important to add any missing price to the Pricelist Center, to ensure accurate Consumption reports as generated as users analyze their spend over time with the Consumption Overview page. To determine what SaaS Subscriptions/Licenses require prices, go to the Pricelist Center and click on the “Missing Prices” 1 tab.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/01/word-image-8.png" alt="" height="307" width="638"><figcaption><p><strong>Figure 9 – Missing Prices Tab</strong></p></figcaption></figure>

If this is the first-time entering prices, users may notice several Subscriptions/License with missing prices.

Please add the proper pricing to each Subscription/License by clicking on the “+ Add new price” button on the right.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/01/word-image-9.png" alt="" height="234" width="1472"><figcaption><p><strong>Figure 10 – Adding Pricing to Subscription/License</strong></p></figcaption></figure>

| 1 | The “Effective Date” field is used as the starting date for the price entered. PyraCloud only collect SaaS data based on when the SaaS Subscription was added to PyraCloud. So dates can either be the date the SaaS Subscription was added to PyraCloud or the date in which users purchased these subscription/licenses (for their own accounting purposes). Anything before the integration with PyraCloud will be ignored. If users don’t know the prices for their SaaS license they will need to refer to the individual who purchased the SaaS service for their organization. |
| - | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2 | This is where users input the price for your SaaS subscription/license. Once complete, click on “Add” to the add this price to the subscription/ license in question.                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 3 | The Currency is set based on the contract information stored in PyraCloud. If a change of currency is required, please contact support@pyracloud.com or your SoftwareONE Account team.                                                                                                                                                                                                                                                                                                                                                                                                |

Adding prices require a recalculation of the historical spend information within our system. This may take up to 24 hours to complete.

### Managing SaaS Prices <a href="#managing-saas-prices" id="managing-saas-prices"></a>

After the SaaS prices are added, users may want to update them in the future or remove themif they were not accurate. To do so, find the SaaS prices in the Pricelist Center. Navigate to the Pricelist Center and click on the “Customer Set Prices” 1 tab.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/01/word-image-10.png" alt="" height="554" width="1107"><figcaption><p><strong>Figure 11 – Customer Set Prices Tab</strong></p></figcaption></figure>

On this page, users will see all the current prices that have been set for all of their SaaS products. If users would like to refine this list to a specific Price List or Product name, use the filters above to find the specific Price Lists or products.

By clicking on “View” users can review the history of Prices and their start dates, e.g. if users are renewing a contract with a different price or would like to see how far back prices are applied. Within this Product Details view the user can view the historical prices, change them or add new ones.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/01/word-image-11.png" alt="" height="463" width="1349"><figcaption><p><strong>Figure 12 – Managing SaaS Prices</strong></p></figcaption></figure>

It might be possible, that a user can’t “Edit Price” or “Add Price” due to his user permission. Please reach out to your administrator to change this permission within the User Management.
