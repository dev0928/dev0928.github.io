---
title: "Architecture Decision Records"
date: 2023-03-25T11:24:01-04:00
draft: true
slug: arch-decision-records
toc: true
tags: ["Architecture"]
---

### What are Architecture Decision Records (ADRs)?

Architecture Decision Records (ADRs) are the documents used to  **record the reasoning behind certain design decisions in projects** for future reference. ADRs help understand the current state of the application's architecture and infrastructure choices, facilitating future design decisions.   

ADRs are typically created in the markdown format and maintained in the version control like the rest of the application codebase. ADRs can be hosted in the application's wiki section, making it accessible to business stakeholders.

### Benefits of ADRs

Maintaining ADRs helps in the following scenarios:

- When new team members rolled onto the project, new members could greatly benefit in understanding the application's design decisions by reviewing the ADRs.
- Helps maintain the record of the design decisions in a long-running project, so existing members can use them as a reference.
- ADRs help in understanding the current state of the application during the project handover to another team.

### Use cases for ADRs

Project members could create an ADR for every significant project decision. Typical use cases for ADRs are:

- Project’s product choices - decisions/reasons behind the product choice
- The thought process behind the technology stack selection
- Cloud resources - specifically configurations chosen for the cloud resources
- Decisions around non-functional requirements (security, scalability, availability, etc.)
- Deployment method decisions

### Format of ADRs

There are several templates and tools available for maintaining ADRs. Refer to the [ADR GitHub Organization](https://adr.github.io/ "ADR GitHub Organization") for potential options. Stick to one of the templates and keep it consistent based on the project’s needs. 

Here is an example template mainly based on the templates located [here](https://github.com/joelparkerhenderson/architecture-decision-record/tree/main/templates "ADR Templates").

---------------------------------------------------------------------------------------------
In each ADR file, write these sections:

# Title

## Status

What is the status, such as proposed, accepted, rejected, deprecated, superseded, etc.?

## Deciders

List of the project team members that were part of this decision.

## Decision Date

Date this ADR decided.

## Context

What issue motivates this decision or change?

## Options 

What are the potential options considered?

## Pros and Cons of the considered options

## Decision

What is the change that is being proposed and done?

## Consequences

What becomes more accessible or more difficult because of this change?

--------------------------------------------------------------------------------


