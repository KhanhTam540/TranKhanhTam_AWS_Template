---
title: "Event 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---


# Bài thu hoạch “FCAJ Community Day”

### Mục Đích Của Sự Kiện


- Giới thiệu các use case thực tế về AI agents và tự động hóa trên AWS
- Trình bày cách thiết kế voice agents cho hội thoại tự nhiên và có khả năng mở rộng
- Trình bày về DevOps Agent ( Devops Agent là gì?, Một số use case phù hợp với DevOps Agent,...)
- Phân tích cách AI có thể hỗ trợ vận hành, năng suất làm việc và quy trình doanh nghiệp (cụ thể là công việc HR)
- Giới thiệu về Amazon Q cũng như hướng dẫn những thao tác cơ bản với Amazon Q

### Danh Sách Diễn Giả

- **anh Steve Trần** - CTO Cloud Thinker
- **anh Hiếu Nghị, anh Kiệt, anh Trung** 
- **chị Bảo và anh Nguyên** - Cloud Kinetics
- **anh Trường và chị Minh Anh** - Noventiq 
- **anh Toàn và anh Hiếu Nghị** - 

### Nôi Dung Của Sự Kiện

#### AgenticOps for your Cloud

Phần này giới thiệu ý tưởng chuyển từ mô hình giám sát và cảnh báo truyền thống sang phản hồi sự cố thông minh hơn. Thay vì chỉ phát hiện lỗi và gửi cảnh báo cho con người, một hệ thống phản hồi sự cố có hỗ trợ AI có thể phân tích vấn đề, đề xuất hành động và hỗ trợ xử lý nhanh hơn.

Nội dung Phần chia sẻ cho thấy AI có thể hỗ trợ đội ngũ vận hành bằng cách giảm các tác vụ điều tra lặp lại. Trong môi trường cloud hiện đại, hệ thống tạo ra rất nhiều log, metric và event. AI có thể giúp tóm tắt thông tin, xác định nguyên nhân tiềm năng và đề xuất bước xử lý tiếp theo.

#### Voice Agents: Building Voice Agent at Scale

Phần này tập trung vào việc xây dựng voice agents có khả năng tương tác với người dùng một cách tự nhiên và gần giống con người. Các diễn giả nhấn mạnh rằng làm cho mô hình AI có thể nói không còn là phần khó nhất. Thách thức thật sự xuất hiện khi hệ thống cần hoạt động ổn định trong môi trường production.

Một hệ thống voice agent thường gồm nhiều thành phần:

- Speech-to-Text để chuyển giọng nói người dùng thành văn bản
- Large Language Model để hiểu yêu cầu và tạo phản hồi
- Text-to-Speech để chuyển phản hồi thành giọng nói
- Lớp giao tiếp thời gian thực để duy trì hội thoại mượt mà
- Tích hợp với công cụ nghiệp vụ để thực hiện hành động thực tế

Phần chia sẻ nhấn mạnh một số thách thức khi triển khai production:

- Giữ độ trễ thấp trong pipeline STT → LLM → TTS
- Xử lý ngắt lời mà không cắt lời người dùng quá sớm
- Nhận diện đúng ngữ cảnh, sắc thái và ý định
- Hỗ trợ hội thoại tự nhiên bằng tiếng Việt
- Kết nối voice agents với công cụ để thực hiện tác vụ thực tế
- Cân bằng giữa chất lượng phản hồi, chi phí hạ tầng và khả năng mở rộng

#### AWS DevOps Agent: Your Always-Available Operations Teammate

Phần này trình bày cách AI agents có thể hỗ trợ đội ngũ DevOps như một trợ lý vận hành luôn sẵn sàng. Trong công việc hằng ngày, DevOps engineer thường phải kiểm tra log, phân tích cảnh báo, xem lỗi triển khai, kiểm tra trạng thái hạ tầng và phản hồi sự cố.

Một AI DevOps agent có thể hỗ trợ bằng cách:

