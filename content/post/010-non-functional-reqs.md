---
title: "Non-functional Requirements"
date: 2023-07-03T17:16:12-04:00
draft: true
slug: non-functional-requirements
toc: true
tags: ["SDLC"]
---

### Non-functional requirements

There are two categories of requirements - **functional** and **non-functional**. Let’s say we are building an e-commerce web application - the application parts that users interact with - the products page, the shopping cart, and the payment section are **functional requirements**. In contrast, non-tangible aspects such as how fast the application responds to users’ requests or how secure the application is are **non-functional requirements**.
   
As the functional requirements are part of the business requirements, they are tracked and developed as features from the earlier stage of the project. But project teams sometimes don’t clearly define the non-functional requirements resulting in significant issues discovered late in the project.  

### Types of NFRs

The table below outlines a few NFR types along with their definition. The below list is by no means exhaustive. Also, tracked NFRs could vary depending on the application’s context. 

| NFR         | Definition  | 
| :---        | :---        | 
| Security    | How well the system and its data is protected against unauthorized access and data breaches       |
| Privacy     | How well the users' personal and sensitive data is processed, securely stored, and maintained by the system        |
| Compliance     | How well the system is compliant with the industry standards and regulations     | 
| Performance     | How fast the system can respond to users' requests |
| Reliability     | The ability of a system to provide consistent output regardless of functionality and availability of certain special conditions |
| Scalability     | Could the system effectively handle the increase in traffic or seasonal load |
| Observability     | Can the system's internal state be monitored through the logs and produced outputs without requiring any additional changes to the application code         | 
| Maintainability     | Is the system easy to maintain? Can the system's internal state be updated through external configuration without the application change?        | 
| Recoverability     | Does the system have mechanisms to recover from failures?         | 
| Extensibility     |   Is the system easy to update for adding new features      | 
| Interoperability     | How well the components of the system work together     | 
| Deployability     | How easily and effectively changes can be deployed        |
| Accessibility     | Is the system accessible to all user groups, including people with disabilities?        | 
| Usability     | Is the system easy to work with and intuitive to operate?        | 
 
### NFR Considerations

- Creating a list of relevant NFRs for the project is a collective effort; The project’s product manager, engineers, architects, and customer representatives should work together to define non-functional requirements.
- A list of relevant NFRs should be well-defined and prioritized earlier in the project.
- Organizations could create and maintain an exhaustive NFR checklist for collective awareness.
- Organizations could come up with internal standards for some of the non-functional requirements.
- Standardize some of the common NFRs’ implementation for easier adoption by the individual project teams.
- The project teams should include the effort needed for implementing the NFRs while sizing the features.
- Also, consider NFR testing efforts while scoping the project.
- It is worth checking available cloud resources’ NFR offerings during the application’s design phase. 

### Conclusion
 
The project teams should revisit implemented NFRs on a regular basis. For example - NFRs related to security and compliance could periodically change depending on the regulations and technology changes. Developing a proactive strategy for implementing NFRs for the project and organization is a worthwhile and rewarding effort.  
