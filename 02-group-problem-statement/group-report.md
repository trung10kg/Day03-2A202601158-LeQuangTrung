# Group Report - Day 02

## Thành Viên Nhóm

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm |
|-----|-----------|-------------|--------------------|
| 1 | Lê Trí Tùng | 2A202601458 | Nhóm trưởng, điều phối thảo luận, đề xuất problem, vẽ workflow |
| 2 | Lê Tuấn Minh | 2A202601390 | Pitch problem, đóng góp candidate |
| 3 | Vũ Xuân Anh | 2A202602010 | Challenge problem, góp ý workflow |
| 4 | Lê Quang Trung | 2A202601158 | Research giải pháp tương tự |
| 5 | Vũ Đình Huy | 2A202601288 | Validation nhanh, ghi nhận tín hiệu xác nhận/phản bác |
| 6 | Nguyễn Thị Nam Phương | 2A202601720 | Góp ý Problem Statement và boundary |
| 7 | Đỗ Thị Thanh Loan | 2A202601654 | Tổng hợp notes, hỗ trợ gom cluster |
| 8 | Nguyễn Thuỳ Trang | 2A202601294 | Review metric và impact |
| 9 | Nguyễn Quốc Bảo | 2A202601726 | So sánh Rule / Workflow / Agent |
| 10 | Nguyễn Cao Quang Anh | 2A202601352 | Review decision cuối và fallback |

---

# 1. Candidate Problems Từ Cả Nhóm

| # | Người đưa ra | Nhóm | Candidate problem | Người gặp vấn đề | Điểm nghẽn | Cảm nhận nhanh |
|---|---:|---|---|---|---|---|
| 1 | Vũ Xuân Anh | 2 | Sinh viên mất thời gian nắm thông tin vận hành, quy trình xử lý sự cố và phương án giải quyết nhanh. | Sinh viên trong chương trình/lab | Thông tin vận hành rải rác, không biết hỏi ai hoặc làm bước nào trước | Gần bài toán hỗ trợ vận hành |
| 2 | Nguyễn Cao Quang Anh | 2 | Thông tin từ lab coach/BTC không đến đủ học viên; câu hỏi lặp lại trong OH/WS. | Học viên, lab coach, BTC | Truyền thông không đồng bộ | Pain rõ, nhiều người gặp |
| 3 | Lê Trí Tùng | 2 | Sinh viên mất thời gian kiểm tra bài lab cần nộp gì từ nhiều nguồn. | Sinh viên làm bài lab | Phải tự đọc README, worksheet, example và tin nhắn để lập checklist | Workflow rõ, metric đo được |
| 4 | Nguyễn Thị Nam Phương | 3 | Dự đoán phạm vi lan rộng của cháy rừng vào ngày tiếp theo bằng TimeSeries. | Đơn vị theo dõi cháy rừng, đội ứng cứu | Cần dữ liệu thời gian, thời tiết, địa hình và mô hình dự đoán | Impact lớn, scope rộng |
| 5 | Đỗ Thị Thanh Loan | 3 | Giảng viên mất nhiều thời gian chấm bài ngắn và bài lập trình, khiến feedback chậm và chung chung. | Giảng viên, sinh viên | Chấm bài lặp lại, feedback cá nhân hóa tốn thời gian | Cần boundary chấm điểm rõ |
| 6 | Nguyễn Thùy Trang | 3 | Tình huống phạm lỗi 50/50 thiếu cách khách quan để đối chiếu quyết định trọng tài với luật và bối cảnh. | Trọng tài, người xem, đội bóng | Clip thiếu bối cảnh, luật được hiểu khác nhau | Khó lấy dữ liệu chuẩn |
| 7 | Lê Tuấn Minh | 1 | Sinh viên mất thời gian tìm lại thông tin cũ từ Discord, Google Drive, LMS, Notion. | Sinh viên làm bài cá nhân/nhóm | Search nhiều nguồn | Pain phổ biến |
| 8 | Nguyễn Quốc Bảo | 1 | Sinh viên mất thời gian tìm lại thông tin cũ từ Discord, Google Drive, LMS, Notion. | Sinh viên làm bài cá nhân/nhóm | Khó biết bản nào mới nhất | Trùng pattern với #7 |
| 9 | Lê Quang Trung | 1 | Người bán hàng phải lặp lại việc trả lời các câu hỏi giống nhau khi chăm sóc khách hàng. | Chủ shop, nhân viên bán hàng, khách hàng | Câu hỏi lặp lại về giá, tồn kho, vận chuyển, chính sách | Có thể dùng FAQ/rule |
| 10 | Vũ Đình Huy | 1 | Chăm sóc khách hàng trong bán hàng bị lặp lại nhiều thao tác trả lời và tư vấn cơ bản. | Người bán hàng, khách mua | Trả lời thủ công nhiều câu hỏi giống nhau | Gần candidate #9 |

