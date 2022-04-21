---
title: "S"
linkTitle: "S"
weight: 4
description: >
  ## Scalability
---

Simply put, scalability refers to the ability to increase or decrease compute resources to meet changing demand or load.

Several Google Cloud Platform services such as [Cloud Run]({{< relref "cloud-run.md" >}} "Cloud Run") and [Cloud Functions]({{< relref "firebase_cloud_functions.md" >}} "Cloud Functions") automatically scale up or down depending upon changing demands.

### Horizontal and Vertical Scaling

<p align="center">
    <img src="scalability.avif" alt="Horizontal and Vertical Scaling" height="80%" width="80%" />
</p>

In the early 2000s or before cloud computing became accessible to an individual, a website would typically be hosted on a Linux machine, exposed to the internet via an IP address, and networking handled by an Apache or Nginx server. Thus, the web application was deployed _on-premises_. Say this web app is Facebook, which was first deployed on a server belonging to Harvard University in the US.

#### Vertical scaling

Soon the social media platform becomes a hit and the standalone server cannot handle the increased demand. A more powerful machine/server is needed that can run the same copy of code for the web app. Thus, the infrastructure needed to _scale up_ with the changing demand; this kind of scaling is called as **vertical scaling**, where more compute resources are added to the same machine such as RAM or storage.

External storage can easily be added to a running machine. However, as RAM cannot be added externally, the machine first needs to be shut down and the existing RAM needs to be replaced with a larger RAM. This means that the website will no longer be available to anyone and there will be a disruption of service.

#### Horizontal scaling

Now students outside the Harvard University campus are using Facebook, as far as in the UK! Their requests and data are all managed in this one big machine at Harvard University. With a further increase in load and unavailability of an even powerful machine, what can be done? If not a more powerful machine, a smaller machine that can run the same instance of the web app can be used. Here, the infrastructure is _scaled out_ and this kind of scaling is called as **horizontal scaling**.

An entire new machine needs to be purchased/rented and configured for the web app to be run on it. Thus, the cost increases exponentially as more and more machines are used.

#### Comparison

| Horizontal Scaling                                                                       | Vertical Scaling                                                                           |
| ---------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| A load balancer such as Nginx is required to route incoming requests to multiple servers | Since there is only one machine, all the load is bear by it and no load balancer is needed |
| Reliable as failure of one server does not affect other servers                          | Single point of failure as there is only one server                                        |
| If a shared database is being used, data consistency needs to be taken care of           | No issue of data inconsistency                                                             |
| Scales out without any disruption of service                                             | Scales up with downtime depending upon compute resource to be added                        |
| Cost increases exponentially                                                             | Cost increase linearly                                                                     |
| Desirable for a microservices architecture                                               | Desirable for a monolithic architecture                                                    |
