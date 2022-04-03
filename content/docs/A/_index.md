---
title: "A"
linkTitle: "A"
weight: 4
description: >
  Automation
---

<!-- {{% pageinfo %}}
Automation
{{% /pageinfo %}} -->

> The rule of the cloud is to ruthlessly automate everything
>
> \- Patrick Gelsinger, CEO Intel, ex-CEO VMWare

Apart from taking advantage of compute resources, such as a remote server or a database, cloud computing in its essence deals with automation of the software delivery process. The following are the 3 steps that are automated in this delivery process:

### Application Development

There are several tasks that a developer would like to include in their development workflow such as running unit tests, deploying the application on each new change, let's say this change is making a new commit to a GitHub repository. Such repetitive tasks can be automated on GitHub with the help of **A**ctions.

### Deployment Configuration

Say you are building a Python or a Node.js web application. What software does your local machine need to run this project? Let's start from the basics, an operating system. Node.js or the Python interpreter to run the scripts that you'll write, `npm` or `pip` to install and manage the required dependencies and so on. Now what if you have to deploy this application, say on Heroku or Google **A**pp Engine. You only provide the source code and the list of dependencies to it. However, behind the scenes, there are a lot more configurations that are done for you. Such as the choice of the machine/server on which your code will run, the operating system it will run on, etc. All of this is part of deployment configuration which is automated for you. As a developer, you only provide the code and the platform does the configurations for you.

This concept can also be extended to Infrastructure-as-Code. What if you want to specify the kind of machine your code should run on, the operating system that your code runs on, the version of Python or Node.js runtime that you need? With this, you have a lot more configurations to be done on your own. For big companies, with many such applications deployed, imagine how many such configurations they have to specify for each deployment? In order to automate configurations for Infrastructure-as-Code, many cloud technologies are available today, namely **A**nsible, Puppet, Chef.

### Scaling

Imagine you have built a web application deployed using some cloud service and is accessed by hundreds of users every week. Let's say it is your personal blog. One of your stories becomes a major hit and now you get thousands of users visitng your website, interacting with it. We can say that now there is an increased _load_ on your website. How will you deal with this? This additional load can be carried out by autoscaling which is provided out of the box by most cloud platforms providing compute resources. By autoscaling, the number of servers or virtual machines running on a single server can be _scaled_ as per the load without requiring any manual intervention.
