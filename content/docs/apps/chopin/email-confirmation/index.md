---
title: "Email Confirmation"
description: "With post-it, you could add automated email order confirmation to Chopin store with any gmail account."
lead: "With post-it, you could add automated email order confirmation to Chopin store with any gmail account."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "chopin"
weight: 290
toc: true
---

## Post-It Permission

Go to [Post-It](https://telescope.apiobuild.com/app/post-it) (apio\'s communication automation service) to authorize the Gmail account you'd like to send confirmation emails from. This app requires you to grant us permission to send emails on your behalf.

- Click `View Emails` and then <i class="fas fa-plus-circle"></i> (plus sign) to add a Gmail
- Log in to your Google account
- Click `Allow` to grant apio access to send email on your behalf

{{< alert icon="⚠️" text="If you'd like to send emails from an account that's not the one you use to log in Telescope, be sure to update Email in contact information section." ext-href="/docs/apps/chopin/contact-information/#email" >}}

## Custom Email Messages

{{< alert icon="💡" text="What does Confirmation Email look like  →" ext-href="https://apiobuild.com/blog/introducing-post-it-email-automation-service/#email-template" >}}

Go to `Order Settings` section in [Chopin app](https://telescope.apiobuild.com/app/chopin) to finish setting up custom email messages.

### Send Order Confirmation

Enable this feature to send an automated email order confirmation after the customer place an order.

{{< alert icon="⚠️" text="You must give us permission to send emails via Post-It" ext-href="https://telescope.apiobuild.com/app/post-it" >}}

### Order Confirmation Email Subject

Customize the subject of order confirmation email. Use `<store_name>` and `<order_number>` to show the name of your store and the order number.

**Example:**

Default subject line is "Your Order from `<store_name>` [`<order_number>`]”.

{{< img src="c_order_2.png" >}}

"🎁 `<store_name>` has a surprise for you! Order number: `<order_number>`" will look like this:

{{< img src="c_order_3.png" >}}

### Configure Custom Email Messaging

- Field: We currently only support custom email based on different payment methods
- Field Value: Choose the payment method that will apply this custom message
- Email Message: Customize the content to **replace** default payment instruction in confirmation emails
   - Use `<total>` to indicate the total amount
   - Use `<method>` to indicate the applied payment method
   - Use `<handle>` to indicate the account information (handle,id, or phone number) of applied payment method
   - To recreate PayPal.Me link, use the following: `<a href="<handle>/<total>" target="_blank">Paypal</a>`

{{< alert icon="💡" text="If you prefer the default wording but don't remember it, you can always delete the custom message rule" >}}

**Example:**

Default message when people choose to pay with Zelle:

{{< img src="custom_email.png" >}}

When I update the custom message to
"We're getting your cookies ready to be shipped, but not until you pay `<handle>` `<total>` via `<method>`. Don't worry, reheat instruction will be included in the package!"

The Email will look like this:

{{< img src="custom_email_2.png" >}}

{{< alert icon="💡" text="While we currently only support payment-based custom message, feel free to add any information as needed." >}}
