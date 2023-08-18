---
description: >-
  Define your organizational structure and assign cloud resources based on your
  business requirements.
---

# About Custom Groups

***

Custom groups allow you to define an organizational hierarchy (for reporting and budgeting) and govern cloud environments (resources running on Azure, AWS, and Office365 licenses).

With Custom Groups, you can build a hierarchical structure based on custom-defined dimensions, for example, departments, teams, or projects, and map resources.

<figure><img src="../../.gitbook/assets/image (87) (1).png" alt=""><figcaption></figcaption></figure>

***

### Using custom groups <a href="#using-custom-groups" id="using-custom-groups"></a>

To keep the organizational assignments of a resource (tag) consistent with the tagging on the cloud provider environment, Custom Groups interfaces with the Tags and Resources. This allows you to ensure data consistency within PyraCloud and within the cloud environments of Azure and AWS.

The built-in functionalities across Custom Groups and Resources allow users to decide how to handle those tag assignments (lock, allow overwrite, and so on) and are included as a framework that can be configured according to your individual requirements.

***

### Prerequisites <a href="#before-you-start" id="before-you-start"></a>

* **Define the objectives**: Before creating custom groups, ensure that you document the objectives for the structure. The common requirements that influence the setup of Custom Groups include the following:

| Requirement type | Description                                                                                                                                                                                                                                               |
| ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Business related | <ul><li>What is the granularity of chargeback requirements?</li><li>What is the granularity of budget requirements?</li><li>What are the reporting requirements (e.g. every month the global cost to CIO and department, split by departments)?</li></ul> |
| IT related       | <ul><li>Is tagging already in use and how?</li><li>Is it enough to stay high level or is there a need to also report on different stages of the workload (e.g. Test, UAT, Production, etc.)?</li></ul>                                                    |

* **Define the Group Structure**: Custom Groups are structured in a way that they allow almost endless scenarios of an organizational setup. Therefore the horizontal (Groups) and vertical (Group Levels) structure must be defined:
* **Identify the Right Group Levels**:  Custom Groups use structure levels to define the levels of an organization, and are used to assign individual groups. Examples of common dimensions are:
  * Company
  * Location
  * Department
  * Team
  * Service

These dimensions are directly mapped to Tags and Resources as tag keys. This allows you to directly synchronize between PyraCloud and the Cloud Provider.

{% hint style="warning" %}
**IMPORTANT**: Identifying the right setup and sequence of dimensions is critical to keeping flexibility throughout the use of Custom Groups. The dimensions are the predecessor to the hierarchical structure of Custom Groups and changing a dimension requires removing the groups.
{% endhint %}

* Identify the Right Groupings: Defining the group name is a bit more flexible than defining the dimensions. Group names correspond with the tag values and can be created and deleted at any time. Examples of common group names include:
  * SoftwareONE (for Company)
  * Switzerland (for Location)
  * Marketing (for Department)
  * Sales Area South (for Team)
  * Mail (for Service)

You can assign one group across the same parent dimension to allow for cross-vertical reporting. For example:

* 1st dimension values for Location: Switzerland, USA, Brazil, and so on.
* 2nd dimension values for Department: Finance, HR, and so on.

This will allow reporting, budgeting, and chargeback by location including the corresponding departments (top-down), and run cross-vertical reporting by department (independent from location).

***

### Customer Scenarios <a href="#customer-scenarios" id="customer-scenarios"></a>

To better outline the link between the organizational requirements and the recommendation on how to structure your groups in Custom Groups, the following customer scenarios will be used throughout the document and reflect 3 examples:

#### **Example I:  Default Customer Scenario**

This scenario represents organizations that are:

* Single company
* Flat structure
* Single Country
* Most likely department's view
* Changes to the organization are unlikely

In this case, the recommendation is to define two dimensions:

<figure><img src="../../.gitbook/assets/image (88) (1).png" alt="" width="365"><figcaption></figcaption></figure>

#### **Example II: Enterprise Customer Scenario**

This scenario represents organizations that are:

* Group of companies
* Requires support for M\&A
* Multi-country
* Fragmented department structure
*   Organization changes throughout the year

    <figure><img src="../../.gitbook/assets/image (89) (1).png" alt="" width="375"><figcaption></figcaption></figure>

#### **Example III: Service-Based Scenario**

This scenario represents organizations that are:

* Services oriented
* Multi-customer (internal and external)
* Focus on release management
* Frequent on-/off-boarding

The recommendation is to define 3 dimensions:

<figure><img src="../../.gitbook/assets/image (90) (1).png" alt="" width="375"><figcaption></figcaption></figure>



{% hint style="info" %}
**NOTE**: The primary purpose of Custom Groups is to create a multi-dimensional and hierarchical view as preparation for any further use in the Client Portal. It builds on top of Resources. The Resources component is responsible for the synchronization back to the cloud provider. Custom Groups allow changes to the structure and assignment of resources but maintain the changes in their own database. Changes made anywhere within Custom Groups are then applied to Resources and are visible there.
{% endhint %}
