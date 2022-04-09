---
title: “F”
linkTitle: “F”
weight: 4
description: >
  Function-as-a-Service(FaaS)
---

<!-- {{% pageinfo %}}
FaaS
{{% /pageinfo %}} -->

> In the serverless world, Function-as-a-Service allows to write small pieces of code that do something Just like any other function, but serverless. That means: The function is sleeping in a fluffy cloudy container and only when it is needed, it wakes up and does something, and the good news: A sleeping function doesn’t cause cost.
>
> \- Carlos Roggan 


### What is Function-as-a-Service?

Function-as-a-Service (FaaS) is a serverless way to execute modular pieces of code on the edge. FaaS lets developers write and update a piece of code on the fly, which can then be executed in response to an event, such as a user clicking on an element in a web application. This makes it easy to scale code and is a cost-efficient way to implement microservices.

Hosting a software application on the internet typically requires provisioning and managing a virtual or physical server and managing an operating system and web server hosting processes. With FaaS, the physical hardware, virtual machine operating system, and web server software management are all handled automatically by your cloud service provider. This allows you to focus solely on individual functions in your application code.

### How FaaS works?
FaaS gives developers an abstraction for running web applications in response to events, without managing servers. For example, uploading a file could trigger custom code that transcodes the file into a variety of formats.
FaaS infrastructure is usually metered on-demand by the service provider, primarily through an event-driven execution model, so it’s there when you need it but it doesn’t require any server processes to be running constantly in the background, like platform-as-a-service (PaaS) would. 

Functions can be accessed through one of several triggers that you define when you create the function. For use in an app, functions can occur on events that happen in the database. For example, a function can be triggered when a new item is written to a database, changed, or deleted from the database.

An “on-event” function might send an email to a user when their account is created. A function could also be written to send a notification to a user, or set of users, in a chatroom when a new message has been written to the room (equivalent to a new write on the database).

### What are the advantages of using FaaS?
- **Improved developer velocity** 
      With FaaS, developers can spend more time writing application logic and less time worrying about servers and deploys. This typically means a much faster development turnaround.
- **Built-in scalability**        
      Since FaaS code is inherently scalable, developers don’t have to worry about creating contingencies for high traffic or heavy use. The serverless provider will handle all of the scaling concerns.
- **Cost efficiency**         
      Unlike traditional cloud providers, serverless FaaS providers do not charge their clients for idle computation time. Because of this, clients only pay for as much computation time as they use, and do not need to waste money 
      over-provisioning cloud resources.
- Functions can be written in almost any programming language


### What are the drawbacks of FaaS?
- **Less system control**         
      Having a third party manage part of the infrastructure makes it tough to understand the whole system 
      and adds debugging challenges.
- **More complexity required for testing**        
      It can be very difficult to incorporate FaaS code into a local testing environment, making thorough testing 	of an application a more intensive task.

### Use Cases
Because it enables transactions to be isolated and scaled easily, FaaS is good for high-volume and embarrassingly parallel workloads. It can also be used to create backend systems or for activities such as data processing, format conversion, encoding, or data aggregation.
FaaS is also a good tool for Web apps, backends, data/stream processing, or to create online chatbots or back ends for IoT devices.

FaaS can help you manage and use third-party services. If you’re considering Android app development, for example, you can adopt a FaaS approach to keep your costs in check. Because you’re only charged when your app connects to the cloud for a specific function like batch processing, costs can be considerably lower than they would using a traditional approach.

### FaaS vs Serverless
Serverless and Functions-as-a-Service (FaaS) are often conflated with one another but the truth is that FaaS is actually a subset of serverless. Serverless is focused on any service category, be it compute, storage, database, messaging, api gateways, etc. where configuration, management, and billing of servers are invisible to the end user. FaaS, on the other hand, while perhaps the most central technology in serverless architectures, is focused on the event-driven computing paradigm wherein application code, or containers, only run in response to events or requests.
The combination of FaaS and common back-end services (such as databases, messaging, and authentication) connected primarily through an event-driven architecture is what provides the best benefits for serverless developers.





