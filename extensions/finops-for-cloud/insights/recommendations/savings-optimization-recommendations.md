# Savings Optimization Recommendations

{% hint style="info" %}
All parameters in **bold** are custom parameters. You can change the parameters by selecting<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGAAAABgCAYAAADimHc4AAAAAXNSR0IArs4c6QAAAw9JREFUeF7tnMuNE0EQhqs6Bx4ZIMGBAOAA0zbIhABEAAJiYREbwUIIrMDugQMEwAEkMuCRwxQarediCTHdas3fZf0+rrq6Zr6va3ddU7YKX1ACCs3O5EIB4ENAARQAJgBOzwqgADABcHpWAAWACYDTswIoAEwAnJ4VQAFgAuD0rAAKABMAp2cFUEAega7rNiKyCSFcM7ObY7Sqfh2G4YeInPd9f563I3a1qwqIMZ6JyKP/IHuTUnqMxTo/uxsBMUabf1siKSUX9+biImOMz0XkZY4AEXmRUjrJjFl8efMC1uv1rWEYPpeQCSHc3m63X0pil4ppXkCM8bWIPCkEcppSeloYu0iYBwEfReROIY1PKaW7hbGLhDUvoOu636p6qYSGmf3p+/5ySexSMc0LiDH+FJErhUB+pZSuFsYuEta8gNVq9d7M7pXQUNUPu93ufknsUjHNC+i67kRVn5UAMbNXfd+P/8I2+/IgYKOq70oImtmD1lsTzQsYwc9sQRw6ctGScCFgL4GtiJJfAzVjZrYkXLQgJi5uKmC64H1r4qGIXDezG+PPVfWbiHwPIbxtvfVweCDdCahZUS3sRQFgCxRAAWAC4PSsAAoAEwCnZwVQAJgAOL27CuBcEPDEzGzKuWjCuWtFcC4Ie/I5F4Tiz7kgFPl9Xs4F4QVwLgjpgHNBSPoXz4M5F4R0wLkgJH0R4VwQXgDngsAOOBeEFjDmZyuiAQucC2pAAueCGpBwTJfg7oHMMcEf74UCwEYpgALABMDpWQEUACYATs8KoIA8ApwLyuNVdTXngqrizNuMzbg8XlVXz2zCHeZ08WG95v8Icy6o6lnO34xzQfnMqkbEGDkXVJVo5macC8oEVns554JqE83cj3NBmcBqL+dcUG2imfuNrQd+X1AmtNrLZ7YgDtO6+KhS82/EJqpsRdQ+1gX7zWxJuGhBTLfvpgKmC+ZcUMHJZci/CbirgGOTSQFgoxRAAWAC4PSsAAoAEwCnZwVQAJgAOD0rgALABMDpWQEUACYATs8KoAAwAXB6VgBYwF/mZEdwBsiwPwAAAABJRU5ErkJggg==" alt="<svg xmlns=&#x22;http://www.w3.org/2000/svg&#x22; height=&#x22;24px&#x22; viewBox=&#x22;0 -960 960 960&#x22; width=&#x22;24px&#x22; fill=&#x22;#434343&#x22;><path d=&#x22;M480-160q-33 0-56.5-23.5T400-240q0-33 23.5-56.5T480-320q33 0 56.5 23.5T560-240q0 33-23.5 56.5T480-160Zm0-240q-33 0-56.5-23.5T400-480q0-33 23.5-56.5T480-560q33 0 56.5 23.5T560-480q0 33-23.5 56.5T480-400Zm0-240q-33 0-56.5-23.5T400-720q0-33 23.5-56.5T480-800q33 0 56.5 23.5T560-720q0 33-23.5 56.5T480-640Z&#x22;/></svg>" data-size="line">on the card and selecting [Settings](./#settings).&#x20;
{% endhint %}

## Abandoned instances <a href="#abandoned-instances" id="abandoned-instances"></a>

Instances that have an average CPU consumption of less than **5%** and network traffic below **1000 bytes/s** for the last **7 days**. We recommend terminating these instances to reduce expenses.&#x20;

## Obsolete images <a href="#obsolete-images" id="obsolete-images"></a>

Images that haven't been used for a while might be subject to deletion, which would unlock the underlying snapshots. Image selection criteria:

* The image creation date was more than 1 week ago.
* No instances have been created from/related to this image in the past **7 days**.

You can download the list of obsolete images as JSON for subsequent automated processing with the help of [Cleanup Scripts](clean-up-scripts-based-on-recommendations.md).&#x20;

## Obsolete snapshots <a href="#obsolete-snapshots" id="obsolete-snapshots"></a>

Redundant and old snapshots save up on storage expenses if deleted. You can download the list of snapshots as JSON for use in further implementations like clean-up scripts and maintenance procedures. Selection criteria:

* The source EBS volume doesn't exist anymore.
* No AMIs are created from this EBS snapshot.
* It hasn't been used for volume creation for the last **4 days**.

