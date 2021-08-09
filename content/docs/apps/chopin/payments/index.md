---
title: "Payments"
description: "Chopin supports both and offline (manual) payment methods. While credit card is the mainstream payment method supported by most e-commerce platforms, we recognize many smaller businesses don't have POS or even a dedicated bank account. Therefore we have many customized payment options available."
lead: "Chopin supports both online and offline (manual) payment methods. While credit card is the mainstream payment method supported by most e-commerce platforms, we recognize many smaller businesses don't have POS or even a dedicated bank account. Therefore we have many customized payment options available."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "chopin"
weight: 270
toc: true
---

{{< img src="e_payment_button_21.png" >}}

Each payment method will appear as a **button** on your store. If you don't add any payment options, there will be a **"Submit Order"** button. You can enable as many payment options as you'd like.

[Jump to payment method options →](#online-payment-processors)

Visit our [Demo Store](https://chopin.apiobuild.com/demo-store) and see how they work in real world. If you don't see your preferred payment methods, [drop us a message →]({{<ref "/docs/introduction/introduction/index.md#contact-us" >}})

## Order Minimum

Your customers' order total has to be greater than the minimum amount set to be able to place the order.

## Currency

Store currency is default to USD (US Dollar). Choose your preferred currency code from the dropdown menu.

{{< alert icon="💡" text="Learn more about currency code →" ext-href="https://en.wikipedia.org/wiki/ISO_4217#Active_codes" >}}

## Online Payment Processors

Integrating online payment platforms allows Chopin to **verify transactions and post the result in realtime** to order google sheet. Merchants will no longer have to manually confirm and verify each payment from customers.

### Stripe

We currently support [Stripe](https://stripe.com/payments) as online payment processor for our [Basic tier users](https://apiobuild.com/#pricing). This allows customers pay with credit cards and debit cards.

[Contact us to integrate Stripe account with your Chopin store →]({{<ref "/docs/introduction/introduction/index.md#contact-us" >}})

Stripe impose processing fee of **[2.9% + 30¢](https://stripe.com/pricing)**. The fee will be deducted directly from your any payment you received via Stripe. apio doesn't take additional cut from your profits!

{{< alert icon="💡" text="Read more on Stripe vs Paypal →" rel-href="/docs/apps/chopin/troubleshoot/#difference-between-stripe-and-paypal-business" >}}

<span style="display: none">
- [PayPal](https://www.paypal.com/us/webapps/mpp/merchant-fees)
</span>

## Offline (Manual) Payment Options

We also support popular manual payment options around the world. Manual payment means that the transaction will be handled outside of the Chopin checkout process and we won't be able to verify these payments on your behalf. The payment method selected by the customer will be posted to order google sheet.

We are always looking to support as many payment methods as we possibly could. [Reach out to us](https://apiobuild.com/docs/docs/introduction/introduction/#contact-us) to add new payment methods!

### Paypal.Me

{{< alert icon="💡" text="Learn more about Paypal.Me →" ext-href="https://www.paypal.com/paypalme/" >}}

{{< alert icon="💡" text="How to create Paypal.Me link →" rel-href="/docs/apps/chopin/troubleshoot/#how-to-set-up-paypalme" >}}

Provide your [Paypal.Me link](https://apiobuild.com/docs/docs/apps/chopin/troubleshoot/#how-to-set-up-paypalme). It should look like: `https://www.paypal.me/youraccount`.

If you accept manual payments, we recommend PayPal.Me as this is the only manual option that auto-generate the order total amount and payee information for customers during checkout.

### Zelle

{{< alert icon="💡" text="Learn more about Zelle →" ext-href="https://www.zellepay.com/" >}}

Provide your Zelle email or phone number.

### Venmo

{{< alert icon="💡" text="Learn more about Venmo →" ext-href="https://venmo.com/" >}}

Provide your Venmo handle.

### E-transfer

{{< alert icon="💡" text="Learn more about E-transfer →" ext-href="https://www.interac.ca/en/consumers/products/interac-e-transfer/" >}}

Provide your E-Transfer email or mobile number.

### Revolut `NEW`

{{< alert icon="💡" text="Learn more about Revolut →" ext-href="https://www.revolut.com/" >}}

Provide your Revolut mobile number or handle.

### PayNow `NEW`

{{< alert icon="💡" text="Learn more about PayNow →" ext-href="https://abs.org.sg/consumer-banking/pay-now" >}}

Provide your mobile number, Singapore NRIC/FIN, or Virtual Payment Address (VPA).

### Bank Transfer `NEW`

Provide instruction on bank transfer, which might include name, bank address, account number, routing number, etc. If you need more space to provide detailed instruction, feel free to [customize the confirmation email message](https://apiobuild.com/docs/docs/apps/chopin/email-confirmation/#configure-custom-email-messaging).

### Money Order `NEW`

Provide instruction on who and where the money order should be mailed to.

### Pay at Pick-Up

Select this method, if you wish to collect payment when customers pick up their orders.

No need to enter any details for this payment method. You can provide more instruction with [customized  confirmation email message](https://apiobuild.com/docs/docs/apps/chopin/email-confirmation/#configure-custom-email-messaging).

### Collect on Delivery

Select this payment method if you or the courier will collect payment when the order is delivered to customers.

No need to enter any details for this payment method. You can provide more instruction with [customized  confirmation email message](https://apiobuild.com/docs/docs/apps/chopin/email-confirmation/#configure-custom-email-messaging).

## Configure with Confirmation Email

{{< alert icon="💡" text="What does Confirmation Email look like  →" ext-href="https://apiobuild.com/blog/introducing-post-it-email-automation-service/#email-template" >}}

We already pre-configure the payment instruction in confirmation emails for you, which includes order total, payment method, and account information. If you'd like to **replace** that information in another language or provide additional wording, you can customize the message in Order Settings under Custom Email Messages.

[Read more about how to set up costom email message →](/docs/apps/chopin/email-confirmation/)
