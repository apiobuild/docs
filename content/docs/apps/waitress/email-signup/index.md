---
title: "Create Email Signup Form"
description: "Want to collect emails or short forms on your website but don't want to setup a backend. Don't like the embedded google form layout but only the functionality? In this post will walk through how to create a email signup or any forms with the Waitress app in three easy steps."
lead: "Want to collect emails or short forms on your website but don't want to setup a backend. Don't like the embedded google form layout but only the functionality? In this post will walk through how to create a email signup or any forms with the Waitress app in three easy steps."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "waitress"
weight: 320
toc: true
---

Navigate to [Waitress App on Telescope](https://telescope.apiobuild.com/app/waitress) to start.

## 1. Create New Google Sheet

[Create a new google sheets →](https://docs.google.com/spreadsheets/create)

You don't need to create a new one if you wish to use an existing one. Just go to the one you wish to use and follow the instruction on Telescope:

{{< alert icon="💡" text="Pop-up blocker could disable the login window. Allow or disable pop-up blocker if you are not able to sign-in." >}}

1. Click Share on the top right of the google sheet
2. Share to `waitress-dev@apio-277201.iam.gserviceaccount.com` as an Editor
3. Copy the google sheet to the console and click the 🔓 icon to authorize us to access your google sheets.
  {{< img src="waitress-app-instruction.png" >}}
4. Copy the API url with you, we will need it in the next step.
  {{< img src="copy-waitress-route.png" >}}

## 2. Create Auth Token

<!-- trampoline auth ref -->
<!-- trampoline token -->

In order to use apio's platform services outside of Telescope, we require general users to create apio's platform auth token. To create a token:

{{< alert icon="💡" text="Pop-up blocker could disable the login window. Allow or disable pop-up blocker if you are not able to sign-in." >}}

If you are not signed in yet, click on the Sign In icon on the top left corner on Telescope:

{{< img src="telescope-sign-in.png" >}}

## 3. Add HTML Form
