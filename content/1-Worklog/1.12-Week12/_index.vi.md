---
title: "Worklog Tuần 12"
date: 2026-06-06
weight: 2
chapter: false
pre: " <b> 1.12 </b> "
---


### Mục tiêu tuần 12:

* Kiểm thử triển khai cuối cho backend, frontend, CloudFront và truy cập production.

* Kiểm tra tính toàn vẹn hồ sơ bệnh án, xác thực ledger, thông tin giao dịch AMB và luồng callback thanh toán.

* Hoàn thiện nội dung báo cáo, minh chứng kiểm thử, hướng dẫn triển khai và tài liệu dự án.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Kiểm tra triển khai cuối bằng cách deploy lại backend, build frontend, upload lên S3, xóa cache CloudFront và kiểm tra website production.                            | 06/07/2026 | 06/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Kiểm thử xác thực ledger, kiểm tra blockHash và previousHash, đồng thời xác minh hồ sơ bệnh án sau khi reset dataset và backfill. | 07/07/2026 | 07/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Rà soát các trường giao dịch AMB và luồng xác nhận thanh toán VNPay/MoMo, gồm callback, mã giao dịch và cập nhật trạng thái hóa đơn. | 08/07/2026 | 08/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Kiểm tra IAM, quyền truy cập Cognito, CloudWatch Logs, cấu hình CloudFront, việc sử dụng AMB và rủi ro chi phí liên quan đến thanh toán. | 09/07/2026 | 09/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   |- Chuẩn bị nội dung báo cáo cuối gồm kiến trúc, các bước triển khai, hướng dẫn dataset, sử dụng AMB, luồng thanh toán và minh chứng kiểm thử. | 10/07/2026 | 10/07/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 12:

* Hoàn thành kiểm tra triển khai cuối và truy cập môi trường production.

* Kiểm tra hiển thị hồ sơ bệnh án theo CCCD và xác thực Medical Integrity Ledger.

* Rà soát thông tin giao dịch AMB, luồng thanh toán VNPay/MoMo và tài liệu báo cáo cuối.