# 01 — Individual Problem Scan

> Bản draft dựa trên 5 candidate problems được đưa ra. Các tần suất và thời lượng bên dưới là ước lượng ban đầu, cần thay bằng log, ticket, phỏng vấn hoặc số đo thực tế trước khi nộp chính thức.

## Phase 1 — Scan 5 problems

| # | Lăng kính | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật / giả định cần kiểm chứng |
|---|---|---|---|---|
| 1 | Tốn thời gian, AI có thể tốt hơn | Rà soát hợp đồng pháp lý mất nhiều thời gian vì phải đọc từng điều khoản, tìm điểm khác với mẫu chuẩn và đánh dấu rủi ro. | Luật sư, chuyên viên pháp chế, bộ phận mua hàng và kinh doanh. | Mỗi hợp đồng có thể mất 1–3 giờ để đọc và so sánh; cần kiểm tra bằng mẫu hợp đồng thực tế và thời gian review. |
| 2 | Lặp lại, tốn thời gian | HR & Hành chính bị quá tải bởi các câu hỏi và yêu cầu lặp lại về quy trình, giấy tờ, nghỉ phép, onboarding, phòng họp và mua sắm. | Nhân viên HR/Admin và toàn bộ nhân viên cần hỗ trợ. | Cùng một nhóm câu hỏi xuất hiện nhiều lần qua chat/email; cần đếm số request theo tuần và thời gian xử lý trung bình. |
| 3 | Lặp lại, pain từ người khác | IT Helpdesk phải tiếp nhận, phân loại và trả lời các lỗi nội bộ lặp lại như quên mật khẩu, lỗi phần mềm, không kết nối được mạng hoặc không biết quy trình yêu cầu quyền truy cập. | Nhân viên gặp lỗi và nhân viên IT hỗ trợ. | Ticket thường thiếu thông tin, phải hỏi lại nhiều lần; cần lấy ticket log để đo thời gian phản hồi, xử lý và tỷ lệ lặp lỗi. |
| 4 | Tốn thời gian, AI có thể tốt hơn | Sales Enablement khó tìm đúng tài liệu bán hàng, case study, bảng giá và câu trả lời cho từng nhóm khách hàng khi chuẩn bị cuộc gặp. | Nhân viên kinh doanh, sales manager và khách hàng tiềm năng. | Nhân viên phải tìm trong nhiều thư mục hoặc hỏi đồng nghiệp; cần đo thời gian chuẩn bị và số lần dùng sai/thiếu tài liệu. |
| 5 | AI có thể tốt hơn, rủi ro cao | Healthcare Triage khó phân loại ban đầu các triệu chứng và hướng dẫn bước tiếp theo một cách nhất quán khi lượng bệnh nhân hoặc tin nhắn tăng. | Nhân viên tiếp nhận, điều phối phòng khám, bác sĩ và bệnh nhân. | Thông tin ban đầu thường thiếu hoặc không theo cấu trúc; cần xác minh thời gian chờ, tỷ lệ phải hỏi bổ sung và quy trình an toàn hiện tại. Không dùng AI để tự chẩn đoán hoặc quyết định cấp cứu. |

## Phase 2 — Chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | IT Helpdesk | Workflow lặp lại, actor rõ, có ticket log và metric định lượng được. AI có thể hỗ trợ phân loại, tìm bài hướng dẫn và soạn câu trả lời trong phạm vi an toàn. | Chất lượng knowledge base, quyền truy cập dữ liệu và tỷ lệ lỗi có thể tự xử lý chưa rõ. |
| 2 | Rà soát hợp đồng pháp lý | Impact cao; phần trích xuất điều khoản, so sánh với mẫu và tạo danh sách điểm cần chú ý có thể giảm thời gian đọc ban đầu. | Không rõ loại hợp đồng nào có mẫu chuẩn; AI không được tự đưa kết luận pháp lý hoặc phê duyệt thay luật sư. |
| 3 | HR & Hành chính | Nhiều yêu cầu lặp lại, dễ vẽ workflow và có thể bắt đầu bằng FAQ/form/routing có kiểm soát. | Cần phân biệt câu hỏi đơn giản với trường hợp cần bảo mật hoặc quyết định của HR. |

