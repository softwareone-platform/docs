---
description: >-
  You can allow the Client Portal and SoftwareOne to access your Microsoft
  tenant.
---

# How can I configure conditional access to allow PyraCloud?

Microsoft has released a preview feature to support allowing access to service providers (like SoftwareOne) through Conditional Access policies. To learn about Conditional Access, see the [Microsoft documentation](https://learn.microsoft.com/en-us/azure/active-directory/external-identities/authentication-conditional-access#conditional-access-for-external-users.).&#x20;

***

### Prerequisites <a href="#prerequisites" id="prerequisites"></a>

* **Your SoftwareOne reseller tenant IDs**: To exclude SoftwareOne and the Client Portal from your blocking Conditional Access policies, you'll need the Microsoft Tenant IDs of SoftwareOne’s reseller tenants that relate to you. Even though SoftwareOne has over one hundred of these reseller tenants, only one or two will apply to you. The only way to find out the reseller tenant IDs you need to use is to log a support ticket with our Support team.

***

### Configuring conditional access <a href="#configure-conditional-access" id="configure-conditional-access"></a>

1. Determine which Conditional Access policies are blocking SoftwareOne and the Client Portal. Before you can exclude Client Portal and SoftwareOne from your policies, you need to know exactly which policies are affecting access. You can do this using the **What If** capability of Conditional Access. To do so:
   1. In the Azure portal, navigate to [Azure AD Conditional Access](https://portal.azure.com/#view/Microsoft\_AAD\_ConditionalAccess/ConditionalAccessBlade/\~/Policies).&#x20;

<figure><img src="../../.gitbook/assets/Azure AD Conditional Access.png" alt=""><figcaption></figcaption></figure>

2. Select **What If** in the top navigation bar.
3. Select **No user or service principal selected** to choose a user.
4. Choose the following settings:
   1. Select identity type: **User**
   2. Select: **Guest or external users**
   3. Select: **Service provider users (preview)**
   4. Select organization (preview)
      * Click **No tenant selected**
      * Enter the Tenant ID you obtained from Support at the start of this article
      * Click the tenant that is found
      * Click the **Select** button

Click **What If**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2022/10/image-5-1024x795.png" alt="" height="795" width="1024"><figcaption><p>Figure 4 – Policies that will apply</p></figcaption></figure>

At the bottom of the page, you will see the list of **Policies that will apply**. Make a note of these policies as these are the ones you will need to modify to exclude PyraCloud and SoftwareOne.

### Exclude PyraCloud and SoftwareOne from a policy <a href="#exclude-pyracloud-and-softwareone-from-a-policy" id="exclude-pyracloud-and-softwareone-from-a-policy"></a>

**Note**: When modifying Conditional Access policy exclusions, do not remove any of your existing excluded users, groups, or other principals. With Conditional Access, there is a very real possibility of locking yourself out of your tenant. Only attempt the following steps if you are a Conditional Access expert and you are confident configuring them.

SoftwareOne cannot be held liable for damages caused by the misconfiguration of this feature.

In the Azure portal, navigate to [Azure AD Conditional Access](https://portal.azure.com/#view/Microsoft\_AAD\_ConditionalAccess/ConditionalAccessBlade/\~/Policies).

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2022/10/image-1-1024x672.png" alt="" height="672" width="1024"><figcaption><p>Figure 5 – Azure AD Conditional Access</p></figcaption></figure>

In the list of policies, click one of the policies that applied in the last step.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2022/10/image-6-1024x584.png" alt="" height="584" width="1024"><figcaption><p>Figure 6 – Select Policy</p></figcaption></figure>

Under **Assignments**, click the **Users** section.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2022/10/image-7-1024x584.png" alt="" height="584" width="1024"><figcaption><p>Figure 7 – Assignments</p></figcaption></figure>

Click **Exclude**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2022/10/image-8-1024x584.png" alt="" height="584" width="1024"><figcaption><p>Figure 8 – Exclude</p></figcaption></figure>

Select the **Guest or external users** checkbox.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2022/10/image-10-1024x584.png" alt="" height="584" width="1024"><figcaption><p>Figure 9 – Guest or external users check box</p></figcaption></figure>

Select the **Select** radio button

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2022/10/image-12-1024x584.png" alt="" height="584" width="1024"><figcaption><p>Figure 10 – Specify external Azure AD organization radio button – Select</p></figcaption></figure>

Click **0 Azure AD organizations selected**

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2022/10/image-13-1024x584.png" alt="" height="584" width="1024"><figcaption><p>Figure 11 – 0 Azure AD organizations selected</p></figcaption></figure>

Enter the Tenant ID you obtained from Support at the start of this article, then select the checkbox next to the SoftwareONE reseller tenant.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2022/10/image-14-1024x584.png" alt="" height="584" width="1024"><figcaption><p>Figure 12 – Enter Tenant ID</p></figcaption></figure>

Click **Select**

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2022/10/image-15-1024x776.png" alt="" height="776" width="1024"><figcaption><p>Figure 13 – Select</p></figcaption></figure>

**Note**: When modifying Conditional Access policy exclusions, do not remove any of your existing excluded users, groups, or other principals. With Conditional Access, there is a very real possibility of locking yourself out of your tenant. Only attempt the following steps if you are a Conditional Access expert and you are confident configuring them.

SoftwareOne cannot be held liable for damages caused by the misconfiguration of this feature.

**Note**: At this point, you may wish to temporarily change the policy to **Report-only** to check whether existing access is still working correctly. If you do this, please remember to enable the policy again once you are confident it is working as expected.

Click **Save**.

Repeat the steps in this section for each policy that you noted in the previous section.
