---
title: "L"
linkTitle: "L"
weight: 4
description: >
 Load Balancing
---

<!-- {{% pageinfo %}}
Load Balancing
{{% /pageinfo %}} -->

### What is Load Balancing?

Imagine you’re in charge of a complex website, and it’s an online hit! It continues to face high amounts of traffic and you’re not sure your website backend can handle the amount of traffic from all over the world. You know you need to use load balancers, but the options are confusing. It can be hard to know exactly how to settle on a load balancing architecture that meets your needs, and figure out the prerequisites you need, for the best performance, without making too much of a dent in your wallet.
To start, you need to know what load balancing is and why it’s so important to the long-lasting success of your application.

>Load balancing is the process of distributing traffic across your network of servers to ensure that the system does not get overwhelmed and all requests are handled easily and efficiently.
> 

Modern high‑traffic websites serve hundreds of thousands, if not millions, of concurrent requests from users or clients and return the correct text, images, video, or application data, all in a fast and reliable manner. You’ve probably all experienced visiting your favorite website, only to get long wait times, connection timeout errors, or images and videos buffering. And a lot of the times, this is because the website backend is unable to cost‑effectively scale to meet these high volumes.
The logical answer here is to add more backend servers to help serve traffic. But the next question becomes, how do you distribute traffic to those backend servers based on capacity and health?
This is where load balancing makes a splash.

In the seven-layer Open System Interconnection (OSI) model, network firewalls are at levels one to three (L1-Physical Wiring, L2-Data Link and L3-Network). Meanwhile, load balancing happens between layers four to seven (L4-Transport, L5-Session, L6-Presentation and L7-Application).

![](1.jpeg)


### Load Balancers
As an organization meets demand for its applications, the load balancer decides which servers can handle that traffic. This maintains a good user experience.
Load balancers manage the flow of information between the server and an endpoint device (PC, laptop, tablet or smartphone). The server could be on-premises, in a data center or the public cloud. The server can also be physical or virtualized. The load balancer helps servers move data efficiently, optimizes the use of application delivery resources and prevents server overloads. Load balancers conduct continuous health checks on servers to ensure they can handle requests. If necessary, the load balancer removes unhealthy servers from the pool until they are restored. Some load balancers even trigger the creation of new virtualized application servers to cope with increased demand.
Traditionally, load balancers consist of a hardware appliance. Yet they are increasingly becoming software-defined. This is why load balancers are an essential part of an organization’s digital strategy.

Load balancers have different capabilities, which include:
- **L4** — directs traffic based on data from network and transport layer protocols, such as IP address and TCP port.
- **L7** — adds content switching to load balancing. This allows routing decisions based on attributes like HTTP header, uniform resource identifier, SSL session ID and HTML form data.
- **GSLB** — Global Server Load Balancing extends L4 and L7 capabilities to servers in different geographic locations.


### Why Load Balancing?

There is a limitation to the number of requests a single computer can handle at a given time. When faced with a sudden surge in requests, your application will load slowly, the network will time out, and your server will creak. You have two options: scale up or scale out.

When you scale up (vertical scale), you increase the capacity of a single machine by adding more storage (Disk) or processing power (RAM, CPU) to an existing single machine as needed on demand. But scaling up has a limit — you’ll get to a point where you cannot add more RAM or CPUs.

A better strategy is to scale out (horizontal scale), which involves the distribution of loads across as many servers as necessary to handle the workload. In this case, you can scale infinitely by adding more physical machines to an existing pool of resources.

### Load Balancing and Security
Load Balancing plays an important security role as computing moves evermore to the cloud. The off-loading function of a load balancer defends an organization against distributed denial-of-service (DDoS) attacks. It does this by shifting attack traffic from the corporate server to a public cloud provider. DDoS attacks represent a large portion of cybercrime as their number and size continues to rise. Hardware defense, such as a perimeter firewall, can be costly and require significant maintenance. Software load balancers with cloud offload provide efficient and cost-effective protection.

### Load Balancing Algorithms
There are a variety of load balancing methods, which use different algorithms best suited for a particular situation.
- **Least Connection Method** — directs traffic to the server with the fewest active connections. Most useful when there are a large number of persistent connections in the traffic unevenly distributed between the servers.

- **Least Response Time Method** — directs traffic to the server with the fewest active connections and the lowest average response time.

- **Round Robin Method** — rotates servers by directing traffic to the first available server and then moves that server to the bottom of the queue. Most useful when servers are of equal specification and there are not many persistent connections.

- **IP Hash** — the IP address of the client determines which server receives the request.


### The Benefits
Load balancing can do more than just act as a network traffic cop. Software load balancers provide benefits like predictive analytics that determine traffic bottlenecks before they happen. As a result, the software load balancer gives an organization actionable insights. These are key to automation and can help drive business decisions.
The benefits of load balancing include the following:

- **Prevents Network Server Overload**        
      When using load balancers in the cloud, you can distribute your workload among several servers, network units, data centers, and cloud providers. This lets you effectively prevent network server overload during traffic surges. 

- **High Availability**               
      The concept of high availability means that your entire system won’t be shut down whenever a system component goes down or fails. You can use load balancers to simply redirect requests to healthy nodes in the event that one fails.

- **Better Resource Utilization**                
      Load balancing is centered around the principle of efficiently distributing workloads across data centers and through multiple resources, such as disks, servers, clusters, or computers. It maximizes throughput, optimizes the use of available resources, avoids overload of any single resource, and minimizes response time.
      
- **Prevent a Single Source of Failure**             
	Load balancers are able to detect unhealthy nodes in your cluster through various algorithmic and health-checking techniques. In the event of failure, loads can be transferred to a different node without affecting your users, affording you the time to address the problem rather than treating it as an emergency.






