---
title: "Continuous Delivery Vs. Continuous Deployment"
date: 2023-01-18T13:41:54-05:00
slug: continuous-delivery-deployment
toc: true
tags: ["DevOps"]
draft: true
---

## What is the difference between continuous delivery and deployment?

This write-up clarifies the subtle difference between continuous delivery and continuous deployment. Let’s first review the meaning of continuous integration.

### Continuous integration

Continuous integration is a DevOps development practice where developers merge their code into a central version control branch for integration so that the automated pipeline process can compile and validate committed code by performing various scans and tests to create a build artifact.

### Continuous delivery

Continuous delivery is the automated pipeline process that produces releasable artifacts ready to be promoted to the production environment. The delivery pipeline could include various kinds of automated tests and deployment to lower-tier environments. With continuous delivery, releasable artifact gets deployed to production through a **manual approval** process.

### Continuous deployment

The continuous deployment process is similar to continuous delivery except the releasable artifact is automatically pushed to production at the end of the automated pipeline. 
