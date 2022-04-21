---
title: "R"
linkTitle: "R"
weight: 4
description: >
 Reliability
---

<!-- {{% pageinfo %}}
Reliability
{{% /pageinfo %}} -->

>As the adoption of cloud computing continues to rise, and customers demand 24/7 access to their services and data, reliability remains a challenge for cloud service providers everywhere. It’s not a matter of *if* an outage will occur; it’s strictly a matter of *when*. This means it’s critical for organizations to understand how best to design and deliver reliable cloud services. 
>

### What is reliability in cloud computing?

When you access an app or service in the cloud, you can reasonably expect that:
- The app or service is up and running.
- You can access what you need from any device at any time from any location.
- There will be no interruptions or downtime.
- Your connection is secure.
- You will be able to perform the tasks you need to get your job done. 

Reliability refers to the probability that the system will meet certain performance standards in yielding correct output for a desired time duration.

Reliability can be used to understand how well the service will be available in context of different real-world conditions. For instance, a cloud solution may be available with a Service Level Agreement (SLA) commitment of 99.999 percent, but vulnerabilities to sophisticated cyber-attacks may cause IT outages beyond the control of the vendor. As a result, the service may be compromised for several days, thereby reducing the effective availability of the IT service.


### How can you measure Reliability?

In an ideal world, your system would be 100% reliable. But that is probably not an attainable goal. In the real world, things will go wrong. You will see faults from things such as server downtime, software failure, security breaches, user errors, and other unexpected incidents. 

The Reliability of a system is challenging to measure. There may be several ways to measure the probability of failure of system components that impact the availability of the system.
A common metric is to calculate the Mean Time Between Failures (MTBF).

**MTBF = (total elapsed time – sum of downtime)/number of failures**

MTBF represents the time duration between a component failure of the system. Similarly, organizations may also evaluate the Mean Time To Repair (MTTR), a metric that represents the time duration to repair a failed system component such that the overall system is available as per the agreed SLA commitment.

Other ways to measure reliability may include metrics such as fault tolerance levels of the system. Greater the fault tolerance of a given system component, lower is the susceptibility of the overall system to be disrupted under changing real-world conditions.
The measurement of Reliability is driven by the frequency and impact of failures.

For either metric, organizations need to make decisions on how much time loss and frequency of failures they can bear without disrupting the overall system performance for end-users. Similarly, they need to decide how much they can afford to spend on the service, infrastructure and support to meet certain standards of availability and reliability of the system.

### How To Achieve Reliability In The Cloud?

If we accept the fact failures will occur, then the outcomes that organizations may want to consider in relation to their cloud services, fall into four main categories:
1. **Maximize service availability to customers.**               
	Make sure the service does what the customer wants, when they want it, as much of the time as possible.
2. **Minimize the impact of any failure on customers.**                      
	Assume something will go wrong and design the service in a way that it will be the non-critical components that fail first; the criticalcomponents keep working. Isolate the failure as much as possible so the minimum number of customers is impacted. And if the service goes down completely, focus on reducing the amount of time any one customer cannot use the service at all.
3. **Maximize service performance.**                     
	Reduce the impact to customers at times when performance may be negatively impacted, such as during an unexpected spike in traffic.
4. **Maximize business continuity.**                           
	Focus on how the organization and the service respond when a failure occurs. Automate recovery where possible and disaster recovery drills should be carried out to ensure the organization is fully prepared to deal with the inevitable failure.

However, there are three best practices for reliability in the cloud. Following these practices may negate some or all of the scenarios listed above:
- Foundations
- Change Management
- Failure Management

To achieve reliability, a system must have a well-planned foundation and monitoring in place, with mechanisms for handling changes in demand or requirements. The system should be designed to detect failure and automatically heal itself.

#### Foundations

Before architecting any system, foundational requirements that influence reliability should be in place. For example, you must have sufficient network bandwidth to your data centre. These requirements are sometimes neglected (because they are beyond a single project's scope). This neglect can have a significant impact on the ability to deliver a reliable system. In an on-premises environment, these requirements can cause long lead times due to dependencies and therefore must be incorporated during initial planning.

#### Change Management

Being aware of how change affects a system allows you to plan proactively, and monitoring allows you to quickly identify trends that could lead to capacity issues or SLA breaches. In traditional environments, change-control processes are often manual and must be carefully coordinated with auditing to effectively control who makes changes and when they are made.

#### Failure Management

In any system of reasonable complexity, it is expected that failures will occur. It is generally of interest to know how to become aware of these failures, respond to them, and prevent them from happening again.
Regularly back up your data and test your backup files to ensure you can recover from both logical and physical errors. A key to managing failure is the frequent and automated testing of systems to cause failure, and then observe how they recover. Do this on a regular schedule and ensure that such testing is also triggered after significant system changes.
The objective is to thoroughly test your system-recovery processes so that you are confident that you can recover all your data and continue to serve your customers, even in the face of sustained problems. Your recovery processes should be as well exercised as your normal production processes.


### How reliable is Google Cloud?

Nothing is 100% reliable. When designing application architecture, you have to assume there will be failures. Historically, this has meant deploying across racks, rooms and data centres to ensure that local switch, power and geographic incidents do not affect your entire infrastructure.
When deploying on the cloud, this translates to deploying across zones and regions. A zone is supposed to be isolated from other zones but close enough to allow low latency and low cost networking. However, since zones are close by, they are still susceptible to geographic events e.g. Storms. That’s why you deploy across multiple regions. For complete redundancy, provider diversity is the ultimate goal.
Because each zone is an independent entity, zone failures do not affect other zones.

From the latest Outage, we can see that Google has added multiple layers of protection that were not present in previous outages. These include:
1. **Automation:** Using tools to apply configuration changes makes it easy to do them consistently and repeatedly. You mitigate human errors such as typos or incorrect configurations.
2. **Verification:** Google has software which not only generates the config but also verifies it. The problem is the most recent outage was that although the verification step discovered the problems, the rollout was not aborted due to bugs in the rollout process.
3. **Staged rollouts:** The incident actually began several hours before the global impact was seen. Past outages have seen changes applied globally at the same time but now changes are rolled out gradually. Unfortunately this didn’t help because although alerts were generated, their investigation took longer than it took to complete the global rollout.
4. **Canaries:** Rolling out changes to a small set of the entire infrastructure allows you to observe the impact in production. This step is absent from previous Google outages but is now a specific step. Unfortunately, although the canary deploy did show the problem, the rollout was not aborted due to a separate software bug.

Google Compute Engine guarantees 99.95% uptime which equates to 4 hours and 23 minutes of downtime per year.

