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

Don't see a customization that fits your need? [Drop us a message →](/docs/introduction/introduction/#contact-us)

## Order Settings

### Currency `NEW`

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

## Shipping

### Shipping Option

Setup multiple options and the coresponding shipping cost. This will appear as a dropdown menu. You can also use this section to show pick-up dates/locations.

### Free Shipping

Set a qualifying order total for free shipping.

### Delivery Zipcode

{{< alert icon="⚠️" text="We currently only support US zipcodes." >}}

We can validate customers' addresses based on a list or lists of zipcodes provided, so you don't have to worry out-of-zone delivery. Use commas (,) to separate zipcodes.

{{< img src="f_shipping.png" >}}

## Discount

{{< img src="g_discount.png" >}}

### Discount Type

Set up a dollar value discount or a percent discount.

### Discount Category

Apply discount to only specified category.

### Discount Threshold

Enter a qualifying order (category) total for discount.

### Dollar Off

Dollar value to be taken off from order total for qualified order (category) total. Enter this for dollor discount type.

### Percent Off

Percent of order total to be taken off from order total for qualified order (category) total. Enter this for percent discount type.

## Tax

{{< alert icon="💡" text="<a href='/docs/apps/chopin/product-configuration/#no_tax'>How to remove tax for certain products →</a>" >}}

Use this field to customize the tax rate in your area.
