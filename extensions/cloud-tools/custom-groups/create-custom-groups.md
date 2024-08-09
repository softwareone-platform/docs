---
description: You can create, remove, and manage custom groups.
---

# Create Custom Groups

## Creating custom groups <a href="#navigate-to-custom-groups" id="navigate-to-custom-groups"></a>

Follow these steps to create custom groups:

1. From the main menu, navigate to **Cloud tools >** **Custom Groups**.&#x20;
2. Click **Create a group** to start building the group structure.&#x20;
3.  On the **Edit Group Structure** page, set up the structure levels. Choose Tag Keys as Structure Levels.&#x20;

    <figure><img src="../../../.gitbook/assets/image (14) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If you are using tags on your provider platform to organize your resources, you can use these tags to create the structure. If you don't want to use existing tags, you can create your structure manually.
{% endhint %}

4.  Assign groups to the created structure levels. To create the groups, choose the **New** group functionality for the required structure level:

    <figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

You can create groups using already existing tags or manually.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If any resources have tags matching to created groups, they will automatically be assigned.
{% endhint %}

**Example**

| Example             | High-Level Org Chart                                                                  | Dimensions in Custom Groups                                                                               |
| ------------------- | ------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| Default Customer    | ![](<../../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>) | ![](<../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>) |
| Enterprise Customer | ![](<../../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)     | ![](<../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)         |
| Service Based       | ![](<../../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)     | ![](<../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)                 |

## Creating the structure automatically <a href="#create-structure-automatically" id="create-structure-automatically"></a>

It is possible to create Custom Groups automatically. The system can create groups for you based on existing tag combinations that match the defined structure levels.

Enable the following option when editing the structure for this automation:

<figure><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

If groups do not exist, they will automatically be created if automation is enabled and there is a matching tag combination in your infrastructure. This process constantly runs in the background. The group will also be created once you modify resource tags in Resources or you use Resource Rules. The mechanism does not automatically remove any existing groups.

When the automation is enabled, it is not possible to remove a group with resources assigned. Such a group would immediately be created again.

## Removing empty groups automatically <a href="#remove-empty-groups-automatically" id="remove-empty-groups-automatically"></a>

Enable the following option to allow the system to automatically remove groups without resources and budgets:

<figure><img src="../../../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Once enabled, the system will periodically scan your structure and remove groups that have no resources assigned and no budgets created.

Consider this setting if you want to have your structure maintained fully automatic.

## Assigning resources to a group <a href="#assign-resources-to-a-group" id="assign-resources-to-a-group"></a>

Once the structure has been created, users can go back to Custom Groups to see all resources:

<figure><img src="../../../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

You will see the view shown below. The next step is to navigate to “Unassigned Resources”:

<figure><img src="../../../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

In unassigned resources, users will find all resources that are not assigned to groups.

Users can use filters to find resources in order to assign them to a specific group.

There are two possible ways to group resources:

* Assign resources to a group.
* Assign resources to multiple groups

## Assigning resources to a group <a href="#assign-resources-to-a-group-2" id="assign-resources-to-a-group-2"></a>

If required, search for the resources. Then select the check boxes of the resources, click on “Move” and select the group:

<figure><img src="../../../.gitbook/assets/image (14) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (15) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Those resources are now assigned to the selected group and their entire resource spend will be fully associated with this group.

Assigned resources receive tags that reflect the group assignment structure. As an example, the resources assigned to group “Location-A” have the following tags:

<figure><img src="../../../.gitbook/assets/image (16) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Assigning resources to multiple groups <a href="#assign-resources-to-multiple-groups" id="assign-resources-to-multiple-groups"></a>

Assigning resources to multiple groups means that the spend of such resources will be split between selected groups according to the way users specify.

If required, search for the resources. Then, select the checkboxes and select **Edit Allocation**.

<figure><img src="../../../.gitbook/assets/image (17) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Specify the split details on the Split Allocation page:

<figure><img src="../../../.gitbook/assets/image (18) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Select the groups and provide an allocation percentage for each group.

<figure><img src="../../../.gitbook/assets/image (19) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Repeat the step to select groups and specify the allocation percentages. If this is done, select **Save Cost Split**:

The cost of those resources split will be assigned in the following way:

* 70% of the cost is assigned to the group emea > HR
* 30% of the cost is assigned to the group: krakow1

Users can see the split resources assigned to the groups provided. They are marked with the “Split” icon.

<figure><img src="../../../.gitbook/assets/image (20) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Split resources will not receive tags reflecting the assignment to the group structure. Assigning such tags to the resource on the provider platform (for example, Azure) will not change the group assignment.
{% endhint %}

## Managing group association <a href="#manage-group-association" id="manage-group-association"></a>

Resource group assignments can be managed through the following modules:

* **Custom Groups -** Go to the details of a resource and select **View Cost Allocation**.

<figure><img src="../../../.gitbook/assets/image (22) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (23) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* **Resources** **-** Go to the selected Resource Details page. Resource group assignment information is provided in the **Groups** section.

<figure><img src="../../../.gitbook/assets/image (24) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
