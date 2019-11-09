---
templateKey: blog-post
title: A Practical Guide to Kubernetes
date: 2019-11-09T14:43:02.465Z
description: >-
  Kubernetes was first developed by a team at Google. It is based on their
  experience from running containers at scale for years. Later on, it was
  donated to Cloud Native Computing Foundation (CNCF). It is a true open source
  project with probably the highest velocity in history.
featuredpost: true
featuredimage: /img/kubernetes.png
tags:
  - kubernetes
---


## What is Kubernetes?

Kubernetes was first developed by a team at Google. It is based on their experience from running containers at scale for years. Later on, it was donated to Cloud Native Computing Foundation (CNCF). It is a true open source project with probably the highest velocity in history.

![](/img/5275456112689152.svg)

## Why Kubernetes?

* We can use it to deploy our services, to roll out new releases without downtime, and to scale (or de-scale) those services.
* It is portable.
* It can run on a public or private cloud.
* It can run on-premise or in a hybrid environment.
* We can move a Kubernetes cluster from one hosting vendor to another without changing (almost) any of the deployment and management processes.
* Kubernetes can be easily extended to serve nearly any needs. We can choose which modules we’ll use, and we can develop additional features ourselves and plug them in.
* Kubernetes will decide where to run something and how to maintain the state we specify.
* Kubernetes can place replicas of a service on the most appropriate server, restart them when needed, replicate them, and scale them.
* Self-healing is a feature included in its design from the start. On the other hand, self-adaptation is coming soon as well.
* Zero-downtime deployments, fault tolerance, high availability, scaling, scheduling, and self-healing add significant value in Kubernetes.
* We can use it to mount volumes for stateful applications.
* It allows us to store confidential information as secrets.
* We can use it to validate the health of our services.
* It can load balance requests and monitor resources.
* It provides service discovery and easy access to logs.

## Understanding kubectl

Kubernetes’ command-line tool, `kubectl`, is used to manage a cluster and applications running inside it. We’ll use `kubectl` a lot throughout the book, so we won’t go into details just yet. Instead, we’ll discuss its commands through examples that will follow shortly. For now, think of it as your interlocutor with a Kubernetes cluster.

![](/img/kubectl.svg)

Linux

```
curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
```
