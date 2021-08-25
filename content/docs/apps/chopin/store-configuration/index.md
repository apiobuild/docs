---
title: "Store Configuration"
description: "Chopin works out of box without any further configuration. However, for those who'd like to add custom rules and business automations, we've made it easy to add customization and localization to work with businesses from all over the world."
lead: "Chopin works out of box without any further configuration. However, for those who'd like to add custom rules and business automations, we've made it easy to add customization and localization to work with businesses from all over the world."
date: 2020-10-06T08:48:57+00:00
lastmod: 2021-08-18T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "chopin"
weight: 250
toc: true
---

[How to create a Chopin store →]({{< ref "create-new-store" >}})

After the store is created. Go to [Chopin App on Telescope](https://telescope.apiobuild.com/app/chopin) to add customization and configuration for your store. You can update this information anytime (except store name and waitress APIs) and the updates will be reflected in real-time.

- Click <i class="fas fa-save"></i> (save sign) to save your updates. Click <i class="fas fa-trash"></i> (trash can sign) to delete the store completely.
- Click <i class="fas fa-plus-circle"></i> (plus sign) to add new information and click <i class="fas fa-minus-circle"></i> (minus sign) to delete the information.

## Store Info

General store information shown to anyone visiting your store and on social media sharings.

{{< img src="a_store_info_21.png" >}}

### Store Name

The store name used when [creating the store]({{< ref "create-new-store" >}}). This cannot be modified.

### Logo url

Give your store a logo. This image will also be the [favicon](https://en.wikipedia.org/wiki/Favicon) of your store.

{{< alert icon="💡" text="How to create image url?" rel-href="/docs/apps/chopin/troubleshoot/#images" >}}

### Store Description

Let your customers know what your store is about: brand story, shipping/return policy, or any information you'd like to include. Up to 1000 characters.

Styling with **markdown** is supported.

Default font color is white. You can change it to black in the [Layout section]({{< ref "/docs/apps/chopin/store-configuration/index.md#light-page-theme" >}}).

{{< alert icon="💡" text="Learn more about markdown →" rel-href="/docs/apps/chopin/troubleshoot/#what-is-markdown" >}}

### Announcement

News to share with your customers.

## Layout

{{< img src="b_layout_1_21.png" >}}

### Store Background Image url

Add a background image.

### Store Background Color

Or you can select a solid color from swatch or enter a [hex code](https://htmlcolorcodes.com/).

### Page Header Height

You can adjust height of your background image. Default is 100% and it will take up the entire screen.

{{< alert icon="⚠️" text="The page height affects how much space for your store description, so don't make this area too small!" >}}

### Light Page Theme

Check this box to make the font color of [store description](#store-description) from white to black.

### Category Bar Layout

Choose your preferred category bar layout:

- hide: won't show categories at all.
- enlarge: default design with text under category image.
- small: condensed design with text on image.

Category image is the first image of the first product within that category.

{{< img src="category_bar.png" >}}

{{< alert icon="💡" text="Learn more about our category bar design →" ext-href="https://apiobuild.com/blog/news-ui-updates/#new-ui-better-navigation" >}}

### Out of Stock Message

Text shown when the product has `max_qty` = 0.

In catalog google sheet, when input "0" in the `max_qty` field the indicated product will show "Coming Soon!" on your chopin store.

You can customize this text. For example, it can be "Coming Soon", "Back in October" etc.

{{< img src="b_layout_2.png" >}}

## Order Settings

[Checkout Order Settings Docs →]({{< ref "order-settings" >}})

## Contact Information

[Checkout Contact Information Docs →]({{< ref "contact-information" >}})

## Payment Methods

[Checkout Payment Methods Docs →]({{< ref "payments" >}})

## Shipping, Discount and Tax

[Checkout Shipping, Discount and Tax Docs →]({{< ref "/docs/apps/chopin/order-settings/index.md#shipping" >}})

## Waitress API

These are auto-generated when the store was created.

By default we use apio's own [Waitress API](https://telescope.apiobuild.com/app/waitress) as catalog and order APIs. We welcome you to bring your own API, [Drop us a message →]({{< ref "/docs/introduction/introduction/index.md#contact-us" >}}).
