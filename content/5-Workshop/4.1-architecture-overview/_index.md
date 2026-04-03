---
title : "Architecture Overview"
date : 2024-01-01 
weight : 1 
chapter : false
pre : " <b> 4.1. </b> "
---

#### Introduction

EduTrust is a learning support system with AI chatbot assistance and AI camera-based exam monitoring. It is deployed on AWS to ensure scalability, security, and stable operations.

#### High-Level AWS Architecture

Internet → Amplify → Application Load Balancer → EC2 Auto Scaling → Backend services

#### Core Components (By Layer)

**Client/Presentation Layer**

- AWS Amplify: host the frontend and connect the custom domain.

**Traffic/Delivery Layer**

- Application Load Balancer: routes traffic to backend services.

**Compute/Service Layer**

- EC2 Auto Scaling: runs backend services based on load.
- Backend services: API, AI processing, camera events, auth.

**Data Layer**

- Data storage: logs, videos, and exam results (S3/DB).

#### High Availability (HA) & Multi-AZ

- EC2 Auto Scaling spans multiple AZs for HA.
- ALB distributes traffic across AZs.
- Managed data services (RDS/S3) increase durability.

#### Main Flow

1. Users access the frontend via Amplify.
2. Frontend calls APIs through the Application Load Balancer.
3. Backend handles business logic, AI processing, and camera events.
4. Data is stored and presented back to users.
