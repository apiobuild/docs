---
title: "Product Configuration"
description: "Copy and paste product catalog from your existing system or simply edit the catalog google sheet to start adding product to your store. Store will update in real-time with the catalog google sheet."
lead: "Copy and paste product catalog from your existing system or simply edit the catalog google sheet to start adding product to your store. Store will update in real-time with the catalog google sheet."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "chopin"
weight: 230
toc: true
---

<iframe width="560" height="315" src="https://www.youtube.com/embed/w9IXo0i1xSE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

By default, [your store would look like below.](https://chopin.apiobuild.com/google-oauth2%7C106308532747537725517/3b99cc9c-6c28-45dd-9786-8521fe0a2e47) We are pretty sure you're not selling Cool Cat and Funny Cat.

<!--
TODO: create short url for this store
-->

To add and update products, go to your **catalog google sheet**.

{{< img src="default-products.png" >}}

### Catalog Google Sheet

Edit product details by updating the following fields on the catalog google sheet:

{{< alert icon="⚠️" text="There should not be any empty line(s) between rows." >}}

{{< alert icon="⚠️" text="Only items with valid <b>name</b> and <b>price</b> will be shown on your store." >}}

You can find your catalog google sheet url on the Waitress API section of the Chopin App. Simply put `https://docs.google.com/spreadsheets/d/` + sheet id (selected area in image below) in the browser address bar.

{{< img src="waitress-api.png" >}}

### name (required)

*Unique* name/id starts with any alphabet and contains **only dashes (-), underscores (_), and alphanumeric** for each product. No spaces.

Example: `sku-132`, `cake_strawberry`,`a`

### nickname

Product names that will appear on the store page, they can be **any language, symbol, and even emoji 🤩**.

### description

More information about the product. Styling with **markdown** is supported.

{{< alert icon="💡" text="What is Markdown →" rel-href="/docs/apps/chopin/troubleshoot/#what-is-markdown" >}}

{{< alert icon="💡" text="You can add another line in cell by press ⌘ + Enter on a Mac or Ctrl + Enter on Windows" ext-href="https://support.google.com/docs/answer/46973?co=GENIE.Platform%3DDesktop&hl=en" >}}

### image_url

URL of the product image(s). Multiple image urls can be separated by comma (,).

We recommend upload images to [an image hosting website]({{< ref "/docs/apps/chopin/troubleshoot/index.md#how-can-i-create-image-url" >}}) instead of pulling images from Google Drive, Dropbox, or social media.

Our default gif will appear on your store when there's no input in the image_url cell.

{{< alert icon="💡" text="Why is image url not working? →" rel-href="/docs/apps/chopin/troubleshoot/#images" >}}

### price (required)

Product price, no need to enter "$" (dollar sign).

{{< alert icon="💡" text="How to update currency? →" rel-href="/docs/apps/chopin/payments/#currency" >}}

### max_qty

Maximum quantity that **one customer** can buy. If max_qty = 0, it will show out-of-stock message (default is `Coming Soon`) under the product.

We support advanced inventory management that can prevent your from oversell. [Contact us to learn more!]({{< ref "/docs/introduction/introduction/index.md#contact-us" >}})

{{< alert icon="💡" text="How to customize out-of-stock message →" rel-href="/docs/apps/chopin/store-configuration/#out-of-stock-message" >}}

### category

To allow customer to filter products. Multiple categories can be separated by comma (,).

### hide

Enter "x" (or any other characters), this product will not appear on your store.

### no_tax

Enter "x" (or any other characters), sales tax won't apply to this product.

### example

{{< img src="catalog_sheet_ex1.png" >}}

If you want to /docs/apps/chopin/multi-option-product-configuration/, you will need to add some more columns manually. Tap through the next page to learn how that work.
