---
title: "Worklog Tuần 10"
date: 2026-06-22
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---



### Mục tiêu tuần 10:

* Xây dựng hạ tầng AWS cốt lõi cho hệ thống SmartHospital P2TB bằng AWS CDK.

* Cấu hình xác thực, backend API, lưu trữ dữ liệu, hosting frontend và phân phối qua CloudFront.

* Chuẩn bị dataset ban đầu và kiểm tra kết nối giữa frontend, backend, Cognito và DynamoDB.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Cấu hình các tài nguyên AWS chính bằng CDK, gồm Lambda, bảng DynamoDB, Cognito User Pool, API Gateway, S3 bucket và CloudFront distribution.               | 22/06/2026   | 22/06/2026      |<https://cloudjourney.awsstudygroup.com/> |
| 3   | - Thiết lập xác thực người dùng, tạo Cognito groups và kiểm tra luồng đăng nhập cho tài khoản Admin, Bác sĩ, Nhân sự y tế và Bệnh nhân.                          | 23/06/2026   | 23/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Triển khai các API Lambda ban đầu cho hồ sơ người dùng, thông tin bệnh nhân, thông tin bác sĩ, dữ liệu lịch hẹn và truy cập hồ sơ bệnh án.                     | 24/06/2026  | 24/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Xây dựng frontend React, upload file tĩnh lên S3, cấu hình CloudFront và kiểm tra truy cập website thông qua domain triển khai.                                  | 25/06/2026  | 25/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | Tạo dữ liệu mẫu cho người dùng, bệnh nhân, bác sĩ, lịch hẹn, hồ sơ, xét nghiệm, hóa đơn và kiểm tra frontend lấy dữ liệu từ DynamoDB.                           | 26/06/2026   | 26/06/2026      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 10:

* Cấu hình thành công hạ tầng AWS chính bằng CDK.

* Hoàn thành thiết lập Cognito authentication và nhóm phân quyền.

* Triển khai các API backend đầu tiên bằng Lambda và API Gateway.

* Đưa frontend lên S3 và phân phối qua CloudFront.

* Tạo bộ dữ liệu mẫu đầu tiên để kiểm thử hệ thống.