---
title: "Worklog Tuần 2"
date: 2026-05-01
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---



### Mục tiêu tuần 2:

* Hiểu rõ các thành phần cốt lõi trong kiến trúc đám mây: Quản lý định danh, Mạng ảo và Tài nguyên điện toán.
* Thực hành triển khai môi trường mạng cô lập, an toàn và cấu hình máy chủ ảo đi kèm phân quyền dịch vụ bảo mật.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - - Tìm hiểu về Quản lý quyền truy cập với AWS Identity and Access Management (IAM). <br>- Thực hành: Tạo IAM Users, Groups và áp dụng các Policies chi tiết theo nguyên tắc Quyền hạn tối thiểu (Least Privilege).                                                                                    | 27/04/2026   | 27/04/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Tìm hiểu kiến thức cốt lõi về mạng với Amazon Virtual Private Cloud (VPC).<br>- Thực hành: Tự thiết kế hệ thống mạng ảo cơ bản, khởi tạo các phân vùng Public/Private Subnets và cấu hình Route Tables.                | 28/04/2026 | 28/04/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Tiếp tục cấu hình VPC và kiểm soát lưu lượng mạng.<br>- Thực hành: Thiết lập Internet Gateways để kết nối Internet, cấu hình Security Groups và Network ACLs (NACLs) để bảo vệ tài nguyên.                             | 29/04/2026   | 29/04/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Tìm hiểu kiến thức cốt lõi về máy chủ với Amazon Elastic Compute Cloud (EC2).<br>- Thực hành: Khởi chạy máy chủ ảo, cấu hình các ổ đĩa lưu trữ Elastic Block Store (EBS) và quản lý vòng đời của EC2.                  | 30/04/2026   | 30/04/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Tìm hiểu về cơ chế Instance Profiling sử dụng IAM Roles cho EC2.<br>- Thực hành: Tạo và gán IAM Roles vào các thực thể EC2 nhằm cấp quyền tương tác an toàn, không dùng mã truy cập cố định với các dịch vụ AWS khác (như Amazon S3).                                                                                           | 01/05/2026   | 01/05/2026      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 2:

* Hiểu sâu sắc về dịch vụ AWS IAM và làm chủ quy trình phân quyền chi tiết thông qua việc thiết lập Xác thực đa yếu tố (MFA) cùng nguyên tắc Quyền hạn tối thiểu.

* Xây dựng và thiết kế thành công môi trường mạng ảo cô lập bằng Amazon VPC, kiểm soát hiệu quả lưu lượng dữ liệu ra/vào nhờ Internet Gateway, Security Groups và hệ thống tường lửa không trạng thái Network ACLs.

* Thành thạo kỹ năng triển khai và quản trị tài nguyên điện toán ảo trên Amazon EC2 với các hệ điều hành khác nhau, bao gồm việc cấu hình cặp khóa bảo mật (Key Pairs) và không gian lưu trữ khối EBS.

* Làm chủ cơ chế thiết lập Instance Profiles và IAM Roles cho máy chủ EC2, đảm bảo ứng dụng vận hành trên máy chủ tự động tương tác an toàn với các dịch vụ lưu trữ mà không làm lộ lọt thông tin đăng nhập hoặc khóa truy cập dài hạn của AWS.