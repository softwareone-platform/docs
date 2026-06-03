---
description: Cancel specific subscriptions in your agreement.
---

# Terminate subscription

You can terminate a subscription if you no longer need it or don't want it to renew.&#x20;

Subscriptions are linked to agreements, and the termination process depends on the number of active subscriptions in the agreement.

* If the agreement includes multiple active subscriptions and you want to cancel all subscriptions, you must terminate the entire agreement by placing a termination order. For details, see [Terminate agreement](../agreements/terminate-agreements.md).&#x20;
* If the agreement includes multiple active subscriptions and you want to cancel some but not all, you must place a termination order for each specific subscription.

Only active subscriptions can be terminated. Additionally. submitting a termination order for a subscription doesn't guarantee termination. Termination orders are sent to the vendor, who decides the outcome.

### Terminate a subscription

To terminate a subscription:

1. Go to **Marketplace** > **Subscriptions**.
2. Select the subscription to terminate.
3. On the subscription details page, select the dropdown arrow <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGAAAABgCAYAAADimHc4AAAAAXNSR0IArs4c6QAAAopJREFUeF7tmk1OwmAURQvL0f04Z+SaHDF3P7ocNI2pCYZAudx+9z1zGPN+vnN6CaXsJl5RArvodIZPCAhfBAhAQJhAeDwJQECYQHg8CUBAmEB4PAlAQJhAeDwJQECYQHg8CUBAmEB4PAlAQJhAeDwJQECYQHg8CUBAmEB4PAlAQJhAeDwJQECYQHg8CUBAmEB4PAlAQJhAeDwJQECYQHh8JAGHw+vT8fj2GT772fjUTsMFzAc97ffv+9PppYqE5E5DBSwHnaav52nafVSQkN5pmIDzgy7pz0qosNMQAZcPmpVQZafNBVw/aEZCpZ02FbDuoGMlVNtpUwEz2koHrrTL72U34rt4hYNX2OES680TsAxNAkjOvnWBDxOQ+jiqDH9mMlTAaAnV4UcEjJLQAX5MwNYSusCPCthKQif4cQFuCd3glxDgktARfhkBj0roCr+UAFXCXDc/4Pl5xnDrlf35O3onfAuNesf8U9cTfrkEaBLWqK135S9bD78TXoPr/o+ja13rwi+bAF8SasMvL+CxJNSH30KAJqEH/DYC7pPQB34rAesk9ILfTsB1Cf3gtxRwWUJP+G0FnEuYpgp/cVx7f/P3fWVvxNYcaP4Rbn5flT/5rtn5XwlQDlytpnUCqsFU9kGAQs1YgwAjTKUVAhRqxhoEGGEqrRCgUDPWIMAIU2mFAIWasQYBRphKKwQo1Iw1CDDCVFohQKFmrEGAEabSCgEKNWMNAowwlVYIUKgZaxBghKm0QoBCzViDACNMpRUCFGrGGgQYYSqtEKBQM9YgwAhTaYUAhZqxBgFGmEorBCjUjDUIMMJUWiFAoWasQYARptIKAQo1Yw0CjDCVVghQqBlrEGCEqbT6Bgoy2nAnTiZDAAAAAElFTkSuQmCC" alt="" data-size="line">, then choose **Terminate**.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/subscription_terminate.png" alt=""><figcaption><p>Use the <strong>Terminate</strong> option to cancel the subscription. </p></figcaption></figure></div>

4. In the guided **Terminate subscription** flow, do the following:
   1. **Items** – Check that the item quantity is zero, then select **Next**.&#x20;
   2. **Order details** – Provide any reference details and order notes. Then, select **Next**.
   3. **Review order** – Review the order details. When done, select **Place order**.
   4. **Summary** – Select **View order** to open the order details page or select **Close**.

Once the termination order is submitted, the subscription status changes to **Terminating**, and the agreement status changes to **Updating**. This means that no other orders can be placed against the subscription until the termination order either completes or fails.

If the order is successfully processed, the subscription status changes to **Terminated**. All items are removed from the subscription, and the agreement either returns to **Active** if there are other active subscriptions or it moves to **Terminated** if no active subscriptions remain.

If the order cannot be processed, both the subscription and the agreement revert to **Active**.