- Tóm tắt cảnh báo và sự cố
- Tìm kiếm log và metric
- Đề xuất các bước troubleshooting
- Giải thích thay đổi hạ tầng
- Hỗ trợ phân tích deployment
- Giảm các công việc vận hành lặp lại

Phần chia sẻ cho thấy AI không thay thế DevOps engineer. Thay vào đó, AI hỗ trợ kỹ sư bằng cách giảm thời gian điều tra thủ công và giúp họ tập trung vào các quyết định quan trọng hơn.

#### AI-Powered Productivity: Workforce Planning For Enterprise

Phần này tập trung vào cách AI cải thiện năng suất và hỗ trợ lập kế hoạch nguồn lực trong môi trường doanh nghiệp. Workforce planning yêu cầu tổ chức hiểu rõ phân bổ nguồn lực, khối lượng công việc của đội nhóm, yêu cầu kỹ năng, nhu cầu kinh doanh và các ràng buộc vận hành.

AI có thể hỗ trợ workforce planning bằng cách phân tích dữ liệu, nhận diện xu hướng và giúp nhà quản lý đưa ra quyết định tốt hơn. Thay vì chỉ dựa vào bảng tính thủ công hoặc báo cáo tĩnh, hệ thống có hỗ trợ AI có thể cung cấp góc nhìn linh hoạt và dựa trên dữ liệu hơn.

Phần này nhấn mạnh rằng công cụ AI productivity nên được thiết kế để hỗ trợ ra quyết định. Chúng không chỉ tạo câu trả lời, mà còn giúp tổ chức hiểu mô hình dữ liệu, cải thiện kế hoạch và giảm khối lượng công việc hành chính.

#### Building Secure Private MCP Connection with Amazon Q

Phần này tập trung vào kết nối riêng tư an toàn cho Model Context Protocol, hay MCP. MCP là một khái niệm quan trọng trong hệ thống AI agents hiện đại vì nó cho phép agent kết nối với công cụ bên ngoài, nguồn dữ liệu và hệ thống nghiệp vụ.

Phần chia sẻ nhấn mạnh rằng việc kết nối AI agents với công cụ cần được thực hiện cẩn thận. Nếu một AI agent có thể truy cập hệ thống nội bộ, bảo mật trở thành yếu tố rất quan trọng. Kiến trúc cần kiểm soát agent được dùng công cụ nào, được truy cập dữ liệu nào và hành động được cấp quyền ra sao.

Một số điểm quan trọng từ Phần này gồm:

- AI agents cần truy cập an toàn vào công cụ và dữ liệu doanh nghiệp
- Kết nối riêng tư giúp giảm rủi ro lộ ra mạng công cộng
- Kiểm soát truy cập cần được thiết kế cẩn thận
- Dữ liệu nhạy cảm cần được bảo vệ
- Kiến trúc ưu tiên bảo mật là yêu cầu bắt buộc cho hệ thống AI production

### Nội dung nổi bật

#### AI agents đang chuyển từ demo sang hệ thống production

Một trong những thông điệp quan trọng của sự kiện là AI agents không còn chỉ dừng lại ở các bản demo thử nghiệm. Nhiều tổ chức đang tìm cách dùng agents để hỗ trợ các tác vụ thực tế như hội thoại với khách hàng, vận hành DevOps, quy trình năng suất và tích hợp doanh nghiệp an toàn.

Tuy nhiên, hệ thống AI production cần nhiều hơn một prototype hoạt động được. Nó cần đáng tin cậy, bảo mật, có khả năng mở rộng và tối ưu chi phí.

#### Voice AI cần thiết kế toàn hệ thống

Phần Voice Agents cho thấy việc tạo một cuộc hội thoại AI giống con người bao gồm rất nhiều thành phần. Hệ thống phải xử lý âm thanh, hiểu ý định, tạo phản hồi và nói tự nhiên trong khi vẫn giữ độ trễ thấp.

Đối với hội thoại tiếng Việt, thách thức có thể lớn hơn vì hệ thống cần xử lý ngữ điệu, ngữ cảnh, ngắt lời và biến thể ngôn ngữ tự nhiên.

