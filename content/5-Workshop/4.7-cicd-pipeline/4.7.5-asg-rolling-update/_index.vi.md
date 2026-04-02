---
title : "Job ASG Rolling Update"
date : 2024-01-01
weight : 5
chapter : false
pre : " <b> 4.6.5 </b> "
---

#### Job ASG Rolling Update gồm những task

1. **Update Launch Template**: trỏ tới AMI/image mới.
2. **Rolling update**: thay thế dần instance cũ.
3. **Health check**: đảm bảo instance mới healthy.

#### Vai trò

+ Deploy backend không downtime và kiểm soát rủi ro.
