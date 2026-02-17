# Can SoftwareOne access my AWS account?

SoftwareOne doesn't have direct access to your AWS-linked accounts. With the End Customer Account Model (ECAM) model, you retain control of the root alias and password.&#x20;

However, if you are associated with a SoftwareOne payer account, SoftwareOne can restrict certain features on your linked accounts through what are known as "guardrails." For example, access to invoices may be limited because they are processed through the SoftwareOne payer account between SoftwareOne and AWS.

If you want to transfer your entire AWS organization to SoftwareOne, you must provide the root credentials for the SoftwareOne payer account.

SoftwareOne Marketplace will own and manage all payer accounts, while you will keep control of your linked accounts. Root credentials for all SoftwareOne Marketplace payer accounts are securely stored within a two-way MFA solution, ensuring that no single individual can access them.&#x20;
