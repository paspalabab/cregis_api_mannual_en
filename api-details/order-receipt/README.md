# Order receipt

## Usage Scenario <a href="#l1fz-1704960774228" id="l1fz-1704960774228"></a>

During a specific time period, the platform recommends assigning a unique exclusive payment address for each order. All payment operations for that order within the time period will revolve around this address. The advantages are as follows:

1. The business system calls the address generation request to assign an exclusive payment address to the order.
2. For each asset type, a payment account is allocated as the order's payment account address.
3. The payment account can be reused for the order until it expires, is canceled, or all funds are received, facilitating multiple payments.
4. The unique correspondence between orders and exclusive addresses ensures clarity in financial transactions.

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

## Usage Process <a href="#agvn-1704960774228" id="agvn-1704960774228"></a>

As mentioned above, a unique corresponding payment address will be assigned to each order, typically occurring when creating a new order and requiring the customer to make payment within a specified time period. The specific process is as follows:

<figure><img src="../../.gitbook/assets/image (9).png" alt="" width="375"><figcaption></figcaption></figure>

1. Create Order
   1. The business system creates an order.
2. Determine Currency Support
   1. If not supported, the initiation of order payment cannot proceed.
3. Initiate Order Payment
   1. The business system calls the address generation request to assign an exclusive payment address to the order.
   2. For each asset type, a payment account is allocated as the order's payment account address.
   3. The payment account can be reused for the order until it expires or is canceled, facilitating multiple payments.
   4. The unique correspondence between orders and exclusive addresses ensures clarity in financial transactions.
4. Monitor Customer Payments
   1. Actively monitor deposits into the payment account.
   2. The order needs to specify a notification callback address.
5. Customer Payment
   1. Customers can choose to make payments to the order's exclusive account through any third-party wallet.
6. Payment Notification/Query
   1. After customer payment, the notification callback address will receive a payment notification.
7. Timeout/Cancelation
   1. After timeout or active cancelation, the payment action for this order terminates.

## Related APIs <a href="#yf8b-1704960516492" id="yf8b-1704960516492"></a>

{% content-ref url="request-greater-than-order-deposit-creation.md" %}
[request-greater-than-order-deposit-creation.md](request-greater-than-order-deposit-creation.md)
{% endcontent-ref %}

{% content-ref url="request-greater-than-order-deposit-query.md" %}
[request-greater-than-order-deposit-query.md](request-greater-than-order-deposit-query.md)
{% endcontent-ref %}

{% content-ref url="request-greater-than-order-deposit-cancellation.md" %}
[request-greater-than-order-deposit-cancellation.md](request-greater-than-order-deposit-cancellation.md)
{% endcontent-ref %}

{% content-ref url="callback-greater-than-order-deposit-notification.md" %}
[callback-greater-than-order-deposit-notification.md](callback-greater-than-order-deposit-notification.md)
{% endcontent-ref %}
