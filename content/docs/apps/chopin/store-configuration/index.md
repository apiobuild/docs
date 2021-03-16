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

{{< alert icon="💡" text="How to create image url?" rel-href="/docs/apps/chopin/troubleshoot/#images" >}}

Give your store a logo.

### Store Description *(optional)*

{{< alert icon="💡" text="Learn more about markdown →" ext-href="https://www.markdownguide.org/cheat-sheet/" >}}

Let your customers know what your store is about, brand story, shipping/return policy, or any information you'd like to include. Up to 1000 characters. Styling with markdown is supported.

### Announcement *(optional)*

News to share with your customers.

## Layout

### Store Background Image url *(optional)*

Add a background image.

### Store Background Color *(optional)*

{{< alert icon="💡" text="Learn more about hex code →" ext-href="https://htmlcolorcodes.com/" >}}

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

[Checkout Order Settings Docs →]({{< ref "order-settings" >}})

## Contact Information

[Checkout Contact Information Docs →]({{< ref "contact-information" >}})

## Shipping, Discount and Tax

[Checkout Shipping, Discount and Tax Docs →]({{< ref "order-settings" >}})

## Waitress API

These are auto-generated when the store was created.

By default we use apio's own [Waitress API](https://telescope.apiobuild.com/app/waitress) as catalog and order APIs. We welcome you to bring your own API, [Drop us a message →]({{<ref "/docs/introduction/introduction/index.md#contact-us" >}}).
