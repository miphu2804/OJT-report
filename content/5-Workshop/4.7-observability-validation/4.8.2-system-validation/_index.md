---
title : "SNS Email Alerts"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 4.7.2 </b> "
---

#### Goal

Send email notifications when CloudWatch alarms exceed thresholds.

#### Create SNS Topic

1. Create an SNS Topic for alerts.
2. Subscribe email recipients and confirm the subscription.

#### Create CloudWatch Alarm

1. Select metrics to monitor (ALB 5xx, CPU/Memory, instance unhealthy).
2. Set thresholds and evaluation periods.
3. Attach the SNS Topic to the alarm.

#### Verification

1. Trigger a test condition to fire the alarm.
2. Confirm the email is delivered.
3. Ensure the alert contains sufficient troubleshooting context.
