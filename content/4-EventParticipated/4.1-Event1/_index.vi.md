---
title: "Event 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---


# Cloud Mastery Series: Khám phá Generative AI

### Mục Đích Của Sự Kiện

- Chia sẻ best practices trong thiết kế ứng dụng hiện đại, tối ưu hiệu năng qua CloudFront (CDN) và lưu trữ S3.
- Giới thiệu phương pháp Prompt Engineering và quy trình xây dựng AI Agent tự vận hành.
- Hướng dẫn lựa chọn compute phù hợp, so sánh từ thiết bị Edge (Raspberry Pi/Arduino) đến Cloud (Lambda/Fargate).
- Giới thiệu công cụ AI như Proptimizer và Strands Agents để tự động hóa quy trình.

### Danh Sách Diễn Giả & Nội Dung Chi Tiết

#### 1. Banh Cam Vinh - Data Engineer (Building AI Agent with Strands)

- **Chủ đề:** Xây dựng AI Agent có khả năng tự hành.
- **Nội dung trọng tâm:**
- **Khái niệm:** AI Agent không chỉ trả lời mà còn có khả năng lập kế hoạch, sử dụng công cụ (APIs, Database) và tự đưa ra quyết định.
- **Strands Agents:** Framework giúp kết nối LLM với thế giới thực qua "Tool definition" và vòng lặp "Agentic Loop".
- **Ưu điểm:** Truy cập dữ liệu thời gian thực và thực hiện luồng công việc phức tạp mà LLM thuần túy không làm được.

#### 2. Nguyen Tuan Thinh - DevOps Engineer (Automated Prompt Engineering)

- **Chủ đề:** Nghệ thuật giao tiếp với AI và tối ưu hóa chi phí.
- **Nội dung trọng tâm:**
- **Vấn đề:** Prompt chung chung dẫn đến kết quả kém, lãng phí token và tăng chi phí (ví dụ: Claude Opus có giá $25/1M output tokens).
- **Giải pháp:** Xây dựng prompt có cấu trúc gồm 7 thành phần: Role, Instruction, Context, Input, Output Format, Examples, và Constraints.
- **Kỹ thuật nâng cao:** Chain-of-Thought (CoT), Tree-of-Thoughts (ToT), và RAG.
- **Công cụ:** Demo Proptimizer - tiện ích trình duyệt giúp tối ưu hóa prompt và chat với AI mọi nơi.

#### 3. Aiden Dinh - Operation Engineer (AIoT Projects: Locker Management)

- **Chủ đề:** Ứng dụng AIoT trong vận hành thực tế.
- **Nội dung trọng tâm:**
- **Dự án Smart Locker:** Tự động hóa việc mượn đồ tại CLB bằng nhận diện khuôn mặt thay cho quản lý thủ công.
- **Kiến trúc phần cứng:** Arduino thu thập dữ liệu cảm biến (RFID, Reed Switch), Raspberry Pi làm MQTT Broker.
- **Dịch vụ Cloud:**
- **AWS IoT Core:** Trung tâm kết nối và bảo mật thiết bị.
- **Amazon Rekognition:** Phân tích hình ảnh để xác thực thành viên.
- **DynamoDB & S3:** Lưu trữ thông tin người dùng và hình ảnh sự kiện.


### Những Gì Học Được

#### Tư Duy Thiết Kế
#### Kiến Trúc Kỹ Thuật

- Cách kết hợp linh hoạt giữa các dịch vụ Serverless (Lambda, API Gateway) và AI Service (Bedrock, Rekognition).
- Nắm rõ cách thiết kế kiến trúc Event-driven cho các hệ thống có yếu tố phần cứng và dữ liệu thời gian thực.

#### Chiến Lược Hiện Đại Hóa

- Chuyển đổi từ các câu lệnh rời rạc sang hệ thống Agent có khả năng suy luận đa bước.

### Ứng Dụng Vào Công Việc

- **Tối ưu hóa Prompt:** Áp dụng nguyên tắc "Be Clear & Specific" và dùng delimiters để tăng chất lượng phản hồi từ AI.
- **Thử nghiệm AI Agent:** Nghiên cứu tích hợp Strands Agents vào các quy trình cần truy xuất dữ liệu từ API nội bộ.

### Trải nghiệm trong event

Tham gia workshop **"Cloud Mastery Series: Khám phá Generative AI"** là một trải nghiệm thực tế và có chiều sâu, giúp hiểu rõ cách ứng dụng GenAI vào sản phẩm thật và vận hành hệ thống AI hiệu quả hơn.

#### Trải nghiệm kỹ thuật thực tế
- Xem demo hệ thống **Smart Locker**, hiểu rõ luồng dữ liệu đi từ cảm biến lên Cloud và trả kết quả nhận diện khuôn mặt trong vài giây.
- Theo dõi cách kết hợp giữa phần cứng (Arduino/Raspberry Pi) và dịch vụ AWS để xây dựng bài toán AIoT có thể triển khai thực tế.

#### Bài học rút ra về chi phí và hiệu quả
- Hiểu rằng tối ưu prompt và kiến trúc agent là yếu tố quan trọng để cân bằng chất lượng, tốc độ và chi phí vận hành.
