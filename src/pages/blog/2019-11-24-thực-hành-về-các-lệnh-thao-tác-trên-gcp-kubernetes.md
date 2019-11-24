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

2. Lệnh kubectl create -f

`kubectl get pods`

`nano declarative-pod.yaml`

```
apiVersion: v1
kind: Pod
metadata:
  name: declarative-pod
spec:
  containers:
  - name: memory-demo-ctr
    image: nginx
```

`kubectl create -f declarative-pod.yaml`

(copy the pod name from get pods)

`kubectl exec -it memory-demo-ctr -- /bin/bash`

`echo Hello nginx! We are so Declarative! > /usr/share/nginx/html/index.html`

`apt-get update`

`apt-get install curl`

`curl localhost`

Kết quả:

```
root@declarative-pod:/# curl localhost
Hello nginx! We are so Declarative!
```

3. Lệnh kubectl apply -f

`kubectl get pods`

`kubectl describe po declarative-pod`

`nano declarative-pod.yaml`

`(change the image from nginx to busybox)`

(save changes and exit)

`kubectl apply -f declarative-pod.yaml`

`kubectl get pods`

`kubectl describe (updated pod)`
``
