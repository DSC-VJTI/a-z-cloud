---
title: "Eventarc"
weight: 4
description: >
  A unified eventing experience in Google Cloud.
---

Eventarc allows you to build event-driven architectures without having to implement, customize, or maintain the underlying infrastructure. Eventarc offers a standardized solution to manage the flow of state changes, called events, between decoupled microservices. When triggered, Eventarc routes these events through Pub/Sub subscriptions to various destinations while managing delivery, security, authorization, observability, and error-handling for you.

You can manage Eventarc from the Google Cloud Console, from the command line using the gcloud CLI, or by using the Eventarc API.

### Benefits Of Eventarc

Eventarc provides an easier path to receive events not only from Pub/Sub topics but from a number of Google Cloud sources with its Audit Log and Pub/Sub integration. Any service with Audit Log integration or any application that can send a message to a Pub/Sub topic can be event sources for Eventarc. You don’t have to worry about the underlying infrastructure with Eventarc. It is a managed service with no clusters to set up or maintain.

It also has some concrete benefits beyond the easy integration. It provides consistency and structure to how events are generated, routed, and consumed.

### Learn

Check out the [Eventarc documentation](https://cloud.google.com/eventarc/docs) for more information.

A few code samples are available [here](https://cloud.google.com/eventarc/docs#code-samples).
