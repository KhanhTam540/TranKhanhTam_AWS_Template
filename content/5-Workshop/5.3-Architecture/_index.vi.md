---
title : "Kiến trúc và thứ tự phụ thuộc"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.3. </b> "
---

#### Kiến trúc

Bài lab MedChain AI sử dụng các dịch vụ AWS sau:

+ **CloudFront** để publish website và chuyển tiếp request `/api/*`.
+ **S3** để host frontend và lưu tài liệu y tế.
+ **API Gateway** để mở API backend.
+ **Lambda** để chạy logic nghiệp vụ backend.
+ **DynamoDB** để lưu dữ liệu ứng dụng.
+ **Cognito** để xác thực người dùng và phân quyền vai trò.
+ **Secrets Manager** để lưu cấu hình tích hợp.
+ **Amazon Managed Blockchain Ethereum** để ghi bằng chứng ledger blockchain thật.
+ **CloudWatch** để giám sát logs, metrics và lỗi.
+ **VNPay Sandbox** là cổng thanh toán bên ngoài.

Người dùng truy cập hệ thống bằng CloudFront distribution domain.

![Sơ đồ kiến trúc](/images/5-Workshop/5.3-Architecture/architecture-0.png)

![Sơ đồ kiến trúc](/images/5-Workshop/5.3-Architecture/architecture-1.png)
#### Thứ tự phụ thuộc

Thứ tự triển khai rất quan trọng vì một số tài nguyên cần output từ bước trước.

1. AWS account, budget, region và local profile.
2. CDK bootstrap resources.
3. VNPay Sandbox credentials.
4. AMB Ethereum node.
5. Secrets Manager configuration và environment variables.
6. CDK application stack.
7. DynamoDB, S3, Cognito, Lambda, API Gateway và CloudFront.
8. Seed dữ liệu mẫu.
9. Build frontend và upload lên S3.
10. CloudFront invalidation.
11. VNPay IPN và Return URL dùng CloudFront domain.
12. Kiểm thử end-to-end và monitoring.
13. Cleanup theo thứ tự ngược lại.

