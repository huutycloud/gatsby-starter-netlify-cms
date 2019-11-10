---
templateKey: blog-post
title: A Practical Guide to Kubernetes - P2
date: 2019-11-10T09:03:39.439Z
description: >-
  Kubernetes Services provide addresses through which associated Pods can be
  accessed.
featuredpost: true
featuredimage: /img/kubernetes.png
tags:
  - kubernetes
---
## ClusterIP

ClusterIP (the default type) exposes the port only inside the cluster. Such a port would not be accessible from anywhere outside. ClusterIP is useful when we want to enable communication between Pods and still prevent any external access.

## Why Use Ingress Objects?

> Ingress objects manage external access to the applications running inside a Kubernetes cluster.

## The Volumes

> We can describe Volumes as a way to access a file system that might be running on the same host or somewhere else. No matter where that file system is, it is external to the containers that mount volumes. There can be many reasons why someone might mount a Volume, with state preservation being only one of them.

## Creating A Production-Ready Kubernetes Cluster

Creating a Kubernetes cluster is not trivial. We have to make many choices, and we can easily get lost in the myriad of options. The number of permutations is getting close to infinite and, yet, our clusters need to be configured consistently.
