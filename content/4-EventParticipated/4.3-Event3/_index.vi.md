---
title: "Event 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.3. </b> "
---

# Cloud Mastery Series #3: Security

### Mục Đích Của Sự Kiện

- Buổi workshop tập trung vào bảo mật AWS theo hướng thực hành, từ Networking, IAM cho đến các lớp phòng thủ nâng cao.
- Triển khai các cấu hình bảo mật mạng trên AWS như SG, NACL, VPC, CIDR, Subnet, IGW và VPC Endpoint.
- Xây dựng tài khoản AWS và quản lí user với AWS IAM, đồng thời tìm hiểu SCP, Permission Boundary, Credential Rotation và các policy/rule ràng buộc.
- Tối ưu các dịch vụ tường lửa trên AWS như WAF, Shield, Network Firewall và Firewall Manager.
- Củng cố kiến thức qua demo trực tiếp và video minh họa.

### Danh Sách Diễn Giả & Nội Dung Chi Tiết

- **Diễn giả:** Lâm An Thịnh, Nguyễn Phan Quốc Việt, Huỳnh Hoàng Long và Đặng Thị Minh Thư.
- Nội dung được triển khai theo ba mảng chính: bảo mật mạng, quản lý danh tính/quyền truy cập và phòng thủ nhiều lớp.
- Demo trực tiếp và video minh họa giúp liên kết các khái niệm với tình huống triển khai thực tế.

#### Bảo Mật Mạng Trên AWS

- VPC giúp cô lập tài nguyên theo từng môi trường và từng vùng mạng riêng.
- Security Group và Network ACL bổ sung cho nhau trong việc kiểm soát truy cập ở cấp Instance và Subnet.
- CIDR và Subnet hỗ trợ thiết kế dải mạng hợp lý, dễ mở rộng và dễ quản trị.
- Internet Gateway và VPC Endpoint giúp kiểm soát luồng truy cập giữa private resources và dịch vụ AWS.

#### Quản Lí Danh Tính Và Quyền Truy Cập Với IAM

- AWS IAM hỗ trợ quản lý user, group, role và policy theo cấu trúc rõ ràng.
- SCP và Permission Boundary giúp giới hạn quyền ở cấp tổ chức và cấp identity.
- Credential Rotation là bước quan trọng để giảm rủi ro lộ thông tin truy cập.
- Tư duy Least Privilege giúp cấp quyền đúng mức cần thiết, không dư thừa.

#### Tường Lửa Và Lớp Phòng Thủ Nâng Cao

- AWS WAF hỗ trợ lọc lưu lượng độc hại ở tầng ứng dụng.
- AWS Shield tăng khả năng chống chịu trước các cuộc tấn công DDoS.
- Network Firewall cho phép kiểm soát lưu lượng ở cấp mạng linh hoạt hơn.
- Firewall Manager giúp quản trị tập trung các chính sách bảo mật trên nhiều tài khoản và dịch vụ.

### Những Gì Học Được

#### Tư Duy Bảo Mật

Bảo mật trên AWS nên được thiết kế theo nhiều lớp, không phụ thuộc vào một công cụ đơn lẻ.

#### Quản Trị Quyền Truy Cập

IAM, SCP, Permission Boundary và Credential Rotation là bộ công cụ cốt lõi để kiểm soát quyền truy cập theo nguyên tắc tối thiểu cần thiết.

#### Phòng Thủ Nhiều Lớp

Thiết kế mạng tốt ngay từ đầu giúp giảm lỗi cấu hình và rủi ro bảo mật về sau. WAF, Shield và Network Firewall nên được xem là một phần của kiến trúc vận hành.

### Ứng Dụng Vào Công Việc

- Áp dụng tư duy phân tách mạng rõ ràng hơn cho dự án EduTrust để tổ chức tài nguyên, Subnet và luồng truy cập hợp lý.
- Xem xét quy trình quản lý user, role và policy chặt chẽ hơn để giảm rủi ro trong vận hành AWS.
- Cân nhắc bổ sung các lớp phòng thủ ở tầng ứng dụng và tầng mạng cho các dịch vụ public-facing.
- Duy trì thói quen rà soát quyền truy cập và xoay vòng Credential theo định kỳ.

### Trải nghiệm trong event

Tham gia **"Cloud Mastery Series #3: Security"** mang lại góc nhìn thực tế về bảo mật Cloud, từ cách thiết kế mạng đến quản trị truy cập và phòng thủ nhiều lớp.

#### Thực tiễn

- Các demo trực tiếp và video minh họa giúp hình dung rõ hơn cách cấu hình bảo mật trên AWS trong tình huống thực tế.
- Việc kết hợp Networking, Identity Management và Firewall cho thấy bức tranh bảo mật hoàn chỉnh hơn thay vì chỉ tập trung vào một dịch vụ riêng lẻ.

#### Bài học rút ra

- Bảo mật cần được thiết kế từ đầu, không nên chờ đến khi hệ thống đi vào vận hành mới bổ sung.
- Quyền truy cập nên theo nguyên tắc tối thiểu cần thiết và được kiểm soát ở nhiều lớp.
- Mạng riêng, phân vùng hợp lý và quản trị truy cập tốt là nền tảng cho một hệ thống AWS an toàn và bền vững.
- Tự động hóa và chuẩn hóa policy giúp giảm lỗi con người và tăng tính nhất quán khi mở rộng.