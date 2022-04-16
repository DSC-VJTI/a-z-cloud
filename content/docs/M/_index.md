---
title: "M"
linkTitle: "M"
weight: 4
description: >
  ## Microservices
---

> ...the microservice architectural style is an approach to developing a single application as a suite of small services, each running in its own process and communicating with lightweight mechanisms, often an HTTP resource API.
>
> \- Martin Fowler, Renowned author, Chief Scientist at ThoughtWorks

The above quote on microservices architecture is often deemed to be the textbook definition. Before we dive into what is a microservice, let's look at the traditional practice of designing and developing software i.e., as a monolith.

## Monolithic Architecture

In a monolithic architecture, application tiers can be described as:

- part of the same unit
- managed in a single repository
- sharing existing resources (e.g. CPU and memory)
- developed in one programming language
- released using a single binary

<p align="center">
<img src="monolith-example.png" alt="Monolithic Architecture Example" height="30%" width="30%" />
</p>

As student developers, we tend to follow this approach with a web framework such as Django or Spring where the UI and business logic are part of one repository. Thus, when we deploy such an application, we need to package the entire application as a single unit. Hence, if multiple people were to contribute on the application, their changes won't be reflected unless the entire application is deployed again.

## Microservices Architecture

In a microservice architecture, application tiers are managed independently, as different units. Each unit has the following characteristics:

- managed in a separate repository
- own allocated resources (e.g. CPU and memory)
- well-defined API for connection to other units
- implemented using the programming language of choice
- released using its own binary

<p align="center">
<img src="microservice-example.png" alt="Microservices Architecture Example" height="75%" width="75%" />
</p>

To gain agility in the development cycle, several concerns (independent features) of a monolith can be split into microservices that can be developed and deployed individually. With such an architecture, the application becomes fault tolerant as there is no single point of failure - even if one microservice goes down or crashes, other microservices will still work at their concerns are independent.

## Trade-offs

- Development Complexity: represents the effort required to deploy and manage an application.
- Scalability: captures how an application is able to scales up and down, based on the incoming traffic.
- Time to Deploy: encapsulates the build of a delivery pipeline that is used to ship features.
- Flexibility: implies the ability to adapt to new technologies and introduce new functionalities.
- Operational Cost: represents the cost of necessary resources to release a product.
- Reliability: captures practices for an application to recover from failure and tools to monitor an application.

| Trade-off              | Monolith                                                                                                                                                                    | Microservices                                                                                                                                                                      |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Development Complexity | one programming language, one repository, enables sequential development                                                                                                    | multiple programming languages, multiple repositories, enables concurrent development                                                                                              |
| Scalability            | replication of the entire stack; hence it's heavy on resource consumption                                                                                                   | replication of a single unit, providing on-demand consumption of resources                                                                                                         |
| Time to Deploy         | one delivery pipeline that deploys the entire stack; more risk with each deployment leading to a lower velocity rate                                                        | multiple delivery pipelines that deploy separate units; less risk with each deployment leading to a higher feature development rate                                                |
| Flexibility            | low rate, since the entire application stack might need restructuring to incorporate new functionalities                                                                    | high rate, since changing an independent unit is straightforward                                                                                                                   |
| Operational Cost       | low initial cost, since one code base and one pipeline should be managed. However, the cost increases exponentially when the application needs to operate at scale          | high initial cost, since multiple repositories and pipelines require management. However, at scale, the cost remains proportional to the consumed resources at that point in time. |
| Reliability            | in a failure scenario, the entire stack needs to be recovered. Also, the visibility into each functionality is low, since all the logs and metrics are aggregated together. | in a failure scenario, only the failed unit needs to be recovered. Also, there is high visibility into the logs and metrics for each unit.                                         |
