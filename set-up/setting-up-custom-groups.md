---
description: >-
  Define your organizational structure and assign cloud resources based on your
  business requirements.
---

# Setting up custom groups

Custom Groups allow you to define an organizational hierarchy (for reporting, budgeting, etc.) and govern cloud environments (resources running on Azure, AWS, and Office365 licenses).

With Custom Groups, you can build a hierarchical structure based on custom-defined dimensions (e.g. departments, teams, or projects) and subsequently map resources to it.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/08/word-image-32.png" alt="" width="563"><figcaption></figcaption></figure>

***

### Using custom groups <a href="#using-custom-groups" id="using-custom-groups"></a>

In order to keep the organizational assignments of a resource (tag) consistent with the tagging on the cloud provider environment, Custom Groups interfaces with the Tags and Resources. This allows users to ensure data consistency within PyraCloud and within the cloud environments of Azure and AWS.

The built-in functionalities across Custom Groups and Resources allow users to decide how to handle those tag assignments (lock, allow overwrite, etc.) and are included as a framework that can be configured according to your individual requirements.

***

### Before you start <a href="#before-you-start" id="before-you-start"></a>

The first and most important step is to document the objectives for the structure. Common requirements that influence the setup of Custom Groups include the following:

**Business Related**

* What is the granularity of chargeback requirements?
* What is the granularity of budget requirements?
* What are the reporting requirements (e.g. every month the global cost to CIO and department, split by departments)?

**IT Related**

* Is tagging already in use and how?
* Is it enough to stay high level or is there a need to also report on different stages of the workload (e.g. Test, UAT, Production, etc.)?

#### Define the Group Structure <a href="#define-the-group-structure" id="define-the-group-structure"></a>

Custom Groups are structured in a way that they allow almost endless scenarios of an organizational setup. Therefore the horizontal (Groups) and vertical (Group Levels) structure must be defined:

**Identify the Right Group Levels**

Custom Groups use structure levels to define the levels of an organization, and is used to assign individual groups. Examples for common dimensions are:

* Company
* Location
* Department
* Team
* Service

These dimensions are directly mapped to Tags and Resources as tag keys. This allows one to directly synchronize between PyraCloud and the Cloud Provider.

{% hint style="info" %}
**Note**: Identifying the right setup and sequence of dimensions is critical to keeping flexibility throughout the use of Custom Groups. The dimensions are the predecessor to the hierarchical structure of Custom Groups and changing a dimension requires removing the groups.
{% endhint %}

**Identify the Right Groupings**

Defining the group name is a bit more flexible than defining the dimensions. Group names correspond with the tag values and can be created and deleted any time. Examples for common group names are:

* SoftwareONE (for Company)
* Switzerland (for Location)
* Marketing (for Department)
* Sales Area South (for Team)
* Mail (for Service)

{% hint style="info" %}
**Note**: One group can be assigned across the same parent dimension in order to allow for cross-vertical reporting. For example:

1st dimension values for Location: Switzerland, USA, Brazil, and so on.\
2nd dimension values for Department: Finance, HR, and so on.

This will allow to Run reports, budgeting, and chargeback by location including the corresponding departments (top-down), and run cross-vertical reporting by department (independent from location)
{% endhint %}

***

### Customer Scenarios <a href="#customer-scenarios" id="customer-scenarios"></a>

In order to better outline the link between the organizational requirements and the recommendation on how to structure your groups in Custom Groups, the following customer scenarios will be used throughout the document and reflect 3 examples:

**Example I:  Default Customer Scenario**

This is a scenario representing organizations that are:

* Single company
* Flat structure
* Single Country
* Most likely department's view
* Changes to the organization are unlikely

Here the recommendation is to define two dimensions:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/08/word-image-34.png" alt="" height="197" width="371"><figcaption></figcaption></figure>

**Example II: Enterprise Customer Scenario**

This is a scenario representing organizations that are:

* Group of companies
* Requires support for M\&A
* Multi-country
* Fragmented department structure
* Organization changes throughout the year

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/08/word-image-35.png" alt="" height="289" width="378"><figcaption></figcaption></figure>

**Example III: Service-Based Scenario**

This is a scenario representing organizations that are:

* Services oriented
* Multi-customer (internal and external)
* Focus on release management
* Frequent on-/off-boarding

The recommendation is to define 3 dimensions:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/08/word-image-36.png" alt="" height="364" width="299"><figcaption></figcaption></figure>



{% hint style="info" %}
**Note**: The primary purpose of Custom Groups is to create a multi-dimensional and hierarchical view as preparation for any further use in PyraCloud. It builds on top of Resources. The Resources component is responsible for the synchronization back to the cloud provider. Custom Groups allow changes to the structure and assignment of resources but maintain the changes in their own database. Changes made anywhere within Custom Groups are then applied to Resources and are visible there.
{% endhint %}

