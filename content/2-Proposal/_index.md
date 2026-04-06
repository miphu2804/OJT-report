---
title: "Proposal"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---
# EduTrust — AI-Powered Online Exam Monitoring Platform
## A Fullstack AWS-Based Solution for Exam Proctoring and Smart Learning Support

### 1. Executive Summary
EduTrust is an online exam management platform designed for educational environments (schools and training centers), aiming to digitize exam operations, monitor exam rooms with AI, and support learning through an intelligent chatbot. The system serves three main user groups: **Admin** (school management), **Teachers** (create exams and supervise), and **Students** (take exams and view results). The backend uses FastAPI (Python) with MongoDB, Redis, Amazon S3, and a YOLO model to detect cheating via camera. The frontend is built with Next.js and Tailwind CSS, deployed on AWS Amplify.

### 2. Problem Statement
*Current Problem*  
Running online exams in schools faces multiple challenges: manual proctoring is labor-intensive, cheating is difficult to detect (phone usage, multiple faces in frame, leaving camera view), there is no centralized system to manage classes — exams — results, and students lack intelligent learning support tools.

*Solution*  
EduTrust provides a comprehensive platform including:
- **Class & Exam Management**: Admin creates classes, assigns homeroom and subject teachers; teachers create multiple-choice exams with secret keys and set start/end times.
- **AI Exam Proctoring**: Integrates YOLOv26n (object detection) to detect violations in real-time via webcam — including multiple faces (MULTIPLE_FACES), camera disappearance (FACE_DISAPPEARED: cell Phone), and forbidden objects (FORBIDDEN_OBJECT). Violation evidence images are uploaded to Amazon S3 and logged to MongoDB.
- **AI Learning Assistant**: A multi-agent system using Pydantic AI with specialized agents (technical, social, general, web search) to help students search knowledge, ask questions, and find learning materials.
- **Authentication & Security**: JWT tokens (using Cognito) with role-based access control (RBAC).

*Benefits and Return on Investment (ROI)*  
The solution reduces teachers' manual proctoring workload, improves transparency and fairness in exams, automates grading, records violations with image evidence, and provides a consolidated results dashboard. Operating cost remains low by leveraging MongoDB Atlas (free tier), Redis Cloud, and AWS S3/Amplify. Estimated AWS infrastructure cost is under 5 USD/month for a medium-sized school setup.

### 3. Solution Architecture
The platform follows a **fullstack monorepo** architecture with a Python FastAPI backend and a Next.js frontend, deployed via Docker containers. Data is stored in MongoDB (collections: users, exams, classes, submissions, violations), session/conversation cache uses Redis, and violation images are stored in Amazon S3.
![EduTrust Solution Architecture](/images/2-Proposal/edutrust-architecture.png)

*Services & Technologies Used (Architecture-Aligned)*
- *AWS Amplify + CloudFront*: Host Next.js frontend and deliver content via CDN.
- *AWS Route 53 + AWS ACM*: DNS and TLS/HTTPS certificate management.
- *AWS WAF*: Protect the web layer from common attack patterns.
- *Amazon VPC (public/private subnet)*: Network isolation and public/private segmentation.
- *Application Load Balancer (ALB)*: Route traffic to backend services.
- *Amazon EC2 Auto Scaling*: Operate backend with automatic scale based on load.
- *Amazon ECR*: Store backend Docker images.
- *Amazon S3*: Store violation images, ALB logs, and Terraform state.
- *Amazon DynamoDB*: Fast key-value data storage (as shown in architecture).
- *Amazon ElastiCache for Redis*: Cache session/conversation and frequently accessed data.
- *Amazon Cognito*: User authentication and role-based authorization.
- *Amazon CloudWatch + VPC Flow Logs + SNS*: Monitoring, logging, and alerting.
- *AWS KMS + SSM Parameter Store + PrivateLink*: Secret protection and secure internal access.
- *Terraform + GitHub Actions*: IaC and CI/CD deployment automation.

*Application Stack*
- *FastAPI*: Async backend API framework with auto-generated docs (Swagger/ReDoc).
- *Next.js 16 + Tailwind CSS v4*: Frontend SPA with App Router and server/client components.
- *YOLOv26n (Ultralytics)*: Object detection model for exam proctoring.
- *Pydantic AI + LiteLLM*: Multi-agent orchestrator for learning support chatbot.
- *Docker*: Backend containerization with multi-stage build (Ubuntu 24.04).

*Component Design*
- *Authentication (Auth)*: JWT access/refresh token, cookie-based session management, RBAC (admin/teacher/student).
- *Class Management*: Assign homeroom/subject teachers, add/remove students, auto update status (active/inactive).
- *Exam Management*: Create multiple-choice exams, auto-generate secret keys, time control (start/end), auto-grading on submission.
- *Camera Proctoring (Detection)*: CameraService receives frames, ObjectDetector (YOLO) detects violations, ViolationLogger writes logs to MongoDB + S3, ScreenshotUtils captures evidence images.
- *AI Agent*: UnifiedAgent orchestrates sub-agents (technical, social, general, web_search) via tool delegation and WebSocket streaming.

