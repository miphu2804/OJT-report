---
title : "Giải thích DNS records trong Route53"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 4.7.3.3 </b> "
---

#### Các record thường gặp

1. **A/AAAA**: trỏ domain về IP.
2. **CNAME**: trỏ alias domain về tên khác.
3. **NS**: nameserver của Hosted Zone.
4. **TXT**: xác thực domain, SPF/DKIM.
5. **ALIAS**: trỏ về dịch vụ AWS như CloudFront.

#### Trong workshop

+ **ALIAS** trỏ domain về Amplify/CloudFront.
+ **CNAME/TXT** dùng để xác thực ACM.
