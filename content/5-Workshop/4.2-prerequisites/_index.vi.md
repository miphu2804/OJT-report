---
title : "Chuẩn bị"
date : 2024-01-01 
weight : 2
chapter : false
pre : " <b> 4.2. </b> "
---

#### Công cụ cần cài

+ Terraform 1.14.6
+ Python 3.11
+ Node.js
+ uv
+ Docker

#### Vì sao cần các công cụ này

+ **Terraform 1.14.6**: quản lý hạ tầng AWS bằng code.
+ **Python 3.11**: chạy backend services và script hỗ trợ.
+ **Node.js**: build và chạy frontend.
+ **uv**: quản lý môi trường và dependencies Python nhanh.
+ **Docker**: build image và chạy service nhất quán.

#### Cài đặt cho môi trường Staging/Production (Ubuntu/Debian)

1. **Cập nhật hệ thống**
```
sudo apt update
sudo apt -y upgrade
```
2. **Cài Docker**
```
sudo apt -y install docker.io
sudo systemctl enable --now docker
```
3. **Cài Node.js (LTS)**
```
sudo apt -y install nodejs npm
```
4. **Cài Python 3.11**
```
sudo apt -y install python3.11
sudo apt -y install python3.11-venv
sudo apt -y install python3.11-dev
```
5. **Cài uv**
```
curl -LsSf https://astral.sh/uv/install.sh | sh
```
6. **Cài Terraform 1.14.6**
```
sudo apt -y install wget
sudo apt -y install unzip
wget https://releases.hashicorp.com/terraform/1.14.6/terraform_1.14.6_linux_amd64.zip
unzip terraform_1.14.6_linux_amd64.zip
sudo mv terraform /usr/local/bin/terraform
```

#### API keys cần có và cách lấy

1. **AWS_ACCESS_KEY_ID / AWS_SECRET_ACCESS_KEY**
   + Tạo IAM user/role có quyền deploy.
   + Lấy Access Key trong AWS IAM → Security credentials.
2. **API key cho AI/LLM (chatbot)**
   + Tạo API key tại nhà cung cấp AI (OpenAI/Anthropic/Google...).
   + Lưu vào secrets để dùng trong backend.
3. **Email service key (nếu dùng)**
   + Tạo credential trên SES/SendGrid/Mailgun.
   + Lưu SMTP user/password vào secrets.
4. **Auth provider (nếu dùng Cognito)**
   + Tạo User Pool và App Client.
   + Lấy `COGNITO_USER_POOL_ID` và `COGNITO_CLIENT_ID`.

#### API keys cần có

+ AWS access key và secret key.
+ API key cho AI/LLM (chatbot).
+ Các khóa dịch vụ email hoặc auth nếu dùng.
