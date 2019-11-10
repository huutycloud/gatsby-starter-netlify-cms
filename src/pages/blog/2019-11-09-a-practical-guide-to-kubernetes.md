---
templateKey: blog-post
title: A Practical Guide to Kubernetes - P1
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

## Understanding Minikube

Linux
Minikube supports several virtualization technologies. We’ll use VirtualBox throughout the book since it is the only virtualization supported in all operating systems. If you do not have it already, please head to the Download VirtualBox page and get the version that matches your OS.

```
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/
```

You must turn off Secure Boot on BIOS and run this command to create a Local Kubernetes Cluster with Minikube.

`minikube start --vm-driver=virtualbox`

## Pods

Pods are equivalent to bricks we use to build houses. Both are uneventful and not much by themselves. Yet, they are fundamental building blocks without which we could not construct the solution we are set to build.

> A Pod is a way to represent a running process in a cluster.

## Why Single-container Pods?

> A Pod is a collection of containers. However, that does not mean that multi-container Pods are common. They are rare. Most Pods you’ll create will be single container units.

## Understanding ReplicaSets

Most applications should be scalable and all must be fault tolerant. Pods do not provide those features, ReplicaSets do.

> ReplicaSet’s primary function is to ensure that the specified number of replicas of a service are (almost) always running.

go-demo-2.yml

```
apiVersion:  apps/v1
kind: ReplicaSet
metadata:
  name: go-demo-2
spec:
  replicas: 2
  selector:
    matchLabels:
      type: backend
      service: go-demo-2
  template:
    metadata:
      labels:
        type: backend
        service: go-demo-2
        db: mongo
        language: go
    spec:
      containers:
      - name: db
        image: mongo:3.3
      - name: api
        image: vfarcic/go-demo-2
        env:
        - name: DB
          value: localhost
        livenessProbe:
          httpGet:
            path: /demo/hello
            port: 8080
```

`kubectl create -f rs/go-demo-2.yml`

`kubectl get rs`

![](/img/5998773148844032.png)
