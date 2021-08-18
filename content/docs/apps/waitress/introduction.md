---
title: "What's Waitress"
description: "Waitress provides simple CRUD (create, read, update, delete) interface on Google Sheets API. It wraps complex Google API authorization and  Google Sheets read/insert APIs into apio platform's email based tokens and conventional CRUD method endpoint."
lead: "Waitress provides simple CRUD (create, read, update, delete) interface on Google Sheets API. It wraps complex Google API authorization and  Google Sheets read/insert APIs into apio platform's email based tokens and conventional CRUD method endpoint."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "waitress"
weight: 310
toc: true
---

{{< alert icon="💡" text="Learn more about CRUD →" ext-href="https://en.wikipedia.org/wiki/Create,_read,_update_and_delete" >}}

[Waitress by apio](https://telescope.apiobuild.com/app/waitress) allows users to quickly prototype complex APIs and use Google Sheets as a lightweight (and FREE) document store for your applications.

## Use Case

### Collect Email Signup

On [apiobuild.com](https://apiobuild.com/#sign-up), we've also leveraged Waitress as a way to collect emails.

<!-- TODO: add live example -->
<!-- TODO: add goldfish ref -->

The functionality is integrated directly on [Goldfish (One Page Website Creator)](https://telescope.apiobuild.com/app/goldfish) to allow Goldfish users to collect emails to google sheets on their one page websites.

<!-- TODO: read more how to use on your own domain -->

### Send Batch Personalized Email

<!-- TODO: post-it ref -->
<!-- TODO: how to create your own -->

At apio, we use Waitress with [Post-it](https://telescope.apiobuild.com/app/post-it) to send personalized emails to our customers for service updates.

### Backend API Database

Waitress can also replace lightweight document store for backend and frontend applications.

For example, the app tiles on [Telescope](https://telescope.apiobuild.com/) is actually served from a Google Sheets through Waitress.

Another great example is Waitress's integration with Chopin. Chopin store can read and update catalog and shopper's order from/to Google Sheets in realtime via Waitress.

This has save us from a lot of deployment headache and database infrastructure costs when prototyping new web app.

{{< alert icon="💡" text="Learn more about App Script →" ext-href="https://developers.google.com/apps-script/guides/sheets" >}}

One of the very powerful usage we've discovered overtime is the ability to combine App Script along with other Google Sheets' built-in functions to mock complex API behavior that could sometimes takes weeks if not months to implement even for developers.

{{< alert icon="💡" text="Read more about Chopin's Inventory Management →" rel-href="/docs/apps/chopin/introduction/#manage-inventory" >}}

A great example is that we have helped our Chopin users to setup complex rules and functions to manage inventory. This type of backend customizations will usually takes months of development time. Both App Script and Google Sheets' built-in function have made experimenting with different business rules a lot quicker and easier.

## Summary

Thought of more use cases but not sure how to use it? [Drop us a message →]({{< ref "/docs/introduction/introduction/index.md#contact-us" >}}).
