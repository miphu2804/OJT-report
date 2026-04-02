---
title : "Terraform Infrastructure"
date : 2024-01-01 
weight : 7
chapter : false
pre : " <b> 5.7. </b> "
---

#### Cách chạy

1. Chạy local: `terraform init` → `plan` → `apply`.
2. Chạy qua CI/CD: dùng pipeline có bước Terraform.

#### Tài nguyên được tạo

+ VPC, subnets, route tables.
+ ALB, ASG, EC2.
+ S3 buckets, ECR.
+ RDS hoặc database service.
+ IAM roles và policies.
