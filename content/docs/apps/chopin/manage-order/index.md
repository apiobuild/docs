---
title: "Manage Order"
description: "All transaction records will show on your Order Google Sheet. This page will show you how to understand your order data. You can easily view, organize, and analyze your data within Google Sheets."
lead: "All transaction records will show on your Order Google Sheet. This page will show you how to understand your order data. You can easily view, organize, and analyze your data within Google Sheets."
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

## Order Google Sheet

When creating your Chopin store, you already copied the title row to you Order Google Sheet. If we roll out new features or you add new custom fields, the new columns will be created automatically.

Feel free to change the order and move columns around. You can even hide the columns you don't want to see. However, the **`order_number` cell should always be on A1**.

{{< alert icon="💡" text="See more FAQs about Order Sheet →" rel-href="/docs/apps/chopin/troubleshoot/#order-google-sheet">}}

### A successful order

Each order consists of multiple rows:

- 1st row: The first row includes everything but the [product details](#product-details).
- 2nd ~ Nth rows: The next few rows display only the [purchased product(s) details](#product-details). 
  - Each product gets its own row. 
  - N = How many unique products your customers buy.
- (N+1)th row: When there're additional [events](#event-type) happened (i.e. payment method changed, credit card failed), you will see additional rows posted with only [payment details](#payment-details).

The `order_number` and `order_number_short` will appear on all the rows that belong to the same order.

{{< img src="gs-order.png" >}}

{{< alert icon="💡" text="You can sort the entire order sheet if you find the rows are not aligned →" rel-href="/docs/apps/chopin/troubleshoot/#how-to-sort-my-orders">}}

### Basic Order Information

- order_number: A unique order number for your reference, as sometimes the short order number can be duplicated.
- **order_number_short**: A 8-digit shorter order number that shows up on order confirmation page and emails.
- order_created: When the order is placed in customer's *local time*.
- order_created_tz: The customer's *local timezone*.
- **order_created_sys**: When the order is placed in *UTC (Coordinated Universal Time)*.
- store_id: The store id where the order is placed. You can use same order sheet for multiple Chopin stores.

{{< alert icon="💡" text="For first come first served orders, use `order_created_sys` for the most accurate result, as it doesn't affected by customer's local timezone or language settings." >}}

### Customer Details

- user_name: Customer's name.
- user_email: Customer's email.
- user_phone: Customer's phone number.
- user_address: Custome's shipping address.

{{< alert icon="💡" text="See how to make these fields mandatory →" rel-href="/docs/apps/chopin/order-settings/#user-input-fields" >}}

### Order Details

- order_subtotal: Order subtotal that doesn't include shipping costs and discounts.
- order_shipping_option: [Shipping option](/docs/apps/chopin/order-settings/#shipping) selected by customer.
- order_shipping: [Shipping cost](/docs/apps/chopin/order-settings/#shipping) applied to the order.
- order_tax_rate: [Tax rate](/docs/apps/chopin/order-settings/#tax) applied to the order.
- order_tax: Tax amount.
- **order_total**: Order total that your customer should pay.

### Product Details

- product_name: [Product name (id)](/docs/apps/chopin/product-configuration/#name-required) of the purchased product.
- **product_nickname**: [Product nickname (display name)](/docs/apps/chopin/product-configuration/#nickname) of the purchased product.
- product_qty: Quantity of the purchased product.
- product_price: [Unit price](/docs/apps/chopin/product-configuration/#price-required) of the purchased products.

### Payment Details

- **payment_method**: [Payment method](https://apiobuild.com/docs/docs/apps/chopin/payments/) used for the order.
- event_created: When the event is created in UTC time.
- order_created_sys: When the order is created in UTC time.
- order_discount: [Discount amount](/docs/apps/chopin/order-settings/#discount) applied to the order.
- **event_type**: [Event](#event-type) indicates different stages of the order, i.e. order_submitted, payment_submitted, etc.
- event_description: Detailed description of the event.
- payment_tracking_id: Stripe payment id that you can cross-refer in your Stripe account.
- error: Error message for why the Stripe transaction failed. i.e. wrong cvc code, rejected card, etc.

### Custom Fields

If you collect additional information by setting up the [custom user input](/docs/apps/chopin/order-settings/#user-input-fields), you will see additional columns pops up automatically.

## Event Type

Below is a lists of event types you'll see on your Order Google Sheet. You can also find explanation in `event_description` column next to `event type`.

- **order_submitted**: Customer submitted the order but payment has not yet submitted.
- payment_method_updated: Customer has updated their payment method.

{{< alert icon="💡" text="If you only enable offline payments, `order_submitted` event is all you need to fulfill the order. Be sure to verify payments with your selected payment method." >}}

- **payment_submitted**: Customer submitted the order and online payment successfully. This event only applies if you enable Stripe payments.

{{< alert icon="💡" text="If you enable Stripe payments, you need to see both `order_submitted` and `payment_submitted` events to fulfill the order." >}}

- payment_failed: Stripe can't process this payment. Check what went wrong in [error](#payment-details) column.
- require_action: Customer submitted the order but requires further action to verify payment (only applicable to credit cards that require [3-D secure](https://en.wikipedia.org/wiki/3-D_Secure), mostly for EU users).