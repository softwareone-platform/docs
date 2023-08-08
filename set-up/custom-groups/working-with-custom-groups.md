---
description: You can create, remove, and manage custom groups.
---

# Working with custom groups

***

### Creating custom groups <a href="#navigate-to-custom-groups" id="navigate-to-custom-groups"></a>

**To create custom groups**

1. From the main menu, navigate to **Setup** and select **Custom Groups**.&#x20;
2. Select **Create a group** to start building the group structure.&#x20;
3. On the **Edit Group Structure** page, set up the structure levels. Choose Tag Keys as Structure Levels.&#x20;

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/02/02_Custom-Groups_First-time-view_04-Choose-tag-keys-as-structure-levels.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If you are using tags on your provider platform to organize your resources, you can use these tags to create the structure. If you do not want to use existing tags, you can create your structure manually.
{% endhint %}

4. Assign groups to the created structure levels. To create the groups, choose the “**New**” group functionality for the required structure level:

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
