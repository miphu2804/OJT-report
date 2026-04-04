---
title: "Event 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.2. </b> "
---

# Cloud Mastery Series: DevOps Fundamentals & Infrastructure

### Event Objectives

- Share best practices to address challenges in managing and operating systems at production scale (production workloads).
- Introduce container orchestration, fault-tolerant architecture, and infrastructure automation concepts.
- Introduce Elixir and practical use cases in modern infrastructure operations.
- Guide compute decisions by comparing self-managed Kubernetes with managed services such as Amazon EKS.
- Present modern toolsets including Helm, K9s, Mix, Observer, and Terraform.

### Speaker List & Detailed Content

#### 1. Bao Huynh - Junior Cloud Native Developer @ Endava (Kubernetes)

- **Topic:** Architecting for the Cloud with Kubernetes.
- **Main content:**
- **Challenge:** Manually managing thousands of containers in production is impractical, requiring self-healing and scalability.
- **K8s architecture:** A deep dive into Control Plane (the control brain) and Worker Nodes (where workloads run).
- **Core objects:** Pods, Deployments (update management), ConfigMaps, and Secrets (configuration/security management).
- **Cloud solution:** Amazon EKS helps reduce the operational burden of managing cluster infrastructure.

#### 2. Nguyen Ta Minh Triet - R&D Member @ ITea Lab (Elixir in DevOps)

- **Topic:** Elixir as a Unified Solution for Massively Concurrent & Fault-Tolerant Infrastructure.
- **Main content:**
- **Technology advantage:** Elixir runs on the BEAM VM, enabling millions of concurrent connections with lightweight processes.
- **"Let It Crash" philosophy:** Instead of trying to catch every error, the system uses Supervision Trees to restart failed processes automatically.
- **Economic impact:** A practical case study showed cost reduction from $30,000/month (Serverless Node.js/Lambda) to under $400/month after switching to Elixir.
- **Integrated tools:** Mix (build tool), Hex (package manager), and Observer (real-time system monitoring).

#### 3. Thinh Nguyen - FCAJ Cloud Engineer Trainee (Infrastructure as Code)

- **Topic:** IaC with Terraform on AWS.
- **Main content:**
- **Problem:** ClickOps (manual console operations) is error-prone, inconsistent, and hard to collaborate on.
- **IaC solution:** Use code to manage cloud resources for automation and reusability.
- **Terraform & HCL:** HashiCorp's open-source tool using HCL to define multi-cloud infrastructure (AWS, Azure, GCP).
- **Execution workflow:** Core commands include `init` (initialize), `plan` (preview changes), `apply` (deploy), and `destroy` (remove resources).

### What I Learned

#### Automation Mindset

- Infrastructure should be defined as code so it can be versioned just like application source code.

#### Fault Tolerance

- Designing systems with self-healing capability (as seen in Elixir and Kubernetes) is more important than trying to write code that never fails.

#### Cost Optimization

- Choosing the right technology (Elixir for highly concurrent workloads) and deployment model (EKS for Kubernetes) delivers strong ROI.

### Applying to Work

- **EduTrust project:** Apply Terraform to set up standardized AWS infrastructure, making it easier to replicate Dev/Staging/Prod environments.
- **Application deployment:** Package microservices into Docker and orchestrate with Kubernetes for high availability.
- **Performance improvement:** Leverage functional programming principles and event-driven architecture from Elixir for real-time features.

### Event Experience

Attending **"Cloud Mastery Series: DevOps Fundamentals & Infrastructure"** provided a very practical perspective on operating modern infrastructure with automation, fault tolerance, and cost efficiency.

#### Practical exposure
- Demo sessions with `kubectl` commands and Terraform `plan/apply` workflows helped clarify the day-to-day work of a cloud engineer.

#### Multi-dimensional perspective
- The combination of infrastructure (IaC), orchestration (Kubernetes), and a high-performance language (Elixir) formed a logical DevOps learning journey that is easy to apply in real projects.
