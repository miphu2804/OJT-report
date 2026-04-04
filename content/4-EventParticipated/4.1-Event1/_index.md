---
title: "Event 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Cloud Mastery Series: Exploring Generative AI

### Event Objectives

- Share best practices in modern application design, optimize performance using CloudFront (CDN) and S3 storage.
- Introduce Prompt Engineering methods and workflows for building autonomous AI Agents.
- Provide guidance on compute selection, from Edge devices (Raspberry Pi/Arduino) to Cloud services (Lambda/Fargate).
- Present AI tools such as Proptimizer and Strands Agents for workflow automation.

### Speaker List & Detailed Content

#### 1. Banh Cam Vinh - Data Engineer (Building AI Agent with Strands)

- **Topic:** Building autonomous AI Agents.
- **Main points:**
- **Concept:** AI Agents do more than answer questions; they can plan, use tools (APIs, Databases), and make decisions.
- **Strands Agents:** A framework that connects LLMs to the real world through "Tool definitions" and an "Agentic Loop."
- **Advantage:** Accesses real-time data and executes complex workflows that pure LLMs cannot handle.

#### 2. Nguyen Tuan Thinh - DevOps Engineer (Automated Prompt Engineering)

- **Topic:** The art of communicating with AI and cost optimization.
- **Main points:**
- **Problem:** Generic prompts produce weak results, waste tokens, and increase cost (for example, Claude Opus at $25 per 1M output tokens).
- **Solution:** Build structured prompts with 7 components: Role, Instruction, Context, Input, Output Format, Examples, and Constraints.
- **Advanced techniques:** Chain-of-Thought (CoT), Tree-of-Thoughts (ToT), and RAG.
- **Tool:** Proptimizer demo - a browser utility to optimize prompts and chat with AI anywhere.

#### 3. Aiden Dinh - Operation Engineer (AIoT Projects: Locker Management)

- **Topic:** AIoT applications in real operations.
- **Main points:**
- **Smart Locker project:** Automates club item borrowing with face recognition instead of manual management.
- **Hardware architecture:** Arduino collects sensor data (RFID, Reed Switch), Raspberry Pi acts as the MQTT Broker.
- **Cloud services:**
- **AWS IoT Core:** Central hub for secure device connectivity.
- **Amazon Rekognition:** Image analysis for member verification.
- **DynamoDB & S3:** Stores user information and event images.


### What I Learned

#### Design Mindset
#### Technical Architecture

- How to combine Serverless services (Lambda, API Gateway) with AI services (Bedrock, Rekognition) effectively.
- Better understanding of how to design Event-driven architecture for systems involving hardware and real-time data.

#### Modernization Strategy

- Transitioning from isolated commands to Agent-based systems capable of multi-step reasoning.

### Applying to Work

- **Prompt optimization:** Apply the "Be Clear & Specific" principle and use delimiters to improve AI response quality.
- **AI Agent experimentation:** Explore integrating Strands Agents into workflows that require data retrieval from internal APIs.

### Event Experience

Attending **"Cloud Mastery Series: Exploring Generative AI"** was a practical and in-depth experience, helping me better understand how to apply GenAI to real products and run AI systems more effectively.

#### Hands-on technical experience
- Watched a live **Smart Locker** demo and clearly understood how data flows from sensors to the Cloud, then returns face recognition results within seconds.
- Observed how hardware (Arduino/Raspberry Pi) can be combined with AWS services to build AIoT solutions ready for real deployment.

#### Lessons learned about cost and efficiency
- Understood that prompt optimization and agent architecture are key factors in balancing quality, speed, and operating cost.
