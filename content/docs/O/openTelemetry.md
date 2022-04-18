---
title: "OpenTelemetry"
weight: 4
description: >
   An open-source standard for logs, metrics, and traces.
---


### What is OpenTelemetry?

OpenTelemetry (also referred to as OTel) is an open-source observability framework made up of a collection of tools, APIs, and SDKs. Otel enables IT teams to instrument, generate, collect, and export telemetry data for analysis and to understand software performance and behavior.

Having a common format for how observability data is collected and sent is where OpenTelemetry comes into play. As a Cloud Native Computing Foundation (CNCF) incubating project, OTel aims to provide unified sets of vendor-agnostic libraries and APIs — mainly for collecting data and transferring it somewhere. Since the project’s start, many vendors have come on board to help make rich data collection easier and more consumable.


### What is telemetry data?

Capturing data is critical to understanding how your applications and infrastructure are performing at any given time. This information is gathered from remote, often inaccessible points within your ecosystem and processed by some sort of tool or equipment. Monitoring begins here. The data is incredibly plentiful and difficult to store over long periods due to capacity limitations — a reason why private and public cloud storage services have been a boon to DevOps teams.

Logs, metrics, and traces make up the bulk of all telemetry data.


- **Logs** are important because you’ll naturally want an event-based record of any notable anomalies across the system. Structured, unstructured, or in plain text, these readable files can tell you the results of any transaction involving an endpoint within your multicloud environment. However, not all logs are inherently reviewable — a problem that’s given rise to external log analysis tools.

- **Metrics** are numerical data points represented as counts or measures that are often calculated or aggregated over a period of time. Metrics originate from several sources including infrastructure, hosts, and third-party sources. While logs aren’t always accessible, most metrics tend to be reachable via query. Timestamps, values, and even event names can preemptively uncover a growing problem that needs remediation.

- **Traces** are the act of following a process (for example, an API request or other system activity) from start to finish, showing how services connect. Keeping a watch over this pathway is critical to understanding how your ecosystem works, if it’s working effectively, and if any troubleshooting is necessary. Span data is a hallmark of tracing — which includes information such as unique identifiers, operation names, timestamps, logs, events, and indexes.

### How does OpenTelemetry work?

OTel is a specialized protocol for collecting telemetry data and exporting it to a target system. Since the CNCF project itself is open source, the end goal is making data collection more system-agnostic than it currently is. But how is that data generated?

The data life cycle has multiple steps from start to finish. Here are the steps the solution takes, and the data it generates along the way:

- Instruments your code with APIs, telling system components what metrics to gather and how to gather them
- Pools the data using SDKs, and transports it for processing and exporting
- Breaks down the data, samples it, filters it to reduce noise or errors, and enriches it using multi-source contextualization
- Converts and exports the data
- Conducts more filtering in time-based batches, then moves the data onward to a predetermined backend.

### OpenTelemetry components
OTel consists of a few different components as depicted in the following figure. Let’s take a high-level look at each one from left to right:

<p align = "center">
<img src = "https://marvel-b1-cdn.bc0a.com/f00000000236551/dt-cdn.net/wp-content/uploads/2020/07/OT.png" alt="OpenTelemetry Components" >
</p>
<p align = "center">
OpenTelemetry Components
</p>   
<br/>


##### APIs

These are core components and language-specific (such as Java, Python, .Net, and so on). APIs provide the basic “plumbing” for your application.

##### SDK
This is also a language-specific component and is the middleman that provides the bridge between the APIs and the exporter. The SDK allows for additional configuration, such as request filtering and transaction sampling.

##### In-process exporter
This allows you to configure which backend(s) you want it sent to. The exporter decouples the instrumentation from the backend configuration. This makes it easy to switch backends without the pain of re-instrumenting your code.

##### Collector
The collector receives, processes, and exports telemetry data. While not technically required, it is an extremely useful component to the OpenTelemetry architecture because it allows greater flexibility for receiving and sending the application telemetry to the backend(s).
The collector has two deployment models:
1. An agent that resides on the same host as the application (for example, binary, DaemonSet, sidecar, and so on)
2. A standalone process completely separate from the application
Since the collector is just a specification for collecting and sending telemetry, it still requires a backend to receive and store the data.


### Benefits of OpenTelemetry

OTel provides a de facto standard for adding observable instrumentation to cloud-native applications. This means companies don’t need to spend valuable time developing a mechanism for collecting critical application data and can spend more time delivering new features instead.
It’s akin to how Kubernetes became the standard for container orchestration. This broad adoption has made it easier for organizations to implement container deployments since they don’t need to build their own enterprise-grade orchestration platform. Using Kubernetes as the analog for what it can become, it’s easy to see the benefits it can provide to the entire industry.


### Learn

Learn more about OpenTelemetry from the official [documentation](https://opentelemetry.io/docs/)







