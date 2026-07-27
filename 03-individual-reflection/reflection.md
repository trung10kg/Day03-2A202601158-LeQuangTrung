# 03 — Individual Reflection

## Tôi đã tham gia vào phần nào?

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| **Scan cá nhân** | Quét rộng và phân tích 5 candidate problems dựa trên trải nghiệm thực tế; xây dựng chi tiết top 3 Problem Cards. | Đưa ra danh mục vấn đề đa dạng lăng kính, trong đó case "IT Helpdesk" được chọn làm card tâm đắc nhất để pitch cho nhóm. |
| **Pitch Problem Card** | Trình bày thuyết phục về case "IT Helpdesk", làm rõ bối cảnh, workflow, bottleneck (bước hỏi lại thông tin) và metric đo lường. | Thuyết phục được nhóm đưa case này vào shortlist và cuối cùng đồng thuận chọn làm candidate chung để đào sâu. |
| **Challenge bài của bạn khác** | Đặt câu hỏi phản biện về tính bảo mật dữ liệu của case "Rà soát hợp đồng pháp lý" và tính thực tế của việc tự động hóa "HR & hành chính" bằng AI. | Giúp nhóm nhận diện được các rào cản lớn về pháp lý/bảo mật, từ đó loại bớt các bài toán có rủi ro quá cao hoặc scope quá rộng. |
| **Gom trùng / cluster** | Đóng góp ý kiến phân loại các candidate của nhóm thành 4 nhóm chính (Reporting, Search, Review, Follow-up). | Giúp nhóm có cái nhìn tổng quan và hệ thống trước khi tiến hành chấm điểm shortlist. |
| **Chọn candidate problem** | Cùng nhóm phân tích và chấm điểm các candidate theo bảng tiêu chí định lượng (Actor, Workflow, Impact, Khả thi trong lab). | Nhóm thống nhất chọn "IT Helpdesk" với điểm số vượt trội nhờ tính rõ ràng của quy trình và tính sẵn có của dữ liệu. |
| **Validation / research** | Nghiên cứu các giải pháp hiện tại trên thị trường (Atlassian Jira Reports, Zendesk AI, Slack AI) và phân tích các bài học thực tế. | Rút ra kết luận quan trọng: Không nên tự build từ đầu một agent tự chạy, mà nên áp dụng mô hình "AI draft, Human approve" (Workflow). |
| **Workflow nhóm** | Phối hợp vẽ sơ đồ Current State và Future State; làm rõ sự khác biệt giữa Active Time (thao tác) và Elapsed Time (chờ đợi). | Tạo ra sơ đồ workflow trực quan bằng Mermaid, phân định rõ điểm can thiệp của AI và điểm kiểm soát của con người (Human Boundary). |
| **Problem Statement** | Tham gia xây dựng và hiệu chỉnh bản thảo từ v0 sang v1; định nghĩa chi tiết các trường thông tin đặc biệt là Metric và Boundary. | Hoàn thiện Problem Statement v1 sắc bén, thực tế và có tính định lượng cao. |
| **Rule / Workflow / Agent** | Lập luận phản biện về 3 cấp độ giải pháp; phân tích tại sao Rule không đủ và Agent lại quá nhiều rủi ro bảo mật. | Nhóm đồng thuận lựa chọn giải pháp ở mức độ **Workflow** để vừa giải quyết được bottleneck vừa đảm bảo an toàn vận hành. |
| **Decision** | Đề xuất kế hoạch Pilot nhỏ (2 tuần với dữ liệu mẫu) và thiết lập cơ chế Rollback chi tiết nếu AI gặp lỗi nghiêm trọng. | Hoàn thiện quyết định "Go" có căn cứ khoa học, kiểm soát được rủi ro thay vì quyết định cảm tính theo trào lưu AI. |

---

