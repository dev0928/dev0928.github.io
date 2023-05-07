---
title: "SDLC Stages"
date: 2023-05-07T11:07:59-04:00
draft: true
slug: sdlc-stages
toc: true
tags: ["SDLC"]
---

### Stages of SDLC

**Software Development Life Cycle (SDLC)** is a set of activities that typically are performed during the development of software.

This article highlights some of the critical activities and the best practices in each stage of the SDLC. The below diagram depicts the various stages of SDLC. 

{{< figure src="/images/008-01-sdlc-stages.png" title="Stages of SDLC" >}}

### Feasibility Analysis

The feasibility stage identifies whether the planned software development idea is financially worthwhile and technically feasible.

#### Key activities / Best practices

- Understand the problem
    1. Meet with the business stakeholders to get an overview of the business problem.
    1. Understand timeline requirements.
    1. Determine the target audience.
    1. Determine high-level objectives for the newly built software. 

- Finalize high-level approach
    1. Many organizations have shifted towards building their solutions using the cloud-native approach - Finalize the details around where and how the project would be built and hosted.
    1. Determine the best possible technology stack for the solution.
    1. Ensure the selected tech stack aligns with the organization’s broader technology landscape.
    1. Create PoCs to validate some of the critical aspects of the solution.

- Create project estimation 
    1. Determine the resources (project team) needed for building the solution.
    1. Determine the optimal timeline for the project.
    1. Perform a cost-benefit analysis and share it with the business stakeholders.

Feasibility analysis is the first and foremost stage of the SDLC. Project success depends on a deep understanding of the business problem which can be achieved by working closely with the business team. 

### Requirements Gathering

The requirements gathering and analysis stage tries to get an extensive understanding of the project by reviewing the functional and non-functional requirements at a deeper level.

#### Key activities / Best practices

- Determine functional requirements
    1. Gather requirements around high-level features of the project.
    1. Gather data requirements
    1. Identify the data sources for the project
    1. Develop an acceptable data synchronization strategy

- Identify non-functional requirements
    1. Gather requirements around scalability, portability, availability, security, and reliability.
    1. Also, gather the project’s performance requirements. 
    1. Collect details around localization, globalization, and device compatibility requirements.

### Design

The high-level architecture and the services/components get created during the design phase of the SDLC. At this stage, the UI / UX designer creates mockups for the UI components of the project. 

#### Key activities / Best practices

- Create solution architecture
    1. Review architecture with the project’s technical stakeholders.
    1. Describe various components of the solution.
    1. Devise the security strategy for individual components.
    1. Create a plan for inter-service communication.

- Create UI design
    1. Design mockups based on user requirements.
    1. Get buy-in on the UI / UX design.

- Create cloud-native development principles guidelines
    1. Ensure that the development team is aware of the 15-factor development principles for the successful delivery of the software.

While it is more expensive to change some of the design decisions at a later stage of the project, it is also desirable to keep some parts of the design more flexible to accommodate changing needs of the business. Hence, the design phase is also part of the Agile iteration cycle in the above diagram.  

### Planning

The planning phase of the SDLC is iterative in nature for the projects that follow Agile methodology. 

#### Key activities / Best practices

- Establish communication guidelines for the project team.
- Choose a suitable project management methodology.
- Choose the right set of project management tools and all project team members have access to the tool.
- Break down business requirements into epics, features and user stories.  
- Perform backlog grooming by working with the product owner.
- Conduct sprint planning
- Set up cadence for various meetings such as stand-ups and srpint reviews.
- Establish a Definition of Done (DoD) guidelines.

### Development

The goal of the development phase is to ensure that the current iteration’s user stories are completed following the DoD guidelines. Although the development and testing phases are two distinct phases in the above SDLC diagram, they typically are performed in parallel. In most projects, developers would also be writing automated unit and integration tests to ensure the modules under development are working as expected during the development phase. 

#### Key activities / Best practices

- Create version control to track changes (one codebase, one application)
- Establish good dependency management guidelines.
- Ensure that the built application is self-contained and does not rely on any software from its hosted environment. The use of containerization software such as Docker would eliminate the need.
- Follow the API-first approach.
- Establish testing guidelines and test coverage standards.   

### Testing

Testing is one of the critical phases of the SDLC. One of the key goals of the cloud-native approach is speed - delivering changes frequently and often. Test automation enables the ability to deliver features without introducing a regression. Automated tests help with regression errors during these changes.

#### Key activities / Best practices

- Establish standards around different types of necessary test coverage based on the project.
- Ensure automated tests run as part of the code check-in process.
- Set up expectations around test quality and build pipeline failures due to test failures. 

### Continuous Integration / Delivery (CI/CD)

CI / CD is an automated deployment pipeline process triggered every time a change is committed to the version control system. The deployment pipeline runs various validation steps containing vulnerability scans and automated tests. The build pipeline helps create releasable artifacts ready to be deployed to different environments as part of the continuous delivery pipeline. Automated pipelines ensure changes are validated reliably, quickly, and often.

Another automation approach that is particularly very important is infrastructure provisioning automation. Tools such as Terraform enable the provisioning of necessary cloud resources stably and reliably across tiers. 
 
#### Key activities / Best practices

- Provision infrastructure resources through an IaC tool.
- Maintain infrastructure provisioning details in the version control for reliable change management.
- Set up deployment pipelines for infrastructure change automation. 
- Build project CI / CD pipelines in the earlier stage of the project.

### UAT / Sprint Review

Getting continuous feedback at the end of every iteration (sprint) ensures that the business stakeholders review the incremental changes and provide valuable feedback regularly in the Agile development process. 

#### Key activities / Best practices

- Establish time commitment expectations with the business stakeholder team during the initial stage of the project.
- Ensure business and development teams are part of the sprint review sessions to initiate a valuable feedback loop. 

### Production Launch

Cloud-native applications built with the best practices described earlier would be ready for production launch through the already established automated delivery pipelines with a business approval process established as part of the automated pipeline.

However, ensure that the newly built application is observable before the application’s production launch. Observability is ensuring that the internal state of the systems is available from outside in the form of traceable logs and metrics. This will help with the maintenance of the application post-launch.

### Operation and Maintenance

In this phase of the SDLC, applications are monitored to ensure that they continue to function as expected. With the cloud-native approach, key maintenance activities such as hosted environment’s operating system patches could be handled by the cloud provider eliminating the need for specific project resources.  

#### Key activities / Best practices

- Fix bugs discovered after the launch.
- Upgrade applications to newer versions of software to address security vulnerabilities.
- Enhance applications based on new feature requests. 

### Conclusion

The *Software Development Life Cycle* is a systematic way of building software that started in the 1960s. It is a proven way to ensure that high-quality software is built and released effectively in an optimized manner. As cloud-native applications are highly distributed systems, it is even more important to use the described SDLC best practices to build the solutions effectively from the ground up. 