The list of obsolete snapshots can be downloaded as JSON for subsequent automated processing with the help of [Cleanup Scripts](clean-up-scripts-based-on-recommendations.md).

## Obsolete IPs <a href="#obsolete-ips" id="obsolete-ips"></a>

Obsolete IPs can be tracked for Azure and AWS clouds to reduce expenses. The following is the selection criteria for the obsolete IPs:

* The IP was created more than **7 days** ago.
* The IP hasn't been used in the last **7 days**.
* It costs money to be kept.

## Not attached volumes <a href="#not-attached-volumes" id="not-attached-volumes"></a>

Notification about volumes that haven't been attached for more than one day. These are considered to be forgotten or no longer relevant. We recommend that you delete such resources.

You can download the list of unattached volumes as JSON for subsequent automated processing with the help of [Cleanup Scripts](clean-up-scripts-based-on-recommendations.md).&#x20;

## Underutilized instances <a href="#underutilized-instances" id="underutilized-instances"></a>

This recommendation is aimed at the detection of underutilized instances in AWS and Azure and suggests more suitable flavors for these machines. An instance is considered to be underutilized if:

* It is active.
* It exists for more than **3 days**.
* Its CPU metric average for the past **3 days** is less than 80%.

## Reserved instances opportunities <a href="#reserved-instances-opportunities" id="reserved-instances-opportunities"></a>

This card contains instances that are active and have sustainable compute consumers for more than **90 days**. Instances that haven't been covered with Reserved Instances or Saving Plans are also included.

For all such instances, consider purchasing Reserved Instances to save on compute usage. Check **RI/SP Coverage** to see the detailed breakdown of current reservations.

## Abandoned kinesis streams <a href="#abandoned-kinesis-streams" id="abandoned-kinesis-streams"></a>

This card shows Kinesis Streams with provisioned Shard capacity that haven't performed operations in the last **7 days**. Consider removing them to reduce expenses.

## Instances with migration opportunities <a href="#instances-with-migration-opportunities" id="instances-with-migration-opportunities"></a>

This card shows opportunities to migrate instances if the tool detects that the same instance type is cheaper in a geographically close region (within the same continent).

Some of your active instances might cost less in another nearby region with the same specifications. Consider migrating them to the recommended region to reduce expenses.

## Instances for shutdown <a href="#instances-for-shutdown" id="instances-for-shutdown"></a>

This recommendation means that some of your instances have an inactivity pattern that allows you to set up an on/off power schedule (average CPU consumption is less than **5%** and network traffic below **1000 bytes/s** for the last **14 days**). Consider creating a power schedule to reduce expenses.

## Instances with spot (pre-emptible) opportunities <a href="#instances-with-spot-preemptible-opportunities" id="instances-with-spot-preemptible-opportunities"></a>

This list contains instances that:

* Are running for the last **3 days**.
* Have existed for less than **6 hours**.
* Were not created as Spot (or Preemptible) Instances. Consider using Spot (Preemptible) Instances.&#x20;

## Underutilized RDS instances <a href="#underutilized-rds-instances" id="underutilized-rds-instances"></a>

An underutilized instance is one average CPU consumption of less than **80%** for the last **3 days**. FinOps for Cloud detects such active RDS instances and lists them on the card. Consider switching to the recommended size from the same family to reduce expenses.

## Obsolete snapshot chains <a href="#obsolete-snapshot-chains" id="obsolete-snapshot-chains"></a>

Some snapshot chains don't have source volumes or images created from their snapshots and have not been used for volume creation for the last **3 days**. Consider their deletion to save on snapshot storage expenses.&#x20;

## Instances with subscription opportunities <a href="#instances-with-subscription-opportunities" id="instances-with-subscription-opportunities"></a>

The instances in the list are active and have been identified as sustained compute consumers (for more than **90 days**) but are not covered by subscription or Savings Plans. Consider purchasing subscriptions to reduce computing costs.

## Not deallocated instances <a href="#not-deallocated-instances" id="not-deallocated-instances"></a>

Detection of inactive, non-deallocated machines that have not been running for more than **1 day** and are still billed by the cloud.

You can download the list of non-deallocated VMs as JSON for subsequent automated processing with the help of [Cleanup Scripts](clean-up-scripts-based-on-recommendations.md).&#x20;

## Instances eligible for generation upgrade <a href="#instances-eligible-for-generation-upgrade" id="instances-eligible-for-generation-upgrade"></a>

Upgrade older generation instances to the latest generation within the same family.

## Abandoned Amazon S3 buckets <a href="#abandoned-amazon-s3-buckets" id="abandoned-amazon-s3-buckets"></a>

A bucket is abandoned if the average data size is less than **1024 megabytes**, the Tier1 request quantity is less than **100**, and the `GET`request quantity is less than **2000** for the last **7 days**.

We recommend that you delete it to reduce expenses. Change the check period and other parameters in the card's **Settings**.
