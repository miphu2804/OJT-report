---
title : "Custom Domain & HTTPS"
date : 2024-01-01
weight : 10
chapter : false
pre : " <b> 5.10. </b> "
---

#### 2 cách cấu hình

1. **Dùng ARN có sẵn**: nhập ARN chứng chỉ ACM.
2. **Terraform tự tạo**: tạo ACM + Route53.

#### Ghi chú

+ DNS cần trỏ đúng về Amplify/CloudFront.
+ Chờ chứng chỉ phát hành trước khi bật HTTPS.