---

# 2. Gom Trùng / Cluster

| Cluster | Candidates included | Pattern chung | Ghi chú |
|---|---|---|---|
| A - Thông tin lab và bài nộp | #1, #2, #3, #7, #8 | Sinh viên mất thời gian tìm, hiểu và kiểm tra thông tin học tập/lab từ nhiều nguồn | Cluster mạnh nhất, gần bối cảnh lab |
| B - Chăm sóc khách hàng lặp lại | #9, #10 | Người bán hàng phải trả lời nhiều câu hỏi giống nhau | Workflow rõ, có thể xử lý bằng FAQ/rule |
| C - Chấm bài và phản hồi học tập | #5 | Giảng viên mất thời gian chấm bài, sinh viên nhận feedback chậm | Impact rõ, cần boundary cẩn thận |
| D - Dự đoán / phân tích bối cảnh phức tạp | #4, #6 | Cần dữ liệu, mô hình hoặc bối cảnh đầy đủ để ra quyết định | Scope rộng, khó validate nhanh |

---

# 3. Shortlist Và Score

| Candidate | Vì sao vào shortlist | Rủi ro / điều chưa rõ |
|---|---|---|
| #3 - Lê Trí Tùng: kiểm tra bài lab cần nộp gì | Actor rõ, workflow nhỏ, metric đo được, làm được trong lab | Cần xác nhận pain xảy ra với nhiều bạn |
| #2 - Nguyễn Cao Quang Anh: thông tin lab coach/BTC không đến đủ học viên | Pain ảnh hưởng nhiều học viên, câu hỏi lặp lại là tín hiệu thật | Scope có thể rộng sang vận hành toàn chương trình |
| #7/#8 - Tìm lại thông tin cũ từ nhiều nguồn | Nhiều người gặp, liên quan trực tiếp học tập và báo cáo nhóm | Vướng data access nhiều nguồn |
| #9/#10 - Chăm sóc khách hàng lặp lại | Workflow rõ, dễ so sánh Rule/Workflow/Agent | Xa bối cảnh học/lab của nhóm |

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| #3 - Kiểm tra bài lab cần nộp gì | 5 | 5 | 4 | 5 | 5 | 5 | 5 | 34 |
| #2 - Truyền tải thông tin lab coach/BTC | 5 | 4 | 4 | 4 | 4 | 4 | 5 | 30 |
| #7/#8 - Tìm lại thông tin cũ từ nhiều nguồn | 5 | 4 | 4 | 4 | 3 | 4 | 5 | 29 |
| #9/#10 - Chăm sóc khách hàng lặp lại | 4 | 5 | 3 | 4 | 4 | 5 | 3 | 28 |

**Candidate nhóm chọn:** đề tài của **Lê Trí Tùng**.

```text
Sinh viên mất thời gian kiểm tra bài lab cần nộp gì từ nhiều nguồn.
```

**Lý do chọn:**

- Actor cụ thể: sinh viên đang làm bài lab.
- Workflow rõ: đọc README, worksheet, example, tin nhắn rồi tự lập checklist.
- Bottleneck rõ: tự tổng hợp yêu cầu và đối chiếu với bài đang làm.
- Metric đo được: thời gian check bài và số field bị thiếu.
- Scope nhỏ, phù hợp thời gian lab.

---

# 4. Quick Validation

