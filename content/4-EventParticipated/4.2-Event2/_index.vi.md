---
title: "Event 2"
date: 2025-11-17
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Báo Cáo Sau Sự Kiện: AWS Cloud Mastery Series #2 — DevOps on AWS

## Mục Tiêu Sự Kiện

- Củng cố tư duy DevOps và các nguyên tắc văn hóa cốt lõi.
- Giới thiệu hệ thống dịch vụ AWS hỗ trợ CI/CD: CodeCommit, CodeBuild, CodeDeploy, CodePipeline.
- Khai thác chuyên sâu về Infrastructure as Code (IaC) thông qua CloudFormation và AWS CDK.
- Tìm hiểu các dịch vụ container (ECS, EKS, App Runner) và bộ công cụ quan sát hệ thống (CloudWatch, X-Ray).

## Điểm Nhấn Chính

### Buổi Sáng: CI/CD Pipeline & Infrastructure as Code (08:30 – 12:00)

- Tư duy DevOps: làm rõ các nguyên tắc nền tảng và bộ chỉ số DORA (Deployment Frequency, MTTR,...).
- Hệ thống CI/CD:
  - Quản lý mã nguồn: AWS CodeCommit và chiến lược Git (GitFlow vs. Trunk-based).
  - Build & test: AWS CodeBuild.
  - Triển khai: AWS CodeDeploy (Blue/Green, Canary, Rolling).
  - Điều phối: tự động hóa pipeline với AWS CodePipeline.
- Demo: trình bày quy trình CI/CD hoàn chỉnh từ đầu đến cuối.
- IaC:
  - CloudFormation: templates, stacks và drift detection.
  - AWS CDK: constructs, patterns tái sử dụng và khả năng hỗ trợ đa ngôn ngữ.
- Trình diễn & thảo luận: triển khai bằng CloudFormation và CDK; so sánh ưu - nhược điểm giữa hai công cụ.

### Buổi Chiều: Containers, Observability & Best Practices (13:00 – 17:00)

- Dịch vụ Container:
  - Docker: các khái niệm cốt lõi về containerization.
  - Amazon ECR: lưu trữ, quét hình ảnh và quản lý vòng đời.
  - ECS & EKS: chiến lược triển khai, khả năng scaling và cơ chế orchestration.
  - App Runner: lựa chọn PaaS đơn giản cho ứng dụng container.
- Giám sát & quan sát hệ thống:
  - AWS CloudWatch: metrics, logs, cảnh báo và dashboards.
  - AWS X-Ray: theo dõi phân tán cho microservices.
- Best practices:
  - Feature flags, A/B testing.
  - Quy trình xử lý sự cố và postmortem.
- Demo & case study: đối chiếu các chiến lược triển khai trong hệ thống microservices.

## Key Takeaways

- Văn hóa DevOps: hiểu rõ DORA metrics và tư duy tự động hóa.
- CI/CD: nắm được cách tích hợp các dịch vụ AWS Code; áp dụng các chiến lược triển khai nâng cao như Blue/Green và Canary.
- IaC: nền tảng cần thiết về CloudFormation và CDK để tối ưu template và các kiến trúc multi-stack.
- Observability: tầm quan trọng của giám sát toàn diện qua CloudWatch và X-Ray để xử lý lỗi (CORS, Lambda, v.v.).
- Container services (ECS/EKS) định hướng cho những kiến trúc phức tạp hơn trong tương lai.
- Các bài demo CI/CD & IaC giúp nhóm hiểu rõ cách cải thiện quy trình triển khai.

## Trải Nghiệm Sự Kiện

- Buổi workshop kéo dài một ngày với nội dung sâu và thực tiễn.
- Các phần demo, case study mang lại giá trị ứng dụng trực tiếp vào dự án.
- Cơ hội trao đổi và kết nối tốt với cộng đồng và các chuyên gia.