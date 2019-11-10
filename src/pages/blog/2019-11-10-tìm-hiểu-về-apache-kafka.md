---
templateKey: blog-post
title: Tìm hiểu về Apache Kafka
date: 2019-11-10T15:00:11.044Z
description: Tìm hiểu về Apache Kafka
featuredpost: true
featuredimage: /img/apache-kafka.png
tags:
  - kafka
---
## Zookeeper là gì ?

Zookeeper là một dịch vụ (một server) tập trung cho việc duy trì thông tin cấu hình, đặt tên, cung cấp sự đồng bộ phân tán, cung cấp dịch vụ nhóm.

## **Trách nhiệm của Zookeeper trong Kafka**

* Đăng ký tiến trình
* Duy trì một danh sách topics cùng nhau
* Thực hiện nắm quyền điều hành trong trường hợp tiến trình bị ngắt
* Lưu trữ Kafka cluster id
* Store ACLs (Access Control Lists) nếu bảo mật được bật

Một cụm Kafka thường có số lượng máy chủ là 1,3,5,7,9. Mình sẽ sử dụng 3 con server để đảm bảo tính sẵn sàng cao của Kafka Cluster.

**_Reference:_**

https://stackjava.com/apache-kafka/zookeeper-la-gi-tim-hieu-apache-zookeeper.html
