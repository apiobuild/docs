---
title: "Overview"
description: "apio is a low code business automation platform built for small businesses and entrepreneurs."
lead: "apio is a low code business automation platform built for small businesses and entrepreneurs."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "introduction"
weight: 10
toc: true
---

## Mission

At apio, we truly believe that no matter the size of the business, everyone should have access to high quality software tailored for business needs at affordable cost. Not every business can afford enterprise business software to offer streamlined customer experience; however, we pride ourselves in building easy-to-use yet flexible software that helps small business owner to provide best in class customers experience while keeping the warmth in the relationship.

## Platform Offering

{{< alert icon="💡" text="Learn more about APIs →" rel-href="/docs/introduction/architecture/#api" >}}

The platform is consisted of standalone microservices (also available as APIs) and platform UI to create and configure workflows.

### Telescope (Platform UI)

[Telescope (Platform UI)](https://telescope.apiobuild.com/) is available on desktop, tablet and mobile devices. It's the main interface to create and configure any microservices offered on our platform. Microservices can be configured in `app` tiles. Sometimes, an automation or service can be combination of multiple microservices, to simplify the experience, the `flow` tiles contain step by step instruction and configuration to create full service.

{{< img src="telescope-screenshot.png" >}}

### App

{{< alert icon="💡" text="Learn more about microservices →" rel-href="/docs/introduction/architecture/#microservice" >}}

An app is a standalone microservice with dedicated functionality. For example, **[Chopin App](https://telescope.apiobuild.com/app/chopin)** creates instant one page online store with pre-defined integrations to catalog and order services. **[Waitress App](https://telescope.apiobuild.com/app/waitress")** is a **Google Sheets** wrapper API to fetch and append data.

For technical users, each app is always available as API, API spec can be found in the **[DOCUMENTATION](https://telescope.apiobuild.com/app/chopin/swagger)** on the app page.

### Flow

A flow is a simplified step by step configuration to create a full service or an automation workflow leveraging one or more microservices. For example, the **[Chopin Stores Flow](https://telescope.apiobuild.com/flow/chopin-stores)** creates an one-page online store with google sheets and gmail integration, the flow creates and configures Chopin, Waitress and Post-it app resources.

<!-- ## Showcase

See what others have build with apio. [Showcase →](/showcase) -->

## Contact Us

We are always here to talk.

[Find a time to chat →](https://calendly.com/apiobuild)

[Contact customer support →](https://m.me/apiobuild)

<a href="mailto:apiobuild@gmail.com">Email us →</a>  

## Contribute

We are currently closed-source platform. However, we have ambitious plan to open-source our entire platform. <!-- [Signup here →](/developer-sign-up)-->