Các vấn đề Sales Enablement và Healthcare Triage vẫn đáng nghiên cứu, nhưng Sales cần kiểm chứng chất lượng và độ cập nhật của nội dung, còn Healthcare có rủi ro an toàn cao hơn và cần human-in-the-loop chặt chẽ.

---

## Problem Card #1 — IT Helpdesk

**Problem 1 câu:** Nhân viên mất thời gian chờ IT xử lý các lỗi nội bộ lặp lại, trong khi ticket thường thiếu thông tin nên IT phải hỏi lại trước khi bắt đầu.

**Actor:** Nhân viên nội bộ và IT Helpdesk.

**Thời điểm / bối cảnh:** Khi nhân viên không đăng nhập được, gặp lỗi phần mềm, mất kết nối mạng hoặc cần quyền truy cập.

**Current workflow:**

```text
[Nhân viên gặp lỗi]
        -> [Gửi chat/email/ticket]
        -> [IT đọc và phân loại]
        -> [Hỏi lại thông tin hoặc ảnh chụp màn hình]
        -> [Tìm hướng dẫn / xử lý]
        -> [Xác nhận với nhân viên và đóng ticket]
```

**Bottleneck:** Phân loại ban đầu và thu thập đủ thông tin; ước lượng 10–20 phút mỗi ticket, cần kiểm chứng bằng ticket log.

**Impact:** Nhân viên bị gián đoạn công việc; IT mất thời gian trả lời các câu hỏi giống nhau và khó ưu tiên lỗi nghiêm trọng.

**Success metric:** Giảm thời gian phản hồi đầu tiên và thời gian xử lý trung vị; tăng tỷ lệ ticket có đủ thông tin ngay từ lần gửi đầu; theo dõi tỷ lệ câu trả lời phải IT sửa lại.

**Non-AI alternative:** Chuẩn hóa form ticket, tạo menu phân loại, viết knowledge base và macro trả lời cho các lỗi phổ biến.

**AI hypothesis:** AI đọc mô tả lỗi, gợi ý category/priority, hỏi bổ sung các trường còn thiếu và đề xuất bài hướng dẫn phù hợp. IT duyệt trước khi gửi và xử lý các trường hợp nhạy cảm.

**Quick gut:** [ ] No AI / process fix  [ ] Rule  [x] Workflow  [ ] Agent  [ ] Chưa biết

### Draft workflow

```text
CURRENT STATE — ước lượng 25–45 phút/ticket
[Gửi yêu cầu tự do: 5']
-> [IT đọc và phân loại: 5–10']
-> [Hỏi lại thông tin: 5–15']
-> [Tìm hướng dẫn và xử lý: 10–20']
-> [Xác nhận, cập nhật và đóng: 5']

FUTURE STATE — mục tiêu cần thử nghiệm
[Form có trường bắt buộc: 2']
-> [AI gợi ý category, priority và câu hỏi bổ sung: 1']
-> [AI đề xuất bài hướng dẫn / draft trả lời: 1']
-> [IT kiểm tra và gửi hoặc xử lý: 8–20']
-> [Cập nhật ticket và đóng: 2']

Human boundary: IT phê duyệt câu trả lời, quyền truy cập, thay đổi hệ thống và mọi ticket có dấu hiệu bảo mật.
Fallback: nếu AI không tìm thấy nguồn phù hợp hoặc confidence thấp, chuyển thẳng cho IT.
```

## Problem Card #2 — Rà soát hợp đồng pháp lý

**Problem 1 câu:** Pháp chế phải đọc và so sánh thủ công nhiều hợp đồng, khiến việc phát hiện điều khoản khác mẫu hoặc rủi ro tiềm ẩn bị chậm.

**Actor:** Luật sư/chuyên viên pháp chế; người gửi hợp đồng từ Sales, Procurement hoặc đối tác.