***

### Navigating to custom groups <a href="#navigate-to-custom-groups" id="navigate-to-custom-groups"></a>

Navigate to Custom Groups (**Setup** > **Custom Groups**). The Custom Groups page will open. If this is the first time anyone within the organization has used Custom Groups, they will find an empty page with the task to create groups:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/Custom-Groups_First-time-view_01-1024x645.png" alt=""><figcaption></figcaption></figure>

***

### Setting up the group structure <a href="#setup-the-group-structure" id="setup-the-group-structure"></a>

Select **Create a group** to start building the structure:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/Custom-Groups_First-time-view_02-Create-a-group-1024x645.png" alt=""><figcaption></figcaption></figure>

The **Edit Group Structure** page is displayed.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/Custom-Groups_First-time-view_03-Edit-Group-Structure-1024x347.png" alt="" height="347" width="1024"><figcaption></figcaption></figure>

***

### Setting up the structure levels <a href="#setup-the-structure-levels" id="setup-the-structure-levels"></a>

The first step is to set up Structure Levels. They are the foundation of the structure you will create.

If you are using tags on your provider platform to organize your resources, you can use these tags to create the structure. In this case, start by choosing Tag Keys as Structure Levels.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/02_Custom-Groups_First-time-view_04-Choose-tag-keys-as-structure-levels.png" alt=""><figcaption></figcaption></figure>

If you do not want to use existing tags, you can create your structure manually.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/02_Custom-Groups_First-time-view_05-Add-structure-levels-manually-1.png" alt="" height="193" width="592"><figcaption></figcaption></figure>

**Examples**

3 examples are outlined below for reference:

| Example             | High-Level Org Chart                                                                                            | Dimensions in Custom Groups                                                                                     |
| ------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Default Customer    | <img src="https://help.pyracloud.com/wp-content/uploads/2019/08/word-image-44.png" alt="" data-size="original"> | <img src="https://help.pyracloud.com/wp-content/uploads/2019/08/word-image-45.png" alt="" data-size="original"> |
| Enterprise Customer | <img src="https://help.pyracloud.com/wp-content/uploads/2019/08/word-image-46.png" alt="" data-size="original"> | <img src="https://help.pyracloud.com/wp-content/uploads/2019/08/word-image-47.png" alt="" data-size="original"> |
| Service Based       | <img src="https://help.pyracloud.com/wp-content/uploads/2019/08/word-image-48.png" alt="" data-size="original"> | <img src="https://help.pyracloud.com/wp-content/uploads/2019/08/word-image-49.png" alt="" data-size="original"> |

***

### Setting up the groups <a href="#set-up-the-groups" id="set-up-the-groups"></a>

The next step is to assign groups to the created structure levels. To create the groups choose the “New” group functionality for the required structure level:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/02_Custom-Groups_First-time-view_06-Add-groups-1024x379.png" alt="" height="379" width="1024"><figcaption></figcaption></figure>

You can create groups using already existing tags or manually.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/02_Custom-Groups_First-time-view_07-Add-group-based-on-existing-tags.png" alt="" height="299" width="330"><figcaption></figcaption></figure>

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/02_Custom-Groups_First-time-view_08-Add-group-manually_01.png" alt="" height="309" width="324"><figcaption></figcaption></figure>

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/02_Custom-Groups_First-time-view_08-Add-group-manually_02.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Note**: If there are any resources that have tags matching to created groups, they will automatically be assigned.
{% endhint %}

**Example**

| Example             | High-Level Org Chart                                                                                            | Dimensions in Custom Groups                                                                                     |
| ------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Default Customer    | <img src="https://help.pyracloud.com/wp-content/uploads/2019/08/word-image-54.png" alt="" data-size="original"> | <img src="https://help.pyracloud.com/wp-content/uploads/2019/08/word-image-55.png" alt="" data-size="original"> |
| Enterprise Customer | <img src="https://help.pyracloud.com/wp-content/uploads/2019/08/word-image-56.png" alt="" data-size="original"> | <img src="https://help.pyracloud.com/wp-content/uploads/2019/08/word-image-57.png" alt="" data-size="original"> |
| Service Based       | <img src="https://help.pyracloud.com/wp-content/uploads/2019/08/word-image-58.png" alt="" data-size="original"> | <img src="https://help.pyracloud.com/wp-content/uploads/2019/08/word-image-59.png" alt="" data-size="original"> |

***

### Creating structure automatically <a href="#create-structure-automatically" id="create-structure-automatically"></a>

It is possible to create Custom Groups automatically. The system can create groups for you based on existing tag combinations that match the defined structure levels.

Enable the following option when editing the structure for this automation:

