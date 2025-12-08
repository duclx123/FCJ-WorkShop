---
title: "Worklog Tuần 11"
date: 2025-11-17
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Tiêu đề Tuần 11: **Tối Ưu Hiệu Năng Frontend trong Ứng Dụng Cloud**

### Mục tiêu Tuần 11:

* Tối ưu hiệu năng frontend khi tương tác với backend AWS.  
* Áp dụng chiến lược caching nâng cao (client-side + API Gateway caching).  
* Cải thiện độ phản hồi UI trong điều kiện độ trễ cao hoặc throttling.  
* Tối ưu build frontend: bundling, tree-shaking, code splitting.  
* Triển khai các kỹ thuật bảo mật cho frontend chạy trên hạ tầng cloud.  

---

### Các công việc cần triển khai trong tuần này:

| Ngày | Công việc | Bắt đầu | Hoàn thành | Nguồn tài liệu |
|------|-----------|---------|-------------|--------------------|
| 2 | - Tìm hiểu caching trình duyệt, ETags, Cache-Control.<br>- Dùng SWR/react-query để tối ưu fetch dữ liệu.<br>- Áp dụng client-side caching thực tế.<br><br>→ Giảm tải API và tăng tốc ứng dụng. | 17/11/2025 | 17/11/2025 | React Query Docs |
| 3 | - Phân tích Lighthouse metrics.<br>- Tối ưu các tài nguyên render-blocking.<br>- Tối ưu hình ảnh và áp dụng lazy loading.<br><br>→ Cải thiện điểm hiệu năng web. | 18/11/2025 | 18/11/2025 | Web.Dev |
| 4 | - Cấu hình API Gateway caching.<br>- Kiểm tra cold vs warm Lambda ảnh hưởng UI thế nào.<br>- Xây UI fallback cho trường hợp Lambda cold start.<br><br>→ Tối ưu UI theo hành vi cloud thực tế. | 19/11/2025 | 19/11/2025 | AWS API Gateway Docs |
| 5 | - Tối ưu bundling: tree shaking, code splitting.<br>- Giảm kích thước bundle để tăng tốc load trang.<br><br>→ Tối ưu build production. | 20/11/2025 | 20/11/2025 | Webpack/Vite Docs |
| 6 | - Ôn tập bảo mật: XSS, CSRF, lưu trữ token, enforce HTTPS.<br>- Thực hành best practices của AWS Cognito.<br>- Bảo vệ biến môi trường trong Amplify CI/CD.<br><br>→ Tăng cường bảo mật frontend trên cloud. | 21/11/2025 | 21/11/2025 | AWS Cognito Docs |

---

### Thành tựu Tuần 11

#### 1. Chiến Lược Caching & Fetching Hiệu Quả  
- Triển khai SWR/react-query để quản lý cache thông minh.  
- Giảm đáng kể số lượng request nhờ deduplication và cache persistence.

#### 2. Hiệu Năng Ứng Dụng Tăng Đáng Kể  
- Tăng điểm Lighthouse bằng cách loại bỏ render-blocking assets.  
- Lazy loading và nén ảnh giúp UI tải mượt và nhanh hơn.

#### 3. UI Tối Ưu cho Cloud  
- Bật caching của API Gateway giúp latency thấp hơn đáng kể.  
- Thêm fallback khi cold start Lambda để tránh UI “đơ”.

#### 4. Build Production Nhẹ và Nhanh  
- Sử dụng dynamic import + tree shaking giảm kích thước bundle.  
- Thời gian tải trang đầu tiên nhanh hơn nhiều.

#### 5. Nâng Cao Bảo Mật Frontend  
- Giảm nguy cơ XSS/CSRF với sanitizing + token handling chuẩn.  
- Bảo mật biến môi trường trong Amplify và enforce HTTPS.
