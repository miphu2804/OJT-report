---
title: "Event 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.3. </b> "
---

# Cloud Mastery Series #3: Security

### Event Objectives

- This workshop focused on practical AWS security, from networking and IAM to advanced layers of defense.
- It covered core networking controls such as SG, NACL, VPC, CIDR, Subnet, IGW, and VPC Endpoint.
- It also covered AWS IAM, SCP, Permission Boundary, credential rotation, and policy-based access control.
- The session highlighted firewall services such as WAF, Shield, Network Firewall, and Firewall Manager.
- The concepts were reinforced through live demos and video walkthroughs.

### Speaker List & Detailed Content

- **Speakers:** Lam An Thinh, Nguyen Phan Quoc Viet, Huynh Hoang Long, and Dang Thi Minh Thu.
- The session was organized around three main themes: network security, identity and access control, and layered defense.
- Live demos and video walkthroughs helped connect the concepts to real deployment scenarios.

#### AWS Network Security

- VPC helps isolate resources by environment and keeps private network segments clearly separated.
- Security Group and Network ACL complement each other at the instance and subnet levels.
- CIDR and Subnet make network planning easier to scale and manage.
- Internet Gateway and VPC Endpoint help control traffic between private resources and AWS services.

#### Identity and Access Management

- AWS IAM provides a clear structure for managing users, groups, roles, and policies.
- SCPs and Permission Boundaries help narrow access at the organization and identity levels.
- Credential rotation is an important step for reducing the risk of leaked access credentials.
- Least privilege remains the core principle for granting only the permissions that are actually needed.

#### Firewall and Advanced Defense

- AWS WAF filters malicious traffic at the application layer.
- AWS Shield improves resilience against DDoS attacks.
- Network Firewall gives more flexible control over network traffic.
- Firewall Manager centralizes security policy management across multiple accounts and services.

### What I Learned

#### Security Mindset

AWS security works best as a layered design rather than a single-tool solution.

#### Access Governance

IAM, SCP, Permission Boundaries, and credential rotation are key pieces for keeping access aligned with least privilege.

#### Layered Defense

Good network design from the start reduces configuration mistakes and later security risk. WAF, Shield, and Network Firewall should be treated as part of the operating architecture.

### Applying to Work

- Apply clearer network segmentation in EduTrust to organize resources, subnets, and access flows more cleanly.
- Tighten the process for managing users, roles, and policies to reduce AWS operational risk.
- Consider adding more protection at both the application and network layers for public-facing services.
- Keep regular access reviews and credential rotation as part of the team routine.

### Event Experience

Attending **"Cloud Mastery Series #3: Security"** gave a practical view of cloud security, from network design to access governance and layered defense.

#### Practical exposure

- Live demos and video examples made the AWS security setup easier to understand in real operational scenarios.
- Combining networking, identity management, and firewalls showed a more complete security picture than focusing on a single service.

#### Lessons learned

- Security should be designed up front instead of added after the system is already running.
- Access should follow least privilege and be controlled at multiple layers.
- Private networking, sensible segmentation, and strong access governance are the foundation of a secure AWS system.
- Automation and policy standardization reduce human error and improve consistency at scale.