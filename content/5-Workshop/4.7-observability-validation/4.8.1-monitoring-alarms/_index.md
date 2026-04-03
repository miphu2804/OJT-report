---
title : "CloudWatch Log Monitoring"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 4.7.1 </b> "
---

#### Overview

Use CloudWatch to collect and monitor system logs and key metrics to detect errors early and track performance trends.

#### Logs to Monitor

1. **Application logs**: request, errors, API latency.
2. **ALB logs**: 4xx/5xx and latency.
3. **System metrics**: CPU, memory, disk (via CloudWatch Agent).

#### Why Monitoring Matters

1. Detect application failures and bottlenecks early.
2. Track traffic quality and error rates from users.
3. Prevent downtime by alerting on resource pressure.

#### Note

Alarm + SNS configuration is covered in the next section.


