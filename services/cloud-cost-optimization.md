# Cloud Cost Optimization

Cloud Cost Optimization is a capability within PyraCloud that allows organizations to deliver optimization to their cloud infrastructure, and deliver savings through various strategies that form a part of the framework.

* Studies show that organizations are wasting approximately 35-45% of their cloud spend. Areas of waste include over-provisioned or idle instances, abandoned cloud resources, and sub-optimal license assignment methodology. Customers do not maximize value in license assignments, and most do not have a process to check compliance.
* SoftwareONE continuously follows the Azure pricing mechanisms to pinpoint ways that will allow for right-costing and right-sizing savings.\

  * **Right-costing** savings are those that allow you to optimize costs by leveraging commercial/licensing constructs
  * **Right-sizing** savings are those that allow you to optimize cost by changing the technical specifications of the resources that are running in the cloud environment
* SoftwareONE’s Cloud Cost Optimization Service leverages our unique methodology to achieve the best of both right-costing and right-sizing optimization strategies.

***

### Accessing Cloud Cost Optimization <a href="#accessing-cloud-cost-optimization" id="accessing-cloud-cost-optimization"></a>

**To access Cloud Cost Optimization**

* From the main menu, navigate to **Services** and select **Cloud Cost Optimization**.

***

### Requirements for Cloud Cost Optimization <a href="#requirements-for-cloud-cost-optimization" id="requirements-for-cloud-cost-optimization"></a>

