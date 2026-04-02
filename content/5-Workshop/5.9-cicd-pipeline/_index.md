---
title : "CI/CD Pipeline"
date : 2024-01-01
weight : 9
chapter : false
pre : " <b> 5.9. </b> "
---

#### Flow diagram

CI → Packer → Terraform → Build ECR → ASG Rolling Update

#### Notes

+ CI runs lint/test.
+ Packer builds AMI.
+ Terraform updates infra.
+ ECR stores images.
+ ASG rolling updates backend.
