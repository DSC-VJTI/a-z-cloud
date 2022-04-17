---
title: "N"
linkTitle: "N"
weight: 4
description: >
  ## Nginx
---

> Note: Nginx is pronounced as "engine-ex".

Nginx is an open-source web server that, since its initial success as a web server, is now also used as a reverse proxy, HTTP cache, and load balancer.

Some high-profile companies using Nginx include Autodesk, Atlassian, Intuit, T-Mobile, GitLab, DuckDuckGo, Microsoft, IBM, Google, Adobe, Salesforce, VMWare, Xerox, LinkedIn, Cisco, Facebook, Target, Citrix Systems, Twitter, Apple, Intel, and many more.

Nginx was originally created by Igor Sysoev, with its first public release in October 2004. Igor initially conceived the software as an answer to the C10k problem, which is a problem regarding the performance issue of handling 10,000 concurrent connections.

Because its roots are in performance optimization under scale, Nginx often outperforms other popular web servers in benchmark tests, especially in situations with static content and/or high concurrent requests.

### How Does Nginx Work?

Nginx is built to offer low memory usage and high concurrency. Rather than creating new processes for each web request, Nginx uses an asynchronous, event-driven approach where requests are handled in a single thread.

With Nginx, one master process can control multiple worker processes. The master maintains the worker processes, while the workers do the actual processing. Because Nginx is asynchronous, each request can be executed by the worker concurrently without blocking other requests.

### Benefits Of Using Nginx

- Installations and configurations are simple and easy

- Fastest and the best for serving static files

- Compatibility with commonly-used web apps

- Load Balancing Support

- No risk in switching over to Nginx

- Support from Nginx service professionals
