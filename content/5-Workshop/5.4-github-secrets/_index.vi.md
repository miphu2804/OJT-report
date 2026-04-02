---
title : "GitHub Secrets"
date : 2024-01-01
weight : 4
chapter : false
pre : " <b> 5.4. </b> "
---

#### 4 secrets bắt buộc

1. `AWS_ACCESS_KEY_ID`
2. `AWS_SECRET_ACCESS_KEY`
3. `TERRAFORM_VARIABLES`
4. `BACKEND_ENV_FILE`

#### Ghi chú

+ Lưu các secrets ở repo settings → Actions → Secrets.
+ `TERRAFORM_VARIABLES` và `BACKEND_ENV_FILE` nên dùng format multi-line.
