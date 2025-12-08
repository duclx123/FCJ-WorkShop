---
title: "Worklog Tuần 10"
date: 2025-11-10
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu Tuần 10:

* Hiểu cách frontend hoạt động trong **workflow serverless thực tế** (Lambda → DynamoDB → API Gateway).  
* Triển khai xử lý dữ liệu nâng cao: pagination, filter, optimistic update.  
* Nắm rõ quy trình deploy frontend qua **Amplify Hosting CI/CD**.  
* Cải thiện độ ổn định của ứng dụng bằng error boundary, retry logic.  
* Tăng cường kiến trúc UI sẵn sàng cho môi trường production.

---

### Các công việc cần triển khai trong tuần này:

| Ngày | Công việc | Bắt đầu | Hoàn thành | Nguồn tài liệu |
|------|-----------|---------|-------------|--------------------|
| 2 | - Nghiên cứu Fetch + Axios nâng cao.<br>- Thêm interceptors cho auth và retry.<br>- Đánh giá performance và caching API.<br><br>→ Tăng sự ổn định khi gọi API. | 10/11/2025 | 10/11/2025 | Axios Docs |
| 3 | - Xây UI CRUD kết nối AWS backend.<br>- Kết nối API Gateway + Lambda + DynamoDB.<br>- Thêm pagination & filter vào UI.<br><br>→ Hoàn thiện tích hợp dữ liệu. | 11/11/2025 | 11/11/2025 | AWS Study Group |
| 4 | - Tìm hiểu quy trình deploy trên Amplify.<br>- Cấu hình build preview cho từng branch.<br>- Tạo nhiều môi trường deploy (dev/staging/prod).<br><br>→ Nắm chu trình vận hành của frontend trên AWS. | 12/11/2025 | 12/11/2025 | Amplify Hosting Docs |
| 5 | - Thêm error boundaries vào React.<br>- Implement retry logic cho API fail.<br>- Dùng CloudWatch log để tinh chỉnh UI.<br><br>→ Tăng khả năng chịu lỗi. | 13/11/2025 | 13/11/2025 | React Docs |
| 6 | - Stress test UI bằng delay, lỗi, throttling.<br>- Cải thiện UX: skeleton loading, optimistic UI, fallback states.<br><br>→ Chuẩn bị UI cho môi trường cloud thực tế. | 14/11/2025 | 14/11/2025 | Cloud Design Patterns |

---

### Kết quả Tuần 10

#### 1. Chiến lược Giao Tiếp API Vững Chắc  
- Thêm interceptors (auth + retry) giúp gọi API ổn định hơn.  
- Giảm tỷ lệ thất bại khi gọi API.

#### 2. UI CRUD Hoàn Chỉnh trên AWS Backend  
- Xây xong UI thao tác CRUD qua API Gateway + Lambda + DynamoDB.  
- Pagination & filter đồng bộ với backend.

#### 3. Thành Thạo Quy Trình Deploy Amplify  
- Hiểu CI/CD pipeline của Amplify Hosting.  
- Tạo build preview để test từng feature.

#### 4. Nâng Cao Khả Năng Chịu Lỗi  
- Thêm global error boundaries trong React.  
- Retry/fallback logic cho API không ổn định.  
- Dùng CloudWatch để phân tích lỗi và tinh chỉnh UI.

#### 5. Cải Thiện Trải Nghiệm Người Dùng  
- Test delay/throttling để tối ưu UI.  
- Thêm skeleton loading + optimistic UI để mượt hơn.