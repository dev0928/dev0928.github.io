---
title: "Cloud-native Development Principles"
date: 2023-01-17T13:41:54-05:00
slug: cloud-native-dev-principles
tags: ["Cloud native", "Principles"]
toc: true
draft: true
---

## What are cloud-native development principles?

The engineers working at the Heroku platform have compiled a set of ideal practices for web application development to raise awareness of some of the systemic problems and propose solutions to these problems. These principles are commonly known as [The Twelve-Factor App](https://12factor.net/ "The twelve-factor app").

Later, Kevin Hoffman’s **Beyond the Twelve-Factor Application** book refreshed the original principles and came up with a revised order along with a few newer priniciples to suit modern cloud-native application needs. 

This write-up provides a summary of these development principles based on Kevin Hoffman’s book.

### 1. One codebase, one application

Cloud-native applications must consist of a single codebase tracked in the version control system. If the application has any shared code, it must be maintained as a separate codebase so it can be shared as a library or a service. The same build artifact should be used to deploy in multiple environments (dev, test, QA, and prod) without requiring any explicit changes in the build.   

### 2. API first

API-first principle recommends that individual services within the cloud-native application should provide API contracts up front so other consuming services could readily use these contracts for integrating with the service. Although implementation details of the individual services could change, the published API contract should remain unaffected by the implementation detail changes.

### 3. Dependency management

Cloud-native applications should be self-reliant in terms of all dependencies needed by the application. These dependencies should be explicitly declared and made available from a central location. 

### 4. Design, build, release, and run

Build artifacts created through the build process should be immutable across different environments and should be labeled with a release tag for future reference. Configuration changes across environments should be injected separately so the build artifact remains unaffected by the tier-specific differences.   

### 5. Configuration, credentials, and code

Environment-specific configuration should be kept separately from the codebase so it is not part of the build artifact. Another recommended approach is to use an external configuration that supports version control.

### 6. Logs

Cloud-native applications should provide application logs in the form of a standard output stream but should not be concerned with the maintenance and storage of application logs. 

### 7. Disposability

A cloud-native application's life is ephemeral meaning the number of instances of the application could change depending on the application load. This means cloud-native applications should start and terminate quickly so they can be easily disposable. 

### 8. Backing services

Backing services should be treated as external resources and these services should be made available through configuration. The configuration provides the ability to attach and detach backing services from an application at will, without the need for redeployment of the the application when there are backing service changes. 

### 9. Environment parity

The differences in setup between environments should be kept minimal so there are no issues like solutions working in some environments but not others. These differences could be categorized in three main categories, namely when the services are deployed, who is in-charge of the deployment, and what backing services are used in various environments.

### 10. Administrative processes

Applications usually have administrative tasks such as batch jobs or other maintenance tasks. These tasks should be treated like any other application process and tracked in version control. Also, these tasks should be decoupled from the normal application process so they can be run as one-off jobs on an as-needed basis.   

### 11. Port binding

Application services need to communicate with one another in a cloud-native environment. The cloud-native services should be communicating with each other by their service names and not rely on the actual port the service is listening on for inter-service communication.

### 12. Stateless processes

As scalability is one of the main goals for cloud-native applications, applications' services should be stateless to achieve scalability. State maintenance should be off-loaded to data services. Also, session state and cache management should be externalized from the application processes so applications' services could remain stateless. 

### 13. Concurrency

Multiple instances of application could be deployed to achieve scalability. Scalability can also be achieved when application processes support more than one request at the same time. Some JVM-based servers provide concurrency through threads.   

### 14. Telemetry

Telemetry is making logs, metrics, and health status of individual services readily available for analysis and troubleshooting.

### 15. Authentication and authorization

Authentication is the process of who can access the system and authorization is the process of limiting what they can access. Cloud-native applications should follow a zero-trust approach for security. This means all inter-service communications must be authenticated and authorized. 
