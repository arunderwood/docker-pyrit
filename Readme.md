# Docker-Pyrit

> Taming Pyrit dependencies by packaging via Docker

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Prerequisites](#prerequisites)
  - [Docker](#docker)
  - [Nvidia-docker (Optional)](#nvidia-docker-optional)
- [Usage](#usage)
- [TODO](#todo)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Prerequisites

### Docker

In order to run Docker images you must have the Docker daemon installed.

* Ubuntu - https://docs.docker.com/install/linux/docker-ce/ubuntu/
* Mac OS - https://docs.docker.com/docker-for-mac/install/
* Docker is available for many other platforms.  I have no reason to expect this package won't work on those other systems, but I have not tested them.  

### Nvidia-docker (Optional)

If you have a GPU that supports CUDA, you can install Nvidia's [special Docker daemon](https://github.com/NVIDIA/nvidia-docker) that can pass the enhanced capabilities your GPU to the container.

Nvidia-docker does not currently support MacOS but I have had success running it on Ubuntu 16.04.

Before you install nvidia-docker:

* Install the latest Nvidia graphics drivers for your platform.  These must be the official binary drivers, nvidia-docker will not work with Nouveau.
* Do not install Docker.  If you have Docker installed, the nvidia-docker package will attempt to integrate with it but this gave me nothing but trouble.  In the end, I purged Docker CE and let nvidia-docker install the version it wanted.

## Usage

>TODO

## TODO

Features to add later:

* Add docker-compose to combine Pyrit with MySQL as a storage back end
* Use multi-stage Dockerfile to build the final artifact on the `nvidia/cuda:runtime` to reduce image size
