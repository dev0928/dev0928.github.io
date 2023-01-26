---
title: "Introduction to Cloud-native"
date: 2023-01-16T11:28:57-05:00
slug: cloud-native
tags: ["Cloud-native"]
toc: true
draft: true
---

## What is cloud-native?

Cloud-native applications are highly distributed systems that are **scalable**, **resilient**, **loosely coupled**, **manageable**, and are deployed in the cloud. Cloud-native applications are typically segregated into several services for ease of deployment and maintainability. They leverage the advantages of cloud computing models. 

Here is a definition of cloud-native from Cloud Native Computing Foundation’s (CNCF):

> Cloud native technologies empower organizations to build and run scalable applications in modern, dynamic environments such as public, private, and hybrid clouds. Containers, service meshes, microservices, immutable infrastructure, and declarative APIs exemplify this approach.

### Cloud-native application properties

According to CNCF, cloud-native applications should exhibit below five properties:

{{< figure src="/images/001-01-cloud-native-properities.png" title="Cloud-native properties" >}}
 
#### Scalability
 
Individual systems in cloud-native applications should be highly scalable to meet the demands of the business. Systems should especially support horizontal scalability. As cloud workloads can increase/decrease dynamically, cloud-native applications should take advantage of this feature and be configurable to leverage horizontal scalability.
 
#### Loosely coupled
 
Individual services within a solution should have minimal knowledge about other services. The goal of loose coupling is the ability of the systems within the solution to evolve independently so that other consuming systems are unaffected by the changes. 
 
#### Resilient
 
Failures in individual services of cloud-native applications should be quickly recoverable. Systems should have the capability to maintain a certain level of service in case of adversities.
 
#### Manageability
 
Cloud-native systems should have better control over configuration management and should follow best practices around deployment by using CI/CD automation. Changes made through configuration should not require the redeployment of services for the changes to take effect.  
 
#### Observability  
 
As debugging distributed systems is complex, cloud-native systems should be designed as observable from the ground-up. A system is said to be observable if the internal state of the system is available from outside in the form of traceable logs and metrics to help with analysis and troubleshooting. In other words, a production system is said to be observable if the internal system states are readily available without having to make arbitrary guesses, predict those failure modes in advance, or ship new code to understand that state.  
   
### Why cloud-native?  
 
Many applications start as monoliths as they are simpler to design when compared to distributed systems. But when these applications add more features over time, they result in below listed disadvantages:
 
*Disadvantages of monoliths:*
- Too many developers work on a complex codebase
- Continuous integration becomes relatively difficult
- It takes longer to deploy changes to the production environment due to change coordination
- Teams have less control over the codebase as it is relatively complex
- Components within a monolith are tightly coupled thereby becoming harder to change
- High chance of breaking changes introduced during deployment due to larger deployments
 
*Advantages of cloud-native applications:*
- Smaller teams
- Simpler and easier to understand the codebase
- Faster/frequent/independent deployment of services
- Individually scalable services

### Benefits of cloud-native

Here are some of the benefits of going, cloud-native:

#### Speed

Cloud-native applications that follow best practices such as CI/CD for deployments typically have faster turnaround time in delivering features thereby increasing the business value with a reduced time-to-market.

#### Scalability

If set up correctly, cloud-native applications can scale up and down in seconds through automated configuration to suit the varying demands of the business. 

#### Resilience

Cloud-native applications can be set up to recover from failures and thereby increasing the availability of the system. With several distributed services, system failures are not completely unavoidable. But cloud native systems can be set up in a way that they are self-healing and provide some level of service at least in a degraded manner when there are issues.  

#### Cost

One of the major benefits of utilizing the cloud for deploying applications is the ability to pay for resources using an on-demand pay-per-use model. Therefore, there is no longer a need for companies to make a huge capital expenditure in setting up and maintaining the infrastructure with the cloud model. 
 
### Cloud-native practices

Cloud-native applications also support several best practices around the way the applications are built. They typically follow continuous integration/delivery/deployments (CI/CD) with automated pipelines. They also follow effective DevOps strategies with automated infrastructure provisioning across various environments.  

### Conclusion

If the above-discussed aspects are considered while building a new solution, modern businesses can reap the benefits of the cloud-native approach.

