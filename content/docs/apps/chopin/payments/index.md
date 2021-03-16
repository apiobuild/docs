---
title: "Payments"
description: "Chopin supports both online and offline (manual) payment methods. While credit card is the mainstream payment method supported by most e-commerce platforms, we recognize many smaller businesses don't have POS or even a dedicated bank account. Therefore we have many customized payment options available. We are always looking to support as many payment methods as we possibly could. Reach out to us to add new payment methods."
lead: "Chopin supports both online and offline (manual) payment methods. While credit card is the mainstream payment method supported by most e-commerce platforms, we recognize many smaller businesses don't have POS or even a dedicated bank account. Therefore we have many customized payment options available. We are always looking to support as many payment methods as we possibly could. Reach out to us to add new payment methods."
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

Each payment method will appear as a **button** on your store. If you don't add any payment options, there will be a **"Submit Order"** button. You can enable as many payment options as you'd like.

Visit our [Demo Store](https://chopin.apiobuild.com/demo-store) and see how they work in real world. If you don't see your preferred payment methods, [Drop us a message →]({{<ref "/docs/introduction/introduction/index.md#contact-us" >}})

{{< img src="e_payment_button_21.png" >}}

## Online Payment Processors

We currently support [Stripe](https://stripe.com/payments) as our online payment processor. This allows customers pay with credit cards.

[Contact us]({{ < ref "introduction/#contact-us" > }}) to integrate Stripe account with your Chopin store.

{{< alert icon="💡" text="Learn more about Stripe pricing →" ext-href="https://stripe.com/pricing" >}}

Stripe impose processing fee of **2.9% + 30¢**. The fee will be deducted directly from your any payment you received via stripe. apio doesn't take additional cut from your profits! Click links below for more detailed pricing.

{{< alert icon="💡" text="Read more on Stripe vs Paypal →" rel-href="/docs/apps/chopin/troubleshoot/#difference-between-stripe-and-paypal-business" >}}

<span style="display: none">
- [PayPal](https://www.paypal.com/us/webapps/mpp/merchant-fees)
</span>

Integrating online payment platforms allows Chopin to **verify transactions and post the result in realtime** to order google sheet.
Merchants will no longer have to manually confirm and verify each payment from customers.

## Offline (Manual) Payment Options

We also support popular manual payment options across North America. Manual payment means that the transaction will be handled outside of the Chopin checkout process and we won't be able to verify these payments on your behalf. The payment method selected by the customer will be posted to order google sheet.

### Paypal.Me `NEW`

{{< alert icon="💡" text="Learn more about Paypal.Me →" ext-href="https://www.paypal.com/paypalme/" >}}

{{< alert icon="💡" text="Learn more about how to use create Paypal.Me →" rel-href="/docs/apps/chopin/troubleshoot/#how-to-set-up-paypalme" >}}

Provide your Paypal.Me link. It should look like: `https://www.paypal.me/youraccount`. This is the only manual payment which we can auto-generate the order total amount for customers during checkout. We recommend it over other manual options.

### Zelle

{{< alert icon="💡" text="Learn more about Zelle →" ext-href="https://www.zellepay.com/" >}}

Provide your Zelle email or phone number.

### Venmo

{{< alert icon="💡" text="Learn more about Venmo →" ext-href="https://venmo.com/" >}}

Provide your Venmo handle.

### E-transfer

{{< alert icon="💡" text="Learn more about E-transfer →" ext-href="https://www.interac.ca/en/consumers/products/interac-e-transfer/" >}}

Provide your E-Transfer email or mobile number.

### Pay at Pick-Up

Check this box if you wish to collect payment when customers pick up their orders.

### Collect on Delivery `NEW`

Check this box if you or courier will collect payment when the order is delivered to customers.

