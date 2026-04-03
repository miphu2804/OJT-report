---
title : "WAF Frontend"
date : 2024-01-01
weight : 4
chapter : false
pre : " <b> 4.7.4 </b> "
---

#### Bật WAFv2

1. Tạo Web ACL với managed rules.
2. Gắn Web ACL vào CloudFront/Amplify.

#### Hướng dẫn gắn WAF Frontend cho Amplify

1. Vào AWS WAF → Web ACLs → Create web ACL.
2. Chọn scope **CloudFront** và thêm managed rules.
3. Vào CloudFront → Distribution của Amplify.
4. Trong **Web Application Firewall (WAF)**, chọn Web ACL vừa tạo.
5. Lưu cấu hình và chờ cập nhật hoàn tất.

#### Lưu ý

+ Bật chế độ monitor trước khi block.
+ Theo dõi false positive để tinh chỉnh rule.
