# State Diagram

The following diagram shows the state (status) transition process of a certificate. It shows the possible states a certificate can have and the transition between those states.

<figure><img src="../../../../.gitbook/assets/state_diagram_certificate.png" alt=""><figcaption><p>The state transition diagram of a certificate.</p></figcaption></figure>

<table data-full-width="false"><thead><tr><th width="152">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>New</strong></td><td>This is the initial status of a certificate, and it's assigned by the platform when the certificate is being created.</td></tr><tr><td><strong>Pending</strong></td><td>The certificate has been created successfully, and it's awaiting approval by the vendor.</td></tr><tr><td><strong>Active</strong></td><td>The certificate is active and can be used when placing an order.</td></tr><tr><td><strong>Expired</strong></td><td>The certificate has expired. Expired certificates can be renewed by re-enrolling in the program.</td></tr><tr><td><strong>Updating</strong></td><td>The certificate is being updated due to re-enrollment in the program.</td></tr><tr><td><strong>Terminated</strong></td><td>The certificate has been terminated. Terminated certificates can't be used to re-enroll in a program. </td></tr></tbody></table>
