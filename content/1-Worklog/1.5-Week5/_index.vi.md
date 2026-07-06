---
title: "Worklog Tuần 5"
date: 2026-05-18
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---



### Mục tiêu tuần 5:

* Hiểu rõ lý thuyết nền tảng và cách sử dụng cơ bản các dịch vụ tính toán không máy chủ (Serverless), quản trị hệ thống tập trung và mô hình định nghĩa hạ tầng bằng mã nguồn (IaC).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu lý thuyết nền tảng về điện toán không máy chủ và làm quen cơ bản với AWS Lambda. <br> - Thực hành: Khởi tạo các hàm Lambda đơn giản, cấu hình nguồn kích hoạt tự động (Triggers) và viết logic xử lý cơ bản                                                                                        | 18/05/2026   | 18/05/2026      |<https://cloudjourney.awsstudygroup.com/> |
| 3   | - Tìm hiểu lý thuyết và làm quen với việc quản trị máy chủ tập trung qua AWS Systems Manager (SSM) và Session Manager.<br> - Thực hành: Cấp quyền quản trị cơ bản, thử nghiệm kết nối Terminal an toàn qua trình duyệt không cần mở cổng mạng và lưu trữ cấu hình bằng Parameter Store.                                          | 19/05/2026   | 19/05/2026       | <https://cloudjourney.awsstudygroup.com/> |
| 4  | - Tìm hiểu các khái niệm và thành phần cốt lõi của mô hình định nghĩa hạ tầng bằng mã nguồn (AWS CDK Essentials).<br>- Thực hành: Khởi tạo cấu trúc một dự án CDK tiêu chuẩn, thiết lập môi trường lập trình tại chỗ và làm quen với việc triển khai thử nghiệm các tài nguyên đám mây bằng code.     |  20/05/2026   | 20/05/2026     | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Nghiên cứu sâu hơn về cấu trúc AWS CDK nâng cao (AWS CDK Advanced) và cơ chế phân phối luồng ứng dụng qua Amazon API Gateway. <br>- Thực hành: Viết mã nguồn CDK để định nghĩa cấu hình mạng API Gateway cơ bản và kết nối thử nghiệm luồng request xuống các hàm Lambda ngầm định.              | 21/05/2026   | 21/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Tổng kết kỹ thuật: Tổng hợp lại hệ thống kiến thức lý thuyết đã tiếp cận trong tuần.                                                       | 22/05/2026   | 22/05/206      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 5:


* Nắm vững nền tảng lý thuyết và cơ chế hoạt động cốt lõi của các mô hình công nghệ đám mây hiện đại bao gồm: kiến trúc không máy chủ (Serverless), hệ thống quản lý máy chủ tập trung và giải pháp hạ tầng dạng mã nguồn (IaC).

* Bước đầu đạt kỹ năng thực hành cơ bản trong việc cấu hình API Gateway để tiếp nhận và điều hướng luồng xử lý xuống các hàm tính toán của AWS Lambda.

* Vận hành thành thạo các tính năng cơ bản của AWS Systems Manager (SSM) thông qua việc lưu trữ tập trung các biến cấu hình tại Parameter Store và dùng Session Manager để truy cập trực tiếp dòng lệnh máy chủ một cách an toàn mà không cần giữ chìa khóa SSH truyền thống.

* Làm quen với vòng đời phát triển hạ tầng bằng AWS CDK, biết cách sử dụng mã nguồn lập trình bậc cao để khởi tạo, tổ chức cấu trúc và triển khai các thành phần hệ thống thay vì thao tác thủ công trên giao diện Web.

* Đạt khả năng phối hợp sử dụng song song giao diện Web Console và công cụ dòng lệnh (CLI) để khởi tạo, vận hành và kiểm tra trạng thái hoạt động của các dịch vụ đám mây được học.