---
title : "Kiểm tra hệ thống"
date : 2024-01-01
weight : 13
chapter : false
pre : " <b> 5.13. </b> "
---

#### Health check commands

+ Kiểm tra API: `curl -I <backend_url>/health`.
+ Kiểm tra frontend: truy cập URL Amplify.

#### Test local

+ Chạy backend local với `.env`.
+ Chạy frontend local với `npm run dev`.

#### Tạo Cognito user

+ Tạo user test qua AWS Console.
+ Gán vào nhóm phù hợp.
