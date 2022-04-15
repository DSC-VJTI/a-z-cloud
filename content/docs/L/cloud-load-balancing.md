---
title: "Cloud Load Balancing"
weight: 4
description: >
   High performance, scalable load balancing on Google Cloud Platform.
---

Load balancers are managed services on GCP that distribute traffic across multiple instances of your application. GCP bears the burden of managing operational overhead and reduces the risk of having a non-functional, slow, or overburdened application.
With Google Cloud Load Balancing, you can serve content as close as possible to your users, on a system that can respond to over 1 million queries per second!


### Different load balancing options
To decide which load balancer best suits your implementation, you need to think about whether you need

1. **Global** or **regional** load balancing. Global load balancing means backend endpoints live in multiple regions. Regional load balancing means backend endpoints live in a single region.
2. **External** or **internal** load balancing
3. What **type of traffic** you are serving? HTTP, HTTPS, SSL, TCP, UDP etc.

#### External load balancer
External load balancing includes four options:
* HTTP(S) Load Balancing for HTTP or HTTPS traffic,
* TCP Proxy for TCP traffic for ports other than 80 and 8080, without SSL offload
* SSL Proxy for SSL offload on ports other than 80 or 8080.
* Network Load Balancing for TCP/UDP traffic.

1. ##### HTTP(S) load balancers
    Global HTTP(S) load balancing if for layer-7 traffic
    Google pushed load balancing out to the edge network on front-end servers, as opposed to using the traditional DNS-based approach. Thus, global load-balancing capacity can be behind a single Anycast virtual IPv4 or IPv6 address. This means you can deploy capacity in multiple regions without having to modify the DNS entries or add new load balancer IP address for new regions. So, it is clear that with global HTTP(S) load balancing, you get cross-region failover and overflow!

    With global HTTP(S) load balancing, you get cross-region failover and overflow!
    The distribution algorithm automatically directs traffic to the next closest instance with available capacity in the event of failure of or lack of capacity for instances in the region closest to end user.

2. ##### Proxy based load balancers (TCP and SSL)
    Google Cloud also offers proxy-based load balancers for TCP and SSL traffic, and they use the same globally distributed infrastructure.
    Use TCP proxy load balancer when you are dealing with TCP traffic and do not need SSL offload.
    Generally speaking, your decision to use them would depend on whether you require SSL offload or not. You can find out more in the links below.
    Use SSL proxy load balancer when you are dealing with TCP traffic and need SSL offload.

3. ##### Network load balancer
    While the global HTTP(S) load balancer is for Layer-7 traffic and is built using the Google Front End Engines at the edge of Google’s network, the regional Network Load Balancer is for Layer-4 traffic and is built using Maglev.
    Network load balancer is for the Layer-4 traffic.


#### Internal Load Balancer
With internal load balancing, you can run your applications behind an internal IP address and disperse HTTP/HTTPs traffic to your backend application hosted either on Google Kubernetes Engine (GKE) or Google Compute Engine (GCE).
The internal load balancer is a managed service that can only be accessed on an internal IP address and in the chosen region of your Virtual Private Cloud network. You can use it to route and balance load traffic to your virtual machines. 

Similar to the HTTP(S) Load Balancer and Network Load Balancer, Internal L7 load balancer is neither a hardware appliance nor an instance-based solution, and can support as many connections per second as you need since there’s no load balancer in the path between your client and backend instances.
Internal layer 7 load balancer can support as many connections per second as your need!
 
 

<p align = "center">
<img src = "https://miro.medium.com/max/1400/1*TTUArfpyYhGvsoLJaLrzaA.png" alt="load balancing architecture" width="800" height="500">
</p>
<p align = "center">
The architecture for your website Beyond Treat (your one stop shop for vegan dog treats) would look something like this with an internal load balancer for the internal traffic, external global HTTPS load balancer for the incoming traffic.
</p>   
<br/>

### Learn

Learn more about Cloud Load Balancing from the official [documentation](https://cloud.google.com/load-balancing/docs/load-balancing-overview)

Explore Cloud Load Balancing with the following codelabs:
1. [Host and scale a web app in Google Cloud with Compute Engine](https://codelabs.developers.google.com/codelabs/cloud-webapp-hosting-gce#5)
2. [Setup Network and HTTP Load Balancers](https://kiosk-dot-codelabs-site.appspot.com/codelabs/cloud-load-balancers/index.html?index=..%2F..index#0)





