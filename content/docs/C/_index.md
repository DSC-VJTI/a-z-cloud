---
title: "C"
linkTitle: "C"
weight: 4
description: >
  Continuous Integration and Continuous Delivery (CI/CD)
---

<!-- {{% pageinfo %}}
CI/CD
{{% /pageinfo %}} -->

> As cloud native approaches gather steam, CI/CD practices have to evolve to maintain stability as you increase speed. Because without the right guard rails, it’s like attaching a rocket ship to a go kart. It’s not a very fun ride.
>
> \- Ravi Tharisayi - ex Team Lead and Principal Advisor at IBM

Continuous integration (CI) and continuous delivery (CD) embody a culture, set of operating principles, and collection of practices that enable application development teams to deliver code changes more frequently and reliably. The implementation is also known as the CI/CD pipeline.

CI/CD tools help store the environment-specific parameters that must be packaged with each delivery. CI/CD automation then performs any necessary service calls to web servers, databases, and other services that may need to be restarted or follow other procedures when applications are deployed.

### Continuous Integration

It is a coding philosophy and set of practices that drive development teams to implement small changes and check in code to version control repositories frequently. Because most modern applications require developing code in different platforms and tools, the team needs a mechanism to integrate and validate its changes.

The technical goal of CI is to establish a consistent and automated way to build, package, and test applications. With consistency in the integration process in place, teams are more likely to commit code changes more frequently, which leads to better collaboration and software quality.


### Continuous Delivery 

CD picks up where continuous integration ends. CD automates the delivery of applications to selected infrastructure environments. Most teams work with multiple environments other than the production, such as development and testing environments, and CD ensures there is an automated way to push code changes to them.

A typical CD pipeline has build, test, and deploy stages. More sophisticated pipelines include many of these steps:

- Pulling code from version control and executing a build.
- Executing any required infrastructure steps that are automated as code to stand up or tear down cloud infrastructure.
- Moving code to the target computing environment.
- Managing the environment variables and configuring them for the target environment.
- Pushing application components to their appropriate services, such as web servers, API services, and database services.
- Executing any steps required to restarts services or call service endpoints that are needed for new code pushes.
- Executing continuous tests and rollback environments if tests fail.
- Providing log data and alerts on the state of the delivery

### Implementing CI/CD pipelines with Kubernetes and serverless architectures 

Many teams operating CI/CD pipelines in cloud environments also use **c**ontainers such as **Docker** and orchestration systems such as **Kubernetes**. Containers allow for packaging and shipping applications in standard, portable ways. Containers make it easy to scale up or tear down environments that have variable workloads.
There are many approaches to using containers, infrastructure as code, and CI/CD pipelines together. You can explore the options such as Kubernetes with Jenkins or Kubernetes with Azure DevOps.


