---
title : "System Checks"
date : 2024-01-01
weight : 13
chapter : false
pre : " <b> 5.13. </b> "
---

#### Health check commands

+ Check API: `curl -I <backend_url>/health`.
+ Check frontend: open Amplify URL.

#### Local tests

+ Run backend with `.env`.
+ Run frontend with `npm run dev`.

#### Create Cognito user

+ Create a test user in AWS Console.
+ Assign to the correct group.
