---
title : "Custom Domain & HTTPS"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 4.6.3 </b> "
---

#### Overview

Configure a custom domain following the flow Name.com → Route 53 → ACM → Amplify to enable HTTPS and secure access.

#### Steps

1. Set up Route 53 for the Name.com domain.
2. Issue an ACM certificate using DNS validation.
3. Attach the domain to Amplify and verify HTTPS.
