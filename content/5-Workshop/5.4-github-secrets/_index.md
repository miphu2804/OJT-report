---
title : "GitHub Secrets"
date : 2024-01-01
weight : 4
chapter : false
pre : " <b> 5.4. </b> "
---

#### Required 4 secrets

1. `AWS_ACCESS_KEY_ID`
2. `AWS_SECRET_ACCESS_KEY`
3. `TERRAFORM_VARIABLES`
4. `BACKEND_ENV_FILE`

#### Notes

+ Store secrets in repo settings → Actions → Secrets.
+ `TERRAFORM_VARIABLES` and `BACKEND_ENV_FILE` should use multi-line format.
