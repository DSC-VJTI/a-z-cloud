---
title: "E"
linkTitle: "E"
weight: 4
description: >
  ## Event-Driven Architecture
---

> Microservices — is an architectural style that structures an application as a collection of loosely coupled services, which implement business capabilities. 
>
> \- Chris Richardson

Before understanding Event-Driven Architecture (EDA), let's first understand what an event is,

An **event** is a state change or an update within the system that triggers the action of other systems. It can be anything from a transaction and sensor input to a mouse click and a photo upload, etc.

<br>

With that said, 

**Event-driven architecture** is a design model that connects distributed software systems and allows for efficient communication. EDA makes it possible to exchange information in real time or near real time. It is common in designing apps that rely on microservices (you'll get to know what this mean real soon but for now consider that _when each service runs its own process and communicates through APIs with other services, then these services are considered as microservices_.)

The concept of event-driven architecture is mainly realized through the publish/subscribe communication model (We covered this during GCP'21, hope y'all remember!).

<br>

Just to brief,

Publish/subscribe is a flexible messaging pattern that allows disparate system components to interact with one another asynchronously.


### How does event-driven architecture work?

Event-driven architecture is made up of event producers and event consumers. An event producer detects or senses an event and represents the event as a message. It does not know the consumer of the event, or the outcome of an event. 

After an event has been detected, it is transmitted from the event producer to the event consumers through event channels, where an event processing platform processes the event asynchronously. Event consumers need to be informed when an event has occurred. They might process the event or may only be impacted by it. 

The event processing platform will execute the correct response to an event and send the activity downstream to the right consumers. This downstream activity is where the outcome of an event is seen. 

![EDA](EDA.svg)

### Where can this approach be used in your next project?

**To monitor and receive alerts** for any anomalies or changes to storage buckets, database tables, virtual machines, or other resources.

**To fan out a single event to multiple consumers.** The event router will push the event to all the appropriate consumers, without you having to write customized code. Each service can then process the event in parallel, yet differently.

**To provide interoperability between different technology stacks** while maintaining the independence of each stack.