## Bảng dùng AI trong reflection

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| **Scan** | Gợi ý thêm các vấn đề thực tế theo 4 lăng kính dựa trên bối cảnh học tập/làm việc. | Giúp mở rộng góc nhìn sang các mảng như Sales Enablement và Healthcare Triage mà bản thân chưa từng nghĩ tới. | Đưa ra các ý tưởng quá vĩ mô và chung chung kiểu "Trợ lý AI đa năng hỗ trợ học tập". | Lọc bỏ toàn bộ các ý tưởng chung chung; chỉ giữ lại các vấn đề sát sườn, có quy trình và người dùng cụ thể. |
| **Problem Card** | Phản biện tính chặt chẽ của Problem Card "IT Helpdesk" ban đầu. | Chỉ ra điểm yếu ở phần Metric thành công còn mang tính định tính ("nhanh hơn", "tốt hơn"). | Thường có xu hướng khen ngợi và động viên thay vì tập trung "gạch đá" phản biện sắc bén. | Tự ép bản thân viết lại toàn bộ các Metric thành công theo chuẩn SMART (giảm MTTR từ 4 giờ xuống < 45 phút). |
| **Workflow** | Nhờ AI chuyển đổi mô tả luồng công việc trước/sau thành cú pháp Mermaid. | Tiết kiệm rất nhiều thời gian định dạng và căn chỉnh sơ đồ để nộp bài đẹp mắt. | AI tự động gộp bước "AI draft câu trả lời" và "Gửi cho nhân viên" thành một bước tự động hoàn toàn không có người duyệt. | Tách rời hai bước này; đưa con người (IT Helpdesk) vào làm chốt chặn duyệt cuối cùng (Human Boundary) để đảm bảo an toàn. |
| **Research** | Tóm tắt tính năng và mô hình vận hành của các giải pháp AI Helpdesk hiện hữu. | Giúp đọc nhanh tài liệu sản phẩm của Atlassian Jira Service Desk và Zendesk AI để tìm pattern chung. | Trích dẫn một số con số thống kê về việc tiết kiệm thời gian mà không kèm theo nguồn gốc xác thực. | Kiểm chứng lại từ các nguồn chính thống; loại bỏ các con số thiếu căn cứ; tập trung phân tích sự khác biệt bản chất giữa Rule-based và AI-based. |
| **Problem Statement** | Nhờ AI đóng vai trò một EM (Engineering Manager) khó tính để phản biện bản nháp v0. | Phát hiện ra phần "Boundary" chưa quy định rõ giới hạn quyền hạn truy cập của AI đối với các thư mục hệ thống nhạy cảm. | Đề xuất các thuật ngữ quá học thuật, lý thuyết và xa rời thực tế vận hành của một phòng IT nội bộ. | Viết lại bằng ngôn ngữ vận hành thực tế; quy định rõ AI tuyệt đối không có quyền kết nối API thay đổi trạng thái tài khoản nếu không có IT duyệt. |
| **Rule / Workflow / Agent** | Phân tích rủi ro bảo mật và chi phí vận hành nếu triển khai giải pháp ở cấp độ "Agent". | Cung cấp danh mục rủi ro hệ thống chi tiết (security leak, privilege escalation) khi để Agent tự động xử lý. | Luôn có xu hướng đề xuất chọn mức "Agent" vì "hiện đại và tối ưu nhất" mà bỏ qua bài toán chi phí và độ an toàn của doanh nghiệp. | Phản biện lại AI; thuyết phục nhóm lựa chọn cấp độ **Workflow** vì nó mang lại tỷ lệ ROI (lợi nhuận trên đầu tư) tốt nhất và an toàn tuyệt đối. |
| **Decision** | Gợi ý kịch bản Rollback và các tiêu chí định lượng để dừng dự án (Exit Criteria). | Đề xuất các ngưỡng định lượng rất thực tế (tỷ lệ IT phải sửa lại draft của AI > 70% liên tục trong 2 tuần). | Đưa ra một kế hoạch pilot quá cồng kềnh, phức tạp và tốn kém nguồn lực cho một doanh nghiệp 50-100 người. | Tinh giản kế hoạch pilot về mức tối giản nhất: Chạy bán thủ công (PM/IT tự copy-paste data vào prompt chuẩn) trong 2 tuần để đo đạc thực tế trước khi tích hợp hệ thống. |

---

## Reflection câu hỏi mở

### Tôi học được gì khi nghe top 3 problems của các bạn khác?
Khi lắng nghe top 3 vấn đề của các bạn khác trong nhóm (như case rà soát hợp đồng pháp lý hay HR & hành chính), tôi nhận ra mỗi bộ phận trong doanh nghiệp đều có những nỗi đau rất đặc thù mà người ngoài khó hình dung được. Ví dụ, với case rà soát hợp đồng, tôi học được rằng rào cản lớn nhất không phải là công nghệ AI đọc hiểu, mà là tính pháp lý và tính bảo mật của dữ liệu khách hàng. Điều này giúp tôi hiểu rằng một bài toán AI tốt không chỉ cần giải pháp kỹ thuật khả thi, mà quan trọng hơn là phải vượt qua được các rào cản về mặt vận hành, bảo mật và tuân thủ (compliance).

### Nhóm có lúc nào bị solution-first không?
Có, nhóm đã từng rơi vào cái bẫy "solution-first" ngay từ đầu buổi thảo luận. Vì AI Agent đang là một từ khóa rất "hot", cả nhóm ban đầu đều hào hứng muốn dựng ngay một "Virtual IT Support Agent" chạy hoàn toàn tự động, tự trò chuyện với nhân viên qua Slack và tự động cấu hình/sửa lỗi hệ thống. Tuy nhiên, khi bắt tay vào vẽ workflow hiện tại và đặt câu hỏi phản biện: *"Nếu AI tự động reset quyền truy cập hệ thống nhạy cảm cho một tài khoản bị hack, ai sẽ là người chịu trách nhiệm?"*, nhóm mới giật mình nhận ra mình đang bị công nghệ dẫn dắt. Nhờ đó, chúng tôi đã kéo nhau quay trở lại với bản chất vấn đề, chuyển hướng sang giải pháp cấp độ **Workflow** với ranh giới con người kiểm soát chặt chẽ.