### 4. Technical Implementation
*Implementation Phases*  
The project is divided into 5 main phases:
1. *Learn AWS core services*: Understand architecture services (VPC, EC2/ALB/ASG, S3, ECR, Cognito, CloudWatch, KMS, SSM, WAF) and CI/CD/IaC flow.
2. *Research and architecture design*: Study technologies (FastAPI, Next.js, YOLO, Pydantic AI), design database schema, API contracts, and system architecture.
3. *Develop core features*: Build auth (JWT via Cognito), class CRUD, exam management, and auto-grading.
4. *Integrate AI & Camera*: Integrate YOLO violation detection, build multi-agent chatbot, connect S3/Redis.
5. *Frontend & testing*: Complete Next.js dashboards for 3 roles, run end-to-end tests, and containerize with Docker.

*Technical Requirements*
- *Backend*: Python >= 3.11, FastAPI, Motor (async MongoDB driver), Redis >= 5.0, Boto3 (AWS SDK), Ultralytics (YOLO), Pydantic AI + LiteLLM, Kreuzberg (document parsing), SlowAPI (rate limiting).
- *Frontend*: Next.js 16, React 19, Tailwind CSS v4, Lucide React (icons), React Markdown + KaTeX (math rendering), ONNX Runtime Web, next-intl (i18n).
- *Infrastructure*: Docker (multi-stage build), MongoDB Atlas, Redis Cloud, Amazon S3, AWS Amplify, Logfire (observability).

### 5. Timeline & Milestones
- *Week 1-2*: Learn AWS services in architecture (VPC, EC2/ALB/ASG, S3, ECR, Cognito, CloudWatch, KMS/SSM, WAF) and CI/CD/IaC workflow.
- *Week 3-4*: Research technologies, design architecture and database schema.
- *Week 5-6*: Develop backend core (auth, classes, exams, submissions).
- *Week 7-8*: Integrate YOLO detection, AI chatbot (multi-agent), and S3 storage.
- *Week 9*: Build frontend dashboards (admin/teacher/student views).
- *Week 10*: Integration testing, performance optimization, and Dockerization.

### 6. Budget Estimation

*Assumptions based on architecture*
- Small environment (small staging/production), low-to-medium traffic.
- Backend runs on EC2 Auto Scaling (t3.small, 2 instances), ALB runs 24/7.
- Frontend hosted on Amplify + CloudFront, with WAF.
- Violation data stored on S3 (~10-20 GB/month).

*Estimated monthly infrastructure cost*
- VPC Endpoints (Interface for ECR/SSM/STS/Logs...): ~30-60 USD
- EC2 Auto Scaling (2 x t3.small): ~30-40 USD
- Application Load Balancer: ~16-25 USD
- Amazon S3 (violation images, ALB logs, Terraform state): ~2-6 USD
- Amazon CloudFront + Amplify: ~1-5 USD
- AWS WAF: ~5-10 USD
- Amazon ElastiCache (Redis - small cache): ~15-25 USD
- Amazon DynamoDB (low traffic): ~1-3 USD
- Amazon ECR (image storage): ~1-3 USD
- Amazon Cognito (<= 50k MAU): ~0-2 USD
- Amazon CloudWatch + VPC Flow Logs + SNS: ~5-10 USD
- AWS KMS + SSM Parameter Store: ~1-3 USD
- Data Transfer: ~2-6 USD

*Estimated total*: ~110-195 USD/month (including VPC Endpoints; depends on traffic and S3 volume)

*Third-party API costs*
- OpenAI/LiteLLM API: usage-based.
- External search services (if used): package-based.

### 7. Risk Assessment
*Risk Matrix*
- Low YOLO accuracy (false positive/negative): High impact, medium probability.
- Student camera/network disconnection: Medium impact, medium probability.
- API budget overruns (LLM calls): Medium impact, low probability.
- Migrating from MongoDB to MySQL causes schema/query complexity changes: Medium-high impact, medium probability.

*Mitigation Strategies*
- YOLO: Tune confidence threshold (min 0.5), alert only after consecutive frames, allow teacher manual review.
- Network: Client-side detection with ONNX Runtime Web (fallback), log violations locally and sync when network recovers.
- API cost: Apply rate limiting (SlowAPI), set budget alerts, use lighter models for simple tasks.
- Database: Use repository layer abstraction, normalize schema, prepare migration scripts if switching to MySQL.

*Contingency Plan*
- Switch to manual proctoring (teacher watches camera directly) if AI detection fails.
- Use SQLite/local storage fallback if MongoDB Atlas is unavailable.
- Docker images enable quick deployment on any cloud provider (avoids AWS lock-in).

### 8. Expected Outcomes
*Technical improvements*: Automate exam proctoring with AI (YOLO) to replace manual monitoring. Auto-grade multiple-choice exams, log violations with S3 image evidence, and provide a 24/7 multi-agent AI learning chatbot.  
*Long-term value*: The platform can scale to more schools, support multilingual interfaces (next-intl), integrate additional exam types (essay with AI scoring), and evolve into a full SaaS education platform. Accumulated violation data can be used to improve detection models over time.
