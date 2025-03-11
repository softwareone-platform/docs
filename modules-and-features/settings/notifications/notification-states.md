# Notification States

A notification in the Marketplace Platform goes through several stages during its lifecycle.

The following diagram shows the possible states and the transition between these states:

<figure><img src="../../../.gitbook/assets/notification_states.png" alt=""><figcaption><p>Notification state transition</p></figcaption></figure>

| State          | Definition                                                                                                                                                                               |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **New**        | The email has been created in the system. Note that this state is not visible on the interface.                                                                                          |
| **Queued**     | The email has been queued for sending.                                                                                                                                                   |
| **Discarded**  | The email has been discarded because the individual or account has disabled the notification category, or the contact has an administrative block in place due to bounces or complaints. |
| **Sent**       | The notification has been sent.                                                                                                                                                          |
| **Failed**     | The platform has been unable to send the notification.                                                                                                                                   |
| **Bounced**    | The email has bounced and could not be delivered.                                                                                                                                        |
| **Complained** | A complaint has been raised by the recipient.                                                                                                                                            |
