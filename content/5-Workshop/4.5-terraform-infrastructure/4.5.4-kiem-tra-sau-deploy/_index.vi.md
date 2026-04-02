---
title : "Kiểm tra sau deploy"
date : 2024-01-01
weight : 4
chapter : false
pre : " <b> 4.5.4 </b> "
---

#### Checklist kiểm tra

1. Kiểm tra `terraform output` có giá trị hợp lệ.
2. Xác nhận tài nguyên ở trạng thái **Active/Healthy** trên AWS Console.
3. Kiểm tra endpoint truy cập được và không lỗi 5xx.
4. Kiểm tra tagging/cost control nếu có quy ước nội bộ.
