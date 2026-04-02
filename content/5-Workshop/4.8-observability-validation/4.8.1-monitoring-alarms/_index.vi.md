---
title : "Giám sát & Cảnh báo"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 4.8.1 </b> "
---

#### Giới thiệu CloudWatch & SNS

+ **CloudWatch**: dịch vụ giám sát log và metric cho hệ thống AWS.
+ **SNS**: dịch vụ gửi thông báo (email/SMS/webhook) khi có alarm.

#### CloudWatch giám sát log & metric

1. **Application logs**: request, error, API latency.
2. **ALB logs**: 4xx/5xx và latency.
3. **System metrics**: CPU, memory, disk (CloudWatch Agent).

#### Vì sao cần monitor các log này

+ **Application logs**: phát hiện lỗi nghiệp vụ, lỗi API và bottleneck.
+ **ALB logs**: theo dõi chất lượng truy cập và tỉ lệ lỗi từ phía người dùng.
+ **System metrics**: cảnh báo sớm khi tài nguyên quá tải gây downtime.

#### CloudWatch Alarm & SNS

+ **Khi nào gửi SNS**: ALB 5xx cao, CPU/memory cao, instance unhealthy.
+ **Thông số cần setup**: metric, threshold, evaluation period, SNS topic/email.
