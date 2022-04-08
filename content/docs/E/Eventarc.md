---
title: "Eventarc"
weight: 4
description: >
  A unified eventing experience in Google Cloud.
---

Docker provides various services such as the Docker daemon (`dockerd`), Docker CLI, and Docker Hub Registry that help package applications in containers and host them. As we learned in [containers]({{< relref "containers.md" >}} "Containers"), the several problems of software not being able to run on some machine and portability of software are solved by containers and Docker provides salient tools to make it possible.

![Docker logo](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Docker_%28container_engine%29_logo.svg/915px-Docker_%28container_engine%29_logo.svg.png)

## Docker architecture

Let's discuss the architecture of Docker Engine which comprises of Docker client (CLI), Docker Host that contains the Docker daemon which manages the different containers, and the software that needs to be packaged to a container i.e., an image made available on a registry.

![Docker architecture](https://www.researchgate.net/profile/Yahya-Al-Dhuraibi/publication/308050257/figure/fig1/AS:433709594746881@1480415833510/High-level-overview-of-Docker-architecture.png)

### Docker Hub

This is the default registry that Docker uses to fetch _images_ to be run inside containers. But what is an image? A Docker image is a template file that contains the instructions to create a container. Each image has a base image typically a minimal Linux-based operating system such as Alpine and on top of this image, we can add layers of our own images. This can be done using a `Dockerfile`.

The following is an example `Dockerfile`:

```Dockerfile
FROM python:3.7
LABEL maintainer="Pankaj Khushalani"

COPY ./exercises/python-helloworld /app
WORKDIR /app
RUN pip install -r requirements.txt

CMD [ "python", "app.py" ]
```

Each line contains a keyword following by a flag or a command to be run. In the first line of the `Dockerfile`, the base image follows the `FROM` keyword. Here, `python:3.7` is the name of the base image, which is hosted on Docker Hub and is downloaded when this `Dockerfile` is run. `python:3.7` contains the Linux-based light-weight OS Alpine which comes with Python version 3.7 installed on it.

### Docker daemon

This is the server that hosts and manages the several Docker containers that we would like to run. The communication between different containers is also handled by the daemon. It also plays an important role in creating a Docker container from images pulled from Docker Hub.

### Docker CLI

You can interact with the Docker daemon using Docker CLI. This includes creating a Docker container from a `Dockerfile` or an image directly fetched from Docker Hub, interacting with a Docker container, managing them, etc. You can read the [documentation](https://docs.docker.com/engine/reference/commandline/cli/) for the list of available commands.

## Learn

- Install Docker and have a go at it! Docker Engine comes with Docker Desktop for Windows and macOS, while for Linux distributions, Docker Engine can directly be downloaded and used. You can find the installation guide [here](https://docs.docker.com/engine/install/).

- [DevOps with Docker](https://devopswithdocker.com/) is an MOOC by the University of Helsinki and a great resource to learn the ins and outs of Docker.

- A [video tutorial](https://youtu.be/3c-iBn73dDE) on Docker from Tech World With Nana
