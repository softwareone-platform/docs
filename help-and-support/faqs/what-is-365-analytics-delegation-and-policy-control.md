# What is 365 Analytics delegation and policy control?

Delegation and Policy Control allows a variety of user types to do their jobs more productively, in a secure fashion, and without requiring elevated administration credentials.

### Office 365 Delegated Administration

Delegation and Policy Control (DPC) for Office 365 helps organizations become more productive by enabling granular roles and responsibilities to be assigned to selected users, such as help desk operators, country-level administrators, or even end-users, setting clear boundaries on all delegated permissions.

Providing more granular delegation than the default Microsoft administrator roles is especially important for larger enterprises, companies that have multiple operating entities or business units, universities, and any organization that needs to delegate access widely across the organization.

### The benefits of 365 Analytics DPC

Delegation and Policy Control allow a variety of user types to do their jobs more productively, in a secure fashion, and without requiring elevated administration credentials:&#x20;

* **Helpdesk teams** are able to support users by setting passwords, resetting MFAs, adding a user to a group, enabling access to mailboxes, or creating new mailbox aliases &#x20;
* **Business unit owners** or **procurement** can assign licenses to people in their part of the organization&#x20;
* **Business owners** can manage their own teams whilst ensuring that naming conventions are adhered to&#x20;
* **Office managers** can set out-of-the-office notifications for users within a specific geography or business unit &#x20;
* **HR personnel** can correct data for users in AD or AAD and create mailbox aliases or set forwarding.

### Office 365 Delegated Admin Access

Without a toolset such as 365 Analytics DPC, Office 365 delegated administration is difficult to achieve as there are limited native capabilities for delegating administrative tasks. Many organizations solve this by increasing the number of Global Administrators (GAs), even though this is known to substantially increase security risks.

365 Analytics DPC resolves this dilemma by ensuring designated administrators can see and act on only the users that they are responsible for in a fashion that aligns precisely with their defined administrative role. This enables administrative tasks to be conducted where they are most effective and increases the productivity of the organization.

Having a member of the HR team raise a ticket to change an incorrect detail in AD, or an office manager raise a ticket to set an OOO notification for a user who has departed for vacation without doing so are both examples of how both help desk teams and business users’ productivity can be impacted by the absence of effective delegation.&#x20;

DPC also provides a Virtual Organizational Unit (OU) which provides a way to group users, teams, or other elements into logical units which can then again be used to delegate rights to those who need to operate on these groups or teams.&#x20;

All DPC actions are recorded in a 365 Analytics read-only log file, which enables the organization to track which actions were taken, by whom, and at what time.

### Authorization, Licensing, and Configuration Policies

#### Authorization Policies

Authorization policies allow a delegated administrator to perform a predefined action against a specific set of users. The actions defined in the authorization policy provide the ability to granularly restrict what the delegated admin can see or do.

The policy applies to objects such as Office 365 or on-premise users, a Teams team, or a Mailbox. Over 100 actions can be taken, such as setting a password, creating a Teams channel, adding a user to an AD group, or setting an OOO notification.

#### License Policies&#x20;

License Policies enable organizations to delegate the function of assigning O365 licenses. As an example, a delegated license administrator can be given a quota of licenses that are both E3 and E5 with a quantity of PowerBI and Visio.

The E3 licenses may be restricted to only Exchange, OneDrive, SharePoint, and Teams. The E5 licenses could be unrestricted. When a request is made for a license, the delegated license administrator would assign the appropriate license and that would be removed from their quota.

#### Configuration policies

Configuration policies apply rules to users in a Virtual OU. For example, to ensure that all users have MFA enabled, have a specific Microsoft usage location, or assign a specific license type. This ensures the configuration for users, groups, and other AD objects is correctly configured according to what has been determined appropriate for that group of users.

Configuration Policies ensure standard configurations are applied to particular groups or departments by standardizing objects wherever the policy is applied. For example, if you have a virtual organizational unit for the Sales department, all users in this container will have their Department attribute equal to ‘Sales’. Once a user is moved into this container, he or she will be brought into compliance with the configuration policy for Sales.