The Cloud Cost Optimization solution requires all the permissions for the “Tag and Resource Manager” (look [here](https://help.pyracloud.com/knowledge-base/grant-access-to-pyracloud-for-a-single-azure-subscription/#what-are-the-security-implications)) and “Consumption” modules in Cloud Spend Management (look here).

#### Overview Page <a href="#overview-page" id="overview-page"></a>

The Cloud Cost Optimization Overview page is broken down into two sections –

**Overview Chart** and the **Overview Grid**.

#### **Overview Chart** <a href="#overview-chart" id="overview-chart"></a>

1. Tabs – These summarize cost optimization opportunities for the different cloud environments you may have connected to PyraCloud

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

1. The top pane summarizes savings through a pie chart and a few key metrics (see figure below).

The top pane summarizes the following metrics –

* **Savings breakdown by Strategy** – The pie chart shows a percentage breakdown of achievable Savings as a proportion of the total savings. For e.g. in the chart above, Savings through Azure Hybrid Benefit is 41.45% of Total Predicted Savings (EUR 1,080,421.31). All the numbers are calculated for 1 year or 3 years depending on the selection in the dropdown.
* **Year selection** – The metrics shown on the top pane are based on the year selection of 1 year or 3 years.

Changing the year selection in the dropdown does not persist the year setting in the system. It is only meant to show you the savings achievable over 1 or 3 years. Changing the setting in the backend is only available to Cloud Cost Optimization consultants. If you need to change the year setting, please speak to your Cloud Cost Optimization Consultant, who will be able to do it for you.

* **Total Predicted Cost** – This value represents the cost of your Azure environment over the next year or three years.
* **Total Predicted Savings** – This value represents the savings achievable as a proportion of the total cost.

Calculations across the Cloud Cost Optimization system assume consumption data and costs for the last 2 weeks. This setting can be configured by your Cloud Cost Optimization Consultant to one of last 2 weeks, last 4 weeks, last 12 weeks, last 52 weeks.

#### **Overview Grid** <a href="#overview-grid" id="overview-grid"></a>

2\. The bottom pane contains a grid that breaks down the savings achievable through each of the strategies (see figure below).

The Predicted Savings percentage in the grid for each strategy is a proportion of the cost for that strategy. Therefore this may be different to the percentage shown in the pie chat above (which shows it as a proportion of total savings).

#### Strategy Pages <a href="#strategy-pages" id="strategy-pages"></a>

The Strategy pages each explain an optimization strategy that allows you to achieve savings. This section explains components of any optimization strategy, and allows you to understand common operations on these pages.

The strategies in Cloud Cost Optimization are listed below. If you are looking for something specific relating to any of these strategies, please navigate to the appropriate strategy section.

**Note**: If the strategy contain 0% savings then that strategy will not be visible.

1. Orphaned Resources
2. DEV/TEST (Not available for AWS environments)
3. Rightsizing
4. Resource Automation
5. Cross Region Optimization
6. Instance Modernization
7. Reserved Instances
8. Azure Hybrid Benefit (Not available for AWS environments)
9. Bring your own License

#### **Navigating to next strategy** <a href="#navigating-to-next-strategy" id="navigating-to-next-strategy"></a>

One can navigate to the next strategy in sequence by clicking on the Next Strategy arrow to the top right of the page.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

#### **Marking a strategy as complete / Re-opening a strategy** <a href="#marking-a-strategy-as-complete-re-opening-a-strategy" id="marking-a-strategy-as-complete-re-opening-a-strategy"></a>

A strategy can be marked as complete only if all previous strategies are completed. This is because every complete strategy influences the savings achievable on subsequent strategies. Marking a strategy as complete, will mean no changes can be made to the strategy i.e. no resources can be dismissed from the strategy, or no already dismissed resources can be included in the strategy. In order to do these operations on a completed strategy, one has to re-open a strategy.

One can reopen a strategy, only if all strategies subsequent to it are open.

#### **Key Metrics on Strategy pages** <a href="#key-metrics-on-strategy-pages" id="key-metrics-on-strategy-pages"></a>

**Showing for**

This indicates the year selection that the rest of the metrics are based on. This can only be changed by the Cloud Cost Optimization Consultant. Please reach out to them if you want to change this.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

**Cost at point of optimization**

This indicates the cost at the point of optimizing all the impacted resources in the strategy.

**Why is it called “Cost at point of optimization” ?**

Lets take an example of a resource which is a candidate for the Rightsizing and Cross-Region Optimization strategies. Let us assume that the cost of the resource today is 100$ a year. The cost at point of optimization of the resource on the Rightsizing strategy page will show up as 100$. However, if the resource is being recommended to be rightsized, so that the new cost of the resource is 50$, then the cost at the point of optimization of the resource on the Cross-Region Optimization strategy will show up as 50$. Cost at point of optimization takes into account all savings for the resource on previous strategies. If you want to look at the cost of the resource, Click on customize grid, and choose “Predicted Current Cost”.

Cost at point of optimization for the strategy is the sum of the cost at point of optimization of all resources in the Impacted Resources tab of the strategy.

**Predicted new nost**

This is the predicted new cost of the resources in the strategy once the strategy optimizations have been applied to the resources in the strategy.

**Predicted new savings**

This is the amount of money you can save on the resources in the Impacted resources tab of the given strategy.

#### **Impacted Resources Tab** <a href="#impacted-resources-tab" id="impacted-resources-tab"></a>

This tab shows you a list of the resources that are being recommended as a candidate for the specific strategy optimization in question. If you do not want to optimize the resource using the optimization recommend, one can dismiss the resource from the strategy. Dismissing the strategy will move the strategy into the Dismissed tab, and will not count the cost and savings from the resource towards that strategy.

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

#### What if an impacted resource is no longer a candidate for a strategy ? <a href="#what-if-an-impacted-resource-is-no-longer-a-candidate-for-a-strategy" id="what-if-an-impacted-resource-is-no-longer-a-candidate-for-a-strategy"></a>

In such a scenario, the system will automatically remove the affected candidate from the Impacted Resources tab, and will appropriately reflect the costs and savings on the Strategy and the Overview pages.

Note that if a resource is identified to not be a candidate for a strategy anymore, it will not show up in the Dismissed tab, as the resource has not been manually excluded. Such a resource will show up in the Review changes tab with Status “Removed”.

Similarly, if a new resource is identified as a candidate for a strategy, then the resource will be automatically included in the strategy and the Impacted Resources tab.

#### **Dismissed Tab** <a href="#dismissed-tab" id="dismissed-tab"></a>

The dismissed tab shows resources that have been manually excluded from a strategy by a user. Any dismissed resource can be included back in the strategy so long as the strategy has not been marked as complete.

#### **Review Changes Tab** <a href="#review-changes-tab" id="review-changes-tab"></a>

The review changes tab is a list of all changes to resource candidates applied automatically by the system. Newly identified candidates will show up in the Review Changes tab till they are marked as reviewed as well as the Impacted Resources tab. Candidates which are no longer candidates will also show up in the Review changes tab with status “Removed”.

We recommend that you review the Review changes tab every time you login, so you are aware of all recent activity within the Cloud Cost Optimization system.

#### **Advanced Filters on Impacted Resources, Dismissed and Review Changes tab** <a href="#advanced-filters-on-impacted-resources-dismissed-and-review-changes-tab" id="advanced-filters-on-impacted-resources-dismissed-and-review-changes-tab"></a>

There are a host of filters one can use to narrow the data you are seeing on the tabs based on specific criteria. The filters available are

* Resource Name
* Resource Group
* Subscription
* Tags

Please note that applying a filter will filter all the pages within the tab, as opposed to just the page you are on.

#### **Exporting data from Cloud Cost Optimization** <a href="#exporting-data-from-cloud-cost-optimization" id="exporting-data-from-cloud-cost-optimization"></a>

Each of the strategy pages enable users to export data on the grid to an excel file using the Export button on the top right of the grid.

The export button will only export the columns visible on the grid at the time of the export. However, you can customize the grid to show extra columns using the Customize button to the left of “Export”.

Please note that the export capability is not available on the Overview page yet.

### Strategy – Orphaned Resources <a href="#strategy-orphaned-resources" id="strategy-orphaned-resources"></a>

The Orphaned resources allows one to identify resources that can be shut down or decommissioned as they are not being effectively utilized.

**Note that resources that show up in Orphaned Resources, will not show up in other strategies, as they will be shut down on completion of the Orphaned Resources strategy.**

No configuration is available on this strategy.

### Strategy – DEV/TEST <a href="#strategy-dev-test" id="strategy-dev-test"></a>

This strategy is not available for AWS Cloud Cost Optimization

This strategy identifies resources that can be flagged as Development or Test resources, thereby reducing overall cost on the resource.

No configuration is available on this strategy.

### Strategy – Rightsizing <a href="#strategy-rightsizing" id="strategy-rightsizing"></a>

This strategy identifies resources that can be rightsized to a lower tier/size, thereby reducing overall cost on the resource.

No configuration is available on this strategy.

### Strategy – Instance Modernization <a href="#strategy-instance-modernization" id="strategy-instance-modernization"></a>

Instance modernization is about paying the best price for the same resource while maintaining or improving its capabilities.

No configuration is available on this strategy.

### Strategy – Cross Region Optimization <a href="#strategy-cross-region-optimization" id="strategy-cross-region-optimization"></a>

This strategy identifies resources that can be rehoused in a cheaper region, thereby reducing overall cost on the resource.

#### Strategy Level Configuration for Cross-region Optimization <a href="#strategy-level-configuration-for-cross-region-optimization" id="strategy-level-configuration-for-cross-region-optimization"></a>

Optimization recommendations for this strategy are dependent on selection of a region subset. This selection is done either by the customer or by the consultant.

If the regions have not been selected by the consultant, then you may likely see this on the Cross-Region Optimization strategy page&#x20;

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

In order to move forward, kindly select the regions by clicking on Edit, and select the regions and save changes.

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

The Savings threshold is the minimum savings that needs to be achieved to make the resource viable for Cross-Region Optimization.

Note that the savings threshold used is 10% by default, and this configuration can only be updated by your Cloud Cost Optimization Consultant.

#### Resource Level Region Configuration for Cross-region Optimization <a href="#resource-level-region-configuration-for-cross-region-optimization" id="resource-level-region-configuration-for-cross-region-optimization"></a>

Similar to the regions that can be selected at the strategy level, a region can also be overridden per resource. You may typically want to do this, if there is a particular resource that you want to house in a fixed region, regardless of the savings available through other regions.

Note that resource level region can only be selected from among the region subset already configured by the user or the consultant. For e.g. if the region subset is set to West Europe and North Europe, resource-level region can only be set to one of these two.

You can do this by navigating to Resource Details -> Edit as show below.

Note that if a region is set at a resource level, then it will not be assigned a cheaper region automatically by the system.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

### Strategy – Resource Automation <a href="#strategy-resource-automation" id="strategy-resource-automation"></a>

This strategy identifies resources that can be automated to be on during certain times of the day and shut down during others.

Resource uptime is defaulted to 24 hours a day, 7 days a week. This setting can be updated by your Cloud Cost Optimization consultant if there is a common Automation uptime window for all your resources.

#### Resource Level Uptime Configuration for Resource Automation <a href="#resource-level-uptime-configuration-for-resource-automation" id="resource-level-uptime-configuration-for-resource-automation"></a>

An uptime window can be configured on resource level using Resource Details > Edit, as shown below.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

### Strategy – Reserved Instances <a href="#strategy-reserved-instances" id="strategy-reserved-instances"></a>

If a resource is planned to be used more than 60% of the time during a year, it might make sense to commit the consumption for a period of 1 or 3 years. Doing this can result in savings of up to 40% on compute cost, depending on the resource being committed.

Reserved Instance term is defaulted to 1 year for every resource.

#### Resource Level Reserved Instance Term Configuration <a href="#resource-level-reserved-instance-term-configuration" id="resource-level-reserved-instance-term-configuration"></a>

Reserved Instance term can be configured on resource level using Resource Details -> Edit, as shown below.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

### Strategy – Azure Hybrid Benefit <a href="#strategy-azure-hybrid-benefit" id="strategy-azure-hybrid-benefit"></a>

This strategy is not available for AWS Cloud Cost Optimization

Hybrid Use Benefits for Windows Sever provides, under specific conditions, the option to bring your own Windows Licenses, with active Software Assurance to cover virtual machine licenses in Azure. Using this benefit could save up to 40% on license costs, which are normally hidden behind the virtual machine cost.

No configuration is available on this strategy.

### Strategy – Bring your own License <a href="#strategy-bring-your-own-license" id="strategy-bring-your-own-license"></a>

Similar to Hybrid Use Benefits, Bring Your Own License benefits allow customers to bring other licenses to Azure or AWS, and receive discount for the licensing portion of the cost. In this section we calculate savings for Microsoft SQL Server and Redhat Enterprise License.

No configuration is available to users on this strategy.\
License Cost for Windows, Linux and SQL can be updated by your Cloud Cost Optimization Consultant.
