---
title: "Event 1"
date: 2026-05-23
weight: 2
chapter: false
pre: " <b> 4.1. </b> "
---

# Bài thu hoạch “FCAJ Community Day”

### Mục Đích Của Sự Kiện

- Chia sẻ kiến thức thực tế về AWS, AI, kiến trúc cloud, DevOps và phát triển ứng dụng hiện đại
- Giới thiệu các ứng dụng thực tế của AI agents, LLMs, Amazon CloudFront, Amazon Quick và hệ thống multi-agent
- Giúp sinh viên và người học cloud hiểu cách sử dụng AI hiệu quả hơn thông qua context và tư duy thiết kế hệ thống
- Trình bày các bài học thực tế từ hackathon, hệ thống AI production, kiến trúc CDN và triển khai AI cấp doanh nghiệp
- Tạo môi trường học tập và kết nối cho sinh viên, lập trình viên, DevOps engineer, AI builders và cộng đồng AWS

### Danh Sách Diễn Giả

- **anh Tịnh** – Platform Engineer, GoTymeX  
  Chủ đề: **Context Is Everything - Making AI Actually Work for You**

- **anh Hải Anh** – G-AsiaPacific Vietnam, AWS Community Builder  
  Chủ đề: **Friendly AI Assistant with Amazon Quick**

- **anh Tuấn Thịnh** – DevOps Engineer, First Cloud AI Journey  
  Chủ đề: **From Edge to Origin: CloudFront as Your Foundation**

- **Team VIB**  
  Chủ đề: **36 hrs with LotusHacks – Building UTMorpho from Idea to Reality**

- **anh Đức** – Solution Architect, Cloud Kinetics  
  Chủ đề: **Non-Determinism of “Deterministic” LLM Settings**

- **chị Cát Vy** – Senior Business Systems Analyst, VPBank  
  Chủ đề: **Enterprise-Grade Multi-Agent System: The Case of Startup Credit Scoring**

### Tổng Quan Sự Kiện

**FCAJ Community Day** là một sự kiện cộng đồng tập hợp nhiều Phần chia sẻ kỹ thuật về AWS, AI, kiến trúc cloud, DevOps, hành vi của LLM, xây dựng sản phẩm trong hackathon và hệ thống multi-agent cấp doanh nghiệp. Sự kiện cung cấp cả kiến thức kỹ thuật lẫn kinh nghiệm thực tế từ các diễn giả đang làm việc với cloud và AI trong môi trường thực tế.

Sự kiện có giá trị vì không chỉ tập trung vào một chủ đề duy nhất. Thay vào đó, nội dung bao phủ nhiều mảng công nghệ hiện đại. Người tham gia có thể học cách sử dụng AI hiệu quả hơn thông qua context, cách Amazon Quick hỗ trợ người dùng doanh nghiệp, cách Amazon CloudFront cải thiện hiệu năng và bảo mật từ edge đến origin, cách một đội hackathon xây dựng sản phẩm trong thời gian ngắn, vì sao LLM vẫn có thể không ổn định dù đặt temperature bằng 0, và cách thiết kế hệ thống multi-agent cho bài toán chấm điểm tín dụng startup.

### Nội Dung Nổi Bật

#### Context Is Everything - Making AI Actually Work for You

Phần này giải thích rằng các mô hình AI hiện nay đã rất mạnh, nhưng nhiều câu trả lời kém chất lượng thường đến từ context yếu chứ không hẳn do mô hình yếu. Diễn giả nhấn mạnh rằng AI không thể tự hiểu hoàn toàn mục tiêu, tình huống, ràng buộc hoặc tiêu chí thành công nếu người dùng không cung cấp rõ.

Phần chia sẻ giới thiệu ý nghĩa của context trong sử dụng AI. Context bao gồm mục tiêu của người dùng, tình huống hiện tại, các ràng buộc, bằng chứng liên quan, định dạng kết quả mong muốn và tiêu chí đánh giá câu trả lời tốt. Khi các yếu tố này được cung cấp rõ ràng, AI có thể tạo ra câu trả lời hữu ích và chính xác hơn.

Một số lỗi phổ biến được nêu ra gồm:

- Cung cấp quá nhiều thông tin không liên quan cho AI
- Sao chép toàn bộ bài viết, ảnh chụp hoặc tài liệu mà không lọc nội dung cần thiết
- Nói với AI những điều hiển nhiên mà nó đã biết
- Đặt câu hỏi mơ hồ, không có mục tiêu hoặc ràng buộc
- Tập trung vào số lượng context thay vì chất lượng context

