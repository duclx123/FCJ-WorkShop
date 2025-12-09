---
title: "Blog 3"
date: 2025-01-01
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# Mở rộng AWS Fault Injection Service trong tổ chức của bạn bằng Account Controls  
**Tác giả:** Dylan Reed, Jason Brown, Venkata Moparthi, Isael Pimentel, Satish Kumar  
**Ngày đăng:** 11/04/2025  
**Chuyên mục:** AWS Fault Injection Service (FIS), AWS Resilience Hub (ARH), Management Tools, Resilience

---

## Giới thiệu

AWS Fault Injection Service (FIS) giúp bạn áp dụng **chaos engineering** ở quy mô lớn trong môi trường AWS. Chaos engineering là việc chủ động tạo ra các lỗi có kiểm soát để đánh giá khả năng chịu lỗi và sự phục hồi của hệ thống, giúp nâng cao trải nghiệm người dùng.

Cách tiếp cận chủ động này giúp bạn tự tin hơn vào khả năng phản ứng của hệ thống khi xảy ra sự cố thực tế trong môi trường sản xuất.

Bạn có thể dùng các thí nghiệm FIS để tạo ra các lỗi như:

- Mất điện trong Availability Zone (AZ),  
- Mất kết nối giữa các Region,  
- Gián đoạn mạng tạm thời,

và quan sát ứng dụng phản ứng ra sao.

---

## Khi thực hiện thí nghiệm với lỗi mạng

Trong các thí nghiệm liên quan đến **network fault** như:

- AZ power interruption  
- Region isolation  

bạn cần quyền thay đổi tạm thời cấu hình mạng (ví dụ: `ec2:CreateNetworkAcl`).

Điều này có thể khó khăn nếu tổ chức của bạn sử dụng **mạng tập trung (centralized networking model)**, nơi một nhóm mạng chuyên trách sở hữu và vận hành các tài khoản mạng. Khi đó, các tài khoản ứng dụng có thể không chạy được các hành động mạng trong FIS.

---

## Chuỗi bài viết

Chuỗi ba phần này hướng dẫn cách xác định **safety guardrails** bằng:

- Service Control Policies (SCPs),  
- AWS Identity and Access Management (IAM),

để cho phép ứng dụng chạy thí nghiệm FIS một cách an toàn trong:

- Một tài khoản AWS,  
- Nhiều tài khoản AWS,  
- Hoặc nhiều Region (multi-Region).

---

## Mở rộng AWS FIS trong AWS Organizations

AWS Organizations giúp tổ chức các tài khoản AWS theo cấu trúc phân cấp thông qua **Organizational Units (OUs)**.

**Service Control Policies (SCPs)**:  
Giới hạn quyền truy cập tối đa cho người dùng/role trong tổ chức.

**IAM (trong từng tài khoản)**:  
Quy định quyền truy cập chi tiết cho AWS FIS và các thành phần của nó.

Cấu trúc ví dụ gồm:

- Root OU  
- Sandbox OU  
- Workloads OU (chạy workload)

---

## Chuẩn bị cho các thí nghiệm AWS FIS

Để tạo thí nghiệm (experiment), bạn cần:

- **Experiment template** (chứa định nghĩa hành động lỗi)  
- **IAM role** để thực thi các hành động  
- **Stop conditions**  
- **Safety levers**  
- **Permission controls**

AWS khuyến nghị **chuẩn hóa IAM roles** dùng để tạo template và chạy thí nghiệm.

---

## Chuẩn hóa quyền truy cập AWS FIS

Hai persona chính:

### 1. Account Admin
- Tạo và quản lý SCPs ở cấp OU.  
- Đảm bảo quyền tối thiểu (least privilege).

### 2. IAM Admin
- Tạo IAM roles và policies cho FIS.  
- Policies phải tuân theo SCP.

Hai role tiêu chuẩn cần tạo:

### **AWS-FIS-Experiment-Orchestrator**
- Cho phép tạo, xóa, chỉnh sửa experiment templates.  
- Người dùng cuối sẽ assume role này.

### **AWS-FIS-Experiment-Executor**
- Chỉ được phép chạy các hành động lỗi.  
- Chỉ AWS FIS service được phép assume role này.  

> **Vai trò Executor rất nhạy cảm** vì có thể thay đổi tài nguyên, nên SCP sẽ đóng vai trò guardrail.

---

## Kịch bản thực tế

Trong mô hình mạng tập trung:

- Network team kiểm soát cấu hình mạng.  
- Developer có thể không đủ quyền thực hiện FIS network disruption.  
- Lệnh FIS có thể **thất bại** do thiếu quyền EC2 API.

Vì vậy cần SCP để cho phép chỉ **AWS-FIS-Experiment-Executor** được thực hiện các thay đổi mạng.

---

## SCP mẫu cho Account Admin

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