| Nguồn | Số người / mẫu | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Quick interview | 3 sinh viên | 3/3 từng phải mở lại README/worksheet/example để check bài; 2/3 sợ thiếu field khi nộp | 1 bạn nói nếu có checklist sẵn thì có thể không cần AI | Thu hẹp problem thành "check bài hiện tại với checklist/rubric" |
| Mini poll trong nhóm | 10 thành viên | Nhiều bạn gặp vấn đề tìm/kiểm tra thông tin bài nộp | Không ai cần agent tự động nộp bài | Chọn Workflow có human review |
| Quan sát repo | 3 file nộp bài | File cá nhân ban đầu trống, group report mới có bảng thành viên | Repo mới khởi tạo nên evidence còn hạn chế | Dùng làm tín hiệu phụ, không phải evidence chính |

---

# 5. Research / Evidence

| Nguồn / tool / case | Link | Liên quan gì đến problem? | Bài học cho nhóm |
|---|---|---|---|
| Bayne & Inan (2022) - Online Course Overload Indicator | https://www.irrodl.org/index.php/irrodl/article/view/6223 | Paper khảo sát 378 sinh viên undergraduate; overload trong online course liên quan đến information overload, course design, facilitation | Khi tài nguyên học tập quá nhiều/khó tìm, sinh viên dễ bị cognitive overload; checklist giúp giảm tải |
| GitHub Pull Request checklist | https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-issue-and-pull-request-templates | Checklist giúp người nộp/reviewer không bỏ sót yêu cầu | Nên có checklist rule làm nền |
| GitHub Actions | https://docs.github.com/en/actions | Tự động check cấu trúc file, format, test | Rule phù hợp để check có/không; AI phù hợp cho phần mơ hồ |
| Grammarly | https://www.grammarly.com/ | Writing assistant review bản nháp và gợi ý sửa | AI nên là reviewer, không phải người viết thay |

**Research takeaway:**  
Giải pháp hợp lý là **Workflow**: checklist cố định từ rubric + AI review bản nháp + sinh viên tự xác nhận và sửa.

---

# 6. Current Workflow

```text
CURRENT STATE - khoảng 30 phút/lần check bài

[1 Mở README: 5']
-> [2 Đọc worksheet: 8']
-> [3 Xem deliverable example: 5']
-> [4 Tự lập checklist: 5']
-> [5 Đối chiếu report với checklist: 7']  <-- bottleneck
-> [6 Sửa phần thiếu/mơ hồ]
```

| Bước | Actor | Input | Output | Thời gian | Ghi chú |
|---|---|---|---|---:|---|
| 1 | Sinh viên | README | Hiểu cấu trúc repo | 5' | Nguồn tổng quan |
| 2 | Sinh viên | Worksheet | Biết các phase cần làm | 8' | Dài, nhiều checklist |
| 3 | Sinh viên | Example | Hình dung output | 5' | Dễ đọc lâu |
| 4 | Sinh viên | README + worksheet + example | Checklist cá nhân | 5' | Có thể thiếu field |
| 5 | Sinh viên | Report đang viết | Danh sách phần thiếu | 7' | Bottleneck |
| 6 | Sinh viên | Danh sách phần thiếu | Bài hoàn thiện hơn | Tùy bài | Human ownership |

---

# 7. Future Workflow

```text
FUTURE STATE - khoảng 9 phút/lần check bài

[1 Checklist cố định từ rubric: 1']        -- Rule
-> [2 Sinh viên đưa report đang viết: 1']  -- Human input
-> [3 AI so sánh report với checklist: 1'] -- Workflow step
-> [4 AI chỉ ra mục thiếu/mơ hồ: 1']       -- Workflow step
-> [5 Sinh viên kiểm tra nhận xét: 3']     -- Human boundary
-> [6 Sinh viên tự sửa và check lại]
```

| Metric | Trước | Sau kỳ vọng |
|---|---:|---:|
| Tổng thời gian check bài | 30 phút | Dưới 10 phút |
| Số nguồn phải mở lại | 3-4 nguồn | 1 checklist + report |
| Số field bắt buộc bị thiếu | 2-4 field có thể bị sót | 0 field |
| Bước thủ công | 6/6 | 3/6 |

---

