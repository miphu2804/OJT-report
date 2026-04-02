---
title : "Kiểm thử HA & Security"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 4.8.2 </b> "
---

#### Mục tiêu

+ Đảm bảo hệ thống chạy ổn định, sẵn sàng cao (HA) và an toàn.

#### Test API cơ bản

1. **Health check**: `curl -I <backend_url>/health`.
2. **Auth**: login → lấy token → gọi API protected.
3. **Load nhẹ**: gửi nhiều request liên tục để kiểm tra ổn định.

#### Test FE cơ bản

1. Truy cập frontend qua Amplify.
2. Đăng nhập và thực hiện luồng chính.
3. Kiểm tra lỗi UI và API error handling.

#### Test BE cơ bản

1. Kiểm tra log lỗi trong CloudWatch.
2. Kiểm tra response time trung bình.
3. Kiểm tra retry/timeout khi backend quá tải.

#### Pentest cơ bản

+ Kiểm tra endpoint công khai có bị mở không cần auth.
+ Kiểm tra rate limit và WAF rule hoạt động.
+ Kiểm tra input validation (SQLi/XSS cơ bản).

#### Prompt & tool safety (cơ bản)

1. Kiểm tra khả năng chống prompt injection đối với các yêu cầu vượt quyền.
2. Xác thực chatbot chỉ gọi API trong phạm vi quyền được cấp (RBAC).
3. Đảm bảo chatbot không tiết lộ dữ liệu nhạy cảm hoặc thông tin nội bộ.
