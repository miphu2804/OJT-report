---
title : "CI/CD Pipeline"
date : 2024-01-01
weight : 6
chapter : true
pre : " <b> 4.6. </b> "
---

#### Flow diagram

CI → Packer → Terraform → Build ECR → ASG Rolling Update

#### Notes

+ CI runs lint/test.
+ Packer builds AMI.
+ Terraform updates infra.
+ ECR stores images.
+ ASG rolling updates backend.
