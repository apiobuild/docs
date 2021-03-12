---
title: "Waitress"
description: "Waitress provides simple CRUD interface for Google Sheets. It wraps complex Google API authorization and  Google Sheets read/insert APIs into apio platform's email based tokens and conventional CRUD method endpoint."
lead: "Waitress provides simple CRUD interface for Google Sheets. It wraps complex Google API authorization and  Google Sheets read/insert APIs into apio platform's email based tokens and conventional CRUD method endpoint."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "apps"
weight: 300
toc: true
---

{{< alert icon="💡" text="<a href='https://en.wikipedia.org/wiki/Create,_read,_update_and_delete' target='_blank'>Learn more about CRUD →</a>" >}}

[Waitress by apio](https://telescope.apiobuild.com/app/waitress) is a Google Sheets API wrapper. It simplifies Google Sheets API into simple CRUD methods.

## Use Case

### Collect Email Signup

As you can see on [apiobuild.com](https://apiobuild.com/#sign-up), we've also leveraged Waitress as a way to collect emails.

<!-- TODO: add live example -->
<!-- TODO: add goldfish ref -->

We've also integrated this functionality with [Goldfish (One Page Website Creator)](https://telescope.apiobuild.com/app/goldfish) to allow Goldfish users to collect emails to google sheets on their one page website.

### Send Batch Personalized Email

<!-- TODO: post-it ref -->

At apio, we've also leveraged Waitress with [Post-it](https://telescope.apiobuild.com/app/post-it) to send personalized emails to our customers for service updates.

### Backend API Database

We've used Waitress to replace lightweight database for backend services with Waitress API. The app tiles on [Telescope](https://telescope.apiobuild.com/) is actually served from a Google Sheets through Waitress.

Another great example is Waitress's integration with Chopin. Chopin store can read and update catalog and shopper's order from/to Google Sheets in realtime via Waitress.

This has save us from a lot of deployment headache and database infrastructure costs when prototyping new web app.

{{< alert icon="💡" text="<a href='https://developers.google.com/apps-script/guides/sheets' target='_blank'>Learn more about App Script →</a>" >}}

One of the very powerful usage we've discovered overtime is the ability to combine App Script along with other Google Sheets' built-in functions to mock complex API behavior that could sometimes takes weeks if not months to implement even for developers.

{{< alert icon="💡" text="<a href='/docs/apps/chopin/introduction/#manage-inventory'>Read more Chopin's Inventory Management →</a>" >}}

A great example is that we have helped our Chopin users to setup complex rules and functions to manage inventory. This type of backend customizations will usually takes months of development time. Both App Script and Google Sheets' built-in function have made experimenting with different business rules a lot quicker and easier.

## Summary

Thought of more use cases but not sure how to implement? [Drop us a message →](/docs/introduction/introduction/#contact-us).
