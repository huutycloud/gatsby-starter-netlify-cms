---
templateKey: blog-post
title: A Practical Guide to Kubernetes - P2
date: 2019-11-10T09:03:39.439Z
description: >-
  Kubernetes Services provide addresses through which associated Pods can be
  accessed.
featuredpost: true
featuredimage: /img/5275456112689152.svg
tags:
  - kubernetes
---
## ClusterIP

ClusterIP (the default type) exposes the port only inside the cluster. Such a port would not be accessible from anywhere outside. ClusterIP is useful when we want to enable communication between Pods and still prevent any external access.
