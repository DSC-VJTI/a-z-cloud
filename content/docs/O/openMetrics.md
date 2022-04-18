---
title: "OpenMetrics"
weight: 4
description: >
   The de-facto standard for transmitting cloud-native metrics at scale.
---


> Creating OpenMetrics within CNCF was a given.
>
> \- Richard "RichiH" Hartmann, director of community at Grafana Labs and OpenMetrics founder.


### What is OpenMetrics?
It specifies the de-facto standard for transmitting cloud-native metrics at scale, with support for both text representation and Protocol Buffers. OpenMetrics is a Cloud Native Computing Foundation sandbox project. 
OpenMetrics creates an open standard for transmitting cloud-native metrics at scale. It acts as an open standard for Prometheus and is the officially supported exposition format for the project and compatible solutions. 

Metrics are a specific kind of telemetry data, and when combined with logs and traces, provide a comprehensive view of the performance of cloud native applications.  

OpenMetrics was spun out of Prometheus to provide a specification and de-facto standard format for metrics.

It is used or supported by most CNCF projects and many wider cloud native ecosystem projects. Furthermore, any changes are considered closely with Cortex, Prometheus, Kubernetes, and Thanos.

OpenMetrics is used in production by many large enterprises, including GitLab, DoorDash, Grafana Labs, Chronosphere, Everquote, and SoundCloud. 

### What’s new in OpenMetrics?

The good news? OpenMetrics is largely the same as the Prometheus text format.
One of the biggest changes was to implement the convention for counters to end in *_total*, which is now mandatory on time series.
If you are already following that convention, it will be a seamless change, If not, then when your client libraries switch, your metrics names are going to change. 

For example, if you have a metric called *cpu_seconds*, inside Prometheus it would end up being called *cpu_seconds_total* once it has migrated over.

Another recent change is that time stamps are now in seconds.

Other improvements and interoperability functions include:
- There is only one way of escaping rather than two.
- There are new ways to detect incomplete scrapes.
- There are higher resolution time stamps. 
- There are 64-bit integer values.
- *_created* was added for metric creation and resets. 
- There are considerations for both push and pull, to make sure OpenMetrics works for everyone.
- The text format is still mandatory, but historically Prometheus also had the protobuf format that went by the wayside with Prometheus v2.0, so OpenMetrics reintroduced protobuf as optional.

One of the biggest features that OpenMetrics introduced is exemplars to link certain metrics to example traces.

<p align = "center">
<img src = "https://grafana.com/static/assets/img/blog/kubecon_openmetrics_grafana_exemplar.png" alt="OpenTelemetry Components" >
</p>
</br>

### Learn

Learn more about OpenMetrics from the official [documentation](https://openmetrics.io/)

Learn more about Prometheus from the official [documentation](https://prometheus.io/)





