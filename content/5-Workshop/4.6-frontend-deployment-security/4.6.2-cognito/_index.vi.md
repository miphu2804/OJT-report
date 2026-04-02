---
title : "Hướng dẫn & giới thiệu Cognito"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 4.7.2 </b> "
---

#### Cognito là gì

+ AWS Cognito cung cấp cơ chế đăng ký/đăng nhập, quản lý user pool và phát hành token xác thực.

#### Biến môi trường cần setup

+ **COGNITO_USER_POOL_ID**: định danh User Pool.
+ **COGNITO_CLIENT_ID**: định danh App Client.
+ **COGNITO_REGION**: region của Cognito.

#### Vai trò trong dự án

+ Frontend dùng Cognito để đăng nhập và nhận token.
+ Backend xác thực token để bảo vệ API.
