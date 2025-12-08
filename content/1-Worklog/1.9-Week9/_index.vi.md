---
title: "Worklog Tuần 9"
date: 2025-11-03
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu Tuần 9:

* Củng cố kỹ năng frontend cốt lõi (React, kiến trúc component).  
* Hiểu cách frontend kết nối với backend chạy trên AWS (API Gateway, Lambda).  
* Nắm vững quản lý biến môi trường và bảo mật khi gọi API.  
* Xây dựng môi trường dev đồng bộ với backend serverless.

---

### Các công việc cần triển khai trong tuần này:

| Ngày | Công việc | Bắt đầu | Hoàn thành | Nguồn tài liệu |
|------|-----------|---------|-------------|--------------------|
| 2 | - Ôn lại React căn bản (hooks, props, state).<br>- Tạo component UI tái sử dụng.<br><br>→ Xây nền tảng React ổn định. | 03/11/2025 | 03/11/2025 | React Docs |
| 3 | - Học cách kết nối frontend với **API Gateway**.<br>- Gửi thử GET/POST đến API serverless.<br>- Xử lý loading, error, success.<br><br>→ Hiểu cơ chế frontend ↔ AWS backend. | 04/11/2025 | 04/11/2025 | AWS Study Group |
| 4 | - Thiết lập **biến môi trường** (.env.local/.env.production).<br>- Tìm hiểu Amplify inject env như thế nào.<br>- Ẩn key và chống lộ secret.<br><br>→ Cải thiện bảo mật tích hợp backend. | 05/11/2025 | 05/11/2025 | Amplify Docs |
| 5 | - Nghiên cứu **CORS**, header auth, token.<br>- Triển khai gọi API yêu cầu token.<br><br>→ Bảo mật giao tiếp giữa UI và AWS. | 06/11/2025 | 06/11/2025 | AWS Security Docs |
| 6 | - Xây demo UI kết nối với API Lambda.<br>- Deploy thử bản test trên Amplify.<br><br>→ Hoàn tất workflow frontend serverless. | 07/11/2025 | 07/11/2025 | Amplify Hosting Guide |

---

### Thành tựu Tuần 9

#### 1. Củng cố React Fundamentals  
- Vững hơn về kiến trúc component và quản lý trạng thái.  
- Tạo bộ UI component chuẩn hóa.

#### 2. Giao tiếp API Cloud  
- Gọi API Gateway thành công từ frontend.  
- Xử lý trạng thái tải và lỗi bài bản.

#### 3. Bảo mật biến môi trường  
- Thiết lập env dev/prod đúng chuẩn.  
- Không để lộ key trong code bundle.

#### 4. Bảo mật request  
- Thêm token vào request và hiểu cơ chế bảo mật.<br>  
- Nắm được CORS và quản lý truy cập cross-origin.

#### 5. Demo Serverless hoàn chỉnh  
- Deploy frontend trên Amplify thành công.  
- Kiểm tra hoạt động end-to-end với Lambda API.