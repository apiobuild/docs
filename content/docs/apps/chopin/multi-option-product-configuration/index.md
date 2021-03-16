---
title: "Multi Option Products"
description: "We support multi option products. To configure, simply add a few more columns on the catalog google sheet."
lead: "We support multi option products. To configure, simply add a few more columns on the catalog google sheet."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "chopin"
weight: 240
toc: true
---

This is especially helpful if you are selling:

- Clothes with different colors and sizes
- Food with different flavors
- Crafts with different patterns
- Events with different dates

[Checkout How to Add Products with Single Option →]({{< ref "product-configuration" >}})

[Checkout Demo Boutique Store →](https://chopin.apiobuild.com/google-oauth2%7C106308532747537725517/74c00629-b2a7-4e52-b58a-c35deefa8adf)

{{< alert icon="💡" text="Store layout for single option and multi options look a little different. We suggest you organize all multi option products together." >}}

To configure multi option products, simply add the following columns to the catalog google sheet:

- option:name
- option:size
- option:flavor
- option:color

## Supported Option Display

There are 3 multi option display styles and you can configure up to 2:

|             | `option:size`                                                | `option:flavor` | `option:color`  |
| ----------- | ------------------------------------------------------------ | --------------- | --------------- |
| Appearance  | Rectanglur Boxes                                             | Drop-Down Menu  | Color Circles   |
| Field Value | Custom Text                                                  | Custom Text     | HTML Color Name |
|             | {{< img src="option-size.png" >}} | {{< img src="option-flavor.png" >}} | {{< img src="option-color.png" >}} |

### option:size

This field doesn't have to be **sizes** (S, M, L or 5.5, 6, 6.5), it can also be different **styles**. The text you put in to the cell will appear below the product image in the **squared box**.

`option:size` can be in any languages other than English, but cannot contain spaces. Dashes (-) is fine.

### option:flavor

Same as above, this field doesn't have to be **flavors**. The text you put in to the cell will appear below the product image as **drop-down menu**.

`option:flavor` can be in anylanguages other than English, but cannot contain spaces. Dashes (-) is fine.

### option:color

There are two ways to indicate your product color, which will apprear in **circle**.

1. Color Name: Just enter a color (i.e. red, blue, black, etc.). You can refer to [this list](https://htmlcolorcodes.com/color-names/) to find names for specific colors (i.e. lightskyblue, olive, and more).

2. Hex Code: Enter the 6-digit code with # sign. For example, #556B2F for olive.

## Group Products Together

You also need to update `option:name` column to indicate which products belong to the same group.

### option:name

Group the same products together by setting the same value in `option:name`. For example, a dress comes with two colors - white and yellow. The `option:name` fields for these two rows have to be the same, which are `dress`, so the app can identify these *two products* are actually *two options of the same product*.

{{< alert icon="⚠️" text="Remember to follow the same rule of name field - unique name/id contains only dashes, underscores, and alphanumeric. No space is allowed." >}}

## An Example

{{< img src="coat.png" >}}

Let's say you are selling a wool coat that comes with two *colors* (pink, blue) and three *sizes* (S, M, L) for each color. We will need to create 6 rows of products (2 * 3 = 6):

- Pink Coat in S size
- Pink Coat in M size
- Pink Coat in L size
- Blue Coat in S size
- Blue Coat in M size
- Blue Coat in L size

### name

{{< alert icon="⚠️" text="name has to be unique, no two products can share the same name." >}}

All these products should have a unique `name` a.k.a product id, so we will use the naming pattern: `coat-<color>-<size>`. You can also use sku numbers.

{{< img src="step-1-name.png" >}}

### nickname

We'd like the product title changes to the coresponding color when customer taps different color options. We are using "Wool Coat Pink" in the `nickname` field for all sizes of pink coats, and "Wool Coat Blue" for all sizes of blue coats.

{{< img src="step-2-nickname.png" >}}

### option:size

There are three sizes available for each color, so we are adding "S, M, L" for the `option:size` field of both pink and blue coats.

{{< img src="step-3-size.png" >}}

### option:color

{{< alert icon="💡" text="Color Name List →" ext-href="https://htmlcolorcodes.com/color-names/" >}}

We'll put "blue" in the `option:color` fields for all blue coats and "pink" for all pink coats.

{{< img src="step-4-color.png" >}}

### option:name

In order to group these six product as they are actually one product with six options. We'll put "coat" in the `option:name` field six rows.

{{< img src="step-5-name.png" >}}

Now you can see different style and sizing for this wool coat on the store!

{{< img src="coat-example.png" >}}

## Summary

With Chopin, it's really easy to manage thousands products in google sheet. You might need to add product variants in bulk or duplicate it from exiting variants. You don't need to follow complex instructions, just copy and paste the data in your desired way! Try Chopin today and you will be amazed by how easy it is!

Happy Adding More Products! 💰
