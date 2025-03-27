# Notification Email States

A notification email in the Marketplace Platform goes through several stages during its lifecycle.

The following diagram shows the possible states and the transition between these states:

<figure><img src="../../../.gitbook/assets/state_diagram_notification.png" alt=""><figcaption><p>Notification state transition</p></figcaption></figure>

| State          | Definition                                                                                                                                                                                           |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **New**        | This is the initial status for newly created notification emails. This state is not visible on the interface.                                                                                        |
| **Queued**     | The email has been queued for sending to the recipient.                                                                                                                                              |
| **Discarded**  | The notification email has been discarded because the individual or account has disabled the notification category or the contact has an administrative block in place due to bounces or complaints. |
| **Sent**       | The notification email has been sent to the recipient.                                                                                                                                               |
| **Failed**     | The platform was unable to send the notification email.                                                                                                                                              |
| **Bounced**    | The notification email has bounced and couldn't be delivered. This could be due to several reasons, including invalid email addresses, issues with the recipient's mailbox, and so on.               |
| **Complained** | The recipient has reported the notification email as spam or junk.                                                                                                                                   |
