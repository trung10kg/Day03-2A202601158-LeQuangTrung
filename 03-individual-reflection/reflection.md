# 03 — Individual Reflection (Lê Quang Trung - 2A202601158)

## Tôi đã tham gia vào phần nào?

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| **Scan cá nhân** | Quét rộng 10 vấn đề từ trải nghiệm thực tế (học tập, bán hàng, CLB); tập trung vào lăng kính lặp lại và tốn thời gian. | Đóng góp 2 candidate problems vào danh sách nhóm (#9 về Chăm sóc khách hàng và #10 về tư vấn cơ bản). |
| **Pitch Problem Card** | Trình bày case "Người bán hàng trả lời lặp lại" (candidate #9), làm rõ quy trình trả lời FAQ thủ công. | Giúp nhóm có thêm lựa chọn về workflow bán hàng, tuy nhiên sau đó đồng thuận chọn case #3 vì gần gũi với bối cảnh lab hiện tại hơn. |
| **Challenge bài của bạn khác** | Phản biện case "Slack Search" (#7/#8) về vấn đề quyền truy cập dữ liệu (data access) và tính bảo mật khi kết nối nhiều nguồn. | Giúp nhóm nhận diện được rủi ro kỹ thuật và thu hẹp scope vào các bài toán có dữ liệu sẵn có như README/Worksheet. |
| **Gom trùng / cluster** | Tham gia thảo luận để phân loại 12 candidate thành 4 cluster chính (Thông tin lab, CSKH, Chấm bài, Dự đoán). | Giúp nhóm cấu trúc lại suy nghĩ và nhận diện được "Thông tin lab" là cluster mạnh nhất. |
| **Chọn candidate problem** | Cùng nhóm chấm điểm các candidate theo 7 tiêu chí. Đề xuất chọn bài của Tùng (#3) vì tính khả thi cao trong 4 tiếng lab. | Nhóm đạt được sự đồng thuận cao (34 điểm cho #3) và bắt đầu deep-dive vào đúng hướng. |
| **Validation / research** | Đảm nhận vai trò **Research Lead**: Tìm kiếm các paper về "Information Overload" (Bayne & Inan, 2022) và các pattern checklist như GitHub PR, GitHub Actions. | Cung cấp cơ sở khoa học và bằng chứng thực tế cho nhóm; giúp định hình giải pháp theo hướng "AI reviewer" thay vì "AI writer". |
| **Workflow nhóm** | Góp ý cho sơ đồ Current/Future State, đặc biệt là việc tách bước "Sinh viên kiểm tra nhận xét" thành một Human Boundary riêng biệt. | Đảm bảo tính an toàn cho hệ thống; sinh viên vẫn là người chịu trách nhiệm cuối cùng cho bài nộp của mình. |
| **Problem Statement** | Tham gia viết Problem Statement v1, tập trung vào việc liệt kê đầy đủ các field dễ bị bỏ sót trong rubric. | Giúp PS sắc bén hơn, chỉ rõ được rủi ro mất điểm nếu thiếu success metric, boundary hay risk. |
| **Rule / Workflow / Agent** | Lập luận chọn cấp độ **Workflow**: Dùng Rule để check field có/không, dùng AI để check nội dung mơ hồ. | Thuyết phục nhóm không chọn Agent để tránh việc AI tự ý sửa bài của sinh viên mà không qua kiểm duyệt. |
| **Decision** | Review quyết định "Go" và đề xuất Pilot nhỏ nhất là dùng checklist Day 02 để test thử trên bản nháp của nhóm. | Hoàn thiện kế hoạch thực thi thực tế, có điểm dừng (Exit Criteria) rõ ràng nếu AI gợi ý quá chung chung. |

---

## Bảng dùng AI trong reflection

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| **Scan** | Gợi ý thêm problems cho vai trò sinh viên và người bán hàng. | Nhắc tôi nhớ đến nỗi đau "tìm lại thông tin cũ" trong Discord/Drive mà tôi thường bỏ qua. | Gợi ý vài ý tưởng quá rộng như "Quản lý cuộc đời bằng AI". | Bỏ qua các ý tưởng viển vông, tập trung vào các bước nhỏ trong workflow nộp bài lab. |
| **Research** | Tìm các nghiên cứu về Information Overload và Course Design. | Tìm nhanh được bài báo của Bayne & Inan (2022) giúp củng cố lập luận về "Cognitive Overload". | AI đôi khi bịa ra các số liệu thống kê % tiết kiệm thời gian mà không có nguồn link cụ thể. | Kiểm tra lại link nguồn, chỉ giữ lại các luận điểm về pattern (checklist, review) thay vì dùng số liệu ảo. |
| **Workflow** | Dùng AI để tối ưu cú pháp Mermaid cho sơ đồ Before/After. | Vẽ sơ đồ nhanh, chuyên nghiệp và dễ đọc hơn vẽ tay. | AI tự động gộp bước "Review" và "Sửa bài" làm một. | Tách riêng bước "Human review" để làm rõ Boundary và trách nhiệm của sinh viên. |
| **Problem Statement** | Nhờ AI phản biện v0 để tìm lỗ hổng logic. | AI chỉ ra rằng "Success Metric" ban đầu của nhóm còn chung chung (chưa nói rõ giảm từ bao nhiêu xuống bao nhiêu). | AI đề xuất thêm quá nhiều tính năng phụ không cần thiết vào phần scope. | Giữ nguyên scope tối giản, chỉ tập trung vào việc cập nhật con số 30 phút xuống 10 phút. |
| **Decision** | Hỏi AI về các rủi ro (risk) phổ biến khi dùng AI review bài tập. | Gợi ý được rủi ro "AI nhận xét sai hoặc gợi ý chung chung" khiến sinh viên mất lòng tin. | AI đề xuất kế hoạch triển khai quá dài hạn (6 tháng). | Rút gọn thành kế hoạch Pilot 2 tuần và Pilot ngay trong lab để thấy kết quả tức thì. |

---

## Reflection câu hỏi mở

### Tôi học được gì khi nghe top 3 problems của các bạn khác?
Tôi nhận ra rằng cùng một bối cảnh là buổi Lab Day 02, nhưng mỗi người lại có một góc nhìn khác nhau: người thì đau đáu về việc thông tin từ BTC bị trễ, người thì lo lắng về việc không biết nộp bài sao cho đủ field. Điều này dạy tôi rằng "vấn đề" không bao giờ là duy nhất; quan trọng là nhóm phải chọn được vấn đề có **workflow rõ ràng nhất** để giải quyết bằng AI một cách hiệu quả.

### Nhóm có lúc nào bị solution-first không?
Có, ở giai đoạn đầu, khi nhắc đến "kiểm tra bài lab", một số bạn đã nghĩ ngay đến việc xây dựng một "AI Teacher" tự động chấm điểm và sửa bài. Tôi đã phải dùng kết quả research về GitHub Actions để kéo nhóm lại: chúng ta chỉ cần một "Reviewer" hỗ trợ tìm lỗi thiếu sót, còn việc "sửa bài" phải là của sinh viên để đảm bảo tính học thuật. Việc phân biệt rõ AI hỗ trợ (Workflow) và AI làm thay (Agent) đã giúp nhóm tránh được cái bẫy này.

### Tôi có thay đổi ý kiến sau khi bị challenge không?
Ban đầu tôi khá bảo thủ với case #9 (Chăm sóc khách hàng) vì tôi thấy nó có workflow cực kỳ rõ ràng. Tuy nhiên, khi các bạn trong nhóm challenge rằng: *"Chúng ta đang ngồi trong lab này, làm bài toán lab này sẽ giúp ích cho chính chúng ta ngay lập tức"*, tôi đã đồng ý ngay. Tôi nhận ra giá trị của việc giải quyết một "nỗi đau" mà tất cả thành viên trong nhóm đều đang cảm nhận được (shared pain) sẽ tạo ra động lực làm việc tốt hơn.

### Tôi đóng góp gì thật sự vào artifact cuối?
Đóng góp lớn nhất của tôi là **tính thực chứng (evidence)**. Việc tìm ra các paper và pattern thực tế (Grammarly, GitHub) giúp Problem Statement của nhóm không bị lý thuyết suông. Tôi cũng là người kiên trì bảo vệ quan điểm chọn mức độ **Workflow** thay vì **Agent**, giúp nhóm có một bản thiết kế an toàn, ít rủi ro và có khả năng "Go" thực sự sau lab.

### Điều khó nhất khi viết Problem Statement là gì?
Khó nhất là định nghĩa **Boundary**. Chúng tôi đã tranh luận rất nhiều về việc AI được phép "nhận xét" đến mức độ nào. Nếu nhận xét quá sâu, AI sẽ thành người viết hộ. Nếu nhận xét quá nông, nó sẽ không khác gì một checklist bằng mắt thường. Việc tìm ra điểm cân bằng: "AI chỉ ra mục thiếu và gợi ý hướng sửa, không đưa ra câu trả lời trực tiếp" là bước đột phá lớn nhất trong bản PS v1 của chúng tôi.

### Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?
Tôi sẽ challenge nhóm về việc **thiết kế prompt mẫu cho bước Pilot**. Trong lab, chúng tôi mới chỉ dừng lại ở việc chốt "Go", nhưng nếu có thêm 15 phút, tôi muốn cùng nhóm viết thử một bộ Prompt Template để test ngay độ hiệu quả của việc review, từ đó kiểm chứng xem rủi ro "AI gợi ý chung chung" có thực sự nghiêm trọng như chúng tôi lo ngại hay không.

---

## Tự kiểm cuối bài

- [x] **[12đ cá nhân]** Cá nhân có 10 problems và top 3 Problem Cards.
- [x] **[12đ cá nhân]** Tôi đã pitch rõ và challenge nhóm đúng trọng tâm.
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài.
- [x] **[15đ nhóm]** Nhóm có workflow trước/sau.
- [x] **[20đ nhóm]** Nhóm có Problem Statement v0/v1 với metric và boundary rõ.
- [x] **[15đ nhóm]** Nhóm có so sánh No AI / Rule / Workflow / Agent.
- [x] **[10đ nhóm]** Nhóm có Go / Not Yet / No-Go và lý do rõ.
- [x] **[10đ cá nhân]** Reflection cá nhân có nói rõ vai trò trong nhóm, cách dùng AI, điều học được và nếu làm lại sẽ đổi gì.
- [x] **[6đ cá nhân]** Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp với AI.
