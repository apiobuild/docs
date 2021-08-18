---
title: "Analyze Order"
description: "You can utilize functions and formulas within Google Sheets to help you organize and analyze your order data."
lead: "You can utilize functions and formulas within Google Sheets to help you organize and analyze your order data."
date: 2021-08-018T08:48:57+00:00
lastmod: 2021-08-18T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "chopin"
weight: 300
toc: true
---

## Basic Tricks

Here are some basic configurations to help you be more organized. Powered by Google Sheets and provided with raw data, Chopin gives you more flexibilities to analyze your order data.

{{< alert icon="💡" text="You can find more formulas, functions, and formatting options in Google's official  docs →" ext-href="https://support.google.com/docs/topic/9054603" >}}

### Notification

Set up Google Sheets notification rule to get realtime updates on new order submission. Depending on how you'd like to be notified, you could get an email everytime someone places an order or get a summary email at the end of the day.

1. On the top of your Order Google Sheet, click `Tools` > `Notification Rules`.
2. Select `Any changes are made` under "Notify me when…"
3. Choose "when" you want to receive notifications under "Notify me with…"
   - `Email - daily digest` - Send a daily summary of all changes.
   - `Email - right away` - Send an email for every change.
4. Click `Save`.

{{< img src="gs-notification.png" >}}

### Text Wrapping

Sometimes the data in cells will go over the boarder and mix up with the data in neighboring cells. To precent you from misreading data, you can click `text wrapping` from the top panel, and then apply `clip` or `wrap` to entire sheet.

{{< img src="gs-textwrapping.png" >}}

### Hide

Feel free to hide any **columns** you don't need (except `order_number`). For example, if you don't collect shipping address at all, you could hide the `user_address` column.

1. Select the entire column(s) that you don't need to see.
2. Right click, and select `Hide column`.

You can also hide **rows** of fulfilled orders.

1. Select the row(s) that you don't need to see.
2. Right click, and select `Hide row`.

{{< alert icon="⚠️" text="Remember that he 'order_number' cell should always on A1 and cannot be hidden. Do not hide the entire header row." >}}

### Freeze Column

Freezing columns/rows means to lock them at its place, so they remain visible while scrolling through the Google Sheets. This trick helps you easily refer data back to the header or specific columns.

Freeze **title row** so you don't have to scroll to the top all the time:

1. On the top of your Order Google Sheet, click `View` > `Freeze`.
2. Select `1 row`.

Freeze **order number** so you don't lose track:

1. On the top of your Order Google Sheet, click `View` > `Freeze`.
2. Select `2 columns`.

You can customize how you'd like to lock your data:

1. On the second row, click on the last cell you'd like to see.
2. On the top of your Order Google Sheet, click `View` > `Freeze`.
3. Select `Up to current columns`.

{{< alert icon="💡" text="Read more about freeze rows & columns on Google Support →" ext-href="https://support.google.com/docs/answer/9060449" >}}

### Color Coding

Having the data automatically color code with the **conditional formatting** rule will help you spot crucial information right away. Cells will be formatted to change text/background color if they meet certain conditions.

1. Select the entire columns you want to apply format rules to.
2. Click `Format` and then `Conditional formatting`. A toolbar will open to the right.
3. Create a rule on `Single color` tab:
   - Under "Format cells if," choose the condition that you want to trigger the rule.
   - Under "Formatting style, choose what the cell will look like when conditions are met.
4. Click Done.

You can be really creative and set up multiple conditional formatting to fit your needs!

{{< alert icon="💡" text="Read more about conditional formatting on Google Support →" ext-href="https://support.google.com/docs/answer/78413" >}}

#### Example

1. If you'd like to see failed transactions, you could set up conditional formatting for the `event_type` column and make a rule that highlight cells if *text contains* "failed."

{{< img src="gs-conformat-1.png" >}}

2. If you want to see different shipping options in different colors, you could set up conditional formatting for the `order_shipping_option` column and make a rule for each options that change cell background if it text is exactly certain shipping options.

{{< img src="gs-conformat-2.png" >}}

### Pivot Table

Pivot table is one of the most powerful and useful feature in Google Sheets that can summarize your data. You can easily see the quantity sold of each product or who orders whatat a glance.

1. Select the cells with source data you want to use. Important: You must include the header row.
2. In the menu at the top, click `Data` and then `Pivot table`. Select `Insert to new sheet`.
3. Click the pivot table sheet tab, if it’s not already open.
4. In the side panel, next to `Rows`, `Columns`, or `Values`, click `Add`, then choose a value. You can change how your data is listed, sorted, or summarized.
5. You can then further organize your data:
   - Add values to `Filters` to filter what you'd like to see
   - Group certain data by selecting, right click, then `Create pivot group`
   - Rename headers on the pivot table sheet

{{< alert icon="💡" text="Read more about creating pivot table on Google Support →" ext-href="https://support.google.com/docs/answer/1272900" >}}

#### Example

To run analysis for this [dessert store](https://chopin.apiobuild.com/demo-store):

1. You'd probably want to know the **quantity sold of each products** before baking, so you could create a pivot table with the following set-up:

   - Rows: `product_name` (sort by `COUNTA of product_qty`); `product_nickname`
   - Columns: *empty*
   - Values: `product_qty` (summarized by `COUNTA`)
  
   With this table, you can clearly see you need to prepare 12 apple pies, 9 fruit sandwiches, 8 boba teas, etc.

   {{< img src="gs-pivottable-1.png" >}}

2. Then, you'd like to see **who orders what** to be able to pack their purchase together.

   **There's one additional step for all the analysis involving customers.** Since the customer information only appears on the first row and not on the rows with purchased products. You need to fill the customer information to all the rows by:

   - Create a new column, called `user_name_filled` and input function `=IF(ISBLANK(C2),D1, C2)`
      - C = the column of `user_name`
      - D = the newly created column of `user_name_filled`
   - Then apply this function to all the cells within that column

   {{< img src="gs-pivottable-2a.png" >}}

   You could create a new pivot table with the following set-up:

   - Rows: `user_name_filled`; `product_nickname`
   - Columns: *empty*
   - Values: `product_qty` (summarized by `COUNTA`)

   With this table, you can see everyone's order at once: For instance, Alex ordered 3 items total including 1 apple pie, 1 chocolate cake, and 1 mille feuille, etc.

   {{< img src="gs-pivottable-2.png" >}}

{{< alert icon="💡" text="You can use the ISBLANK function to fill the entry of other cells too, i.e. user_email, then add those variables to your pivot table Rows for viewing.">}}

1. The pivot table is dynamic, which means it'll change according to our data in real time. You could **filter out the orders that you've fulfilled**.**

   First, to add a new column on the order sheet called, `fulfilled`. Let's pretend you finished baking for Bella's and Victor's orders. You'd put `x` in all of the coresponding cells in the `fulfilled` column.

   {{< img src="gs-pivottable-3a.png" >}}

   Then you adjust the previous pivot table by adding a filter:
   - Filters: `Fulfilled` (showing `(Blanks)`)

   Now, you wouldn't see Bella's and Victor's orders in this pivot table anymore. The table only shows the orders that you still need to fulfill.

   {{< img src="gs-pivottable-3.png" >}}

The above scenarios should cover most of the use cases when it comes to getting order ready to fulfill. There're many ways to organize and analyze your orders. Try different variable combinations, and you might discover interesting trends. 

Feel free to [contact us]({{< ref "/docs/introduction/introduction/index.md#contact-us" >}}) if you have trouble getting the report you'd like to see.
