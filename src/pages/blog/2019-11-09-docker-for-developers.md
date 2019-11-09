---
templateKey: blog-post
title: Docker for Developers
date: 2019-11-09T08:19:32.101Z
description: >-
  Docker is an engine that runs containers. As a tool, containers allow you to
  solve many challenges created in the growing DevOps trend.
featuredpost: true
featuredimage: /img/docker-logo.png
tags:
  - docker
---
## What is Docker ?

Docker Container is a standardized unit which can be created on the fly to deploy a particular application or environment. It could be an Ubuntu container, CentOs container, etc. to full-fill the requirement from an operating system point of view. Also, it could be an application oriented container like CakePHP container or a Tomcat-Ubuntu container etc.

## Solves Dependency Conflicts

Without containers, the dependencies and files are all placed together on a server. Since managing these dependencies is time-consuming, similar apps are typically grouped on the same server, sharing their dependencies:

![](/img/6418915167043584.svg)

Containers solve this problem since each app will run inside its own container with its own dependencies. Your typical server would look like:

![](/img/4552647455539200.svg)

Each container encapsulates its own dependencies. Which means you can migrate the PHP runtime from version 5.6 to 7.2 in a container without it affecting others. Any other container that would use, for instance, Node.JS would not interfere with any of the Wordpress containers.



**_Reference:_**

* https://www.edureka.co/blog/what-is-docker-container