Phần này cũng giới thiệu sự phát triển từ **prompt** sang **context** và sau đó là **memory**. Một hệ thống AI tốt hơn không chỉ là chatbot trả lời từng câu hỏi độc lập. Nó có thể trở thành một second AI brain, ghi nhớ những gì người dùng đang học, hiểu dự án và mục tiêu, truy xuất thông tin liên quan và cải thiện theo thời gian.

#### Friendly AI Assistant with Amazon Quick

Phần này giới thiệu cách Amazon Quick có thể hỗ trợ người dùng doanh nghiệp bằng cách tạo ra trải nghiệm AI assistant thống nhất hơn. Trong nhiều tổ chức, người dùng nghiệp vụ phải thu thập thông tin từ nhiều nguồn, phân tích tài liệu, tham khảo chuyên gia và lặp lại nhiều tác vụ thường xuyên. Những công việc này tốn thời gian và làm giảm năng suất.

Amazon Quick cung cấp một trải nghiệm tích hợp, nơi người dùng có thể làm việc với dữ liệu công ty, kiến thức thế giới, file do người dùng tải lên, database, data warehouse, dashboard, automation flows và các hành động từ bên thứ ba. Hệ thống cũng bao gồm governance, data security, access controls, guardrails và responsible AI.

Một use case được trình bày là **PM assistant**. Trợ lý này có thể tự động tạo biên bản họp, gửi email cho các bên liên quan và lên lịch cuộc họp tiếp theo. Điều này cho thấy AI có thể hỗ trợ các công việc văn phòng phổ biến và giảm thao tác thủ công lặp lại.

#### From Edge to Origin: CloudFront as Your Foundation

Phần này tập trung vào Amazon CloudFront và cách dịch vụ này có thể đóng vai trò nền tảng cho hiệu năng, bảo mật, độ bền vững và tối ưu chi phí. Diễn giả giải thích rằng mô hình pay-as-you-go của cloud rất mạnh, nhưng cũng có thể tạo ra nỗi lo về chi phí tăng đột biến khi lưu lượng tăng bất ngờ hoặc khi bị tấn công.

Amazon CloudFront giúp giải quyết nhiều vấn đề bằng cách cache nội dung gần người dùng hơn, giảm tải cho origin, cải thiện độ trễ và hỗ trợ các tính năng bảo mật tại edge.

Phần chia sẻ đề cập đến nhiều khả năng quan trọng:

- CDN và edge caching
- Tích hợp AWS WAF
- Bảo vệ DDoS
- Tích hợp Route 53 và DNS
- Origin Shield
- Request collapsing
- Rate limiting và throttling
- Mã hóa HTTPS khi truyền tải
- Origin Access Control
- Signed URLs
- Geographic restrictions
- Origin failover
- Custom error pages
- HTTP compression
- Hỗ trợ HTTP/3
- Edge logic với CloudFront Functions và Lambda@Edge

Phần này cũng giải thích cách CloudFront có thể giảm chi phí cho origin. Ví dụ, khi CloudFront xử lý caching và compression, origin server nhận ít request hơn và tiêu thụ ít CPU hơn. CloudFront cũng có thể giúp giảm data transfer và chi phí load balancer trong một số trường hợp.

#### 36 hrs with LotusHacks – Building UTMorpho from Idea to Reality

Phần này chia sẻ trải nghiệm của Team VIB trong LotusHacks 2026. Đội tham gia hackathon lớn nhất Việt Nam và có 36 giờ để tạo ra một sản phẩm từ ý tưởng đến bản demo.

Phần chia sẻ mô tả hành trình từ lúc đăng ký còn mơ hồ, phát hiện vấn đề thực tế từ công việc hằng ngày, định nghĩa ý tưởng sản phẩm, xây dựng dưới áp lực thời gian và cuối cùng là chuẩn bị phần giới thiệu sản phẩm và demo.

Sản phẩm được nhắc đến trong Phần là **UTMorpho**. Mặc dù dữ liệu slide tập trung nhiều vào hành trình hơn là chi tiết kỹ thuật triển khai, Phần này thể hiện rõ quá trình biến một ý tưởng chưa rõ ràng thành một sản phẩm hoạt động được trong thời gian giới hạn.

Một số bài học thực tế được nhấn mạnh:

- Sự khó chịu trong công việc thực tế có thể tạo ra ý tưởng sản phẩm thật
- Nhiều ý tưởng hơn không đồng nghĩa với ý tưởng tốt hơn
- Hackathon kiểm tra sức bền và khả năng làm việc nhóm
- Đồng bộ giữa các thành viên là yếu tố rất quan trọng
- Xây dựng sản phẩm dưới áp lực cần biết ưu tiên
- Trải nghiệm chỉnh sửa tập trung có thể cải thiện khả năng sử dụng sản phẩm

