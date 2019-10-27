---
templateKey: blog-post
title: 'Day2: Elastic Load Balancing and Auto Scaling'
date: 2019-10-26T13:51:29.626Z
description: Elastic Load Balancing and Auto Scaling
featuredpost: true
featuredimage: /img/chemex.jpg
tags:
  - aws
  - elb
---
## What is Auto Scaling ?

When instance meet a condition. Instance will automatically increase or decrease resource for responsible keep application working stable.

## What is IAM Roles ?

An IAM role is an IAM identity that you can create in your account that has specific permissions.

![](/img/elb.png)

## Elastic Load Blancing Concepts

A load balancer accepts incoming traffic from clients and routes requests to its registered targets (such as EC2 instances) in one or more Availability Zones. The load balancer also monitors the health of its registered targets and ensures that it routes traffic only to healthy targets. When the load balancer detects an unhealthy target, it stops routing traffic to that target. It then resumes routing traffic to that target when it detects that the target is healthy again.

## Elastic Load Balancing supports three types of load balancers:
**Application Load Balancers**
* Operates at the request level
* Routes based on the content of the request (layer 7)

**Network Load Balancers**
* Operates at the connection level
* Routes connection based on IP protocol data (layer 4)

**Classic Load Balancers**
* Performs routing at the Layer 4 and Layer 7
* Old generation; not recommended for new application
