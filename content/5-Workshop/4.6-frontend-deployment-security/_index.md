---
title : "Frontend Deployment & Security"
date : 2024-01-01
weight : 6
chapter : true
pre : " <b> 4.6. </b> "
---

#### Overview

This section focuses on deploying the frontend on AWS Amplify, configuring Cognito for authentication, and enabling WAF for edge protection. When attaching a custom domain to Amplify, DNS records are created automatically; on the domain provider side, you only need to update nameservers so Route 53 manages DNS and ACM validates TLS. This setup reduces manual steps, lowers configuration errors, and keeps HTTPS stable.

#### Content

1. [Frontend deployment with Amplify](4.7.1-setup-amplify-frontend/)
2. [Cognito (User Authentication)](4.7.2-cognito/)
3. [Custom Domain & HTTPS](4.7.3-custom-domain-https/)
4. [WAF for Frontend](4.7.4-waf-frontend/)



