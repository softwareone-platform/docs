# Create Anomaly Detection Policies

Follow these steps to create a new anomaly detection policy:

1. In the FinOps for Cloud portal, select **Anomaly detection** in the left navigation.
2. On the **Anomaly detection** page, click **Add**. The **Create Anomaly Detection Policy** page opens, allowing you to configure the parameters for the policy to be created.
3. Enter a **Policy name** and select the **Policy type** for the new policy. The following policy types are supported:
   * **Resource count** - These anomalies refer to inconsistencies or unexpected variances in the number of resources being utilized or allocated compared to what is expected or what has been provisioned. These anomalies can occur in various cloud resources, such as virtual machines, storage, network bandwidth, or cloud services (like databases and application servers).&#x20;
   * **Expense** - These anomalies are instances where the actual financial expenditure on cloud resources deviates significantly from expected or budgeted costs. These anomalies can be symptomatic of underlying issues such as inefficient resource utilization, misconfigurations, unauthorized access, or even billing errors from cloud service providers.
4. Enter the evaluation period in days and define the threshold percentage.
5. (Optional) Select the filters that will be used to trigger policy alerts. You can apply multiple filters to your policy.&#x20;
6. Click **Save**.

When an anomaly is detected, FinOps for Cloud will send you a notification email.
