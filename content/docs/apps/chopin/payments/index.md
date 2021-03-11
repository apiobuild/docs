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
weight: 260
toc: true
---

Each payment method will appear as a **button** on your store. If you don't add any payment options, there will be a **"Submit Order"** button. You can enable as many payment options as you'd like.

Visit our [Demo Store](https://chopin.apiobuild.com/demo-store) and see how they work in real world. If you don't see your preferred payment methods, [drop us a message →](/docs/introduction/introduction/#contact-us)

{{< img src="e_payment_button_21.png" >}}

## Online Payment Processors

We currently support [Stripe](https://stripe.com/payments) as our online payment processor. This allows customers pay with credit cards. 

[Contact us](/docs/introduction/introduction/#contact-us) to integrate Stripe account with your Chopin store.

{{< alert icon="💡" text="<a href='https://stripe.com/pricing' target='_blank'>Learn more about stripe pricing →</a>" >}}

Stripe impose processing fee of **2.9% + 30¢**. The fee will be deducted directly from your any payment you received via stripe. apio doesn't take additional cut from your profits! Click links below for more detailed pricing.

<!-- TODO: stripe vs paypal -->
{{< alert icon="💡" text="<a href='https://apiobuild.com/blog/troubleshoot-chopin-store/#difference-between-stripe-and-paypal-business' target='_blank'>Read more on Stripe vs Paypal →</a>" >}}

<span style="display: none">
- [PayPal](https://www.paypal.com/us/webapps/mpp/merchant-fees)
</span>

Integrating online payment platforms allows Chopin to **verify transactions and post the result in realtime** to order google sheet.
Merchants will no longer have to manually confirm and verify each payment from customers.

## Offline (Manual) Payment Options

We also support popular manual payment options across North America. Manual payment means that the transaction will be handled outside of the Chopin checkout process and we won't be able to verify these payments on your behalf. The payment method selected by the customer will be posted to order google sheet.

### Paypal.Me `NEW`

{{< alert icon="💡" text="<a href='https://www.paypal.com/paypalme/' target='_blank'>Learn more about Paypal.Me →</a>" >}}

<!-- TODO: add how-to ref -->

Provide your Paypal.Me link. It should look like: `https://www.paypal.me/youraccount`. This is the only manual payment which we can auto-generate the order total amount for customers during checkout. We recommend it over other manual options.

### Zelle

{{< alert icon="💡" text="<a href='https://www.zellepay.com/' target='_blank'>Learn more about Zelle →</a>" >}}

Provide your Zelle email or phone number.

### Venmo

{{< alert icon="💡" text="<a href='https://venmo.com/' target='_blank'>Learn more about Venmo →</a>" >}}

Provide your Venmo handle.

### E-transfer

{{< alert icon="💡" text="<a href='https://www.interac.ca/en/consumers/products/interac-e-transfer/' target='_blank'>Learn more about E-transfer →</a>" >}}

Provide your E-Transfer email or mobile number.

### Pay at Pick-Up

Check this box if you wish to collect payment when customers pick up their orders.

### Collect on Delivery `NEW`

Check this box if you or courier will collect payment when the order is delivered to customers.

