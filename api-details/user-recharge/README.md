# User recharge

## Usage Scenario <a href="#vijj-1704960516492" id="vijj-1704960516492"></a>

For each user, it is recommended to allocate a unique exclusive recharge address. All recharge operations for that user will revolve around this address, providing the following benefits:

1. For each asset type, a recharge account will be assigned to each user.
2. Recharge accounts will be repeatedly used, facilitating users' frequent deposits.
3. The unique correspondence between users and recharge accounts also ensures the clarity of individual financial transactions.

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

## Usage Process <a href="#yf8b-1704960516492" id="yf8b-1704960516492"></a>

As mentioned above, a unique corresponding recharge address will be assigned to each user, typically occurring when onboarding new customers, such as during user registration. The specific process is as follows:

<figure><img src="../../.gitbook/assets/image (7).png" alt="" width="375"><figcaption></figcaption></figure>

1. User Registration
   1. Users initiate new user registration through the business system.
   2. After successful user registration, the business system initiates a request to generate an exclusive recharge account for the user.
2. Determine Currency Support
   1. If not supported, an account cannot be generated.
3. Generate Exclusive Recharge Account
   1. The business system calls the address generation request to assign an exclusive recharge account to the user.
   2. For each asset type, a recharge account is assigned to each user.
   3. Recharge accounts are reused to facilitate users' frequent deposits.
   4. The unique correspondence between users and recharge accounts ensures the clarity of individual financial transactions.
4. Monitor User Deposits
   1. Actively monitor recharge deposits.
   2. Users need to specify a notification callback address.
5. User Recharge
   1. Users can choose to deposit funds into the exclusive recharge account through any third-party wallet.
6. Deposit Notification
   1. After user recharges, the notification callback address will receive a recharge notification.

## Related APIs <a href="#yf8b-1704960516492" id="yf8b-1704960516492"></a>

{% content-ref url="request-greater-than-address-generation.md" %}
[request-greater-than-address-generation.md](request-greater-than-address-generation.md)
{% endcontent-ref %}

{% content-ref url="callback-greater-than-address-deposit-notification.md" %}
[callback-greater-than-address-deposit-notification.md](callback-greater-than-address-deposit-notification.md)
{% endcontent-ref %}
