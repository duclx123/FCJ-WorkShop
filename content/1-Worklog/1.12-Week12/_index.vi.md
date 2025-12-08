---
title: "Worklog Tuần 12"
date: 2025-11-24
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu Tuần 12:

* Tìm hiểu quy trình triển khai frontend tự động trên AWS Amplify hoặc S3 + CloudFront.  
* Thiết lập CI/CD để đảm bảo build và deploy luôn ổn định, nhất quán.  
* Áp dụng cấu hình đa môi trường (dev / staging / prod) cho frontend.  
* Tăng độ tin cậy hệ thống thông qua monitoring, ghi log và kế hoạch rollback.  
* Hoàn thiện tích hợp frontend với toàn bộ backend AWS trước khi đưa vào production.  

---

### Các công việc cần triển khai trong tuần này:

| Ngày | Công việc | Bắt đầu | Hoàn thành | Nguồn tài liệu |
|------|-----------|---------|-------------|----------|
| 2 | - Tìm hiểu cơ chế hoạt động của AWS Amplify Hosting.<br>- Thiết lập môi trường dev/staging/prod.<br>- Cấu hình biến môi trường.<br><br>→ Tạo quy trình deploy nhất quán. | 24/11/2025 | 24/11/2025 | Amplify Hosting Docs |
| 3 | - Tạo pipeline CI/CD bằng Amplify hoặc GitHub Actions.<br>- Tự động build, test, deploy.<br>- Thêm quy tắc deploy theo branch.<br><br>→ Tự động hóa toàn bộ vòng đời triển khai. | 25/11/2025 | 25/11/2025 | GitHub Actions Docs |
| 4 | - Triển khai frontend lên S3 + CloudFront.<br>- Cấu hình cache, invalidation, error page, redirect.<br><br>→ Nắm vững nhiều mô hình hosting khác nhau. | 26/11/2025 | 26/11/2025 | CloudFront Docs |
| 5 | - Bật monitoring bằng CloudWatch + Amplify logging.<br>- Phân tích lỗi, thời gian build, và hiệu năng.<br>- Fix các vấn đề gây mất ổn định khi deploy.<br><br>→ Cải thiện chất lượng vận hành. | 27/11/2025 | 27/11/2025 | CloudWatch Docs |
| 6 | - Kiểm thử full workflow: Frontend → API Gateway → Lambda → DynamoDB.<br>- Test trên cả 3 môi trường.<br>- Viết tài liệu quy trình deploy + rollback.<br><br>→ Đạt trạng thái sẵn sàng cho production. | 28/11/2025 | 28/11/2025 | Internal Docs |

---

### Thành tựu Tuần 12

#### 1. Thiết lập đa môi trường hoàn chỉnh  
- Thiết lập dev/staging/prod trên Amplify thành công.  
- Chuẩn hóa biến môi trường giúp build ổn định và an toàn.

#### 2. CI/CD Tự động hóa hoàn toàn  
- Pipeline GitHub Actions + Amplify hoạt động ổn định.  
- Tự động deploy theo branch, giảm lỗi do thao tác thủ công.

#### 3. Hosting nâng cao với S3 + CloudFront  
- Triển khai bản production thay thế bằng CloudFront để tối ưu hiệu năng.  
- Cấu hình caching và invalidation đúng chuẩn CDN.

#### 4. Theo dõi & Tối ưu Độ Tin Cậy  
- Kích hoạt CloudWatch để theo dõi build, log, và runtime.  
- Phát hiện và xử lý lỗi build, giảm downtime deploy.

#### 5. Kiểm thử tích hợp toàn hệ thống  
- Kiểm thử thành công full pipeline từ frontend tới toàn bộ backend AWS.  
- Ghi lại tài liệu deploy, test, rollback để nhóm dễ dàng tiếp tục phát triển.  
