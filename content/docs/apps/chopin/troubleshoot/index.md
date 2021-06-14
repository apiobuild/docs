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

Not getting answers for your questions? [Drop us a message →]({{<ref "/docs/introduction/introduction/index.md#contact-us" >}})

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

{{< alert icon="💡" text="See Google's Documentation on Google Sheets Notification →" ext-href="https://support.google.com/docs/answer/91588?co=GENIE.Platform%3DDesktop" >}}

You can set up google sheet notification to get realtime updates on new order submission. On the top of your Order google sheet, click `Tools` > `Notification Rules`. Select "when" you want to receive notifications. 

### Can I add/move/hide columns on the order google sheet?

{{< alert icon="⚠️" text="order_number always has to be on the first column and cannot be hidden." >}}

Absolutely! Add a column to save notes or move the column so certain information can be displayed next to each other. **As long as you keep the title row**, Chopin will be able to populate data to matching fields.

### Can I delete data from order google sheet?

{{< alert icon="💡" text="We recommend to hide instead of delete rows whenever you can." >}}

We don't recommend deleting data (actual transactions, retiring products, etc), as they're valuable for future analysis. Instead, hide the rows you don't need (Select row(s) > Right Click > Click `Hide row`) .

### Can I manually type in orders?

Rather than manually typing in orders, we recommend you place another order from your Chopin store. So you can make sure to have a unique order number data for every order.

{{< alert icon="⚠️" text="Do not copy and paste a previous order, as the order number will then duplicate. This will create confusion when analyzing order data." >}}

### How to sort my orders?

Each order consists of several lines of data in order google sheets. Sometimes when many orders come in simultaneously, the data won't be recorded in the right order. You can reorganize the orders by sorting `order_number` and `user_name` accordingly.

1. Highlight the entire sheet or click `ctrl` + `a`.
2. If your sheet includes a header row, freeze the first row.
3. Click `Data` > `Sort range`.
4. Click `Data has header row`.
5. Select `order_number` to be sorted first, then click `Add another sort column`.
6. Select `user_name` to be sorted.
7. Click Sort.

{{< alert icon="💡" text="See Google's Documentation on sort your data →" ext-href="https://support.google.com/docs/answer/3540681?co=GENIE.Platform%3DDesktop&hl=en" >}}

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

Use image hosting services whenever you can. We recommend [Imgbb](https://imgbb.com/).

After uploading an image to those websites, you should use **direct link** or **image url** that points to the actual image.

[A quick video guide for creating image URL →](https://youtu.be/fP28hxRr-FM?t=395)

{{< img src="faq-imgbb.png" >}}

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

## Confirmation Emails

### Why my customers doesn't receive order confirmaion emails?

Check if you complete the followings:

- Grant us permission via [Post-It](https://telescope.apiobuild.com/app/post-it) with the Gmail account you attempt to send emails from
- Select `Send Order Confirmation Email` under `Order Settings` section in [Chopin](https://telescope.apiobuild.com/app/chopin)
- The email you put in the `Contact Information` section is the same as the one you authorize in Post-It

You can also try remove Gmail access and add it again in [Post-It](https://telescope.apiobuild.com/app/post-it).

### Can I customize the order confirmaion content?

We support [custom subject line](/docs/apps/chopin/email-confirmation/#order-confirmation-email-subject) and [custom messaging](/docs/apps/chopin/email-confirmation/#configure-custom-email-messaging) based on payment method. Full customization coming soon!

## Payments

### Difference between Stripe and PayPal Business?

{{< alert icon="💡" text="Read a more about the differences →" ext-href="https://wpforms.com/stripe-vs-paypal-which-one-is-better/" >}}

[Stripe](https://stripe.com/payments) and [PayPal Business](https://www.paypal.com/us/business/website-payments) both accept credit card payments and support realtime transaction verification with Chopin.

{{< alert icon="💡" text="We recommend using Stripe over PayPal Business and currently only support Stripe integration" >}}

With Stripe, customers can enter their credit card information directly on the Chopin store. On the other hand, PayPal requires customers to sign in or enter credit card information in a different pop-up window, this can sometimes result in more abandoned orders.

### Difference between PayPal.Me and PayPal Business?

[PayPal.Me](https://www.paypal.com/paypalme/) works for both personal and business accounts. However, it's still a manual payment method that requires customers to click the link, sign in to their accounts, then pay.

[PayPal Business](https://www.paypal.com/us/business/website-payments) integration guides your customers to enter the payment information and validate the transaction in realtime. If they fail to submit payment, the order won't be recorded on the order google sheet.

### How to set up PayPal.Me?

1. Register a PayPal account.
2. Go to [PayPal.Me website](https://www.paypal.com/paypalme/) and click `Create Your PayPal.Me Link`.
3. Choose your unique url. It looks like this: PayPal.Me/YourBrand.
4. You can also customize your profile in the [PayPal.Me settings](https://www.paypal.com/paypalme/my/settings), including profile photo, cover photo, and personal message.

### I don't see the payment method I need

Chopin supports [credit card](/docs/apps/chopin/payments/#online-payment-processors) and a wide list of [offline payment methods](/docs/apps/chopin/payments/#offline-manual-payment-options). We are always looking to support as many payment methods as we possibly could. [Reach out to us](/docs/introduction/introduction/#contact-us) to add new payment methods!

## Miscellaneous

### Why am I seeing ads on my store?

On our free tier, we use ads income to offset the hosting cost. We also offer [basic tier](https://apiobuild.com/#pricing) at USD$10 per month to remove ads (along with other perks).

{{< alert icon="💡" text="Join apio basic tier now →" ext-href="https://telescope.apiobuild.com/settings/billing">}}

### How to get shortened url for my Chopin Store?

[Upgrade to Basic Plan](https://apiobuild.com/#pricing) to get an apio branded url (`chopin.apiobuild.com/<store_name>`) for as low as $10/month. Feel free to contact us if you want to reroute your Chopin to your domain, if you already have one.

You can also use shortened url services like [Bitly](https://bitly.com/) or [reurl](https://reurl.cc/main/en) to create shortened Chopin Store url.

### What is Markdown?

[Markdown](https://en.wikipedia.org/wiki/Markdown) is a lightweight markup language for creating formatted text using a plain-text editor. In other words, you can use text to style text. 

We support Markdown to style text in various sections, including [store description](/docs/apps/chopin/store-configuration/#store-description) in Chopin and [product description](/docs/apps/chopin/product-configuration/#description) in catalog google sheet.

Some helpful guides:

- [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)
- [Markdown Table Generator](https://www.tablesgenerator.com/markdown_tables)
- [Learn Markdown in 60 secs](https://commonmark.org/help/)

{{< alert icon="💡" text="To start a new paragraph, you need to make an empty line between paragraphs." >}}

### How to retrieve LINE url?

Personal Account

1. Open your LINE app, click <i class="fas fa-user-plus"></i> (Add friends symbol) on `Home` tab.
2. Click `Invite` and select `Invite friend by text message`.
3. Randomly select a friend and click `Invite` (Don't worry! Line will not send text automatically).
4. You will be brought to your texting app and have a draft message with your LINE URL. It will look like this: line.me/ti/p/XXXX

Chat Group

1. Click <i class="fas fa-bars"></i> in your LINE group chat and select `Invite`.
2. Click `Invite Link` and you will see the option to `Copy invite link`. It will look like this: line.me/R/ti/g/XXXX
