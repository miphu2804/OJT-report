---
title : "Terraform Infrastructure"
date : 2024-01-01
weight : 5
chapter : true
pre : " <b> 4.5. </b> "
---

#### How to run

1. Run local: `terraform init` → `plan` → `apply`.
2. Run via CI/CD: use a pipeline with Terraform steps.

#### Resources created

+ VPC, subnets, route tables.
+ ALB, ASG, EC2.
+ S3 buckets, ECR.
+ RDS or database service.
+ IAM roles and policies.