#### DevOps automation giúp giảm áp lực vận hành

Sự kiện cho thấy AI agents có thể giúp đội ngũ vận hành làm việc hiệu quả hơn. Bằng cách phân tích cảnh báo, log và metric, AI có thể giảm thời gian cần để hiểu sự cố và hỗ trợ troubleshooting nhanh hơn.

Điều này có giá trị với đội ngũ cloud vì độ phức tạp vận hành tăng lên khi hệ thống phát triển.

#### Bảo mật là yếu tố thiết yếu khi tích hợp AI agent

Phần MCP nhấn mạnh rằng AI agents phải được kết nối với công cụ một cách an toàn. Nếu AI agent có thể thực hiện hành động trong hệ thống nghiệp vụ, kiến trúc cần có kiểm soát truy cập mạnh, kết nối riêng tư và ranh giới rõ ràng.

Bảo mật cần được thiết kế ngay từ đầu, không nên bổ sung sau cùng.

#### Học tập cộng đồng rất quan trọng

Sự kiện cũng cho thấy giá trị của học tập dựa trên cộng đồng. Người tham gia có thể học không chỉ từ diễn giả, mà còn từ phần thảo luận, demo và kinh nghiệm của những người đang xây dựng hệ thống thực tế.

### Những gì học được

#### Kiến thức kỹ thuật

- AI agents có thể hỗ trợ nhiều lĩnh vực như hội thoại giọng nói, vận hành, năng suất làm việc và quy trình doanh nghiệp.
- Xây dựng hệ thống AI production cần chú ý đến độ trễ, độ tin cậy, khả năng mở rộng, chi phí và bảo mật.
- Voice agents cần pipeline đầy đủ gồm STT, LLM, TTS và xử lý tương tác thời gian thực.
- AI có thể hỗ trợ DevOps bằng cách tóm tắt sự cố, phân tích log và đề xuất bước troubleshooting.
- Kết nối riêng tư an toàn rất quan trọng khi AI agents tương tác với công cụ nghiệp vụ và hệ thống nội bộ.

#### Tư duy kiến trúc

- Ứng dụng AI cần được thiết kế như một hệ thống hoàn chỉnh, không chỉ là bản demo mô hình.
- Kiến trúc phải cân nhắc trải nghiệm người dùng, hạ tầng, tích hợp, bảo mật và vận hành.
- Dịch vụ cloud có thể giúp mở rộng hệ thống AI, nhưng chi phí và độ tin cậy cần được tính toán kỹ.
- Cần có ranh giới bảo mật khi agent có thể truy cập hệ thống nhạy cảm hoặc thực hiện hành động.

#### Bài học cá nhân

- Việc xây dựng AI agents dùng trong thực tế phức tạp hơn nhiều so với tạo một demo đơn giản.
- Tầm quan trọng của việc giảm độ trễ trong hệ thống voice AI.
- Biết được cách AI có thể hỗ trợ đội ngũ DevOps bằng cách giảm công việc điều tra lặp lại.
- Mô hình của hệ thống AI hoạt động như thế nào trong doanh nghiệp.

### Ứng dụng vào công việc

- Áp dụng khái niệm AI agent để tự động hóa các tác vụ lặp lại trong phát triển phần mềm và vận hành cloud.
- Tìm hiểu cách voice agents có thể cải thiện tương tác người dùng trong ứng dụng số.
- Thiết kế hệ thống AI với bảo mật và kiểm soát truy cập ngay từ đầu.
- Sử dụng các dịch vụ cloud-native để xây dựng workflow AI có khả năng mở rộng và đáng tin cậy.
- Cân nhắc độ trễ, chi phí và trải nghiệm người dùng khi thiết kế tính năng có AI.
- Tìm hiểu thêm về Amazon Q và tích hợp công cụ theo MCP cho các use case AI doanh nghiệp.
- Thực hành xây dựng prototype nhỏ trước, sau đó từng bước cải tiến để sẵn sàng cho production.

