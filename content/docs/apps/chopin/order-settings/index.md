---
title: "Order Settings"
description: "Chopin comes with many custom order total calculation and validation settings. Merchants can take advantage of these options to customize order total calculation. We recommend using these rules whenever possible. In general, communicating these rules over descriptions is not only ineffective, it also causes unnecessary confusion to the shoppers (your customers)."
lead: "Chopin comes with many custom order total calculation and validation settings. Merchants can take advantage of these options to customize order total calculation. We recommend using these rules whenever possible. In general, communicating these rules over descriptions is not only ineffective, it also causes unnecessary confusion to the shoppers (your customers)."
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

Don't see a customization that fits your need? [Drop us a message →]({{<ref "/docs/introduction/introduction/index.md#contact-us" >}})

## Order Settings

### User Input Fields

Determine what information you'd like to collect at checkout page.

By default, we only require customers to input in their email. You can check `Hide` box to eliminate certain fields or check `Require` box to make certain fields mandatory.

- Name
- Email
- Phone Number
- Address
- Note

{{< img src="c_order_1_21.png" >}}

{{< alert icon="💡" text="We recommend using note field to collect customization details (i.e. message to be put on the cake) as opposed a way to communicate about the order with your customers." >}}

You can also add customized fields, like dietary restriction, special request, etc.

{{< img src="custom_field.png" >}}

### Order Confirmation

[How to configure order confirmation Emails →]({{< ref "email-confirmation" >}})

## Contact Information

[How to add contact and social media information →]({{< ref "contact-information" >}})

## Payment Methods

[How to configure payment methods →]({{< ref "payments" >}})

## Shipping

### Shipping Option

Setup multiple options and the coresponding shipping cost. This will appear as a dropdown menu. 

You can also use this section to show pick-up dates/locations.

### Free Shipping

Set a qualifying order total for free shipping.

### Delivery Zipcode

We can validate customers' addresses based on a list or lists of zipcodes provided, so you don't have to worry out-of-zone delivery. Use commas (,) to separate zipcodes.

{{< img src="f_shipping.png" >}}

## Discount

{{< img src="g_discount.png" >}}

### Discount Type

Choose from the dropdown menu and set up a `dollar` value discount or a `percent` discount.

### Discount Category

If you wish to apply discount to only specified category, put the desired [category name](/docs/apps/chopin/product-configuration/#category) here.

### Discount Threshold

Enter a qualifying order (category) total for discount.

### Dollar Off

Dollar value to be taken off from order total for qualified order (category) total. Only enter this for dollar discount type.

### Percent Off

Percent of order total to be taken off from order total for qualified order (category) total. Only enter this for percent discount type.

## Tax

Use this field to customize the tax rate in your area. For example, sales tax for New York state is 8.875%, then you enter 8.875 in this field.

If you don't set a value, the default tax rate is 0.

{{< alert icon="💡" text="Remove tax for selected products →" rel-href="/docs/apps/chopin/product-configuration/#no_tax" >}}