Phần này cũng nhắc đến các thách thức như AI overgeneration, token limits, kiệt sức gần thời điểm pitch và khó khăn khi hoàn thiện sản phẩm trong thời gian ngắn.

#### Non-Determinism of “Deterministic” LLM Settings

Phần này giải thích vì sao mô hình ngôn ngữ lớn vẫn có thể tạo ra kết quả khác nhau ngay cả khi cấu hình có vẻ deterministic. Nhiều người dùng cho rằng đặt temperature bằng 0 sẽ đảm bảo cùng một output cho cùng một prompt. Tuy nhiên, diễn giả giải thích rằng giả định này không phải lúc nào cũng đúng.

Phần chia sẻ đầu tiên giải thích cách LLM tạo văn bản. Ở mỗi bước, mô hình tạo điểm số cho các token tiếp theo có thể xuất hiện. Các điểm số này được chuyển thành xác suất bằng softmax, sau đó token tiếp theo được chọn dựa trên cấu hình decoding.

Temperature kiểm soát độ ngẫu nhiên:

- Temperature cao làm tăng độ ngẫu nhiên và sáng tạo
- Temperature gần 0 giúp output nhất quán hơn
- Temperature bằng 0 về mặt lý thuyết sẽ chọn token có xác suất cao nhất

Tuy nhiên, trong hệ thống thực tế, non-determinism vẫn có thể xảy ra. Diễn giả tham chiếu nghiên cứu cho thấy nhiều LLM vẫn tạo output không nhất quán qua nhiều lần chạy lặp lại với cùng prompt, cùng cấu hình và temperature bằng 0.

Nguyên nhân gồm:

- Tính toán floating-point trên GPU
- Các phép toán không có tính kết hợp tuyệt đối
- Thứ tự thực thi song song trên GPU
- Inference batching từ nhà cung cấp API
- Sai khác làm tròn rất nhỏ có thể làm thay đổi token được chọn

Điều này quan trọng vì nhiều use case production yêu cầu độ tin cậy cao, chẳng hạn như truy xuất thông tin y tế, phân tích tài liệu pháp lý, lập kế hoạch tài chính, tạo structured output, benchmarking và regression testing.

Phần chia sẻ đề xuất một số cách giảm thiểu:

- Chạy nhiều lần và dùng majority voting
- Sử dụng structured output như JSON mode hoặc function calling
- Sử dụng constrained decoding khi có thể
- Self-host model khi cần kiểm soát hạ tầng inference
- Thiết kế hệ thống downstream có thể xử lý sự khác biệt
- Kiểm thử kỹ và lặp lại nhiều lần
- Cân nhắc dùng temperature 0.1 nếu temperature 0 gây lặp vô hạn

#### Enterprise-Grade Multi-Agent System: The Case of Startup Credit Scoring

Phần này giới thiệu cách hệ thống multi-agent có thể được sử dụng cho bài toán chấm điểm tín dụng startup. Diễn giả giải thích rằng các hệ thống chấm điểm tín dụng truyền thống được thiết kế cho doanh nghiệp đã hoạt động ổn định, không phải startup.

Chấm điểm tín dụng truyền thống thường yêu cầu:

- Báo cáo tài chính trong nhiều năm
- Lịch sử tín dụng rõ ràng
- Tài sản thế chấp vật lý
- Doanh thu dự đoán được
- Báo cáo theo chuẩn
- Benchmark ngành

Trong khi đó, startup thường có đặc điểm khác:

- Thời gian hoạt động ngắn
- Ít hoặc không có lịch sử tín dụng
- Tài sản chính có thể là IP, đội ngũ và traction
- Mô hình tăng trưởng nhanh hoặc thay đổi hướng đi
- Mô hình kinh doanh mới
- Dữ liệu phi cấu trúc ở khắp nơi

Vì dữ liệu startup có nhiều chiều, một AI agent duy nhất có thể không đủ. Mỗi miền phân tích cần chuyên môn riêng như phân tích tài chính, phân tích thị trường, đánh giá đội ngũ, đánh giá rủi ro và kiểm tra tuân thủ.

Phần này đề xuất kiến trúc **virtual credit committee**, trong đó nhiều agent chuyên biệt phối hợp với nhau:

- Manager agent
- Financial Analyst agent
- Market Analyst agent
- Team Evaluator agent
- Risk Assessor agent
- Compliance agent

