---
title : "CI/CD Guide"
date : 2024-01-01
weight : 5
chapter : true
pre : " <b> 4.5. </b> "
---

#### Overview

This section describes the CI/CD pipeline of EduTrust and how each job works together to ensure consistent, traceable, and safe deployments.

#### Flow

CI → Packer → Terraform → Build ECR → ASG Rolling Update

#### Content

1. [Job CI](4.5.1-ci/)
2. [Job Packer](4.5.2-packer/)
3. [Job Terraform](4.5.3-terraform/)
4. [Job Build ECR](4.5.4-build-ecr/)
5. [Job ASG Rolling Update](4.5.5-asg-rolling-update/)
