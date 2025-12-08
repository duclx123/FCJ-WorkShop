---
title: "Event 3"
date: 2025-11-29
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Báo Cáo Sau Sự Kiện: AWS Cloud Mastery Series #3 — AWS Well-Architected Security Pillar

## Mục Tiêu Sự Kiện

- Giới thiệu vai trò của Security Pillar trong AWS Well-Architected Framework.
- Trình bày năm trụ cột cốt lõi của bảo mật trên cloud: Identity & Access Management, Detection, Infrastructure Protection, Data Protection và Incident Response.
- Cung cấp các best practices và playbook thực tiễn để bảo vệ ứng dụng trên AWS.

## Điểm Nhấn Chính

### Trụ cột 1 — Identity & Access Management (08:50 – 09:30)

- Nguyên tắc: Least Privilege, Zero Trust, Defense in Depth.
- IAM hiện đại: tránh dùng long-term credentials; ưu tiên Roles và Policies.
- IAM Identity Center: Single Sign-On và quản lý Permission Sets.
- Bảo mật multi-account: SCPs (Service Control Policies) và Permission Boundaries.
- Mini demo: kiểm tra IAM policies và mô phỏng quyền truy cập.

### Trụ cột 2 — Detection (09:30 – 09:55)

- Giám sát liên tục: CloudTrail (tầm tổ chức), GuardDuty, Security Hub.
- Logging toàn diện: VPC Flow Logs, ALB logs, S3 access logs.
- Tự động cảnh báo: sử dụng EventBridge.

### Trụ cột 3 — Infrastructure Protection (10:10 – 10:40)

- Bảo mật mạng: phân tách VPC (private vs. public).
- Lớp phòng thủ: Security Groups, NACLs, WAF, Shield, Network Firewall.
- Bảo vệ workload: bảo mật cho EC2 và khái niệm cơ bản dành cho ECS/EKS.

### Trụ cột 4 — Data Protection (10:40 – 11:10)

- Mã hóa: mã hóa dữ liệu khi lưu trữ và truyền tải (S3, EBS, RDS, DynamoDB).
- Quản lý khóa và secrets: KMS, Secrets Manager, Parameter Store.
- Xác định phân loại dữ liệu và guardrails truy cập.

### Trụ cột 5 — Incident Response (11:10 – 11:40)

- Chu trình IR: quy trình ứng phó sự cố theo khuyến nghị của AWS.
- Playbook IR và tự động hóa.
- Tình huống mẫu: lộ IAM key, S3 public, EC2 bị nghi nhiễm malware.
- Tự động hóa phản ứng bằng Lambda / Step Functions.

## Bài Học Rút Ra

- Hiểu rõ năm trụ cột Security và Shared Responsibility Model.
- IAM nâng cao: sử dụng IAM Identity Center, SCPs và loại bỏ long-term credentials.
- Bảo vệ dữ liệu: vai trò quan trọng của KMS và quản lý secrets đúng cách.
- Ứng phó sự cố: xây dựng playbook và tự động hóa bằng serverless.

## Trải Nghiệm Sự Kiện

- Buổi workshop là phiên tổng kết trong chuỗi nội dung, mang lại kiến thức bảo mật quan trọng trước khi hoàn thành dự án.
- Các phần trình bày về IAM Identity Center và Secrets Manager giải quyết tốt các vấn đề của nhóm liên quan đến Sub ID và quản lý API key.
- Các tình huống IR (như S3 public) rất hữu ích để củng cố chính sách bảo mật của dự án.
- Phiên Q&A cuối mang đến định hướng rõ ràng cho lộ trình học tiếp theo (Security Specialty).
