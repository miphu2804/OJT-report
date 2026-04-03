---
title : "WAF Frontend"
date : 2024-01-01
weight : 4
chapter : false
pre : " <b> 4.6.4 </b> "
---

#### Goal

Protect the frontend edge layer (CloudFront) with WAF.

#### Deployment Steps

1. Create a Web ACL in AWS WAF.
2. Choose CloudFront scope and add basic managed rule groups.
3. Attach the Web ACL to the Amplify CloudFront distribution.

#### Rule Verification

1. Test with rate limiting or a temporary IP block.
2. Observe logs/metrics for false positives.

#### Note

Start in monitor mode before switching to block.
