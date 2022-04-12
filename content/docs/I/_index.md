---
title: "I"
linkTitle: "I"
weight: 4
description: >
  Infrastructure-as-a-Service(IaaS)
---

<!-- {{% pageinfo %}}
IaaS
{{% /pageinfo %}} -->

### What is Infrastructure-as-a-Service?

Infrastructure as a Service is a type of cloud computing service providing computing resources over the internet. IaaS is one of three main categories of cloud computing services. The other two are Software as a Service (SaaS) and Platform as a Service (PaaS).
Infrastructure as a Service (IaaS) means that the infrastructure is hosted on the public and/or private cloud, instead of on an on-premises server. It’s delivered to customers on-demand and is fully managed by the IaaS provider. This includes all the infrastructure components an on-premises data center would traditionally entail, such as servers, networking hardware, and storage. 

Often, the IaaS provider also offers a range of services to complement those components, such as detailed billing, security, monitoring, and clustering. Storage resiliency, like backup and recovery processes, is also included. IaaS allows users to develop, grow, and scale without buying and maintaining physical hardware.

### Benefits of Infrastructure-as-a-Service 

You can think of infrastructure as a service a little bit like taxis or hotels. It would be extremely inefficient for people to try to own transportation or housing everywhere they went. The vast majority of the time, their transportation or housing would go unused, and it would provide no value.
It is much more efficient for companies to own huge quantities of transportation or housing. That way, they can provide it to people only when those people need it. The same basic principle applies to computing power and storage space.
Sometimes you might need huge quantities of computing power or storage space, but most of the time, you do not. It would be extremely inefficient for you to have to own all of the servers necessary to manage your occasional increased need for computing power.
It is much more efficient to rent from an infrastructure as a service company so that you only have to pay for your computing or storage when you actually need it.

- **It’s economical**        
      Because IaaS resources are used on demand and enterprises only have to pay for the compute, storage, and networking resources that are actually used, IaaS costs are fairly predictable and can be easily contained and budgeted for.  

- **It’s efficient**               
      IaaS resources are regularly available to businesses when they need them. As a result, enterprises reduce delays when expanding infrastructure and, alternatively, don’t waste resources by overbuilding capacity.

- **It boosts productivity**                
      Because the cloud provider is responsible for setting up and maintaining the underlying physical infrastructure, enterprise IT departments save time and money and can redirect resources to more strategic activities.
      
- **It’s reliable**             
	IaaS has no single point of failure. Even if any one component of the hardware resources fails, the service will usually still remain available.

- **It’s scalable**              
	One of the biggest advantages of IaaS in cloud computing is the capability to scale the resources up and down rapidly according to the needs of the enterprise.

- **It drives faster time to market**               
	Because IaaS offers virtually infinite flexibility and scalability, enterprises can get their work done more efficiently, ensuring faster development life cycles.


### IaaS Architecture

IaaS is broken into three main components: compute, network, and storage. With these offerings, users have the building blocks they need to create their customized systems, as complicated or powerful as they need, and the ability to scale up and down based on current needs.

#### Compute
Foundational IaaS computing resources begin with servers. Servers are powerful computers that tend to have hundreds of Central Processing Units (CPUs), hundreds or thousands of gigabytes (GBs) of Random-access memory (RAM), and thousands of GBs of storage. Servers are expensive to buy and costly and difficult to maintain. IaaS providers maintain data centers that house the physical, bare-metal servers. These physical servers can be partitioned using a hypervisor into smaller “virtual machines”. These virtual machines can run their OS and applications independently while sourcing power from the bare-metal server. 
There are different ways to set up a virtual machine (VM), and the architecture you choose will depend on your needs and the level of abstraction you prefer. 

Compute offerings often include optional add-ons like load balancing, which automatically distributes network traffic to prevent system overload. 
When users purchase a virtual machine through an IaaS provider, they choose the operating system, often referred to as an image, and applications run on that machine. Developers can easily scale vertically by adding more CPU if their VMs don’t have enough processing power or scaling horizontally to increase instances and handle more load. Virtual machines can often be quick and easy to set up.

#### Storage
Storage options are threefold: file storage, object storage and block storage. 
File storage is similar to what we have on our computers at home and stores data as a single entity into a file. The files can exist within each other as other data, so it’s hierarchical. For example, a path for file storage could be “/home/photos/selfie.jpg”. Object storage instead takes saved data as a single entity and appends metadata and an identifier. Object storage deals with whole objects stored over the network. These objects could be things like an image file, logs, or HTML files. Object storage is the most popular option because of its simplicity and cost savings. Block storage is likely underneath the file or object storage. Block storage services are relatively familiar. They provide access to a traditional block storage device over the network and attach it to your virtual machine. It takes data and saves it as blocks of actual bytes or bits. It has advantages over the other two by being faster to transfer data but not user friendly unless abstracted by a file system like in your computer that uses it.

#### Network
The network function talks to the storage function, other VMs, containers, other servers, the internet, the intranet, and other components. It's how information is transferred through the architecture regardless of endpoints. Users will need different networking bandwidths depending on the amount of data transmitted between computing resources. 


### Use Cases
IaaS has multiple applications that span industries, company sizes, and business needs. Startups and small companies may prefer IaaS to avoid the high costs of purchasing and maintaining hardware and software, and companies experiencing rapid growth like the scalability of IaaS. Larger companies may want the ability to buy only the space they will use. They also often use IaaS for redundancy in their setup and to take advantage of the high availability of public cloud providers. 
Some common use cases for IaaS are:
- **Website hosting:** IaaS provides flexible hosting options for developers looking to get their websites up and running quickly and reliably. Using cloud services also allows builders to easily maintain and scale their sites as they grow.
- **Startups:** IaaS allows startups and other small businesses to avoid the high cost of purchasing and maintaining physical hardware to sustain a cool new idea. A startup in a rapid growth period can enjoy the scalability of IaaS.
- **Testing and development:** IaaS allows teams to quickly set up and tear down testing and development environments, allowing new applications to make it to market more quickly.
- **Storage and backup:** Using IaaS for data storage and backup allows an organization to maintain resiliency without the significant overhead of additional on-site hardware. Using an IaaS provider can also help the team manage legal and compliance requirements that may otherwise be difficult to understand or implement.
- **Building and maintaining web applications:** IaaS provides the infrastructure needed to support web applications, such as storage, servers, and networking resources. Web applications can be quickly deployed on IaaS and then can continue to scale up and down with demand, providing reliability for the platform and cost savings for the team. 
- **High-performance computing needs:** Organizations can solve complex problems and conduct detailed research and data analysis using supercomputers and computer grids or clusters. IaaS can provide the infrastructure to maintain those needs. Game developers and streaming services also utilize IaaS for flexibility, maintaining low latency, and saving bandwidth.

### IaaS Pricing
Common IaaS pricing generally follows one of these models:
#### Subscriptions: 
Some providers offer discounts for customers who commit to longer contract terms. Pricing for subscription-based services can be more favorable but also locks you into a vendor for a set amount of time, which can be a disadvantage if your needs change or your experience with that vendor is not up to your expectations.
#### Pay-as-you-go: 
The most common way for traditional IaaS providers to bill is by the hour/second, and users are only charged for what they use. This is beneficial in that generally, a pay-as-you-go model enables you to switch cloud providers easily if needed, and your bill may go up and down depending on usage. However, it can also lead to unexpected increases in cost if usage goes up and pricing models are not always clear.