<div align="left">

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/03_Automate_Automatically-Update-Groups-from-Tags-1-1024x166.png" alt=""><figcaption></figcaption></figure>

</div>

If groups do not exist, they will automatically be created if automation is enabled and there is a matching tag combination in your infrastructure. This process constantly runs in the background. The group will also be created once you modify resource tags in Resources or you use Resource Rules. The mechanism does not automatically remove any existing groups.

a When the automation is enabled, it is not possible to remove a group with resources assigned. Such a group would immediately be created again.

***

### Removing empty groups automatically <a href="#remove-empty-groups-automatically" id="remove-empty-groups-automatically"></a>

Enable the following option to allow the system to automatically remove groups without resources and budgets:

<div align="left">

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/03_Automate_02-Auto-remove-empty-groups-1024x166.png" alt=""><figcaption></figcaption></figure>

</div>

Once enabled, the system will periodically scan your structure and remove groups that have no resources assigned and no budgets created.

Consider this setting if you want to have your structure maintained fully automatic.

***

### Assigning resources to a group <a href="#assign-resources-to-a-group" id="assign-resources-to-a-group"></a>

Once the structure has been created, users can go back to Custom Groups to see all resources:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/05-Assigning-Resources_01-Back-to-Groups-1024x349.png" alt=""><figcaption></figcaption></figure>

Users will see the view shown below. The next step is to navigate to “Unassigned Resources”:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/05-Assigning-Resources_02-Unassigned-resources-1024x441.png" alt=""><figcaption></figcaption></figure>

In unassigned resources, users will find all resources that are not assigned to groups.

Users can use filters to find resources in order to assign them to a specific group.

There are two possible ways to group resources:

* Assign resources to a group.
* Assign resources to multiple groups

***

### Assign resources to a group <a href="#assign-resources-to-a-group-2" id="assign-resources-to-a-group-2"></a>

If required, search for the resources. Then select the check boxes of the resources, click on “Move” and select the group:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/05-Assigning-Resources_03-Select-to-move-resources-1024x543.png" alt=""><figcaption></figcaption></figure>

<div align="left">

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/05-Assigning-Resources_04-Select-group-to-move-resources.png" alt=""><figcaption></figcaption></figure>

</div>

Those resources are now assigned to the selected group and their entire resource spend will be fully associated with this group.

Assigned resources receive tags that reflect the group assignment structure. As an example, the resources assigned to group “Location-A” have the following tags:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/05-Assigning-Resources_05-Resource-with-tags-1024x358.png" alt=""><figcaption></figcaption></figure>

***

### Assigning resources to multiple groups <a href="#assign-resources-to-multiple-groups" id="assign-resources-to-multiple-groups"></a>

Assigning resources to multiple groups means that the spend of such resources will be split between selected groups according to the way users specify.

If required, search for the resources. Then select the check boxes of the resources and click on “Edit Allocation”:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/05-Assigning-Resources_06-Edit-Allocation-1024x552.png" alt=""><figcaption></figcaption></figure>

Users will then see the “Split Allocation” window to specify the split details:

<div align="left">

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/05-Assigning-Resources_07-Split-Allocation-1.png" alt=""><figcaption></figcaption></figure>

</div>

The next step is to select groups and provide allocation percentage for each one:

<div align="left">

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/05-Assigning-Resources_08-Split-Allocation-First-group.png" alt=""><figcaption></figcaption></figure>

</div>

Repeat the step to select groups and specify the allocation percentages. If this is done, select **Save Cost Split**:

<div align="left">

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/05-Assigning-Resources_09-Split-Allocation-Groups-and-Save.png" alt=""><figcaption></figcaption></figure>

</div>

The cost of those resources split will be assigned in the following way:

* 70% of the cost is assigned to the group emea > HR
* 30% of the cost is assigned to the group: krakow1

Users can see the split resources assigned to the groups provided. They are marked with the “Split” icon.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/05-Assigning-Resources_10-Split-icon-for-resources-1024x407.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Note**: Split resources will not receive tags reflecting the assignment to the group structure. Assigning such tags to the resource on the provider platform (e.g. Azure) will not change the group assignment.
{% endhint %}

***

### Managing group association <a href="#manage-group-association" id="manage-group-association"></a>

Resource group assignments can be managed through the following modules:

* Custom Groups: Go to the details of a resource and select **View Cost Allocation**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/05-Assigning-Resources_11-View-Cost-Allocation-Button-1024x274.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/05-Assigning-Resources_12-View-Cost-Allocation-Details-1024x417.png" alt=""><figcaption></figcaption></figure>

* Resources: Go to the selected Resource Details page. Resource group assignment information is provided in the **Groups** section.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/05-Assigning-Resources_13-View-Cost-Allocation-in-Resources-1024x545.png" alt=""><figcaption></figcaption></figure>
