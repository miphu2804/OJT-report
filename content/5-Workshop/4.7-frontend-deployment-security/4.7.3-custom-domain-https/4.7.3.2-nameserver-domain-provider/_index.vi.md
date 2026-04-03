---
title : "Đăng ký nameserver ở domain provider"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 4.7.3.2 </b> "
---

#### Cách làm

1. Vào Route53 → Hosted Zone của domain.
2. Copy 4 bản ghi **NS**.
3. Đăng nhập domain provider (Namecheap, GoDaddy, ...).
4. Thay nameserver mặc định bằng NS của Route53.

#### Lưu ý

+ DNS cần thời gian propagate (thường 5–30 phút).
