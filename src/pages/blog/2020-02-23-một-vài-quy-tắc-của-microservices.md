---
templateKey: blog-post
title: Một vài quy tắc của Microservices
date: 2020-02-23T15:43:00.228Z
description: Một vài quy tắc của Microservices
featuredpost: true
featuredimage: /img/docker-logo.png
tags:
  - microservices
---
* Microservices không nên chia sẻ code hoặc data.
* Tránh sự phụ thuộc lẫn nhau giữa các services và software component
* Độc lập và tự trị là thứ quan trọng hơn tính sử dụng lại
* Không nên để lỗi làm ảnh hưởng tới toàn bộ hệ thống
* Mỗi microservices là một chức năng riêng
* Không được kết nối trực tiếp với nhau mà phải thông qua message bus

Lợi ích của Microservices

* Tăng tính module và dễ dàng phát triển
* Giảm sự phức tạp với lượng code nhỏ hơn
* Cho phép uodate chức năng mà không ảnh hưởng tới khả năng vận hành của toàn hệ thống
* Giảm thiểu cơ hội mà bị hỏng một số thứ không liên quan tới hệ thống
* Cho phép nhiều developer làm việc với hệ thống chung một thời điểm

Những thứ mà Microservices có thể giải quyết nhằm gia tăng hiệu suất

* Mọi thứ nên được chia tách ngoại trừ database
* Microservices sẽ giải quyết quy trình phát triển yếu kém và quy trình deployment
* Chỉ tập trung phát triển chức năng mà không cần trung gian giữa các team khác với nhau
* Phá vỡ rào cản về công nghệ phía sau
