---
title: "Architecture"
description: "Our platform is built with microservice and serverless first architecture. We stride for lean and componentized applications. It's our goal to build affordable and customizable software for the world and beyond."
lead: "Our platform is built with microservice and serverless first architecture. We stride for lean and componentized applications. It's our goal to build affordable and customizable software for the world and beyond."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "introduction"
weight: 30
toc: true
---

## Serverless

[Serverless computing](https://en.wikipedia.org/wiki/Serverless_computing) is core to our design pattern. Applications on our platform are designed to be "stateless" where database can be easily scaled or replaced as needed. This has also allowed us to keep the platform cost low for customers with less need on performance.

## Microservice

[Microservice](https://en.wikipedia.org/wiki/Microservices) is debatable term. In software architecture, it commonly implies the applications are organized around specific functionality and loosely coupled. In order to keep our services flexible and easily extendable, each application on our platform supports specific functionality.

## API

[API](https://en.wikipedia.org/wiki/API) describes the mechanism how software applications communicate with each other. Any "communication" point of the applications on our platform is designed to be easily swappable with either internal or external APIs.
