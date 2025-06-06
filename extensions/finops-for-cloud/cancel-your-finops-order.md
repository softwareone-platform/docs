# Cancel Your FinOps Order

If you need to cancel your FinOps purchase order for any reason, for instance, if you picked the wrong currency while ordering, you can create a termination order for the agreement linked to your order. This tutorial describes how you can do this.

{% hint style="warning" %}
Terminating the agreement disables the corresponding organization in FinOps. It means you will no longer be able to access any data related to this organization, such as your data sources, pools, and users. Additionally, you won't be able to sign in or switch to this organization in FinOps.&#x20;
{% endhint %}

## Prerequisites <a href="#howtoorderamicrosoft365subscriptionforanexistingmicrosofttenant-prerequisites" id="howtoorderamicrosoft365subscriptionforanexistingmicrosofttenant-prerequisites"></a>

Before cancelling your FinOps order, ensure that the agreement linked to the purchase order is **active**. If it's not active, you won't be able to start the termination process.&#x20;

## Implementation

{% stepper %}
{% step %}
**Open the required agreement**

Navigate to the **Agreements** page in the Marketplace Platform. Then, select the agreement to terminate.

On the agreement details page, select the arrow <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGAAAABgCAYAAADimHc4AAAAAXNSR0IArs4c6QAAAopJREFUeF7tmk1OwmAURQvL0f04Z+SaHDF3P7ocNI2pCYZAudx+9z1zGPN+vnN6CaXsJl5RArvodIZPCAhfBAhAQJhAeDwJQECYQHg8CUBAmEB4PAlAQJhAeDwJQECYQHg8CUBAmEB4PAlAQJhAeDwJQECYQHg8CUBAmEB4PAlAQJhAeDwJQECYQHg8CUBAmEB4PAlAQJhAeDwJQECYQHh8JAGHw+vT8fj2GT772fjUTsMFzAc97ffv+9PppYqE5E5DBSwHnaav52nafVSQkN5pmIDzgy7pz0qosNMQAZcPmpVQZafNBVw/aEZCpZ02FbDuoGMlVNtpUwEz2koHrrTL72U34rt4hYNX2OES680TsAxNAkjOvnWBDxOQ+jiqDH9mMlTAaAnV4UcEjJLQAX5MwNYSusCPCthKQif4cQFuCd3glxDgktARfhkBj0roCr+UAFXCXDc/4Pl5xnDrlf35O3onfAuNesf8U9cTfrkEaBLWqK135S9bD78TXoPr/o+ja13rwi+bAF8SasMvL+CxJNSH30KAJqEH/DYC7pPQB34rAesk9ILfTsB1Cf3gtxRwWUJP+G0FnEuYpgp/cVx7f/P3fWVvxNYcaP4Rbn5flT/5rtn5XwlQDlytpnUCqsFU9kGAQs1YgwAjTKUVAhRqxhoEGGEqrRCgUDPWIMAIU2mFAIWasQYBRphKKwQo1Iw1CDDCVFohQKFmrEGAEabSCgEKNWMNAowwlVYIUKgZaxBghKm0QoBCzViDACNMpRUCFGrGGgQYYSqtEKBQM9YgwAhTaYUAhZqxBgFGmEorBCjUjDUIMMJUWiFAoWasQYARptIKAQo1Yw0CjDCVVghQqBlrEGCEqbT6Bgoy2nAnTiZDAAAAAElFTkSuQmCC" alt="" data-size="line">and choose **Terminate** to start the **Terminate agreement** wizard.

<figure><img src="../../.gitbook/assets/finops_terminate.png.png" alt=""><figcaption><p>Terminate option on the agreement details page</p></figcaption></figure>
{% endstep %}

{% step %}
**Use the Terminate Agreement wizard to cancel the order**

Complete the following steps in the Terminate Agreement wizard:

1. **Items** - Make sure the new item quantity is displayed as 0. Then, select **Next**.
2. **Order details** - Add or update the additional ID and other details as necessary. When done, select **Next**.
3. **Review order** - Use the links in the footer to read the terms and conditions. Then, select **Place order** to submit your termination order.
4. **Summary** - Select **View order** to open the order details page. Otherwise, select **Close**.&#x20;
{% endstep %}
{% endstepper %}

## Next steps

After you have submitted the termination order, you can view real-time updates and status on the [order details](../../modules-and-features/marketplace/orders/#subscription-details) page.

When your order has been processed, both the agreement and the subscription associated with the order will be marked as **Terminated** in the Marketplace Platform, and the corresponding organization will be disabled in FinOps.
