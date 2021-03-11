---
title: "Store Configuration"
description: "Chopin works out of box without any further configuration. However, for those who'd like to add custom rules and business automations, we've made it easy to add customization and localization to work with businesses from all over the world."
lead: "Chopin works out of box without any further configuration. However, for those who'd like to add custom rules and business automations, we've made it easy to add customization and localization to work with businesses from all over the world."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "chopin"
weight: 250
toc: true
---

[Checkout How to Create New Store →]({{< ref "create-new-store" >}})

After the store is created. Go to [Chopin App on Telescope](https://telescope.apiobuild.com/app/chopin) to add customization and configuration for your store.

## Store Info

General store information shown to anyone visiting your store and social media shares.

{{< img src="a_store_info_21.png" >}}

### Store Name

The store name used when [creating the store]({{< ref "create-new-store" >}}). This cannot be modified.

### Logo url *(optional)*

<!-- TODO: add image url bulb -->

Give your store a logo.

### Store Description *(optional)*

{{< alert icon="💡" text="<a href='https://www.markdownguide.org/cheat-sheet/' target='_blank'>Learn more about markdown →</a>" >}}

Let your customers know what your store is about, brand story, shipping/return policy, or any information you'd like to include. Up to 1000 characters. Styling with markdown is supported.

### Announcement *(optional)*

News to share with your customers.

## Layout

### Store Background Image url *(optional)*

Add a background image.

### Store Background Color *(optional)*

{{< alert icon="💡" text="<a href='https://htmlcolorcodes.com/' target='_blank'>Learn more about hex code →</a>" >}}

You can easily select color from swatch or enter a hex code.

### Page Header Height `NEW`

You can adjust height of your background image. Default is 100% and it will take up the entire screen.

{{< img src="b_layout_1_21.png" >}}

### Out of Stock Message *(optional)*

Text shown when the product has max_qty = 0.

In catalog google sheet, when input "0" in the `max_qty` field the indicated product will show "Coming Soon!"
on chopin app.

You can customize this text. For example, it can be "Coming Soon", "Back in October" etc.

{{< img src="b_layout_2.png" >}}

## Order Settings

### Store Currency `NEW`

{{< alert icon="💡" text="<a href='https://en.wikipedia.org/wiki/ISO_4217#Active_codes' target='_blank'>Learn more about currency code →</a>" >}}

Currency is default to USD (US Dollar). Choose your preferred currency code from the dropdown menu.

### Order Form

{{< alert icon="💡" text="Use note field to collect customization details (i.e. message to be put on the cake) as opposed a way to communicate about the order with your customers." >}}

Order for input fields. By default, we only require customers to input in their email. You can make other fields you need from customers required.

- Name
- Phone Number
- Address
- Remove Customer Address Field: If you sell digital products or offer store pick-up only, you might not need to collect addesses from customers.
- Add Optional Note Section: To add a field for customers to input any notes.

{{< img src="c_order_1_21.png" >}}

### Order Minimum

Your customers' order total has to greater than the minimum amount set to be able to place the order.

### Order Confirmation

[Checkout How to Configure Order Confirmation Email →]({{< ref "email-confirmation" >}})

## Contact Information

### Email

The email address is default to the email you used to sign into Telescope. You can update to a different email. The email address is also used to send order confirmation emails.

[Checkout How to Configure Order Confirmation Email →]({{< ref "email-confirmation" >}})

### Facebook

Full url to your facebook page or group (eg. https://www.facebook.com/apiobuild)

### Instagram

Instagram handle without @, not the full url (eg. apiobuild)

### LINE

<!-- TODO: move tutorial here -->

{{< alert icon="💡" text="<a href='https://apiobuild.com/blog/troubleshoot-chopin-store/#how-to-retrieve-line-url' target='_blank'>Learn more how to create LINE URL →</a>" >}}

URL to your LINE account or LINE group.

### Phone Number

Start with country code (US: +1) and without dash nor parenthesis (eg. +17181234567).

### Twitter `NEW`

Twitter handle without @ (eg. apiobuild).

### WhatsApp `NEW`

WhatsApp number with country code and without dash, +, nor parenthesis (eg. 12121234567).

{{< img src="d_contact_info.png" >}}

