# 03 — Individual Reflection

> Viết bằng lời của bạn (Phase 7 trong `01-worksheet.md`). Có thể dùng AI gợi ý câu hỏi tự soi, không dùng AI viết thay. 8-12 câu, có chuyện cụ thể.

## Thông tin cá nhân

- Họ và tên: Trần Đức Quân
- Mã học viên: 2A202602922
- Nhóm: Nhóm 6 người (Vĩ, Đức Quân, Minh Tuấn, Minh Quân, Nhật, Khánh)
- Candidate problem nhóm chọn: Tóm tắt & Trích xuất Thuật toán/Thông số Kỹ thuật từ Bài báo Khoa học phục vụ Seminar & Nghiên cứu

---

## 1. Tôi đã tham gia vào phần nào?

Ghi việc cụ thể + kết quả cụ thể. Không ghi chung chung kiểu "tham gia thảo luận".

| Hoạt động | Tôi đã làm gì? (việc cụ thể) | Kết quả / ảnh hưởng tới nhóm |
|---|---|---|
| Scan cá nhân | Scan 20 problems theo 4 lăng kính (Lặp lại: 5, Tốn thời gian: 5, AI tốt hơn: 5, Pain từ người khác: 5). Mỗi problem có actor, workflow sơ bộ và số đo cụ thể. | Đóng góp 3 candidates vào bảng 18 ý của nhóm (#4 xe buýt, #5 tóm tắt chat, #6 nhắc reply). Giúp nhóm có thêm góc nhìn "đời sống cá nhân" bên cạnh góc "kỹ thuật/nghiên cứu" của Vĩ và Tuấn. |
| Pitch Problem Card | Pitch 3 cards: (1) Tự động chọn giờ rời nhà theo xe buýt — workflow 7 bước, metric giảm chờ xe từ 8-12' xuống ≤3'. (2) Tóm tắt nhóm chat công việc. (3) Nhắc reply tin nhắn quan trọng. | Card xe buýt được nhóm đánh giá "workflow rõ nhưng khó tích hợp API real-time". Card tóm tắt chat được gom vào Cluster B nhưng vướng bảo mật. Cả 3 card không được chọn cuối cùng nhưng giúp nhóm thấy rõ tiêu chí loại (API không ổn định, bảo mật dữ liệu). |
| Challenge bài của bạn khác | Hỏi Vĩ: "Nếu AI hallucinate ký hiệu toán học hoặc bỏ sót giả định ngầm thì kỹ sư mất bao lâu để phát hiện? Có tệ hơn đọc thủ công không?" Hỏi Tuấn: "Chuyển paper thành phương án triển khai — ranh giới giữa trích xuất thông số và viết code ở đâu?" | Challenge về hallucination dẫn đến nhóm thiết kế kiến trúc 2 tầng (Math Parser + LLM) và bắt buộc chèn bước Human Boundary 7 phút đối chiếu PDF gốc. Challenge về ranh giới giúp nhóm quyết định "KHÔNG LÀM: tự động sinh code". |
| Gom trùng / cluster | Đề xuất gom ý #5 (tóm tắt chat) của mình với #12 (khôi phục quyết định cũ) của Minh Quân và #16 (bàn giao sự kiện CLB) của Khánh thành Cluster B "Review & Tìm kiếm Dữ liệu Phân mảnh". Nhận ra cả 3 đều vướng bảo mật. | Cluster B bị loại sớm vì rào cản bảo mật, giúp nhóm tập trung vào Cluster A (Trích xuất Tri thức Kỹ thuật) nhanh hơn. |
| Chọn candidate problem | Chấm điểm 5/5 cho "Tóm tắt Paper" ở tiêu chí "Pain có evidence" và "Impact đo được" vì cả 6 thành viên đều đọc paper hàng tuần. Đồng thuận chọn Cluster A. | Bảng score tổng 34/35 cho candidate #1, cao nhất trong 3 shortlist. Nhóm đồng thuận không cần vote lại. |
| Validation / research | Phối hợp với Tuấn và Khánh thực hiện khảo sát nhanh 12 kỹ sư/sinh viên AI. Tổng hợp kết quả: 100% phải đọc paper 2-5 bài/tuần, 83.3% từng tốn nhiều giờ rồi phải bỏ vì không khả thi. | Kết quả khảo sát xác nhận pain thật và giúp nhóm chốt insight: "Kỹ sư cần Engineering Spec Sheet, không cần tóm tắt văn xuôi". Insight này thay đổi hoàn toàn hướng giải pháp của nhóm. |
| Workflow nhóm | Vẽ workflow trước/sau dạng ASCII cho nhóm: Current State 5 bước (95 phút), Future State 4 bước (15 phút). Bấm giờ chi tiết từng bước trong current workflow. Đánh dấu 2 bottleneck (Đọc Methodology 40' + Tìm thông số kỹ thuật 20'). | Workflow trước/sau được nhóm dùng nguyên văn trong group-report. Số liệu bấm giờ (95' → 15') trở thành baseline và target chính cho success metric. |
| Problem Statement | Đề xuất field Boundary: "LÀM: trích xuất thông số kỹ thuật có cấu trúc + citation. KHÔNG LÀM: tự sinh code, tự clone repo, thay thế đọc sâu lý thuyết nền tảng." | Boundary được nhóm giữ nguyên trong PS v0 và v1. Giúp nhóm tránh scope creep khi Nhật đề xuất thêm tính năng auto-code. |
| Rule / Workflow / Agent | Phân tích vì sao Rule (regex/keyword) thất bại với văn bản học thuật: từ khóa "loss" có thể xuất hiện 30 lần trong paper nhưng chỉ 2-3 lần là nói về loss function thật. Ủng hộ chọn Workflow thay vì Agent. | Nhóm đồng thuận chọn Workflow. Phân tích Rule failure giúp trả lời câu hỏi chốt #1 ("Rule có giải được 70-80% case không? → Không"). |
| Decision | Ủng hộ GO. Đề xuất thêm exit criteria: "Nếu Hallucination Rate vượt 15% hoặc thời gian AI trích xuất > 10 phút/paper thì dừng khẩn cấp." | Exit criteria được đưa vào Exit/Rollback Plan chính thức. Giúp nhóm có ngưỡng định lượng rõ ràng thay vì chỉ nói "dừng khi AI sai quá nhiều". |

**Dấu tay rõ nhất của tôi trong artifact cuối (1-2 câu):**

```text
Workflow trước/sau chi tiết từng phút (95' → 15') và bảng Before/After Impact là do tôi bấm giờ và vẽ. Field Boundary trong Problem Statement v0/v1 ("LÀM / KHÔNG LÀM") và Exit criteria định lượng (Hallucination Rate ≤15%) trong Decision là do tôi đề xuất và được nhóm giữ nguyên.
```

---

## 2. Bảng dùng AI (mỗi dòng 1 phase có dùng AI — 2 cột cuối bắt buộc)

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Hỏi AI gợi ý thêm problem theo 4 lăng kính, kèm actor + workflow + cách đo. Đã tự scan 2 ý trước (xe buýt, đặt đồ ăn) rồi mới hỏi AI. | AI mở rộng được 18 ý tưởng thêm, đặc biệt tốt ở nhóm "Pain từ người khác" (quên reply tin nhắn, thực phẩm hết hạn, chu kỳ bảo trì) — những góc mà bản thân chưa nghĩ tới. | Ý "Gợi ý thời điểm uống nước" (#12) AI đưa ra nhưng không phải pain thật nghiêm trọng. Ý "Dự đoán hàng chờ quán ăn" (#13) thiếu data công khai để kiểm chứng. | Bỏ 2 ý không đủ pain. Giữ 18 ý còn lại nhưng bổ sung số đo cụ thể từ trải nghiệm thật (VD: "đợi xe 8-12 phút" là số tôi tự bấm giờ 1 tuần, không phải AI bịa). |
| Problem Card | Dùng AI phản biện 3 Problem Cards: hỏi "đóng vai skeptical PM, chỉ ra điểm yếu, đừng khen". | AI chỉ ra Card xe buýt phụ thuộc API real-time chưa ổn định ở VN — đúng điểm yếu chính. | AI khen Card tóm tắt chat "rất hay" mà không nói rõ rào cản bảo mật dữ liệu nội bộ là showstopper. Tôi phải tự nhận ra khi Khánh challenge. | Thêm điều kiện "chỉ dùng AI khi có API đáng tin cậy" vào boundary Card xe buýt. Với Card chat, tự bổ sung rủi ro bảo mật mà AI bỏ qua. |
| Workflow | Dùng AI hỗ trợ format workflow ASCII cho nhóm (current/future state). | AI format bảng đẹp và gợi ý thêm cột "Ghi chú (handoff? bottleneck?)" mà tôi quên. | AI ước lượng thời gian future state quá lạc quan (nói 5 phút/paper). Thực tế nhóm thống nhất 15 phút vì phải tính cả Human Review 7 phút. | Sửa thời gian future state từ 5' lên 15' dựa trên đánh giá thực tế của nhóm. Giữ format AI gợi ý vì rõ ràng hơn bản tôi vẽ tay. |
| Research | Dùng AI tìm existing tools (Elicit, Papers With Code, ChatPDF/NotebookLM). Yêu cầu "ghi link nguồn, nếu không chắc thì nói rõ". | AI tìm được 3 tool đúng và phân tích đúng điểm mạnh/yếu. Đặc biệt insight "Elicit chỉ tóm tắt academic, không trích xuất engineering spec" rất hữu ích. | AI ban đầu nói "ChatPDF có thể trích xuất thông số kỹ thuật" — sai, vì ChatPDF chỉ trả lời dạng văn xuôi, không có structured schema. | Tự test ChatPDF với 1 paper thật để verify → xác nhận AI sai → sửa lại thành "thiếu schema kỹ thuật chuẩn hóa" trong bảng research. |
| Problem Statement | Dùng AI phản biện PS v0: "chỉ ra field nào mơ hồ, metric đã đo được chưa, boundary rõ chưa." | AI chỉ ra Success Metric v0 chưa có con số cụ thể cho "5 thông số kỹ thuật cốt lõi" — đúng. | AI gợi ý thêm metric "user satisfaction score" — quá chung chung và khó đo trong lab. | Bỏ metric "satisfaction". Thêm metric định lượng: "100% bản Spec Sheet thể hiện chuẩn xác 5 thông số" và "0 trường hợp bị việt vị do thiếu phần cứng". |
| Rule / Workflow / Agent | Dùng AI phân tích khi nào Rule/Workflow/Agent phù hợp cho bài toán paper extraction. | AI giải thích rõ vì sao Agent quá rủi ro (vòng lặp vô tận, chi phí token cao) — giúp nhóm tự tin loại Agent. | AI ban đầu gợi ý "có thể dùng Agent để tự clone repo và chạy thử" — đi ngược boundary nhóm đã đặt ("KHÔNG LÀM: tự sinh code"). | Loại bỏ gợi ý Agent clone repo. Giữ phân tích Rule failure (regex không hiểu ngữ nghĩa) vì phù hợp thực tế. |
| Decision | Không dùng AI cho phần Decision. | — | — | Tự quyết định GO dựa trên bằng chứng validation (12/12 kỹ sư xác nhận pain) và workflow khả thi. Tự đề xuất exit criteria (Hallucination Rate ≤15%) từ kinh nghiệm đọc paper thật, không phải AI gợi ý. |

> Nếu phase nào không dùng AI, ghi `Không dùng` và vì sao tự làm.

---

## 3. Reflection câu hỏi mở

Chọn 3-4 câu trong 6 câu dưới để viết thành đoạn 8-12 câu (không trả lời bullet 1 dòng):
- Tôi học được gì khi nghe top 3 problems của các bạn khác?
- Nhóm có lúc nào bị solution-first, đòi làm Agent cho ngầu không?
- Tôi có thay đổi ý kiến sau khi bị challenge không, vì sao đổi?
- Tôi đóng góp gì thật sự vào artifact cuối, phần nào có dấu tay của tôi?
- Điều khó nhất khi viết Problem Statement là gì, metric hay boundary?
- Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?

**Reflection:**

```text
Khi nghe top 3 problems của Vĩ và Tuấn, tôi nhận ra rằng 3 ý tưởng cá nhân của mình (xe buýt, tóm tắt chat, nhắc reply) đều thuộc dạng "tiện ích đời sống" — pain có thật nhưng impact không đủ sâu so với bài toán "đọc paper khoa học" mà cả nhóm 6 người đều chịu ảnh hưởng hàng tuần. Bài học lớn nhất là: problem tốt không phải problem mình nghĩ ra đầu tiên, mà là problem có actor rộng nhất trong nhóm và bottleneck đau nhất.

Nhóm đã có lúc bị solution-first khi Nhật đề xuất xây Agent tự clone repo GitHub và chạy thử nghiệm luôn. Nghe rất "ngầu" nhưng khi tôi challenge "nếu Agent sinh code lỗi thì ai phát hiện và mất bao lâu sửa?", cả nhóm im lặng 5 giây rồi đồng ý hạ xuống Workflow. Khoảnh khắc đó dạy tôi rằng câu hỏi "nếu AI sai thì sao?" có sức mạnh lớn hơn mọi tính năng fancy.

Tôi đã thay đổi ý kiến sau khi bị challenge. Ban đầu tôi muốn pitch Card xe buýt cho nhóm, nhưng khi Khánh hỏi "data giờ xe buýt real-time ở VN có đáng tin không?", tôi nhận ra rằng toàn bộ giá trị của Card này phụ thuộc vào một thứ tôi không kiểm soát được (API bên thứ 3). Ngược lại, bài toán paper extraction có input là PDF công khai, không phụ thuộc bất kỳ API nào — an toàn hơn nhiều cho một buổi lab. Việc chấp nhận ý tưởng của mình bị loại không dễ, nhưng tiêu chí chọn rõ ràng (actor rộng + data sẵn có + bottleneck rõ) giúp tôi đồng thuận mà không cảm thấy bị áp đặt.

Điều khó nhất khi viết Problem Statement là xác định boundary "KHÔNG LÀM". Nhóm rất muốn thêm tính năng: tự sinh code, tự so sánh nhiều paper, tự đề xuất paper tiếp theo. Tôi phải liên tục nhắc: "Nếu scope phình ra thì metric nào đo? Ai kiểm tra?" Cuối cùng boundary chốt được ("KHÔNG LÀM: tự sinh code, tự clone repo") là kết quả của 3 lần nhóm định mở rộng rồi tự rút lại.

Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở phần validation. Khảo sát 12 người cho kết quả 100% đồng ý — con số quá đẹp khiến tôi nghi ngờ có confirmation bias (hỏi đúng người đã biết pain). Lẽ ra nên hỏi thêm 5-10 người ngoài ngành AI (VD: kỹ sư phần mềm backend, PM) để xem họ có gặp pain tương tự khi đọc tài liệu kỹ thuật dài không — nếu có thì actor rộng hơn, nếu không thì nhóm biết rõ giới hạn của giải pháp.
```

---

## 4. Tự kiểm cuối bài (check trước khi nộp repo)

- [x] [12đ] Cá nhân có 5+ problems + top 3 Problem Cards
- [x] [12đ] Tôi đã pitch rõ + challenge nhóm đúng trọng tâm (ghi ở bảng mục 1)
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài
- [x] [15đ] Nhóm có workflow trước/sau
- [x] [20đ] Nhóm có PS v0/v1 với metric + boundary rõ
- [x] [15đ] Nhóm có so sánh No AI / Rule / Workflow / Agent
- [x] [10đ] Nhóm có Go / Not Yet / No-Go + lý do rõ
- [x] [10đ] Reflection này có vai trò thật + AI giúp/sai ở đâu + điều học được + nếu làm lại đổi gì
- [x] [6đ] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp AI

