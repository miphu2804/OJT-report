---
title : "Terraform Variables"
date : 2024-01-01
weight : 5
chapter : false
pre : " <b> 5.5. </b> "
---

#### terraform.tfvars.example

1. **Nhóm hạ tầng**: VPC, subnet, AZ, CIDR.
2. **Nhóm compute**: instance type, ASG size.
3. **Nhóm storage**: S3 buckets, ECR repo.
4. **Nhóm database**: engine, size, username.
5. **Nhóm security**: CIDR cho SSH, allowed origins.

#### Giá trị mẫu

+ `region = "us-east-1"`
+ `asg_min = 1`, `asg_max = 3`
+ `db_engine = "postgres"`
