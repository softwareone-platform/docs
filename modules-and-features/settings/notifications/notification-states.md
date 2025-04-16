# Notification Email States

A notification email in the Marketplace Platform goes through several stages during its lifecycle.

The following diagram shows the possible states and the transition between these states:

<figure><img src="../../../.gitbook/assets/state_diagram_notification.png" alt=""><figcaption><p>Notification state transition</p></figcaption></figure>

<table><thead><tr><th width="262">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>New</strong></td><td>This is the initial status for newly created notification emails. This state is not visible on the interface.</td></tr><tr><td><strong>Queued</strong></td><td>The email has been queued for sending to the recipient. </td></tr><tr><td><strong>Discarded</strong></td><td>The notification email has been discarded because the individual or account has disabled the notification category or the contact has an administrative block in place due to bounces or complaints.</td></tr><tr><td><strong>Sent</strong></td><td>The notification email has been sent to the recipient.</td></tr><tr><td><strong>Failed</strong></td><td>The platform was unable to send the notification email. </td></tr><tr><td><strong>Bounced</strong></td><td>The notification email has bounced and couldn't be delivered. This could be due to several reasons, including invalid email addresses, issues with the recipient's mailbox, and so on.</td></tr><tr><td><strong>Complained</strong></td><td>The recipient has reported the notification email as spam or junk.</td></tr></tbody></table>
