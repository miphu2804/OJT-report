---
title : "Job Build ECR"
date : 2024-01-01
weight : 4
chapter : false
pre : " <b> 4.6.4 </b> "
---

#### Job Build ECR gồm những task

1. **Login ECR**: xác thực vào registry.
2. **Build image**: build Docker image backend.
3. **Push image**: đẩy image lên ECR.

#### Vai trò

+ Cập nhật phiên bản backend image cho môi trường deploy.