# 8. Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | Sinh viên đang làm repo cá nhân cho Day 02 Lab. |
| **Workflow** | Đọc README, worksheet, deliverable example, tự lập checklist, đối chiếu với report và sửa bài. |
| **Bottleneck** | Tự lập checklist và đối chiếu rubric mất 15-20 phút, dễ thiếu field. |
| **Impact** | Tổng thời gian check bài khoảng 30 phút/lab; bài có thể thiếu Problem Card, workflow, metric, boundary hoặc reflection. |
| **Success Metric** | Giảm thời gian check bài từ 30 phút xuống dưới 10 phút; field bắt buộc bị thiếu trước khi nộp = 0. |
| **Boundary** | AI không viết thay bài cá nhân/reflection; AI chỉ review theo checklist và chỉ ra phần thiếu/mơ hồ. |

---

# 9. So Sánh Rule / Workflow / Agent

| Mức | Phương án | Khi nào đủ | Rủi ro | Chọn? |
|---|---|---|---|---|
| **Rule** | Checklist cố định từ rubric | Đủ để check field có/không | Không đánh giá được phần mơ hồ | Dùng một phần |
| **Workflow** | Checklist -> AI review -> sinh viên kiểm tra -> sinh viên sửa | Phù hợp vì AI chỉ hỗ trợ một bước review | AI có thể nhận xét sai hoặc gợi ý chung chung | Chọn |
| **Agent** | Agent tự đọc repo, tự sửa bài, tự chốt đạt/chưa đạt | Chỉ cần nếu có nhiều repo/file và cần tự động thao tác | Dễ viết thay sinh viên, scope quá rộng | Không chọn |

**Mức chọn:** Workflow.

---

# 10. Problem Statement v1

| Field | Nội dung |
|---|---|
| **Actor** | Sinh viên đang hoàn thiện repo Day 02 Lab trước khi nộp. |
| **Workflow** | Mở README -> đọc worksheet -> xem example -> tự lập checklist -> đối chiếu individual report/group report/reflection -> sửa phần thiếu. |
| **Bottleneck** | Tự lập checklist và đối chiếu nội dung với rubric mất 15-20 phút, dễ bỏ sót success metric, boundary, AI intervention point, risk và decision rationale. |
| **Impact** | Tổng thời gian check bài khoảng 30 phút/lab; bài có nguy cơ mất điểm nếu thiếu field hoặc lập luận mơ hồ. |
| **Success Metric** | Giảm thời gian check bài từ 30 phút xuống dưới 10 phút; 100% field bắt buộc có nội dung trước khi nộp. |
| **Boundary** | AI không viết thay reflection, không bịa trải nghiệm cá nhân, không tự chốt bài đạt/chưa đạt. |
| **AI intervention point** | Sau khi sinh viên có bản nháp report, trước bước nộp bài cuối. |
| **Mức chọn** | Workflow: checklist rule + AI reviewer + human edit. |
| **Rủi ro & người thật kiểm tra** | Risk: AI nhận xét sai hoặc gợi ý chung chung. Người kiểm tra: sinh viên và nhóm. |

---

# 11. Final Decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú |
|---|---|---|
| Actor và workflow đã rõ chưa? | Yes | Sinh viên làm repo lab |
| Baseline và success metric đã đo được chưa? | Yes | 30 phút -> dưới 10 phút |
| Có data/input đủ dùng chưa? | Yes | README, worksheet, example, report đang viết |
| Nếu AI sai, hậu quả có chấp nhận được không? | Yes | Vì sinh viên vẫn review |
| Có người review/owner vận hành không? | Yes | Sinh viên và nhóm |
| Có cách non-AI đơn giản hơn không? | Yes | Checklist thủ công |

**Decision:** Go với scope nhỏ.

**Pilot nhỏ nhất:** dùng checklist Day 02 cho một bản nháp report, AI chỉ trả về danh sách mục thiếu/mơ hồ theo rubric, sinh viên tự sửa.

---

# 12. Tự Kiểm

- [x] Có candidate problems từ cả nhóm.
- [x] Có cluster và shortlist.
- [x] Có validation nhanh.
- [x] Có research/evidence.
- [x] Có workflow trước/sau.
- [x] Có Problem Statement v0/v1.
- [x] Có so sánh Rule / Workflow / Agent.
- [x] Có decision Go / Not Yet / No-Go.
