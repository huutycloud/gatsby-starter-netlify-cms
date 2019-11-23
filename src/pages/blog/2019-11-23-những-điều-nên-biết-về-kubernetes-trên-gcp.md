---
templateKey: blog-post
title: Những điều nên biết về Kubernetes trên GCP
date: 2019-11-23T12:55:48.721Z
description: Trong bài viết này mình sẽ hướng dẫn sử dụng K8S trên Google Cloud Platform
featuredpost: true
featuredimage: /img/kubernetes.png
tags:
  - kubernetes
---
# Mỗi vài khái niệm cần biết trước khi tìm hiểu về K8S

## Container

> A container image is a lightweight, stand-alone,
>  executable package of a piece of software that
>  includes everything needed to run it: code,
>  runtime, system tools, system libraries, settings. 

## Docker

> Docker is a tool that can package an
>  application and its dependencies in a virtual
>  container that can run on any Linux server.

## Kubernetes

> Orchestration technology for containers -
>  convert isolated containers running on
>  different hardware into a cluster

# Thử tạo một Cluster chứa Wordpress trên GCP

Bước 1: Mở Cloud Shell

Chạy lệnh sau để thiết lập vùng AZ mặc định

`gcloud config set compute/zone us-central1-a`

`gcloud config set compute/region us-central1`

Kết quả: 

```
huutycloud@cloudshell:~ (phonic-formula-254913)$ gcloud config set compute/zone us-central1-a
Updated property [compute/zone].
huutycloud@cloudshell:~ (phonic-formula-254913)$ gcloud config set compute/region us-central1
Updated property [compute/region].
```

Bước 2: Khởi tạo Cluster bao gồm 1 Node duy nhất

`gcloud container clusters create my-first-cluster --num-nodes 1`

Nếu các bạn bị lỗi thì nhớ kích hoạt Kubernetes Engine API bằng cách vào đường link ở lỗi

![](/img/error-not-enable-api-k8s.jpg)

![](/img/error-not-enable-api-k8s-2.jpg)
