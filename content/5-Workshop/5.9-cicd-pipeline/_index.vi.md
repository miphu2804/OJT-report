---
title : "CI/CD Pipeline"
date : 2024-01-01
weight : 9
chapter : false
pre : " <b> 5.9. </b> "
---

#### Sơ đồ luồng

CI → Packer → Terraform → Build ECR → ASG Rolling Update

#### Ghi chú

+ CI chạy lint/test.
+ Packer build AMI.
+ Terraform update hạ tầng.
+ ECR lưu image.
+ ASG rolling update backend.
