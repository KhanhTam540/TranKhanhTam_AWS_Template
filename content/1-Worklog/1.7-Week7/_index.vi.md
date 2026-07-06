---
title: "Worklog Tuần 7"
date: 2026-06-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---



### Mục tiêu tuần 7:

* Hiểu rõ lý thuyết nền tảng và cách sử dụng cơ bản hệ thống hàng đợi, truyền thông điệp bất đồng bộ trên AWS.

* Tìm hiểu giải pháp quản lý tập trung và tự động hóa phân phối các chính sách bảo mật, tường lửa mạng.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu lý thuyết nền tảng về hệ thống hàng đợi thông điệp bất đồng bộ với Amazon SQS (Simple Queue Service).                                                                                   | 01/06/2026 |	01/06/2026     | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Tìm hiểu lý thuyết nền tảng về mô hình truyền tin xuất bản/đăng ký (Pub/Sub) với Amazon SNS (Simple Notification Service).                                          | 02/06/2026	| 02/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Thực hành kết hợp tích hợp chuỗi hệ thống tin nhắn đám mây (Tích hợp SQS và SNS). | 03/06/2026	| 03/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Tìm hiểu lý thuyết nền tảng về dịch vụ Quản trị chính sách tường lửa bảo mật tập trung (AWS Firewall Manager).                 | 04/06/2026	| 04/06/2026     | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Tổng kết kỹ thuật: Hệ thống hóa lại toàn bộ kiến thức lý thuyết về tích hợp ứng dụng bất đồng bộ và quản trị an toàn mạng.    | 05/06/2026 |	05/06/2026     | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 7:

* Nắm vững kiến thức nền tảng và cơ chế hoạt động của giải pháp truyền tin liên ứng dụng bất đồng bộ (SQS) và hệ thống phân phối thông báo diện rộng (SNS).

* Làm chủ kịch bản cấu hình tích hợp giữa SNS và SQS để thiết lập luồng xử lý thông tin dạng Fan-out cô lập, giảm thiểu sự ràng buộc trực tiếp (Decoupling) giữa các dịch vụ.

* Hiểu rõ tư duy thiết lập hàng rào bảo mật quy mô lớn, cách quản lý tập trung và tự động hóa áp dụng các bộ quy tắc bảo mật thông qua AWS Firewall Manager.

* Đạt khả năng vận hành, thiết lập cấu hình và kiểm tra trạng thái hoạt động của các dịch vụ truyền tin và quản trị tường lửa mạng một cách trơn tru trên AWS Console.