### Trải nghiệm trong event

Tham gia event **“FCAJ Community Day”** là một trải nghiệm học tập rất hữu ích. Sự kiện cung cấp góc nhìn rộng về cách AWS, AI agents, DevOps automation, Amazon Q và kiến trúc cloud đang được áp dụng trong các tình huống thực tế.

#### Học hỏi từ chia sẻ thực tế

Các Phần trong sự kiện hữu ích vì không chỉ giới thiệu công nghệ ở mức tổng quan. Diễn giả còn phân tích các thách thức thực tế trong production như độ trễ, tích hợp công cụ, trải nghiệm người dùng và bảo mật.

#### Hiểu rõ hơn về thách thức của voice agent

Phần Voice Agents là một trong những phần thú vị nhất của sự kiện. Nội dung cho thấy AI giọng nói thời gian thực khó vì mọi bước trong pipeline đều ảnh hưởng đến trải nghiệm cuối cùng. Chỉ một độ trễ nhỏ ở speech recognition, response generation hoặc text-to-speech cũng có thể khiến cuộc hội thoại trở nên thiếu tự nhiên.

#### Học về AI trong DevOps

Phần DevOps Agent giúp tôi hiểu cách AI có thể hỗ trợ vận hành cloud. Trong các hệ thống thực tế, kỹ sư thường mất nhiều thời gian để kiểm tra cảnh báo, log và metric. AI có thể giúp tóm tắt thông tin và đề xuất hướng xử lý, từ đó làm troubleshooting nhanh và hiệu quả hơn.

#### Hiểu về tích hợp AI an toàn

Phần MCP connection nhấn mạnh tầm quan trọng của bảo mật khi AI agents kết nối với công cụ. Nếu agent được phép thực hiện hành động trong hệ thống nội bộ, kiểm soát truy cập và kết nối riêng tư trở nên rất quan trọng. Điều này giúp tôi hiểu rằng kiến trúc bảo mật là yêu cầu cốt lõi của AI trong doanh nghiệp.

#### Kết nối cộng đồng và cảm hứng học tập

Sự kiện cũng thể hiện sức mạnh của cộng đồng AWS. Sự kiện kết nối sinh viên, người xây dựng sản phẩm, lập trình viên và những người làm cloud có cùng đam mê học hỏi, chia sẻ. Điều này tạo ra môi trường học tập tích cực và khuyến khích người tham gia tiếp tục tìm hiểu sâu hơn về AWS và AI.

#### Bài học rút ra

- AI agents nên được thiết kế dựa trên nhu cầu thực tế của người dùng, không chỉ để demo.
- Voice AI cần độ trễ thấp và khả năng tương tác tự nhiên.
- DevOps automation có thể giảm công việc lặp lại và cải thiện thời gian phản hồi.
- Tích hợp công cụ an toàn là yếu tố thiết yếu đối với hệ thống AI doanh nghiệp.
- Các sự kiện cộng đồng có giá trị lớn vì cung cấp cả kiến thức và cảm hứng thực tế.

#### Một số hình ảnh khi tham gia sự kiện

![Your event picture](/images/4-Event/Event_2/picture-event1-1.jpg)
![Your event picture](/images/4-Event/Event_2/picture-event1-2.jpg)
![Your event picture](/images/4-Event/Event_2/picture-event1-3.jpg)
![Your event picture](/images/4-Event/Event_2/picture-event1-4.jpg)
![Your event picture](/images/4-Event/Event_2/picture-event1-5.jpg)
![Your event picture](/images/4-Event/Event_2/picture-event1-6.jpg)


> Tổng thể, sự kiện giúp tôi hiểu rõ hơn cách AWS và AI có thể kết hợp để xây dựng các giải pháp thực tế, có khả năng mở rộng và an toàn. Đồng thời, sự kiện cũng tạo thêm động lực để tôi tiếp tục học về AI agents, kiến trúc cloud và DevOps automation.