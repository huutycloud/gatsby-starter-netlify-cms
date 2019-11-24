---
templateKey: blog-post
title: Thực hành về các lệnh thao tác trên GCP Kubernetes
date: 2019-11-24T13:57:15.560Z
description: >-
  Trong bài này mình sẽ hướng dẫn các bạn thao tác với K8S bằng Command Line và
  file YAML Definition.
featuredpost: true
featuredimage: /img/5275456112689152.svg
tags:
  - kubernetes
---
1. Lệnh kubectl run

`kubectl run first-deployment --image=nginx`

`kubectl get pods`

`kubectl exec -it first-deployment-774f957bb7-52b24 -- /bin/bash`

`echo Hello nginx! > /usr/share/nginx/html/index.html`

`apt-get update`

`apt-get install curl`

`curl localhost`

Kết quả:

```
root@first-deployment-774f957bb7-52b24:/# curl localhost
Hello nginx!
```