Hệ thống tạo ra các kết quả như credit score, risk rating, confidence level và audit trail.

Phần này cũng giải thích vì sao multi-agent system hiệu quả:

- Chuyên môn hóa theo từng lĩnh vực
- Có cơ chế kiểm tra và cân bằng
- Xử lý song song
- Có khả năng audit
- Dễ mở rộng
- Có khả năng chịu lỗi

Điểm mạnh của Phần này là nhấn mạnh tư duy enterprise-grade. Một bản proof of concept chưa đủ để đưa vào production. Hệ thống AI doanh nghiệp cần bảo mật, quản trị dữ liệu, cô lập mạng, vận hành, yếu tố con người và tuân thủ.

### Những Gì Học Được

#### AI và Context

- AI models rất mạnh, nhưng context yếu có thể dẫn đến kết quả kém.
- Context tốt giúp AI hiểu mục tiêu, ràng buộc và định dạng đầu ra mong muốn.
- Context engineering đang trở thành kỹ năng quan trọng trong tương lai.
- Second AI brain có thể được xây dựng bằng cách kết hợp context, memory, retrieval và generation.

#### AI Assistant và Năng Suất Làm Việc

- AI assistant có thể hỗ trợ người dùng nghiệp vụ bằng cách kết nối dữ liệu công ty và workflow.
- Amazon Quick có thể hỗ trợ datasets, dashboards, automation, chat, research và third-party actions.
- AI assistant thực tế có thể giảm các tác vụ lặp lại như tạo biên bản họp, gửi email và lên lịch họp.

#### CloudFront và Kiến Trúc Cloud

- Amazon CloudFront không chỉ là CDN.
- CloudFront cải thiện hiệu năng, bảo mật, độ tin cậy và tối ưu chi phí.
- Caching, compression, origin shielding, signed URLs và failover có thể giảm tải origin và cải thiện trải nghiệm người dùng.
- Edge services giúp bảo vệ ứng dụng trước tấn công và lưu lượng tăng đột biến.

#### Hackathon và Xây Dựng Sản Phẩm

- Ý tưởng sản phẩm tốt có thể đến từ sự khó chịu trong công việc hằng ngày.
- Hackathon yêu cầu sự tập trung, làm việc nhóm và sức bền.
- Một sản phẩm hoạt động được cần ưu tiên rõ ràng, tích hợp tốt, chuẩn bị demo và storytelling.
- Đồng bộ trong đội thường quan trọng hơn số lượng ý tưởng.

#### Độ Tin Cậy Của LLM

- Temperature bằng 0 không hoàn toàn đảm bảo output deterministic.
- Thực thi GPU, sai khác floating-point và inference batching có thể làm output thay đổi.
- Hệ thống LLM production cần được thiết kế để xử lý sự biến thiên.
- Structured output, multiple runs, testing và constrained decoding có thể cải thiện độ tin cậy.

#### Hệ Thống Multi-Agent Cấp Doanh Nghiệp

- Single-agent phù hợp với workflow đơn giản, nhưng quyết định phức tạp cấp doanh nghiệp có thể cần multi-agent architecture.
- Các agent chuyên biệt có thể cải thiện chất lượng suy luận, khả năng audit và chịu lỗi.
- Enterprise AI phải bao gồm bảo mật, tuân thủ, governance, monitoring và ROI rõ ràng.
- Guardrails là yêu cầu bắt buộc cho hệ thống AI production.

### Ứng Dụng Vào Công Việc

- Chuẩn bị context tốt hơn trước khi yêu cầu AI giải quyết bài toán kỹ thuật hoặc học tập.
- Sử dụng framework context gồm mục tiêu, thông tin liên quan, ràng buộc và tiêu chí thành công.
- Khám phá các use case AI assistant để tự động hóa tác vụ nghiệp vụ hoặc công việc dự án lặp lại.
- Sử dụng CloudFront như lớp nền tảng cho hiệu năng, bảo mật, caching và bảo vệ origin.
- Thiết kế hệ thống có cân nhắc chi phí, đặc biệt khi lưu lượng có thể tăng bất ngờ.
- Xem output của LLM là có tính xác suất và kiểm thử tính năng AI qua nhiều lần chạy.
- Sử dụng JSON mode hoặc function calling khi xây dựng ứng dụng AI cần structured output.
- Cân nhắc multi-agent system cho workflow phức tạp cần nhiều lĩnh vực chuyên môn.
- Bổ sung guardrails, monitoring và compliance check khi đưa hệ thống AI đến gần production.
- Xây dựng prototype nhỏ trước, sau đó cải tiến dần thành giải pháp đáng tin cậy hơn.

