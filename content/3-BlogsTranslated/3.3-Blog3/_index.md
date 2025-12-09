---
title: "Blog 3"
date: 2025-01-01
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---
# Expanding AWS Fault Injection Service in Your Organization with Account Controls  
**Authors:** Dylan Reed, Jason Brown, Venkata Moparthi, Isael Pimentel, Satish Kumar  
**Published Date:** 11/04/2025  
**Categories:** AWS Fault Injection Service (FIS), AWS Resilience Hub (ARH), Management Tools, Resilience

---

## Introduction

AWS Fault Injection Service (FIS) enables you to apply **chaos engineering** at scale in your AWS environment. Chaos engineering involves introducing controlled failures to validate system resilience and recovery, ultimately improving user experience.

This proactive approach builds confidence in your system’s ability to respond to real-world incidents in production.

FIS experiments allow you to simulate failures such as:

- Availability Zone (AZ) power interruptions  
- Region isolation  
- Temporary network disruptions  

to observe how your application behaves under stress.

---

## Running Experiments Involving Network Faults

For network-related fault experiments, such as:

- AZ power interruption  
- Region isolation  

you may need permissions to temporarily modify network configurations (e.g., `ec2:CreateNetworkAcl`).

This presents challenges if your organization uses a **centralized networking model**, where a dedicated networking team manages network accounts. Application accounts may not have the required permissions to perform FIS network actions.

---

## Series Overview

This three-part series covers how to design **safety guardrails** using:

- Service Control Policies (SCPs)  
- AWS Identity and Access Management (IAM)

to enable safe execution of FIS experiments across:

- A single AWS account  
- Multiple AWS accounts  
- Multiple AWS Regions

---

## Expanding AWS FIS Using AWS Organizations

AWS Organizations lets you group AWS accounts into **Organizational Units (OUs)**.

### Service Control Policies (SCPs)  
Define the maximum permissions for identities across the organization.

### IAM  
Controls the detailed, resource-level permissions for AWS FIS and related services within each account.

Example structure:

- Root OU  
- Sandbox OU  
- Workloads OU  

---

## Preparing for AWS FIS Experiments

To build an experiment, you need:

- An **experiment template**  
- An **IAM role** for executing actions  
- **Stop conditions**  
- **Safety mechanisms**  
- **Permission boundaries**

AWS recommends **standardizing IAM roles** for creating and executing experiments.

---

## Standardized Roles for AWS FIS

Two main personas interact with FIS roles:

### 1. Account Admin  
- Creates and manages SCPs  
- Enforces least privilege across OUs

### 2. IAM Admin  
- Creates IAM roles and policies  
- Ensures policies comply with SCPs  

Two standardized roles:

### **AWS-FIS-Experiment-Orchestrator**
- Create, delete, and modify experiment templates  
- Assumed by end users who design experiments  

### **AWS-FIS-Experiment-Executor**
- Executes fault actions  
- Can only be assumed by the AWS FIS service  

> This role is sensitive because it can modify infrastructure resources, so SCP guardrails are essential.

---

## Practical Scenario

In a centralized networking model:

- The networking team owns network configurations  
- Developers lack required EC2 networking permissions  
- FIS network disruption actions may fail due to missing EC2 API permissions  

Therefore, an SCP is required to allow only the  
**AWS-FIS-Experiment-Executor** role to perform network changes.

---

## Example SCP for Account Admin

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "AllowAccessToASpecificRole",
      "Effect": "Deny",
      "Action": [
        "ec2:CreateNetworkAcl",
        "ec2:CreateNetworkAclEntry",
        "ec2:DeleteNetworkAcl",
        "ec2:CreateTags",
        "ec2:DescribeNetworkAcls",
        "ec2:DescribeManagedPrefixLists",
        "ec2:DescribeSubnets",
        "ec2:DescribeVpcs",
        "ec2:ReplaceNetworkAclAssociation",
        "ec2:GetManagedPrefixListEntries"
      ],
      "Resource": "*",
      "Condition": {
        "ArnNotEquals": {
          "aws:PrincipalArn": [
            "arn:aws:iam::*:role/AWS-FIS-Experiment-Executor"
          ]
        }
      }
    }
  ]
}