### Tôi có thay đổi ý kiến sau khi bị challenge không?
Có. Ban đầu, tôi đề xuất giải pháp là bắt buộc người dùng điền một form ticket cực kỳ chi tiết ngay từ đầu để giải quyết triệt để vấn đề thiếu thông tin. Tuy nhiên, các bạn trong nhóm đã challenge tôi rất thuyết phục: *"Nhân viên khi gặp lỗi mạng hoặc lỗi phần mềm đang rất bực mình và bị gián đoạn công việc, nếu bắt họ điền một cái form dài 10 trường thông tin bắt buộc, họ sẽ bỏ qua hệ thống và nhắn tin trực tiếp cho IT qua Slack, dẫn đến quy trình bị vỡ."* 
Tôi nhận ra mình đã quá tập trung vào sự tiện lợi cho IT Helpdesk mà quên đi trải nghiệm của người dùng (User Experience). Tôi đã thay đổi ý kiến, thống nhất với nhóm giải pháp: Người dùng vẫn chat tự do qua Slack, nhưng AI sẽ đóng vai trò triage phía sau để đọc đoạn chat, tự trích xuất thông tin và chủ động chat hỏi bổ sung các trường còn thiếu một cách tự nhiên trước khi tạo ticket chính thức.

### Tôi đóng góp gì thật sự vào artifact cuối?
Đóng góp lớn nhất của tôi là giữ vững mạch logic và tính thực tế cho nhóm trong suốt buổi làm việc. Tôi là người kiên quyết kéo nhóm ra khỏi xu hướng "bị lôi cuốn bởi AI Agent" để đưa về giải pháp "Workflow" an toàn và hiệu quả. Bên cạnh đó, tôi cũng trực tiếp đóng góp trong việc:
1. Phân tách rõ ràng khái niệm **Active Time** và **Elapsed Time** trong sơ đồ workflow để làm nổi bật tác động thực sự của AI lên SLA giải quyết ticket.
2. Xây dựng bộ chỉ số thành công chuẩn SMART (MTTR, FRT, FCR, AI Acceptance Rate) thay vì các chỉ số định tính mơ hồ ban đầu.
3. Thiết kế chi tiết phần **Human Boundary** (Ranh giới kiểm soát của con người) và **Exit/Rollback Criteria** trong quyết định "Go", giúp bài nộp nhóm có độ chín chắn và tính khả thi của một dự án thực tế trong doanh nghiệp.

### Điều khó nhất khi viết Problem Statement là gì?
Điều khó nhất là làm thế nào để cô đọng mọi bối cảnh phức tạp vào một bộ khung có cấu trúc chặt chẽ mà không làm mất đi bản chất của nỗi đau thực tế. Khi viết Problem Statement, rất dễ bị sa đà vào việc mô tả chung chung hoặc biến nó thành một bản mô tả giải pháp trá hình. Việc phải bóc tách rõ ràng giữa **Bottleneck** (bước hỏi lại thông tin mất 5-15 phút) và **Impact** (tổng thời gian 25-45 phút/ticket, kéo dài Elapsed Time và làm gián đoạn công việc của nhân viên) đòi hỏi cả nhóm phải tranh luận rất nhiều để thống nhất từng con số và câu chữ.

### Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?
Nếu được làm lại, tôi sẽ challenge nhóm mạnh hơn về **Chất lượng của hệ thống Knowledge Base (KB) hiện tại**. Trong giải pháp của nhóm, chúng ta giả định rằng AI sẽ đọc KB để đề xuất bài hướng dẫn hoặc draft câu trả lời cho IT. Tuy nhiên, trong thực tế tại hầu hết các doanh nghiệp, KB thường bị phân mảnh, lỗi thời và thiếu chính xác. Nếu KB đầu vào chất lượng kém, AI sẽ tạo ra các bản nháp sai lệch (Garbage In, Garbage Out), làm tăng thời gian IT phải sửa đổi và làm giảm lòng tin của IT vào hệ thống. Tôi sẽ yêu cầu nhóm phải bổ sung một bước "Chuẩn hóa và làm sạch KB" vào giai đoạn chuẩn bị trước khi tiến hành Pilot AI.

---

## Tự kiểm cuối bài

- [x] **[12đ cá nhân]** Cá nhân có 5+ problems và top 3 Problem Cards.
- [x] **[12đ cá nhân]** Tôi đã pitch rõ và challenge nhóm đúng trọng tâm.
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài.
- [x] **[15đ nhóm]** Nhóm có workflow trước/sau.
- [x] **[20đ nhóm]** Nhóm có Problem Statement v0/v1 với metric và boundary rõ.
- [x] **[15đ nhóm]** Nhóm có so sánh No AI / Rule / Workflow / Agent.
- [x] **[10đ nhóm]** Nhóm có Go / Not Yet / No-Go và lý do rõ.
- [x] **[10đ cá nhân]** Reflection cá nhân có nói rõ vai trò trong nhóm, cách dùng AI, điều học được và nếu làm lại sẽ đổi gì.
- [x] **[6đ cá nhân]** Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp với AI.
