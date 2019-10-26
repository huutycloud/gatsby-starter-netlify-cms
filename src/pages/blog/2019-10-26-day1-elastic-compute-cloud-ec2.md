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
