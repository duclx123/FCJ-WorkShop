---
title: "Event 3"
date: 2025-11-29
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Event Report: AWS Cloud Mastery Series #3 — AWS Well-Architected Security Pillar

## Event Purpose

- Introduce the role and importance of the Security Pillar in the AWS Well-Architected Framework.
- Explain the five essential cloud security pillars: Identity & Access Management, Detection, Infrastructure Protection, Data Protection, and Incident Response.
- Provide best practices and actionable playbooks for securing cloud-based applications.

## Highlights

### Pillar 1 — Identity & Access Management (08:50 – 09:30)

- Key principles: Least Privilege, Zero Trust, Defense in Depth.
- Modern IAM practices: avoid long-term credentials; prioritize Roles and Policies.
- IAM Identity Center: SSO capabilities and management of Permission Sets.
- Multi-account security: use of SCPs (Service Control Policies) and Permission Boundaries.
- Mini demo: validate IAM policies and simulate access scenarios.

### Pillar 2 — Detection (09:30 – 09:55)

- Continuous monitoring: CloudTrail (organization-level), GuardDuty, Security Hub.
- Comprehensive logging: VPC Flow Logs, ALB logs, S3 access logs.
- Automated alerting: EventBridge integration.

### Pillar 3 — Infrastructure Protection (10:10 – 10:40)

- Network security: VPC segmentation (public vs. private).
- Defense layers: Security Groups, NACLs, WAF, Shield, Network Firewall.
- Workload security: securing EC2 instances and foundational practices for ECS/EKS.

### Pillar 4 — Data Protection (10:40 – 11:10)

- Encryption best practices: protecting data at rest and in transit (S3, EBS, RDS, DynamoDB).
- Key and secret management: KMS, Secrets Manager, Parameter Store.
- Data classification and enforcing access guardrails.

### Pillar 5 — Incident Response (11:10 – 11:40)

- IR lifecycle: AWS-recommended incident response processes.
- Building IR playbooks and automation workflows.
- Sample scenarios: compromised IAM keys, exposed S3 buckets, malware detection on EC2.
- Automated responses with Lambda / Step Functions.

## What I Learned

- Comprehensive understanding of the five AWS Security Pillars and the Shared Responsibility Model.
- Advanced IAM: using IAM Identity Center, SCPs, and eliminating long-term credentials.
- Data security: importance of KMS and proper secret management practices.
- Incident Response: designing playbooks and automating workflows using serverless AWS services.

## Event Experience

- This workshop served as the final wrap-up session in the series, providing critical security knowledge before project delivery.
- Sessions on IAM Identity Center and Secrets Manager helped the team address Sub ID authentication challenges and improve API key management.
- Incident Response scenarios (e.g., public S3 exposure) reinforced the security posture required for the project.
- The final Q&A offered clear guidance for the next learning track (Security Specialty).