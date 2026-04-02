---
title : "Architecture Overview"
date : 2024-01-01 
weight : 1 
chapter : false
pre : " <b> 5.1. </b> "
---

#### Architecture diagram

Internet → Amplify → ALB → EC2 ASG → Backend services

#### Core components

+ **Amplify**: host frontend and connect domain.
+ **ALB**: route traffic to backend.
+ **EC2 Auto Scaling**: run backend services.
+ **Backend services**: API, AI, camera events, auth.

#### Data flow

1. Users access the web app via Internet.
2. Amplify serves frontend and calls APIs.
3. ALB routes requests to EC2 ASG.
4. Backend processes logic and returns results.