### Trải nghiệm trong event

Tham gia **“AWS Vietnam Community Day - May 2026”** là một trải nghiệm học tập rất hữu ích vì sự kiện bao phủ cả kiến thức kỹ thuật chuyên sâu lẫn bài học triển khai thực tế. Các Phần chia sẻ rất đa dạng, từ tư duy sử dụng AI, kiến trúc cloud, độ tin cậy của LLM, trải nghiệm hackathon đến triển khai AI cấp doanh nghiệp.

#### Học cách sử dụng AI tốt hơn

Phần về context giúp tôi nhận ra rằng chất lượng đầu ra của AI phụ thuộc rất lớn vào chất lượng đầu vào. Thay vì chỉ viết prompt ngắn, người dùng nên cung cấp mục tiêu rõ ràng, thông tin liên quan, ràng buộc và tiêu chí thành công. Điều này thay đổi cách tôi nhìn AI từ một chatbot đơn giản thành một hệ thống cần được thiết kế context phù hợp.

#### Hiểu về AI assistant cho người dùng nghiệp vụ

Phần Amazon Quick cho thấy AI assistant có thể hữu ích vượt ra ngoài phạm vi phát triển phần mềm. AI có thể hỗ trợ người dùng nghiệp vụ bằng cách thu thập thông tin, phân tích dữ liệu công ty, tạo ghi chú cuộc họp, gửi email và tự động hóa tác vụ lặp lại. Điều này giúp tôi hiểu cách AI có thể trở thành một phần của công việc hằng ngày.

#### Học CloudFront như một lớp nền tảng

Phần CloudFront hữu ích vì cho thấy CloudFront không chỉ dùng để tăng tốc website tĩnh. Nó còn có thể cải thiện bảo mật, giảm tải origin, chống tấn công, hỗ trợ failover và kiểm soát chi phí. Điều này giúp tôi có góc nhìn rộng hơn về CDN architecture và edge computing.

#### Học từ hành trình hackathon

Phần LotusHacks truyền cảm hứng vì cho thấy quy trình thực tế khi xây dựng sản phẩm dưới áp lực thời gian. Đội phải đi từ phát hiện ý tưởng đến triển khai, tích hợp, demo và pitch trong 36 giờ. Phần này cho thấy xây dựng sản phẩm cần sự tập trung, giao tiếp và sức bền.

#### Hiểu về non-determinism của LLM

Phần về LLM là một trong những phần kỹ thuật nhất. Nội dung giúp tôi hiểu rằng ngay cả khi đặt temperature bằng 0, output của LLM vẫn có thể thay đổi do tính toán GPU, sai khác floating-point và inference batching. Đây là bài học quan trọng cho bất kỳ ai xây dựng ứng dụng AI production.

#### Hiểu về hệ thống multi-agent cấp doanh nghiệp

Phần credit scoring bằng multi-agent giúp tôi hiểu khi nào kiến trúc multi-agent thật sự hữu ích. Đối với các quyết định phức tạp, rủi ro cao và cần audit, nhiều agent chuyên biệt có thể hoạt động như một hội đồng ảo. Kiến trúc này cải thiện chất lượng suy luận, khả năng truy vết và khả năng chịu lỗi.

#### Bài học rút ra

- Kết quả AI tốt cần context tốt.
- AI assistant nên được kết nối với dữ liệu đáng tin cậy và workflow nghiệp vụ.
- CloudFront có thể cải thiện chi phí, hiệu năng, bảo mật và độ tin cậy.
- Hackathon giúp rèn luyện làm việc nhóm, ưu tiên và ra quyết định nhanh.
- LLM cần được kiểm thử kỹ vì cấu hình deterministic vẫn có thể tạo ra biến thiên.
- Enterprise AI cần bảo mật, tuân thủ, monitoring, guardrails và ROI rõ ràng.

#### Một số hình ảnh khi tham gia sự kiện

![Your event picture](/images/4-Event/Event_1/picture-event1-1.jpg)
![Your event picture](/images/4-Event/Event_1/picture-event1-2.jpg)
![Your event picture](/images/4-Event/Event_1/picture-event1-3.jpg)

> Tổng thể, sự kiện giúp tôi hiểu cách AWS và AI có thể được áp dụng trong nhiều tình huống thực tế. Sự kiện cũng cho thấy một hệ thống cloud và AI thành công không chỉ cần công cụ kỹ thuật, mà còn cần tư duy thiết kế tốt, nhận thức bảo mật, kiểm thử và kinh nghiệm triển khai thực tế.