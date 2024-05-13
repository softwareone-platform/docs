---
description: Cloud Cost Optimization Dashboard.
---

# Cloud cost optimization

The Cloud Cost Optimization module allows organizations to deliver optimization to their cloud infrastructure, and deliver savings through various strategies that form a part of the framework.

You can access the dashboard by navigating to the main menu of the Client Portal and selecting  **Cloud tools** > **Cloud Cost Optimization**.&#x20;

{% hint style="info" %}
The Cloud Cost Optimization dashboard requires all the permissions for the Tag and Resource Manager and Consumption modules in Cloud Spend Management.&#x20;
{% endhint %}

## Dashboard interface

The Cloud Cost Optimization Overview page contains two sections **Overview Chart** and the **Overview Grid**.

![](https://872874700-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FB8rr5E9BB4HBPts7pBng%2Fuploads%2FvDlLKXxw37eUXbVH0JUK%2Fimage.png?alt=media\&token=90a48b77-c354-41da-a373-87daad8e9252)

### **Overview chart**

The Azure and AWS tabs summarize cost optimization opportunities for the cloud environments. The top pane summarizes savings through a pie chart and the following metrics:

* **Savings breakdown by Strategy** - The pie chart shows a percentage breakdown of achievable Savings as a proportion of the total savings. For example, in the chart above, Savings through Azure Hybrid Benefit is 41.45% of Total Predicted Savings (EUR 1,080,421.31). All the numbers are calculated for 1 year or 3 years depending on the selection in the dropdown.
* **Year selection** - The metrics shown on the top pane are based on the year selection of 1 year or 3 years.

Changing the year selection in the dropdown does not persist in the year setting in the system. It is only meant to show you the savings achievable over 1 or 3 years. Changing the setting in the backend is only available to Cloud Cost Optimization consultants. If you need to change the year setting, please speak to your Cloud Cost Optimization Consultant, who will be able to do it for you.

* **Total Predicted Cost** - This value represents the cost of your Azure environment over the next year or three years.
* **Total Predicted Savings** - This value represents the savings achievable as a proportion of the total cost.

Calculations across the Cloud Cost Optimization system assume consumption data and costs for the last 2 weeks. This setting can be configured by your Cloud Cost Optimization Consultant to one of the last 2 weeks, last 4 weeks, last 12 weeks, and last 52 weeks.

### **Overview grid**

The grid breaks down the savings achievable through each of the strategies. The **Predicted Savings** **%** in the grid for each strategy is a proportion of the cost for that strategy. Therefore this might be different from the percentage shown in the pie chart above (which shows it as a proportion of total savings).

## Strategy pages

The Strategy pages each explain an optimization strategy that allows you to achieve savings. This section explains the components of any optimization strategy and allows you to understand common operations on these pages. The following are the strategies for Cloud Cost Optimization:

{% hint style="info" %}
If a strategy contains 0% savings, then that strategy will not be visible.
{% endhint %}

1. Orphaned Resources
2. DEV/TEST (Not available for AWS environments)
3. Rightsizing
4. Resource Automation
5. Cross Region Optimization
6. Instance Modernization
7. Reserved Instances
8. Azure Hybrid Benefit (Not available for AWS environments)
9. Bring your own License

## **Strategy page fields**

* **Showing for** -  This indicates the year selection that the rest of the metrics are based on. This can only be changed by the Cloud Cost Optimization Consultant. Please reach out to them if you want to change this.
* **Cost at point of optimization -**  This indicates the cost at the point of optimizing all the impacted resources in the strategy.

<details>

<summary>Why is it called 'Cost at point of optimization'?</summary>

Let's take an example of a resource that is a candidate for the Rightsizing and Cross-Region Optimization strategies. Let us assume that the cost of the resource today is 100$ a year. The cost at the point of optimization of the resource on the Rightsizing strategy page will show up as 100$. However, if the resource is being recommended to be rightsized, so that the new cost of the resource is 50$, then the cost at the point of optimization of the resource on the Cross-Region Optimization strategy will show up as 50$. Cost at the point of optimization takes into account all savings for the resource on previous strategies. If you want to look at the cost of the resource, Click on Customize grid, and choose “Predicted Current Cost”.

Cost at the point of optimization for the strategy is the sum of the cost at the point of optimization of all resources in the Impacted Resources tab of the strategy.

This is the predicted new cost of the resources in the strategy once the strategy optimizations have been applied to the resources in the strategy.

This is the amount of money you can save on the resources in the Impacted Resources tab of the given strategy.

This tab shows you a list of the resources that are being recommended as a candidate for the specific strategy optimization in question. If you do not want to optimize the resource using the optimization recommendation, you can dismiss the resource from the strategy. Dismissing the strategy will move the strategy into the Dismissed tab, and will not count the cost and savings from the resource towards that strategy.

</details>

<details>

<summary><strong>What if an impacted resource is no longer a candidate for a strategy?</strong></summary>

In such a scenario, the system will automatically remove the affected candidate from the Impacted Resources tab, and will appropriately reflect the costs and savings on the Strategy and the Overview pages.

Note that if a resource is identified as not a candidate for a strategy anymore, it will not show up in the Dismissed tab, as the resource has not been manually excluded. Such a resource will show up in the Review Changes tab with the Status “Removed”.

Similarly, if a new resource is identified as a candidate for a strategy, then the resource will be automatically included in the strategy and the Impacted Resources tab.

The dismissed tab shows resources that have been manually excluded from a strategy by a user. Any dismissed resource can be included back in the strategy so long as the strategy has not been marked as complete.

The review changes tab is a list of all changes to resource candidates applied automatically by the system. Newly identified candidates will show up in the Review Changes tab till they are marked as reviewed as well as the Impacted Resources tab. Candidates who are no longer candidates will also show up in the Review Changes tab with the status “Removed”.

We recommend that you review the Review Changes tab every time you log in, so you are aware of all recent activity within the Cloud Cost Optimization system.

</details>

### **Marking a strategy as complete or reopening a strategy**

A strategy can be marked as complete only if all previous strategies are completed. This is because every complete strategy influences the savings achievable on subsequent strategies.&#x20;

Marking a strategy as complete will mean no changes can be made to the strategy i.e. no resources can be dismissed from the strategy, or no already dismissed resources can be included in the strategy. To do these operations on a completed strategy, you must re-open a strategy. You can reopen a strategy, only if all strategies after it are open.

### **Exporting data from Cloud Cost Optimization**

Each of the strategy pages enables users to export data on the grid to an Excel file using the Export button on the top right of the grid.

The export button will only export the columns visible on the grid at the time of the export. However, you can customize the grid to show extra columns using the **Customize** button.

### Strategy – Orphaned Resources <a href="#strategy-orphaned-resources" id="strategy-orphaned-resources"></a>

The Orphaned resources allow one to identify resources that can be shut down or decommissioned as they are not being effectively utilized. Note that resources that show up in Orphaned Resources, will not show up in other strategies, as they will be shut down on completion of the Orphaned Resources strategy.

### Strategy – Instance Modernization <a href="#strategy-instance-modernization" id="strategy-instance-modernization"></a>

Instance modernization is about paying the best price for the same resource while maintaining or improving its capabilities.

### Strategy – Cross Region Optimization <a href="#strategy-cross-region-optimization" id="strategy-cross-region-optimization"></a>

This strategy identifies resources that can be rehoused in a cheaper region, thereby reducing the overall cost of the resource.

### **Strategy Level Configuration for Cross-region Optimization**

Optimization recommendations for this strategy are dependent on the selection of a region subset. This selection is done either by the customer or by the consultant.

If the regions have not been selected, then you may likely see this on the Cross-Region Optimization strategy page.

![](https://872874700-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FB8rr5E9BB4HBPts7pBng%2Fuploads%2Fk9tzAmXaI3uJ23cF9Kik%2Fimage.png?alt=media\&token=386943f4-3c2b-47cd-960a-a2cd984b2067)

In order to move forward, kindly select the regions by clicking on Edit, and select the regions and save changes.

![](https://872874700-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FB8rr5E9BB4HBPts7pBng%2Fuploads%2FHJEo7oTvdilpsziuMD2q%2Fimage.png?alt=media\&token=2a1d78a7-e0de-4b67-81a4-468a9647852e)

The Savings threshold is the minimum savings that needs to be achieved to make the resource viable for Cross-Region Optimization.

Note that the savings threshold used is 10% by default, and this configuration can only be updated by your Cloud Cost Optimization Consultant.

### **Resource Level Region Configuration for Cross-region Optimization**

Similar to the regions that can be selected at the strategy level, a region can be overridden per resource. You may typically want to do this, if there is a particular resource that you want to house in a fixed region, regardless of the savings available through other regions.

Note that resource-level regions can only be selected from among the region subsets already configured by the user or the consultant. E.g. if the region subset is set to West Europe and North Europe, the resource-level region can only be set to one of these two.

You can do this by navigating to Resource Details > Edit.

Note that if a region is set at a resource level, then it will not be assigned a cheaper region automatically by the system.

![](https://872874700-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FB8rr5E9BB4HBPts7pBng%2Fuploads%2FNOxENOK2d57X7MkLGQNF%2Fimage.png?alt=media\&token=e32fd2a3-9cc7-4fbb-8f5c-f1d835b041da)

### Strategy – Resource Automation <a href="#strategy-resource-automation" id="strategy-resource-automation"></a>

This strategy identifies resources that can be automated to be on during certain times of the day and shut down during others.

Resource uptime is defaulted to 24 hours a day, 7 days a week. This setting can be updated by your Cloud Cost Optimization consultant if there is a common Automation uptime window for all your resources.

### **Resource Level Uptime Configuration for Resource Automation**

An uptime window can be configured on resource level using Resource Details > Edit, as shown below.

![](https://872874700-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FB8rr5E9BB4HBPts7pBng%2Fuploads%2FKHM6t6Vq5QwHNyP2Ui9h%2Fimage.png?alt=media\&token=e625035d-8461-414b-8cf8-96546936257c)

### Strategy – Reserved Instances <a href="#strategy-reserved-instances" id="strategy-reserved-instances"></a>

If a resource is planned to be used more than 60% of the time during a year, it might make sense to commit consumption for 1 or 3 years. Doing this can result in savings of up to 40% on compute cost, depending on the resource being committed.

Reserved Instance term is defaulted to 1 year for every resource.

**Resource Level Reserved Instance Term Configuration**

Reserved Instance term can be configured on resource level using Resource Details -> Edit, as shown below.

![](https://872874700-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FB8rr5E9BB4HBPts7pBng%2Fuploads%2Fc7IYpHph9xYmNzDFJb7P%2Fimage.png?alt=media\&token=896fdfd5-4ed1-4760-9cba-5d3ee7aa7ab3)

### Strategy – Azure Hybrid Benefit <a href="#strategy-azure-hybrid-benefit" id="strategy-azure-hybrid-benefit"></a>

This strategy is not available for AWS Cloud Cost Optimization

Hybrid Use Benefits for Windows Sever provides, under specific conditions, the option to bring your own Windows Licenses, with active Software Assurance to cover virtual machine licenses in Azure. Using this benefit could save up to 40% on license costs, which are normally hidden behind the virtual machine cost.

### Strategy – Bring your own License <a href="#strategy-bring-your-own-license" id="strategy-bring-your-own-license"></a>

Similar to Hybrid Use Benefits, Bring Your Own License benefits allow customers to bring other licenses to Azure or AWS, and receive a discount for the licensing portion of the cost. In this section we calculate savings for Microsoft SQL Server and Redhat Enterprise License.

No configuration is available to users on this strategy. License Cost for Windows, Linux and SQL can be updated by your Cloud Cost Optimization Consultant.
