---
title: "V"
linkTitle: "V"
weight: 4
description: >
  ## Virtualization
---

> Server consolidation is the most obvious, long-standing use case, but virtualization is like a Swiss army knife. You can use it in a number of different situations.
>
> \- Raghu Raghuram, CEO VMWare

The act of abstracting the underlying hardware to provide useful IT services to the end-user is called as virtualization. Also abbreviated as _v12n_, virtualization helps in full utilization of a machine's capacity by distributing its capabilities across users and environments.

A common example of virtualization is a virtual machine where the hardware is abstracted from the user and multiple operating systems can be run on the same hardware. When we make use of [Google Compute Engine]({{< relref "google-compute-engine.md" >}} "Google Compute Engine"), a new virtual machine is created on a remote server for our use. Thus, the server's hardware is partitioned to provide some compute power to the customer.

### Hypervisor

<p align="center">
    <img src="hypervisor.png" alt="Role of Hypervisors in Virtualization" height="60%" width="60%" />
</p>

A hypervisor is software that creates and runs virtual machines (VMs). A hypervisor, sometimes called a virtual machine monitor (VMM), isolates the hypervisor operating system and resources from the virtual machines and enables the creation and management of those VMs.

The physical hardware, when used as a hypervisor, is called the host, while the many VMs that use its resources are guests.

The hypervisor treats resources—like CPU, memory, and storage—as a pool that can be easily reallocated between existing guests or to new virtual machines.

Multiple different operating systems can run alongside each other and share the same virtualized hardware resources with a hypervisor. This is a key benefit of virtualization. Without virtualization, you can only run 1 operating system on the hardware.

### Virtualization v/s Containerization

<p align="center">
    <img src="v12n-vs-containerization.png" alt="Virtualization v/s Containerization" height="80%" width="80%" />
</p>

At a high level, containers and VMs seem similar. They are both packaged computing environments that combine various IT components and isolate them from the rest of a system. The important distinction is in how they scale and their portability.

A container is a set of 1 or more processes that are isolated from the rest of the system. The container allows the process to access only the resource requests that have been specified. These resource limits ensure that the container is able to run on a node that has enough capacity.

VMs contain their own operating system (OS), allowing them to perform multiple resource-intensive functions at once. The increased resources available to VMs allow them to abstract, split, duplicate, and emulate entire servers, OSs, desktops, databases, and networks.

A hypervisor also allows you to run multiple operating systems in VMs, but containers are only able to run a single type of operating system. A container running on a Linux server, for example, is only able to run a Linux operating system.

Moreover, with a hypervisor, different kinds of virtualization can be implemented, such as:

- Desktop virtualization

- Data virtualization

- Server virtualization

- Network virtualization

- Operating system virtualization

Windows Subsystem For Linux 2 ([WSL2](https://docs.microsoft.com/en-us/windows/wsl/about)) is a novel example of operating system virtualization by which Windows and a Linux-based OS can be used side-by-side in the Windows host operating system.
