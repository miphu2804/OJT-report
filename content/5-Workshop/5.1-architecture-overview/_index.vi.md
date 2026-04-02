---
title : "Tổng quan kiến trúc"
date : 2024-01-01 
weight : 1
chapter : false
pre : " <b> 5.1. </b> "
---

#### Sơ đồ kiến trúc

Internet → Amplify → ALB → EC2 ASG → Backend services

#### Thành phần chính

+ **Amplify**: host frontend và kết nối domain.
+ **ALB**: phân phối request đến backend.
+ **EC2 Auto Scaling**: chạy các backend services.
+ **Backend services**: API, AI, camera events, auth.

#### Luồng dữ liệu

1. Người dùng truy cập web qua Internet.
2. Amplify phục vụ frontend và gọi API.
3. ALB điều phối request đến EC2 ASG.
4. Backend xử lý logic và trả kết quả.
