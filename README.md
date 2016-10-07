
# Purpose

An **Application Development Environment** (ADE) can be defined as "used to
build enterprise-wide applications that need to be executed and tested on an
array of different computing devices and back-end or integrated platforms."
Since Predix is using **Cloud Foundry** (CF) as the foundation for the PaaS it
can be helpful to have a uniform development environment for building
applications.

This repository contains the Dockerfile used to build an image containing `cf`,
`uaac`, and a few other basic development tools in a linux environment.  By
doing this on docker native users of linux, osx, and windows can have a uniform
experience.

By using *phusion* rather than *alpine* we have a larger image but many common
tools are included such as `git`, `curl`, `tar`, `cron`, etc.

Additionally more language specific application development environments
include tools commonly used among Predix developers.

- py including `pip`, `virtualenv`, etc.
- js including `gulp`, `bower`, etc.
- java including `mvn`, etc.

# Setup

If you haven't already, install Docker for your native environment.
https://docs.docker.com/engine/installation/

You can pull one of my pre-built images by running:

```
docker run --rm --volume=$(pwd):/home/app -it j12y/cf-ade
```

If you prefer or need to customize you can also fork or clone this repos and
build an image locally.

```
docker build -t j12y/cf-ade .
```

You can then find it in your `docker images`.


