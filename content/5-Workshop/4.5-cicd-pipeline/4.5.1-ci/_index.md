---
title : "Job CI"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 4.5.1 </b> "
---

#### Trigger

- Pull request changes in backend/IaC/CI files.
- Merge PR into main (push event).
- Manual workflow_dispatch if needed.

#### Main tasks

1. Pre-commit checks.
2. Backend tests with coverage.
3. Terraform format/validate + security scan.

#### Purpose

Ensure code quality, Terraform hygiene, and security checks before deployment.
