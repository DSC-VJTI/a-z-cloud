---
title: "Cloud Run"
weight: 4
description: >
  Run your microservices effortlessly
---

Cloud Run is a fully-managed compute environment for deploying and scaling serverless HTTP containers without worrying about provisioning machines, configuring clusters, or autoscaling.

<p align="center">
<img src="https://repository-images.githubusercontent.com/189295422/f294aa00-838c-11e9-8e27-a1fdc651371f" alt="Cloud Run logo" height="30%" width="30%" />
</p>

### Benefits of Cloud Run

- No vendor lock-in - Because Cloud Run takes standard OCI containers and implements the standard [Knative](https://cloud.google.com/knative) Serving API, you can easily port over your applications to on-premises or any other cloud environment.

- Fast autoscaling - Microservices deployed in Cloud Run scale automatically based on the number of incoming requests, without you having to configure or manage a full-fledged Kubernetes cluster. Cloud Run scales to zero— that is, uses no resources—if there are no requests.

- Split traffic - Cloud Run enables you to split traffic between multiple revisions, so you can perform gradual rollout such as canary deployments or blue/green deployments.

- Custom domains - You can set up custom domain mapping in Cloud Run and it will provision a TLS certificate for your domain.

- Automatic redundancy - Cloud Run offers automatic redundancy so you don’t have to worry about creating multiple instances for high availability

The following is an example of a microservices architecture using Cloud Run and several GCP services:

![Cloud Run use cases](https://storage.googleapis.com/gweb-cloudblog-publish/images/example_ms_a_callout.max-1700x1700.png)

### Learn

- Cloud Run [documentation](https://cloud.google.com/run/docs)

- Hello Cloud Run with Python [codelab](https://codelabs.developers.google.com/codelabs/cloud-run-hello-python3)

- Deploy a website with Cloud Run [codelab](https://codelabs.developers.google.com/codelabs/cloud-run-deploy)
