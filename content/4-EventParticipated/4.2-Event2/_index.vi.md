---
title: "Event 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.2. </b> "
---

# Cloud Mastery Series: DevOps Fundamentals & Infrastructure

### Mục Đích Của Sự Kiện

- Chia sẻ best practices để giải quyết thách thức trong quản lý và vận hành hệ thống ở quy mô lớn (Production workloads).
- Giới thiệu kiến thức về điều phối container, kiến trúc chịu lỗi cao (Fault-tolerant) và tự động hóa hạ tầng.
- Giới thiệu về ngôn ngữ lập trình Elixir và ứng dụng 
- Hướng dẫn lựa chọn compute, so sánh giữa tự triển khai Kubernetes và dùng dịch vụ quản lý như Amazon EKS.
- Giới thiệu bộ công cụ hiện đại như Helm, K9s, Mix, Observer và Terraform.

### Danh Sách Diễn Giả & Nội Dung Chi Tiết

#### 1. Bảo Huỳnh - Junior Cloud Native Developer @ Endava (Kubernetes)

- **Chủ đề:** Architecting for the Cloud with Kubernetes.
- **Nội dung trọng tâm:**
- **Thách thức:** Việc quản lý thủ công hàng ngàn container trong môi trường Production là bất khả thi, đòi hỏi khả năng tự phục hồi (Self-healing) và mở rộng (Scalability).
- **Kiến trúc K8s:** Đi sâu vào Control Plane (bộ não điều khiển) và Worker Nodes (nơi chạy ứng dụng).
- **Đối tượng cốt lõi:** Pods, Deployments (quản lý cập nhật), ConfigMaps và Secrets (quản lý cấu hình/bảo mật).
- **Giải pháp Cloud:** Amazon EKS giúp giảm bớt gánh nặng quản lý hạ tầng Cluster.

#### 2. Nguyễn Tạ Minh Triết - R&D Member @ ITea Lab (Elixir in DevOps)

- **Chủ đề:** Elixir as a Unified Solution for Massively Concurrent & Fault-Tolerant Infrastructure.
- **Nội dung trọng tâm:**
- **Ưu thế công nghệ:** Elixir chạy trên máy ảo BEAM, cho phép xử lý hàng triệu kết nối đồng thời với tiến trình siêu nhẹ.
- **Triết lý "Let It Crash":** Thay vì cố bắt mọi lỗi, hệ thống dùng Supervision Trees để tự động khởi động lại tiến trình lỗi.
- **Hiệu quả kinh tế:** Case study thực tế cho thấy chuyển từ Serverless (Node.js/Lambda) sang Elixir giúp giảm chi phí từ $30,000/tháng xuống còn dưới $400/tháng.
- **Công cụ tích hợp:** Mix (build tool), Hex (package manager) và Observer (quan sát hệ thống thời gian thực).

#### 3. Thịnh Nguyễn - FCAJ Cloud Engineer Trainee (Infrastructure as Code)

- **Chủ đề:** IaC with Terraform on AWS.
- **Nội dung trọng tâm:**
- **Vấn đề:** ClickOps (thao tác tay trên Console) dễ gây sai sót, thiếu nhất quán và khó cộng tác.
- **Giải pháp IaC:** Dùng mã nguồn để quản lý tài nguyên Cloud, đảm bảo tự động hóa và khả năng tái sử dụng.
- **Terraform & HCL:** Giới thiệu công cụ mã nguồn mở của HashiCorp, dùng ngôn ngữ HCL để định nghĩa hạ tầng đa nền tảng (AWS, Azure, GCP).
- **Quy trình thực thi:** Các lệnh cốt lõi gồm `init` (khởi tạo), `plan` (xem trước thay đổi), `apply` (triển khai) và `destroy` (xóa tài nguyên).

### Những Gì Học Được

#### Tư Duy Tự Động Hóa

- Hạ tầng cần được định nghĩa bằng code để có thể quản lý phiên bản (Versioning) tương tự mã nguồn ứng dụng.

#### Khả Năng Chịu Lỗi

- Thiết kế hệ thống có khả năng tự phục hồi (như Elixir và Kubernetes) quan trọng hơn việc cố viết mã không bao giờ lỗi.

#### Tối Ưu Chi Phí

- Chọn đúng công nghệ (Elixir cho tác vụ song song) và mô hình triển khai (EKS cho Kubernetes) mang lại ROI vượt trội.

### Ứng Dụng Vào Công Việc

- **Dự án EduTrust:** Áp dụng Terraform để thiết lập hạ tầng AWS chuẩn hóa, giúp dễ sao chép môi trường Dev/Staging/Prod.
- **Triển khai ứng dụng:** Đóng gói Microservices vào Docker và điều phối bằng Kubernetes để đảm bảo tính sẵn sàng cao.
- **Tăng hiệu suất:** Tận dụng triết lý lập trình chức năng và kiến trúc hướng sự kiện từ Elixir cho các tính năng xử lý thời gian thực.

### Trải Nghiệm Trong Event

Tham gia workshop **"Cloud Mastery Series: DevOps Fundamentals & Infrastructure"** mang lại góc nhìn rất thực tế về cách vận hành hạ tầng hiện đại theo hướng tự động, chịu lỗi cao và tối ưu chi phí.

#### Thực tiễn
- Các phiên demo về lệnh `kubectl` và quy trình Terraform `plan/apply` giúp hình dung rõ công việc thực tế của một kỹ sư Cloud.

#### Góc nhìn đa chiều
- Sự kết hợp giữa hạ tầng (IaC), điều phối (Kubernetes) và ngôn ngữ hiệu suất cao (Elixir) tạo nên một hành trình kiến thức DevOps logic và dễ ứng dụng vào dự án thật.