**Thời điểm / bối cảnh:** Trước khi ký hợp đồng mới hoặc khi đối tác gửi bản đã chỉnh sửa.

**Current workflow:**

```text
[Nhận file hợp đồng]
-> [Đọc toàn văn]
-> [Tìm điều khoản quan trọng]
-> [So sánh với mẫu / version trước]
-> [Ghi chú điểm khác và rủi ro]
-> [Soạn đề xuất sửa]
-> [Luật sư review và gửi phản hồi]
```

**Bottleneck:** Tìm kiếm và so sánh điều khoản trong tài liệu dài; ước lượng 1–3 giờ mỗi hợp đồng, cần đo theo loại hợp đồng.

**Impact:** Chậm tiến độ ký kết; tăng nguy cơ bỏ sót khác biệt về trách nhiệm, thanh toán, bảo mật, chấm dứt hoặc giới hạn trách nhiệm.

**Success metric:** Giảm thời gian review vòng đầu; không tăng số lỗi/điểm rủi ro bị bỏ sót trong mẫu kiểm tra; đo tỷ lệ đề xuất của AI được luật sư xác nhận là phù hợp.

**Non-AI alternative:** Checklist pháp lý, template chuẩn, công cụ so sánh version và thư viện điều khoản đã phê duyệt.

**AI hypothesis:** AI trích xuất điều khoản, so sánh với mẫu được cung cấp, đánh dấu điểm khác và tạo bảng câu hỏi để luật sư kiểm tra. AI không kết luận hợp đồng “an toàn”, không tự sửa hoặc phê duyệt.

**Quick gut:** [ ] No AI / process fix  [ ] Rule  [x] Workflow  [ ] Agent  [ ] Chưa biết

### Draft workflow

```text
CURRENT STATE — ước lượng 60–180 phút/hợp đồng
[Nhận file và xác định version: 10']
-> [Đọc toàn văn: 30–90']
-> [Tìm điều khoản trọng yếu: 10–30']
-> [So sánh mẫu / version cũ: 10–30']
-> [Ghi chú và đề xuất sửa: 10–30']
-> [Luật sư kiểm tra lần cuối]

FUTURE STATE — mục tiêu cần thử nghiệm
[Nạp hợp đồng + mẫu chuẩn được phép dùng: 2']
-> [AI lập bảng điều khoản và diff: 3–5']
-> [AI đánh dấu điểm cần kiểm tra, kèm trích dẫn: 2–5']
-> [Luật sư xác minh từng điểm và quyết định: 30–90']
-> [Gửi phản hồi / lưu version]

Human boundary: luật sư chịu trách nhiệm về diễn giải, mức độ rủi ro, nội dung sửa và quyết định ký.
Fallback: tài liệu thiếu mẫu chuẩn, dữ liệu nhạy cảm hoặc AI không trích dẫn được nguồn thì review thủ công.
```

## Problem Card #3 — HR & Hành chính

**Problem 1 câu:** HR/Admin bị gián đoạn bởi các yêu cầu lặp lại và phải hướng dẫn thủ công cùng một quy trình cho nhiều nhân viên.

**Actor:** Nhân viên HR/Admin và nhân viên trong công ty.

**Thời điểm / bối cảnh:** Onboarding, xin nghỉ phép, xác nhận giấy tờ, đặt phòng họp, mua sắm văn phòng hoặc hỏi chính sách nội bộ.

**Current workflow:**

```text
[Nhân viên gửi câu hỏi / yêu cầu]
-> [HR/Admin đọc và xác định loại việc]
-> [Tìm chính sách / hỏi người phụ trách]
-> [Trả lời hoặc gửi form]
-> [Theo dõi bổ sung giấy tờ]
-> [Cập nhật trạng thái]
```

**Bottleneck:** Triage và trả lời các yêu cầu đơn giản nhưng rải rác qua nhiều kênh; ước lượng 5–15 phút mỗi yêu cầu, cần thống kê theo tuần.

