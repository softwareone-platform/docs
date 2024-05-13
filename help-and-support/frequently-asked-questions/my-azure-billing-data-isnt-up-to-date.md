# My Azure billing data isn't up to date

The Client Portal uses several Microsoft APIs to pull data that allows you to create Spend reports, [Budgets](../../extensions/cloud-tools/budgets/), and [Chargebacks](../../extensions/cloud-tools/chargebacks/). In some cases, it can take up to 24 hours for the resource cost to be accessed through the interface.

As the Client Portal synchronizes your Azure billing data only once a day, sometimes, it might take 48 hours for the data to refresh.

Additionally, the reconciliation files are available no later than the 8th day of every month. Microsoft invoices partners based on this file. Therefore, we recommend that you send chargebacks after the 8th day of the month. For more information, see [Reconciliation file availability](https://docs.microsoft.com/en-us/partner-center/billing-basics) and [Microsoft Partner Center data delay](https://docs.microsoft.com/en-us/partner-center/daily-rated-usage-recon-files).
