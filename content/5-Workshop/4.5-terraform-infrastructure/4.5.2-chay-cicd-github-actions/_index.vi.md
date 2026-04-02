---
title : "Chạy Terraform bằng CI/CD (GitHub Actions)"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 4.5.2 </b> "
---

#### Chạy Terraform bằng CI/CD (GitHub Actions)

1. Đảm bảo secrets đã cấu hình cho pipeline.
2. Push code lên branch deploy.
3. Workflow chạy theo thứ tự `init → plan → apply`.
4. Theo dõi trạng thái trong tab **Actions**.
