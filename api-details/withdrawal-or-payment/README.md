# Withdrawal or payment

## Usage Scenario <a href="#iv4a-1704960907749" id="iv4a-1704960907749"></a>

For corporate transfers or withdrawals, it is required to operate from the Cregis enterprise wallet. The enterprise wallet strictly manages funds to ensure a reliable and secure fund utilization process. Specific measures include:

1. Strict approval process for disbursement.
2. Multi-party signature withdrawal based on MPC (Multi-Party Computation) technology guarantee.

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

## Usage Process <a href="#pwpv-1704960907749" id="pwpv-1704960907749"></a>

As mentioned above, corporate withdrawals revolve around the enterprise wallet and follow a strict process. The specific process is as follows:

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>



1. Determine Currency Support
2. Verify Target Address Validity
   1. Confirm whether the target address is a valid address on the target blockchain.
3. Verify Address Ownership
   1. Determine if the target address belongs to the same project (pid).
   2. If restricted to internal transfers, terminate the process at this point.
4. Initiate Withdrawal/Payment
   1. Submit the withdrawal request to the enterprise wallet.
5. Withdrawal Query/Monitoring
   1. After the user initiates a withdrawal, the notification callback address will receive a withdrawal status notification.

## Related APIs <a href="#yf8b-1704960516492" id="yf8b-1704960516492"></a>

{% content-ref url="request-greater-than-payout-creation.md" %}
[request-greater-than-payout-creation.md](request-greater-than-payout-creation.md)
{% endcontent-ref %}

{% content-ref url="request-greater-than-payout-query.md" %}
[request-greater-than-payout-query.md](request-greater-than-payout-query.md)
{% endcontent-ref %}

{% content-ref url="callback-greater-than-payout-notification.md" %}
[callback-greater-than-payout-notification.md](callback-greater-than-payout-notification.md)
{% endcontent-ref %}
