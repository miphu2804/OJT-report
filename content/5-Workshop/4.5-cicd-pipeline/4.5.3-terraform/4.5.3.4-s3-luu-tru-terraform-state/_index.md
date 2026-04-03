---
title : "S3 for Terraform State"
date : 2024-01-01
weight : 4
chapter : false
pre : " <b> 4.5.3.4 </b> "
---

#### Goal

Store Terraform state in S3 before running terraform init, ensuring consistent resource tracking.

#### Notes

State storage should be secure and versioned to prevent drift and accidental loss.
