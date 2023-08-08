---
description: Tiles display a summary of your Office 365 Subscription.
---

# Office 365 analytics

The Office 365 consumption module contains tiles with summary information about your Office 365 subscription, sourced from your Office 365 Analytics subscription.

There are two tiles available for your use within PyraCloud.

* One tile shows your Office 365 license position
* The other tile shows your usage statistics of those same licenses.

When you click on either tile, you are provided with more in depth information about your subscription and tips on how to address various licensing or usage scenarios. If you wish to investigate further, you can click on the Office 365 Analytics “Cloud Insider” link to seamlessly log on to the Office 365 Analytics web application.

### Prerequisites <a href="#prerequisites" id="prerequisites"></a>

In order for the Office 365 PyraCloud tiles to function, the following conditions are required:

* An active subscription.
* Provisioned user account matching the customer’s email address
* An active subscription to Office 365 Analytics.
* Provisioned Office 365 Analytics user account matching the customer’s email address.

### Adding the Office 365 Tiles to the Dashboard <a href="#adding-the-office-365-tiles-to-the-dashboard" id="adding-the-office-365-tiles-to-the-dashboard"></a>

To add the Office 365 PyraCloud tiles to your dashboard, logon to PyraCloud. Click “Customize” on the top right of the Dashboard as shown below:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/08/image-31-1024x278.png" alt=""><figcaption><p>Figure 1 – Customize Dashboard<br></p></figcaption></figure>

Then click “+Add Tiles” as shown below:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/08/image-32-1024x281.png" alt=""><figcaption><p>Figure 2 – Add Tile(s)</p></figcaption></figure>

Find the two Office 365 tiles. While holding the CTRL key, select both tiles and then click “Add Selected”.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/08/image-33.png" alt="" height="416" width="526"><figcaption><p>Figure 3 – Adding Office 365 Tiles</p></figcaption></figure>

Once you have added both tiles, you should see them appear as “Office 365 – Licensed” and “Office 365 – In Use”.

If the prerequisites have been met and it has been over an hour since your Office 365 Analytics account was enabled, you should see data within the tiles.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/08/image-34-1024x427.png" alt=""><figcaption><p>Figure 4 – Office 365 Tiles</p></figcaption></figure>

### Understanding the Office 365 Tiles <a href="#understanding-the-office-365-tiles" id="understanding-the-office-365-tiles"></a>

The Office 365 tiles display either “Licensed” or “In Use” information.

The Licensed tile shows your license position with in Office 365, while the “In Use” tile shows how much you are using the licenses you own.

The tiles currently show the three top workloads within Office 365.

The following is an example of the Office 365 Licensed tile:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/08/Licensed-tile-explained.png" alt="" height="152" width="330"><figcaption><p>Figure 5 – Office 365 Licensed Tile Explained</p></figcaption></figure>

1. This is the last time the system synchronized your Office 365 subscription information from Office 365 Analytics.
2.  These three dials show your total licenses for each workload and how many of those licenses are actually assigned to your users. Specifically, if you own an E3 license and have enabled Exchange within that license bundle, that Exchange license will be counted in the Exchange dial as an assigned license and towards to total license count for Exchange. The dial will change colors, based on how many licenses are assigned to users compared to the total licenses available for that workload.

    The following are the “licensed” thresholds on the tile:

    * 0-24% licenses assigned = Red dial, indicating you need to assign more users to that workload
    * 25-74% licenses assigned = Yellow dial, indicating you are under assigned licenses
    * 75-94% licenses assigned = Green dial, this is the ideal license position to be in
    * 95% or greater licenses assigned = Red dial, indicating you should consider freeing up or purchasing more licenses
3. This link will take you to a modal window, which will give you a summary breakdown of your common Office 365 workloads.

The following is an example of the Office 365 In Use Tile:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/08/In-use-tile-explained.png" alt="" height="171" width="364"><figcaption><p>Figure 6 – Office 365 In Use Tile Explained</p></figcaption></figure>

1. This is the last time the system synchronized your Office 365 subscription information from Office 365 Analytics.
2.  These three dials show your active use of the licenses you own for each workload. Active use is measured over a 90 day period. The dial will change colors, based on how many active users you have compared to the total licenses available for that workload.

    The following are the “In Use” thresholds on the tile:

    * 0-49% use of a workload = Red dial, indicating you need to start a user adoption\
      campaign or reconsider the use of that workload
    * 50-74% use of a workload = Yellow dial, indicating you need to investigate why that workload may have low usage
    * 75-100% use of a workload = Green dial, this is the ideal usage scenario to be in
3. This link will take you to a modal window, which will give you a summary breakdown of your common workloads.

### Understanding the Office 365 Modal Window <a href="#understanding-the-office-365-modal-window" id="understanding-the-office-365-modal-window"></a>

When you click on one of the Office 365 tiles, you should see statistics about your Office 365 subscription in a Modal window.

The following is an example of the Office 365 Modal window:

Within the Modal window, you will see various statistics about your Office 365 subscription.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/08/image-35.png" alt="" height="301" width="601"><figcaption><p>Figure 7 – Office 365 Modal Window</p></figcaption></figure>

* The Total Licenses field shows you total licenses for that workload.
* The Licenses Assigned field shows how many of your total licenses are assigned.
* The Licenses In Use field shows how many of your total licenses are being used by your users, based on the last 90 days.
* The Service field shows the common workloads that are a part of your Office 365 subscription. Currently we are only displaying Exchange Online, SharePoint Online, OneDrive for Business, Skype for Business Online, Office 365 ProPlus, and Yammer.
* If you click on one of the workloads with a red alert, you will see more information about why that workload needs your attention.

You can click on the “Cloud Insider” link on the bottom right of the Modal window, which will take you to your Office 365 Analytics subscription.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/08/image-36.png" alt="" height="502" width="999"><figcaption><p>Figure 8 – Cloud Insider Link</p></figcaption></figure>

The Office 365 Analytics site will give you more in depth information about your subscription.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/08/image-37-1024x511.png" alt="" height="511" width="1024"><figcaption><p>Figure 9 – 365 Analytics Site</p></figcaption></figure>

After visiting the Office 365 Analytics site, you can go back to PyraCloud.

PyraCloud does have a login timeout, so depending on how much time you spend in Office 365 Analytics, you may have to log back on to PyraCloud.
