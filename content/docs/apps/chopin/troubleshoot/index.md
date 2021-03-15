---
title: "Troubleshooting"
description: "This page contains commonly seen issues and questions from Chopin users."
lead: "This page contains commonly seen issues and questions from Chopin users."
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

Not getting answers for your questions? [Drop us a message →](/docs/introduction/introduction/#contact-us)

## Catalog Google Sheet

- There should be no empty lines between rows.
- `name` of each product can not be empty nor can be characters other than numbers or alphabets. No spaces either. Product names must be unique.

### No products shown

- All products must have `price` and `name` otherwise they won't be shown.
- Do not remove the existing catalog headers copied from tutorial.

### Images are not shown

Check if your image urls are [direct links](#why-the-images-are-not-shown-properly) by pasting them to the browser.

## Order Google Sheet

### New orders are not aligned with previous orders

`order_number` always has to be on the first column and cannot be hidden.

### Get notification when someone places an order?

{{< alert icon="💡" text="<a href='https://support.google.com/docs/answer/91588?co=GENIE.Platform%3DDesktop' target='_blank'>See Google's Documentation on Google Sheets Notification →</a>" >}}

You can set up google sheet notification to get realtime updates on new order submission. On the top of your Order google sheet, click `Tools` > `Notification Rules`. Select "when" you want to receive notifications. 

### Can I add/move/hide columns on the order google sheet?

{{< alert icon="⚠️" text="order_number always has to be on the first column and cannot be hidden." >}}

Absolutely! Add a column to save notes or move the column so certain information can be displayed next to each other. **As long as you keep the title row**, Chopin will be able to populate data to matching fields.

### Can I delete data from order google sheet?

{{< alert icon="💡" text="We recommend to hide instead of delete rows whenever you can." >}}

We don't recommend deleting data (actual transactions, retiring products, etc), as they're valuable for future analysis. Instead, hide the rows you don't need (Select row(s) > Right Click > Click `Hide row`) .

## Create Chopin Store on Telescope

Follow the steps on [Chopin Flow](https://telescope.apiobuild.com/flow/chopin-stores). You must create **two** google sheets, share editor access with Waitress account, and authorize.

### Cannot find your store

- Check if the current login account in Telescope is the same as the account used to create Chopin store.
- Click the gear button ⚙️ to view [Telescope user settings](https://telescope.apiobuild.com/settings). The current login account is shown on the top. If it's different from the account used to create Chopin store, simply sign out and sign in again with the matching account.

### Unable to authorize google sheet

Pop-up blocker might disable the google sheet authorization login. Disable the plug-in or enable pop-up for telescope, and try [Chopin Flow](https://telescope.apiobuild.com/flow/chopin-stores) again.

## Images

{{< alert icon="⚠️" text="Keep each image under 500kb to make the Chopin store renders faster." >}}

### How can I create image url?

Use image hosting services whenever you can. We recommend:

- [Imgbb](https://imgbb.com/)
- [img.onl](https://img.onl/)  

After uploading an image to those websites, you will should use **direct link** or **image url** that points to the actual image.

{{< img src="faq-image-link.png" >}}

### Why the images are not shown properly?

{{< alert icon="⚠️" text="Do not use image on google drive. Google can ban your account anytime if it's accessed too frequently." >}}

{{< alert icon="⚠️" text="Do not use image from Facebook, Instagram or personal content on social media platforms. These platforms check browser cookies and the image will only work for you and stop working after a while." >}}

Make sure the image url points to the actual image rather than an entire index, webpage, or website. You can put the url in browser to test it out. If you can see the image and only the image, then that's a working url.

### How to find image url from other websites?

{{< alert icon="⚠️" text="Do not use image from Facebook, Instagram or personal content on social media platforms. These images will only work for you and could stop working after a while." >}}

On the page, right-click the image > Select `Copy Image Address`.

### Why do images load slowly?

{{< alert icon="⚠️" text="Keep each image under 500kb to make the Chopin store renders faster." >}}

Large images will slow down the Chopin store render time. Use services like [TinyPNG](https://tinypng.com/) to reduce the file size.

## Payments

### Difference between Stripe and PayPal Business?

{{< alert icon="💡" text="<a href='https://wpforms.com/stripe-vs-paypal-which-one-is-better/' target='_blank'>Read a more about the differences →</a>" >}}

[Stripe](https://stripe.com/payments) and [PayPal Business](https://www.paypal.com/us/business/website-payments) both accept credit card payments and support realtime transaction verification with Chopin. **wWe recommend using Stripe** over PayPal Business.

{{< alert icon="💡" text="We recommend using Stripe over PayPal Business." >}}

With Stripe, customers can enter their credit card information directly on the Chopin store. On the other hand, PayPal requires customers sign in or enter credit card information in a different pop-up window, this can sometimes can result to more abandoned orders.

### Difference between PayPal.Me and PayPal Business?

[PayPal.Me](https://www.paypal.com/paypalme/) works for both personal and business accounts. However, it's still a manual payment method that requires customers to click the link, sign in to their accounts, then pay.

[PayPal Business](https://www.paypal.com/us/business/website-payments) integration guides your customers to enter the payment information and validate the transaction in realtime. If they fail to submit payment, the order won't be recorded on the order google sheet.

### How to set up PayPal.Me?

1. Register a PayPal account.
2. Go to [PayPal.Me website](https://www.paypal.com/paypalme/) and click `Create Your PayPal.Me Link`.
3. Choose your unique url. It looks like this: PayPal.Me/YourBrand.
4. You can also customize your profile in the [PayPal.Me settings](https://www.paypal.com/paypalme/my/settings), including profile photo, cover photo, and personal message.

## Miscellaneous

### How to get shortened url for my Chopin Store?

[Upgrade to Basic Plan](https://apiobuild.com/#pricing) to get an apio branded url (`chopin.apiobuild.com/<store_name>`) for as low as $5/month. Feel free to contact us if you want to reroute your Chopin to your domain, if you already have one.

{{< alert icon="💡" text="You can also use shortened url services like <a href='https://bitly.com/' target='_blank'>Bitly</a> to create shortened Chopin Store url" >}}

### How to retrieve LINE url?

Personal Account

1. Open your LINE app, click <i class="fas fa-user-plus"></i> (Add friends symbol) on `Home` tab.
2. Click `Invite` and select `Invite friend by text message`.
3. Randomly select a friend and click `Invite` (Don't worry! Line will not send text automatically).
4. You will be brought to your texting app and have a draft message with your LINE URL. It will look like this: line.me/ti/p/XXXX

Chat Group

1. Click <i class="fas fa-bars"></i> in your LINE group chat and select `Invite`.
2. Click `Invite Link` and you will see the option to `Copy invite link`. It will look like this: line.me/R/ti/g/XXXX
