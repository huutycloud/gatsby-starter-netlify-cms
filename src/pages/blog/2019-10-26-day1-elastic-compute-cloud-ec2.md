---
templateKey: blog-post
title: 'Day1: Elastic Compute Cloud (EC2)'
date: 2019-10-26T13:09:33.387Z
description: Elastic Compute Cloud (EC2)
featuredpost: true
featuredimage: /img/blog-index.jpg
tags:
  - aws
  - ec2
---
## Overview

Elastic Compute Cloud (EC2) is a service help a user create a virtual machine in cloud. Some people call that by VPS.

AWS Free Tier provides 720 hours run t2.micro to run Windows or Linux operation system instance.

## Terms

AMI: Amazon Machine Images (AMI) is a snapshot of operation system. We use AMI to create an instance. One AMI can have many instances.

EBS: Amazon Elastic Block Store is a volume to store data and OS. Look like an SSD or HDD in your laptop.

## Launch an EC2 Instance

<https://aws.amazon.com/premiumsupport/knowledge-center/launch-instance-custom-ami/>

## Security Group

Security Group is a firewall in instance level.

Inbound: Traffic rule from outside to instance. (Default not allow all)

Outbound: Traffic rule from instance to outside. (Default allow all)

## Public, Private, and Elastic IP addresses

Public IP address:

* Lost when the instance is stopped
* Used in Public Subnets
* No charge
* Associated with a private IP address on the instance

Private IP address:

* Retained when the instance is stopped
* Used in Public and Private Subnets

Elastic IP address:

* Static Public IP address
* You are charged if not used
* Associated with a private IP address on the instance

## NAT Instance vs NAT Gateway

NAT Instance:

* Managed by you
* Can you as a bastion host
* Scale up (instance type) manually and use enhanced networking
* Need to assign Security Group
* No high availability
* Can impliment port forwarding through manual customisation

NAT Gateway

* Managed by AWS
* Cannot access through SSH
* Elastic scalability up to 45Gbps
* No Security Group
* Provides automatic high availability within an AZ and can be placed in multiple AZs
* Does not support port forwarding
