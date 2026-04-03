---
title : "Hướng dẫn setup FE bằng Amplify"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 4.7.1 </b> "
---

#### Amplify là gì

+ AWS Amplify là dịch vụ triển khai frontend giúp tự động build, host và quản lý bản phát hành theo nhánh.
  

#### Kết nối với repo GitHub

1. Tạo app Amplify mới.
2. Chọn **GitHub** và cấp quyền truy cập.
3. Chọn repo EduTrust và nhánh triển khai.

#### Chọn branch

+ Chọn branch theo môi trường (staging/production).
+ Bật auto-deploy nếu cần đồng bộ bản phát hành theo commit.

#### Đăng ký custom domain

1. Vào **Domain management**.
2. Thêm domain và tạo record DNS theo hướng dẫn.
3. Chờ xác minh để bật HTTPS.

#### Cấu hình file amplify.yml

+ Khai báo bước `install`, `build`, `artifacts` theo framework.
+ Đảm bảo đúng thư mục output để build thành công.
