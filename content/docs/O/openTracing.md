---
title: "OpenTracing"
weight: 4
description: >
   An initiative to enable reusable, open source, vendor neutral instrumentation for distributed tracing.
---


>Ideas about distributed tracing and monitoring across multiple systems have certainly generated quite a buzz. It’s becoming more important than ever before to be able to see what’s going on inside our requests as they span across multiple software services. Aiming to harness this importance, the OpenTracing initiative has sprung up to help developers avoid vendor lock-in.
>

### What Is Distributed Tracing?

Distributed tracing is a mechanism you can use to profile and monitor applications. Unlike regular tracing, distributed tracing is more suited to applications built using a microservice architecture, hence the name.

Distributed tracing tracks a single request through all of its journey, from its source to its destination, unlike traditional forms of tracing which just follow a request through a single application domain.
In other words, we can say that distributed tracing is the stitching of multiple requests across multiple systems. The stitching is often done by one or more correlation IDs, and the tracing is often a set of recorded, structured log events across all the systems, stored in a central place.

### What is OpenTracing?

It’s a vendor-agnostic API to help developers easily instrument tracing into their code base. It’s open because no one company owns it. 

OpenTracing wants to form a common language around what a trace is and how to instrument them in our applications. In OpenTracing, a trace is a directed acyclic graph of Spans with References that may look like this

<p align = "center">
<img src = "https://github.com/DSC-VJTI/a-z-cloud/raw/main/content/docs/O/1.png">
</p>
<br/>

This allows us to model how our application calls out to other applications, internal functions, asynchronous jobs, etc. All of these can be modeled as Spans, as we’ll see below.

For example, if I have a consumer website where a customer places orders, I make a call to my payment system and my inventory system before asynchronously acknowledging the order. I can trace the entire order process through every system with an OpenTracing library and can render it like this:

<p align = "center">
<<<<<<< HEAD
<img src = "https://github.com/DSC-VJTI/a-z-cloud/raw/main/content/docs/O/2.png">
=======
<img src = "https://raw.githubusercontent.com/DSC-VJTI/a-z-cloud/main/content/docs/O/2.png">
>>>>>>> 16d224249125fbd40f3e7deb1666f3d78fee4231
</p>
<br/>

Each one of these bracketed blocks is a Span representing a separate software system communicating over messaging or HTTP.

### Terminology
Let’s talk a bit about the components of the OpenTracing API.

- **Tracer**       
	This tracer is the entry point into the tracing API. It gives us the ability to create Spans. It also lets us extract tracing information from external sources and inject information to external destinations.

- **Span**       
	This represents a unit of work in the Trace. For example, a web request that initiates a new Trace is called the root Span. If it calls out to another web service, that HTTP request would be wrapped within a new child Span. Spans carry around a set of tags of information pertinent to the request being carried out. You can also log events within the context of a Span. They can support more complex workflows than web requests, such as asynchronous messaging. They have timestamps attached to them so we can easily construct a timeline of events for the Trace. 

- **SpanContext**      
	The SpanContext is the serializable form of a Span. It lets Span information transfer easily across the wire to other systems.

- **References**         
	So far, Spans can connect to each other via two types of relationship: ChildOf and FollowsFrom. ChildOf Spans are spans like in our previous example, where our ordering website sent child requests to both our payment system and inventory system. FollowsFrom Spans are just a chain of sequential Spans. So, a FollowsFrom Span is just saying, “I started after this other Span.”


### Is OpenTracing still in Use?
OpenTracing is an open-source CNCF (Cloud Native Computing Foundation) project which provides vendor-neutral APIs and instrumentation for distributed tracing. Although OpenTracing and OpenCensus have merged to form OpenTelemetry in early 2019, third-party libraries and frameworks like Hazelcast IMDG still come equipped with OpenTracing pre-instrumentation.

OpenTracing became a CNCF project back in 2016, with the goal of providing a vendor-agnostic specification for distributed tracing, offering developers the ability to trace a request from start to finish by instrumenting their code. Then, Google made the OpenCensus project open source in 2018. This was based on Google’s Census library that was used internally for gathering traces and metrics from their distributed systems. Like the OpenTracing project, the goal of OpenCensus was to give developers a vendor-agnostic library for collecting traces and metrics.
This led to two competing tracing frameworks, which led to the informal reference “the Tracing Wars.” Usually, competition is a good thing for end-users since it breeds innovation. However, in the open-source specification world, competition can lead to poor adoption, contribution, and support.
Going back to the Kubernetes example, imagine how much more disjointed and slow-moving container adoption would be if everybody was using a different orchestration solution. To avoid this, it was announced at KubeCon 2019 in Barcelona that the OpenTracing and OpenCensus projects would converge into one project called OpenTelemetry and join the CNCF.

### Learn

Learn more about OpenTracing from the official [documentation](https://opentracing.io/)