**Impact:** HR/Admin mất thời gian cho việc lặp lại; nhân viên chờ lâu hoặc gửi sai form, làm tăng số vòng trao đổi.

**Success metric:** Giảm số vòng hỏi đáp cho yêu cầu chuẩn; giảm thời gian phản hồi các câu hỏi FAQ; tăng tỷ lệ request được gửi đúng form ngay từ đầu.

**Non-AI alternative:** Một cổng request duy nhất, FAQ có chủ sở hữu, form bắt buộc và rule routing theo loại yêu cầu.

**AI hypothesis:** AI phân loại yêu cầu, trả lời từ nguồn chính sách đã được phê duyệt, điền sẵn form hoặc chuyển đúng người phụ trách. HR/Admin duyệt nội dung chính sách và xử lý ngoại lệ.

**Quick gut:** [ ] No AI / process fix  [x] Rule  [ ] Workflow  [ ] Agent  [ ] Chưa biết

### Draft workflow

```text
CURRENT STATE — ước lượng 5–15 phút/yêu cầu
[Nhắn qua chat/email: 2']
-> [HR/Admin đọc và hỏi thêm: 2–5']
-> [Tìm chính sách / form: 2–5']
-> [Trả lời và theo dõi: 2–5']

FUTURE STATE — mục tiêu cần thử nghiệm
[Form / kênh request thống nhất: 1–2']
-> [Rule phân loại và kiểm tra trường bắt buộc: 1']
-> [AI trả lời FAQ có trích dẫn hoặc đề xuất form: 1']
-> [HR/Admin duyệt ngoại lệ và cập nhật trạng thái: 2–5']

Human boundary: HR/Admin quyết định các trường hợp liên quan đến quyền lợi, kỷ luật, dữ liệu cá nhân hoặc ngoại lệ chính sách.
Fallback: câu hỏi không có trong nguồn chính thức được chuyển cho HR/Admin, không tự suy đoán.
```

## Hai candidate còn lại

### Sales Enablement

Nhân viên kinh doanh cần tìm tài liệu phù hợp với ngành và giai đoạn khách hàng nhưng thông tin nằm ở nhiều nơi. Candidate này phù hợp với workflow tìm kiếm, tóm tắt và gợi ý tài liệu; cần kiểm chứng version của bảng giá, quyền sử dụng case study và khả năng đo tỷ lệ dùng đúng nội dung.

### Healthcare Triage

Nhân viên tiếp nhận cần thu thập triệu chứng có cấu trúc và phân luồng ban đầu nhất quán. Đây là candidate có impact cao nhưng rủi ro cao: chỉ nên nghiên cứu AI hỗ trợ hỏi thông tin, phát hiện dấu hiệu cần chuyển ngay cho nhân viên y tế và nhắc quy trình; không chẩn đoán, kê đơn hoặc thay thế bác sĩ.

## Card muốn pitch nhất

**Card tôi muốn pitch nhất:** IT Helpdesk.

**Vì sao:** Actor, workflow và bottleneck tương đối rõ; dữ liệu ticket có thể giúp đo baseline; có thể thử từ form + knowledge base trước khi dùng AI. Ranh giới kiểm soát của IT cũng dễ xác định hơn so với pháp lý và y tế.

**Câu hỏi muốn nhóm challenge:** Ticket nào thực sự lặp lại đủ nhiều để ưu tiên? Knowledge base hiện tại có cập nhật và đủ chính xác không? Nếu AI trả lời sai, bước phê duyệt và rollback sẽ diễn ra thế nào?

## Ghi chú validation cần làm tiếp

- Lấy một mẫu ticket hoặc request gần đây để đo tần suất, thời gian xử lý và số vòng hỏi lại.
- Hỏi 1–3 người thực hiện workflow về bước tốn thời gian nhất và lỗi thường gặp.
- Xác định dữ liệu nào được phép đưa vào công cụ AI, đặc biệt với hợp đồng, dữ liệu nhân sự và dữ liệu y tế.
- Sau validation, cập nhật lại ranking, baseline metric và quyết định Rule / Workflow / Agent.
