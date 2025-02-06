# Amazon Web Services

FinOps for Cloud is dedicated to improving the cloud usage experience but does not actively interfere with processes in your environment since it only requires **Read-Only** rights for the connected cloud account which is used as the main Data Source for all recommendations.

The following data is used:

1. Billing info - all details related to cloud expenses.
2. State of resources (for actively discoverable types) in the cloud - necessary for applying **Constraints** like TTL and Expense limit as well as for OptScale's **Recommendation Engine**.
3. Monitoring data from the cloud used for identifying underutilized instances.

Naturally, every cloud platform differs in the way the above data is obtained.
