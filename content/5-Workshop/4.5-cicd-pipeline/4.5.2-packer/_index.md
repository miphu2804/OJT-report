---
title : "Job Packer"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 4.5.2 </b> "
---

#### Trigger

- Manual workflow_dispatch.
- workflow_run success from upstream.

#### Main tasks

1. Prepare build environment and AWS credentials.
2. Initialize Packer and check build conditions.
3. Create temporary VPC for AMI build.
4. Clean old AMIs and build a new AMI.
5. Cleanup temporary networking.

#### Purpose

Standardize backend images for consistent deployment.
