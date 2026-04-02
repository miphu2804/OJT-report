---
title : "Đăng ký TLS cert bằng ACM + Route53 trong CI/CD"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 4.7.3.1 </b> "
---

#### Hướng dẫn tổng quan

1. Tạo request certificate trên ACM.
2. Xác thực domain qua DNS (Route53).
3. Khi chứng chỉ ISSUED, pipeline dùng ARN để cấu hình HTTPS.

#### Cách làm trong CI/CD

1. Terraform tạo ACM certificate.
2. Terraform tạo DNS validation records trong Route53.
3. Pipeline chờ ACM verified rồi apply tiếp.
