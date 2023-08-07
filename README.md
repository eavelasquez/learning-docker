# Learning Docker

This repository contains my notes and code while learning Docker. I'm watching the [Docker - Practical Guide for Developers](https://cursos.devtalles.com/courses/docker-guia-practica/) course on DevTalles.

## Docker Overview

Docker is an open platform for developing, shipping, and running applications. Docker enables you to separete your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications. By taking advantage of Docker's methodologies for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production.

- It is runnable instance of an image. You can create, start, stop, move, or delete a container using the Docker API or CLI.
- It can be run on local machines, virtual machines, or deployed to the cloud.
- It is portable (and can be run on any OS).
- It is isolated from other containers and runs its own software, binaries, configurations, etc.

### Docker Architecture

Docker uses a client-server architecture. The Docker *client* talks to the Docker *daemon*, which does the heavy lifting of building, running, and distributing your Docker containers. The Docker client and daemon communicate using a REST API, over UNIX sockets or a network interface.

![Docker Architecture](https://docs.docker.com/assets/images/architecture.svg)

### What is a container?

A container is a sandboxed process running on a host machine that is isolated from all other processes running on that host machine. Tha isolation leverages kernel namespaces and cgroups, feature that have been in Linux for a long time. Docker makes these capabilities approachable an easy to use.

### What is a container image?

A running container uses an isolated filesystem. This isolated filesystem is provided by a container image, and the container image must contain everything needed to run an application - all dependencies, configurations, scripts, binaries, etc. The image also contains other configurations for the container, such as environment variables, a default command to run, and other metadata.

To build the container image, you'll need to use a `Dockerfile`. A `Dockerfile` is simply a text-based file with no file extension that contains a script of instructions. Docker uses this script to build a container image.
