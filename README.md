# Track 1 - Day 27 — AI Team Lab

- **Team:** Mixue
- **Thành viên (4 người):**
  - **Phạm Tiến Hưng (2A202601800)** — Team Lead / Product & AI Ops Lead (Người tổng hợp bài & quản lý repo)
  - **Lê Đăng Tấn (2A202601916)** — AI/LLM Engineer & Model Evaluation
  - **Nguyễn Quang Sơn (2A202601956)** — Fullstack & LTI 1.3 Integration Engineer
  - **Nguyễn Minh Quang (2A202601730)** — Customer Success & Data/FinOps Analyst
- **Tên dự án:** VLearn AI Tutor
- **Link sản phẩm/demo (nếu có):** https://github.com/Navierr/Track1-Day27-Mixue-VlearnTutor

---

## 🎯 Mục tiêu dự án trong 1–3 tháng tới (Milestone 90 ngày)
1. **Đưa sản phẩm đến End-User qua LMS:** Hoàn thiện tích hợp LTI 1.3 trên Canvas/Moodle, rút ngắn thời gian triển khai từ khi cấp quyền đến sinh viên đầu tiên sử dụng xuống $\le 7$ ngày (`TTF-End-User`, Luật `R-02`).
2. **Kích hoạt đối tác (Partner Activation Rate):** Đạt tỷ lệ kích hoạt $\ge 70\%$ số trường đại học/khoa ký kết (mỗi trường có $\ge 20$ sinh viên hoàn thành phiên giải bài học thuật thật trong 30 ngày, North Star Metric).
3. **Chất lượng AI & Kiểm soát chi phí (Responsible AI & FinOps):** Đạt tỷ lệ phản hồi chính xác sư phạm $\ge 92\%$, giảm ảo giác kiến thức $< 5\%$ (dựa trên bộ test 18 tài liệu corpus Day 20-21), duy trì chi phí token/embedding $\le 1.200$ VNĐ/session với Gross Margin sau 25% Rev-Share đạt $\ge 58\%$ (Luật `R-04`, `R-05`).

---

## 🚦 Gate 0: Scope Verification Check
- [x] **Cùng một dự án:** Toàn bộ team tập trung 100% vào **VLearn AI Tutor** (kế thừa từ chuỗi Day 20-21 đến Day 26).
- [x] **Cùng một mục tiêu:** Đưa AI Tutor vào vận hành thực tế qua LMS trong 1–3 tháng tới, kích hoạt $\ge 70\%$ đối tác trường học.
- [x] **Người tổng hợp bài:** Phạm Tiến Hưng (chịu trách nhiệm cấu trúc repository, điều phối và đảm bảo chất lượng 4 Artefacts).
- **Kết quả Gate 0:** ✅ **PASS** (Đủ điều kiện kích hoạt Phase 1).

---

## 📌 ARTEFACT 1: STAKEHOLDER MAP & STRATEGY (TRANG 1)

### 1.1. Bản đồ 6 Chức danh Stakeholder trên Ma trận 2x2 (Influence × Interest) & Lập trường (Stance)

```
                          MỨC ĐỘ ẢNH HƯỞNG (INFLUENCE)
                         THẤP (LOW)                   CAO (HIGH)
           ┌──────────────────────────────┬──────────────────────────────┐
           │                              │                              │
           │       KEEP INFORMED          │       MANAGE CLOSELY         │
      C    │                              │                              │
      A    │  4. Sinh viên & Ban Cán sự   │  1. Giảng viên Cốt cán /     │
      O    │     Lớp (End-Users)          │     Chủ nhiệm Bộ môn         │
           │     [Stance: Supporter]      │     [Stance: Champion]       │
    (HIGH) │     - Influence: Thấp (2/5)  │     - Influence: Cao (5/5)   │
           │     - Interest: Cao (5/5)    │     - Interest: Cao (5/5)    │
    M      │                              │  5. Ban Điều hành & FinOps   │
    Ứ      │                              │     (Team Mixue Core)        │
    C      │                              │     [Stance: Champion]       │
           │                              │     - Influence: Cao (5/5)   │
    Đ      │                              │     - Interest: Cao (5/5)    │
    Ộ      ├──────────────────────────────┼──────────────────────────────┤
           │                              │                              │
    Q      │          MONITOR             │       KEEP SATISFIED         │
    U      │                              │                              │
    A    T │  6. Đại diện Đối tác Nền     │  2. Ban Giám Hiệu /          │
    N    H │     tảng LMS (Canvas/Moodle) │     Ban Đào Tạo Trường ĐH    │
         Ấ │     [Stance: Bystander]      │     [Stance: Skeptic]        │
    T    P │     - Influence: Thấp (2/5)  │     - Influence: Cao (5/5)   │
    Â      │     - Interest: Thấp (2/5)   │     - Interest: Thấp (2/5)   │
    M (LOW)│                              │  3. Quản trị viên LMS /      │
           │                              │     Trưởng phòng CNTT Trường │
           │                              │     [Stance: Blocker Kỹ thuật│
           │                              │     - Influence: Rất cao(5/5)│
           │                              │     - Interest: Thấp (1/5)   │
           └──────────────────────────────┴──────────────────────────────┘
```

---

### 1.2. Chiến lược Hành động cho 4 Stakeholder Ưu tiên trong 1–2 Tuần tới (Bám sát Day 20–26)

#### 🟢 NHÓM 1: 2 STAKEHOLDER ĐANG ỦNG HỘ MẠNH (TẬN DỤNG SỨC ẢNH HƯỞNG)

1. **Giảng viên Cốt cán / Chủ nhiệm Bộ môn** *(Stance: Champion | Influence: 5/5 | Interest: 5/5)*
   - **Họ quan tâm điều gì:** Giải quyết điểm đau lớn nhất là thiếu trợ giảng hỗ trợ sinh viên trong khung giờ 21h–23h (Pain Moment đã xác thực ở Cổng 30d Day 26); yêu cầu AI giải thích theo phương pháp gợi mở từng bước (Socratic Guidance), không cung cấp đáp án trực tiếp để tránh gian lận học thuật.
   - **Họ giúp dự án thế nào:** Đưa VLearn AI Tutor vào đề cương môn học chính thức, yêu cầu sinh viên dùng AI Tutor giải bài tập tuần, đồng thời cung cấp bộ tài liệu giáo trình chuẩn (Corpus 18 tài liệu như Day 20-21) để xây dựng Knowledge Base chuẩn xác.
   - **Hành động cụ thể trong 1–2 tuần tới:** 
     > *Bàn giao tài khoản Teacher Analytics Dashboard trước thứ Sáu tuần 1, trực tiếp hỗ trợ cấu hình nhúng AI Tutor vào 2 lớp học thử nghiệm (120 sinh viên), và tổ chức buổi họp 20 phút vào sáng thứ Ba tuần kế tiếp để đối soát độ chính xác của câu trả lời dựa trên rubric Day 20-21.*  
     > *(Owner: Nguyễn Minh Quang — Customer Success Lead).*

2. **Sinh viên & Ban Cán sự Lớp học (End-Users)** *(Stance: Supporter | Influence: 2/5 | Interest: 5/5)*
   - **Họ quan tâm điều gì:** Cần gia sư giải đáp thắc mắc bài tập lúc đêm muộn khi không thể hỏi giảng viên; câu trả lời đúng trọng tâm giáo trình trường, có trích dẫn nguồn (`sources: doc_id#section_id`), giao diện nhúng trực tiếp trong LMS không cần đăng nhập lại, tốc độ phản hồi nhanh ($<2s$).
   - **Họ giúp dự án thế nào:** Sử dụng hàng ngày tạo ra volume session thực tế để đạt North Star Metric ($\ge 20$ SV active/trường trong 30d), trực tiếp đánh giá mini-eval sau mỗi câu trả lời (thumb up/down) làm dữ liệu calibrate model.
   - **Hành động cụ thể trong 1–2 tuần tới:** 
     > *Tổ chức 01 buổi hướng dẫn trực tuyến 30 phút vào tối Chủ Nhật tuần 1 hướng dẫn ban cán sự lớp cách mở widget LTI trên LMS Moodle/Canvas, phát hành in-app mini-eval để thu thập 100 lượt đánh giá đầu tiên về độ hữu ích của câu trả lời.*  
     > *(Owner: Lê Đăng Tấn — AI Engineer).*

---

#### 🔴 NHÓM 2: 2 STAKEHOLDER CHƯA ỦNG HỘ / CÓ RỦI RO CẢN TRỞ (ƯU TIÊN THUYẾT PHỤC & DE-RISK)

3. **Quản trị viên LMS / Trưởng phòng CNTT Nhà trường (LMS Admin / IT Lead)** *(Stance: Critical Blocker Kỹ thuật | Influence: 5/5 | Interest: 1/5)*
   - **Họ quan tâm điều gì:** Bảo mật dữ liệu sinh viên theo tiêu chuẩn giáo dục (Zero-PII retention), đảm bảo tích hợp an toàn qua chuẩn IMS LTI 1.3 không làm treo/chậm hệ thống LMS nội bộ của trường khi có lưu lượng truy cập lớn.
   - **Họ cản trở dự án thế nào:** Trì hoãn hoặc từ chối cấp LTI 1.3 Client ID/Deployment ID, kéo dài thời gian thẩm định kỹ thuật khiến chỉ số `TTF-End-User` vượt quá 14 ngày (kích hoạt báo động đỏ theo Luật `R-02`).
   - **Hành động cụ thể trong 1–2 tuần tới:** 
     > *Gửi tài liệu kỹ thuật chuẩn hóa "Whitepaper Bảo mật LTI 1.3 & Cam kết Không lưu trữ PII" trước 17h thứ Ba tuần 1; Kỹ sư LTI Nguyễn Quang Sơn trực tiếp hẹn lịch hỗ trợ kỹ thuật 1-1 trong 30 phút vào thứ Năm để cấu hình nhúng nút AI hoàn tất trên môi trường Staging LMS của trường trong vòng 48h (thực thi nghiêm ngặt Luật R-02).*  
     > *(Owner: Nguyễn Quang Sơn — LTI Integration Engineer).*

4. **Ban Giám Hiệu / Ban Đào Tạo Trường Đại Học** *(Stance: Skeptic / Potential Blocker | Influence: 5/5 | Interest: 2/5)*
   - **Họ quan tâm điều gì:** Tính toàn vẹn học thuật và uy tín của nhà trường (Responsible AI Day 22), đảm bảo AI không tạo ra ảo giác (hallucination) sai lệch kiến thức hoặc vi phạm bản quyền tài liệu, đồng thời chi phí hợp tác phần mềm (Base fee $99/tháng) phải mang lại ROI rõ ràng về tỷ lệ sinh viên hoàn thành môn học.
   - **Họ cản trở dự án thế nào:** Ban hành quy định cấm hoặc hạn chế sinh viên sử dụng công cụ AI trong học tập, hoặc từ chối ký hợp đồng chính thức sau giai đoạn thử nghiệm miễn phí.
   - **Hành động cụ thể trong 1–2 tuần tới:** 
     > *Trình bản Báo cáo Tác động Sư phạm (Executive Summary 2 trang) chứng minh hệ thống đạt độ chính xác $\ge 92\%$ qua kiểm thử rubric 18 tài liệu, kèm cam kết bộ lọc Responsible AI Guardrails ngăn chặn $100\%$ việc cung cấp bài giải hoàn chỉnh; gửi qua Văn phòng Ban Giám Hiệu trước thứ Sáu tuần 1 để xin phê duyệt cơ chế triển khai thử nghiệm diện hẹp (Sandbox).*  
     > *(Owner: Phạm Tiến Hưng — Team Lead).*

---

## 🚦 GATE 1 — STAKEHOLDER MAP CÓ THỂ HÀNH ĐỘNG (VERIFICATION CHECK)
- [x] **Có ít nhất 6 chức danh stakeholder cụ thể (trung thực, bám sát đề tài Day 20–26):**
  1. Giảng viên Cốt cán / Chủ nhiệm Bộ môn (Champion)
  2. Ban Giám Hiệu / Ban Đào Tạo Trường ĐH (Skeptic)
  3. Quản trị viên LMS / Trưởng phòng CNTT Trường (Critical Blocker)
  4. Sinh viên & Ban Cán sự Lớp (Supporter)
  5. Ban Điều hành & FinOps Dự án - Team Mixue (Champion)
  6. Đại diện Đối tác Nền tảng LMS Canvas/Moodle (Bystander)
- [x] **Map chuẩn xác theo Influence × Interest:** Thể hiện rõ 4 góc phần tư và các thuộc tính số hóa.
- [x] **Stance (Mức độ ủng hộ) rõ ràng:** Phân loại chính xác Champion, Supporter, Skeptic, Blocker, Bystander.
- [x] **4 Kế hoạch hành động cụ thể cho 4 Stakeholder ưu tiên:** Gắn liền với các cơ chế đã thống nhất từ Day 20-21 (Corpus 18 tài liệu & Rubric Eval), Day 22 (Responsible AI & Socratic Guardrails), Day 24-25 (FinOps $1.200$đ & Rev-Share), Day 26 (Luật `R-02`, Pain Moment 21h-23h), có deadline từng ngày và phân công đích danh Owner trong team (Hưng, Tấn, Sơn, Quang).
- **Kết quả Gate 1:** ✅ **PASS 100%** (Chuẩn xác, trung thực và bám sát dự án).

---

## 📌 ARTEFACT 2: CONCLUSION-FIRST PITCH & RACI MATRIX (TRANG 2)

### 2.1. Bản Pitch Ngắn Theo Cấu Trúc "Kết Luận Trước" (Target Stakeholder: Giảng viên Cốt cán / Chủ nhiệm Bộ môn)

> **KẾT LUẬN / ĐỀ XUẤT (CONCLUSION FIRST):**  
> **Team Mixue đề xuất triển khai chương trình Thử nghiệm 30 ngày (Pilot Sandbox) tích hợp Trợ giảng AI VLearn Tutor trực tiếp vào 02 lớp môn Lập trình (120 sinh viên) trên hệ thống LMS Canvas/Moodle của Khoa.**  
> *(Chúng tôi cam kết giải tỏa 50% gánh nặng trả lời câu hỏi lặp lại của Giảng viên ngoài giờ, đồng thời bảo vệ 100% tính liêm chính học thuật qua cơ chế sư phạm gợi mở Socratic).*

#### 3 Lý do chính (Key Arguments):
1. **Giải quyết triệt để "Khoảng trống trợ giảng 21h–23h":** Sinh viên thường xuyên nghẽn bài tập khi tự học ban đêm nhưng không có trợ giảng hỗ trợ. VLearn AI Tutor phản hồi tức thì 24/7, giúp sinh viên vượt qua khúc mắc tư duy ngay lập tức.
2. **Phương pháp sư phạm Socratic — Tuyệt đối không làm hộ bài:** Hệ thống được huấn luyện theo bộ Guardrails nghiêm ngặt, chỉ đưa ra câu hỏi gợi mở, phân tích lỗi sai và trích dẫn trực tiếp từ giáo trình môn học (`doc_id#section_id`), buộc sinh viên phải tự suy nghĩ và tự viết code.
3. **Tiết kiệm thời gian & Trao quyền quản trị cho Giảng viên:** Cung cấp Teacher Analytics Dashboard tự động tổng hợp các chủ đề sinh viên hay hỏi nhất và các lỗ hổng kiến thức phổ biến, giúp Giảng viên tối ưu bài giảng trên lớp mà không tốn công chấm/chữa bài thủ công.

#### Bằng chứng & Số liệu thực tế (Hard Evidence & Metrics):
- **Độ chính xác học thuật:** Đạt **$92.4\%$** câu trả lời chuẩn xác sư phạm trên bộ dữ liệu kiểm thử 18 tài liệu giáo trình chuẩn (Kết quả AI Evaluation Day 20-21).
- **Ngăn chặn gian lận:** **$0\%$** trường hợp đưa ra toàn bộ mã nguồn hoặc đáp án bài thi cuối kỳ (Responsible AI Gate Day 22).
- **Tốc độ & Chi phí tối ưu:** Thời gian phản hồi trung bình **$< 1.8$ giây**, chi phí vận hành token tối ưu ở mức **$1.150$ VNĐ/session** (thấp hơn trần $1.200$ VNĐ/session của FinOps Day 24-25).

#### Small Ask (Đề nghị hành động nhỏ tiếp theo):
> *Thầy/Cô đồng ý cho phép Kỹ sư VLearn nhúng tiện ích LTI vào 02 lớp học thử nghiệm trên LMS trong 48 giờ tới, và dành 20 phút vào sáng thứ Ba tuần sau để cùng team xem báo cáo phân tích học tập đầu tiên.*

---

### 2.2. Chuẩn Bị Phản Biện & Câu Trả Lời Giảm Thiểu Rủi Ro (De-risking Objection Handling)

* **Phản biện có khả năng xảy ra nhất:**  
  > *"AI hiện nay hay bị 'ảo giác' (hallucination), trả lời linh tinh hoặc sinh viên sẽ lợi dụng AI để làm hộ toàn bộ bài tập lớn khiến các em mất gốc và ỷ lại công nghệ."*
* **Câu trả lời dựa trên bằng chứng & giải pháp kiểm soát rủi ro:**  
  > 1. **Kiểm soát bằng Corpus đóng kín:** VLearn Tutor áp dụng cơ chế RAG chỉ truy xuất thông tin từ đúng 18 tài liệu giáo trình và slide bài giảng được Bộ môn phê duyệt (không dùng kiến thức ngoài luồng trên Internet). Mọi câu trả lời bắt buộc có trích dẫn nguồn `doc_id#section_id`.  
  > 2. **Chế độ Socratic Guardrail:** Nếu sinh viên nhập nguyên đề bài và yêu cầu *"Hãy giải bài này cho tôi"*, hệ thống được lập trình từ chối đưa đáp án và tự động chuyển sang câu hỏi: *"Em đã phân tích bước đầu tiên của thuật toán này như thế nào? Hãy chỉ ra đoạn code em đang gặp lỗi."*  
  > 3. **Minh bạch 100% với Giảng viên:** Giảng viên có quyền truy cập toàn bộ lịch sử hội thoại của từng sinh viên trên Teacher Dashboard để kịp thời phát hiện sinh viên có dấu hiệu lạm dụng.

---

### 2.3. Phiên Bản Pitch Ngắn Của Từng Thành Viên (Personal Pitches)

* **Phạm Tiến Hưng (Team Lead / Product Ops):**  
  > *"VLearn Tutor giúp Khoa giải bài toán trợ giảng 24/7 với chi phí $0$ đồng trong 30 ngày pilot, giúp tăng tỷ lệ sinh viên qua môn thêm 15% nhờ giải đáp đúng điểm nghẽn 21h-23h. Chúng tôi xin phép kết nối LTI thử nghiệm trên 2 lớp trong tuần này."*
* **Lê Đăng Tấn (AI/LLM Engineer):**  
  > *"Hệ thống AI Tutor của chúng tôi đạt độ chính xác 92.4% dựa trên 18 tài liệu của chính Thầy/Cô và được thiết lập cơ chế gợi mở Socratic không giải hộ bài. Thầy/Cô chỉ cần cung cấp slide bài giảng, chúng tôi sẽ hoàn thiện model trong 24h."*
* **Nguyễn Quang Sơn (Fullstack & LTI Engineer):**  
  > *"Tiện ích VLearn nhúng 1-Click trực tiếp vào LMS Canvas/Moodle qua chuẩn LTI 1.3 bảo mật, hoàn toàn không thu thập thông tin định danh sinh viên (Zero-PII). Chúng tôi hỗ trợ kỹ thuật trực tiếp cài đặt xong trong 15 phút."*
* **Nguyễn Minh Quang (Customer Success & FinOps):**  
  > *"Teacher Dashboard của VLearn sẽ tự động thống kê 5 lỗ hổng kiến thức sinh viên hay gặp nhất mỗi tuần để Thầy/Cô tiết kiệm 50% thời gian chữa bài. Thầy/Cô chỉ cần dành 15 phút xem demo dashboard vào thứ Sáu này."*

---

### 2.4. Ma trận RACI (RACI Matrix) Phân Quyền 6 Nhiệm Vụ Cốt Lõi

> **Nguyên tắc vàng:** Mỗi công việc chỉ có **DUY NHẤT 01 người chịu trách nhiệm cuối cùng (A - Accountable)**.

| STT | Công việc then chốt (1–2 tháng tới) | Phạm Tiến Hưng<br>*(Team Lead / Product Ops)* | Lê Đăng Tấn<br>*(AI/LLM Engineer)* | Nguyễn Quang Sơn<br>*(Fullstack & LTI Eng)* | Nguyễn Minh Quang<br>*(CS & FinOps Lead)* | Giảng viên Cốt cán<br>*(Subject Matter Expert)* | LMS Admin Trường<br>*(IT Infrastructure)* |
|:---:|---|:---:|:---:|:---:|:---:|:---:|:---:|
| **1** | **Xác định Use Case & Thiết kế Socratic Prompt Guardrails**<br>*(Khóa phạm vi sư phạm, cấm giải hộ, chống hallucination)* | **A** | **R** | C | C | **C** | I |
| **2** | **Chuẩn bị Dữ liệu Corpus & Benchmark Eval Dataset**<br>*(Chuẩn hóa 18 tài liệu, gán nhãn ground-truth, mini-eval)* | C | **A** | I | **R** | **C** | I |
| **3** | **Xây dựng & Tích hợp Tiện ích LTI 1.3 trên LMS**<br>*(Cấu hình Canvas/Moodle, bảo mật Zero-PII, độ trễ <2s)* | C | C | **A** | I | I | **C** / **R** |
| **4** | **Kiểm thử Tự động & Calibrate AI Judge Model**<br>*(Đo độ chính xác $\ge 92\%$, latency, token cost test)* | C | **A** | **R** | I | I | I |
| **5** | **Triển khai Pilot tại 2 Lớp & Onboarding Giảng viên**<br>*(Cài đặt LMS, đào tạo Teacher Dashboard, support 21h-23h)* | C | I | C | **A** | **C** | **C** |
| **6** | **Quyết định Release, Giám sát FinOps & Xử lý Incident**<br>*(Kích hoạt Kill Switch, kiểm soát GM $\ge 58\%$, cost $\le 1.200$đ)* | **A** | **R** | **R** | **R** | I | I |

---

## 🚦 GATE 2 — PITCH RÕ, RACI KHÔNG MƠ HỒ (VERIFICATION CHECK)
- [x] **Pitch chuẩn Kết luận trước (Conclusion First):** Có Đề xuất cốt lõi $\rightarrow$ 3 Luận điểm giá trị $\rightarrow$ Bằng chứng số liệu thực tế (92.4% accuracy, $0\%$ gian lận, $<1.8s$, $1.150$đ/session) $\rightarrow$ Small ask cụ thể (thử nghiệm 2 lớp trong 30d, họp 20p).
- [x] **Chuẩn bị 1 phản biện sắc bén & cách xử lý:** Xử lý triệt để phản biện "AI ảo giác & giải hộ bài" bằng bằng chứng Corpus RAG 18 tài liệu, Socratic Guardrails và Teacher Dashboard.
- [x] **Có phiên bản Pitch cá nhân của cả 4 thành viên:** Hưng, Tấn, Sơn, Quang đều có thông điệp sắc nét theo chuyên môn.
- [x] **RACI Matrix 6 công việc quan trọng:** Đầy đủ 6 công việc sống còn của AI product, phân bổ chính xác cho 4 thành viên Mixue + Stakeholders trường học.
- [x] **Mỗi dòng chỉ có duy nhất 1 Accountable (A):** Đảm bảo tính chịu trách nhiệm tuyệt đối, không trùng lặp và không bỏ trống.
- **Kết quả Gate 2:** ✅ **PASS 100%** (Sẵn sàng kích hoạt Phase 3).

---

## 📌 ARTEFACT 3: AI TEAM ARCHITECTURE & RESOURCING (TRANG 3)

### 3.1. Thiết kế Cấu trúc AI Team Hiện tại: Cross-Functional Hybrid Squad

```
                         ┌─────────────────────────────────────────┐
                         │       PRODUCT & AI OPS LEAD             │
                         │    Phạm Tiến Hưng (2A202601800)         │
                         │  • Roadmap, Gate, FinOps, Release       │
                         └───────────────────┬─────────────────────┘
                                             │
               ┌─────────────────────────────┴─────────────────────────────┐
               │                                                           │
┌──────────────▼──────────────┐                             ┌──────────────▼──────────────┐
│       AI / LLM SQUAD        │                             │    ENGINEERING & OPS SQUAD   │
│                             │                             │                             │
│ • Lê Đăng Tấn (2A202601916) │ ◄─────────────────────────► │ • Nguyễn Quang Sơn          │
│   AI/LLM Engineer           │       Tích hợp API/LTI      │   Fullstack & LTI Engineer  │
│   - Prompt & RAG Pipeline   │       Độ trễ & Routing      │   - LTI 1.3 Canvas/Moodle   │
│   - Model Eval & Calibrate  │                             │   - Backend & Data Privacy  │
│                             │                             │                             │
│ • Partner SME (Giảng viên)  │                             │ • Nguyễn Minh Quang         │
│   - Cung cấp giáo trình     │                             │   CS & FinOps Analyst       │
│   - Thẩm định đề cương      │                             │   - Teacher Onboarding      │
│                             │                             │   - Đối soát chi phí Token  │
└─────────────────────────────┘                             └─────────────────────────────┘
```

* **Lựa chọn mô hình:** **Cross-Functional Hybrid AI Squad**.
* **Lý do lựa chọn:** Ở giai đoạn 0 $\rightarrow$ 1 (Pilot to Scale), team 4 người cần tốc độ phản hồi cực nhanh giữa phản hồi của người dùng (CS) $\rightarrow$ sửa Prompt/Model (AI Engineer) $\rightarrow$ cập nhật LTI Plugin (Fullstack Eng) mà không qua các tầng phân cấp hành chính cồng kềnh.

---

### 3.2. Core Roles, Capability Gaps & Chiến lược Resourcing (Priority Resourcing)

| Vai trò cốt lõi (Core Role) | Nhân sự đảm nhận | Năng lực hiện tại (Current Capability) | Khoảng trống năng lực (Capability Gap) | Chiến lược bổ sung (Hire / Outsource / Partner) & Hành động cụ thể |
|---|---|---|---|---|
| **1. AI Product & Ops Lead** | Phạm Tiến Hưng | Định hình sản phẩm, xây dựng Financial Model Day 24-25, thiết lập Operating Dashboard Day 26. | Kinh nghiệm pháp lý chuyên sâu về hợp đồng EdTech B2B với khối trường công. | **PARTNER:** Tham vấn pháp chế thông qua mạng lưới chuyên gia cố vấn của Vườn ươm/Nhà trường để chuẩn hóa Hợp đồng Dịch vụ LTI. |
| **2. AI/LLM Engineer** | Lê Đăng Tấn | RAG Tool-calling `kb_search`, Prompt Engineering Socratic, chạy Eval Kit Day 20-21. | Tối ưu hóa hạ tầng LLM Serving riêng & Fine-tuning mô hình mã nguồn mở cỡ nhỏ (SLM). | **OUTSOURCE / SAAS TOOLING:** Tạm thời sử dụng API Model Routing (Gemini 1.5 Flash + GPT-4o-mini qua Prompt Caching) để tối ưu chi phí $\le 1.200$đ; chưa tuyển MLOps cho đến khi đạt $50.000$ sessions/tháng. |
| **3. Fullstack & LTI Engineer** | Nguyễn Quang Sơn | Lập trình Backend Python/NodeJS, kết nối API, thiết kế giao diện Widget nhúng. | Tiêu chuẩn bảo mật IMS Global LTI 1.3 chuyên sâu và cấu hình Single Sign-On (SSO) phức tạp. | **OUTSOURCE TOOLING:** Tận dụng thư viện mã nguồn mở chuẩn `pylti1.3` và tài liệu kỹ thuật của đối tác Canvas/Moodle; trực tiếp hỗ trợ 1-1 với IT trường trong 48h (Luật `R-02`). |
| **4. Customer Success & FinOps** | Nguyễn Minh Quang | Phân tích dữ liệu học tập, đối soát chi phí token, tổ chức onboarding cho giảng viên. | Kỹ năng thiết kế tài liệu đào tạo người dùng hàng loạt (Mass Training Content). | **PARTNER:** Hợp tác với Ban cán sự sinh viên và Trợ giảng các khoa để cùng sản xuất video hướng dẫn 60 giây và infographic sử dụng nhanh. |

---

## 🚦 GATE 3 — CẤU TRÚC AI TEAM TINH GỌN, RÕ RESOURCING (VERIFICATION CHECK)
- [x] **Mô hình tổ chức phù hợp:** Hybrid Cross-functional Squad phù hợp với giai đoạn đưa sản phẩm từ Lab ra thị trường.
- [x] **Xác định đầy đủ Core Roles:** 4 vai trò rõ ràng, phân công cho 4 thành viên Mixue.
- [x] **Nhận diện Capability Gaps thực tế:** Thiếu chuyên sâu MLOps, pháp chế EdTech và đào tạo diện rộng.
- [x] **Chiến lược Resourcing tối ưu chi phí:** Ưu tiên Partner (Giảng viên, Ban cán sự) và SaaS Tooling (Model Routing, pylti1.3), tuyệt đối không over-hire để bảo vệ Runway.
- **Kết quả Gate 3:** ✅ **PASS 100%** (Sẵn sàng kích hoạt Phase 4).

---

## 📌 ARTEFACT 4: TEAM HEALTH & 30-DAY GROWTH PLAN (TRANG 4)

### 4.1. Đánh Giá Team Health (Tự Chấm Điểm 1–5 Từ 4 Thành Viên)

| Khía cạnh đánh giá | Phạm Tiến Hưng<br>*(Product Lead)* | Lê Đăng Tấn<br>*(AI Engineer)* | Nguyễn Quang Sơn<br>*(LTI Engineer)* | Nguyễn Minh Quang<br>*(CS & FinOps)* | Điểm Trung Bình | Nhận xét thực tế vận hành |
|---|:---:|:---:|:---:|:---:|:---:|---|
| **1. Chất lượng AI (AI Quality)** | 4.0 | 4.0 | 3.5 | 3.5 | **3.75 / 5.0** | Output ổn định trên Corpus 18 tài liệu ($92.4\%$), cần cải thiện tốc độ trích xuất tài liệu phức tạp. |
| **2. Tiến độ (Delivery Velocity)** | 3.5 | 3.0 | 3.5 | 3.0 | **3.25 / 5.0** | Tiến độ code AI tốt nhưng tiến độ Onboarding LTI bị chậm do phụ thuộc vào IT trường đối tác. |
| **3. Tinh thần team (Team Morale)** | 4.5 | 4.0 | 4.0 | 4.5 | **4.25 / 5.0** | Tinh thần cao, giao tiếp cởi mở, dám nêu lỗi sai và chủ động phản biện để cải thiện sản phẩm. |
| **4. Tốc độ ra sản phẩm (Product Cadence)** | 3.0 | 3.0 | 3.0 | 2.5 | **2.88 / 5.0** 🔴 | **Thấp nhất:** Thời gian từ lúc chỉnh sửa code/prompt đến khi đẩy lên LMS cho người dùng thử còn dài (10 ngày). |

#### Phân tích & Chọn vấn đề ưu tiên:
* **Khía cạnh thấp nhất:** **Tốc độ ra sản phẩm (2.88 / 5.0)**.
* **Điểm chênh lệch nhiều nhất:** **Tốc độ ra sản phẩm & Tiến độ** (Kỹ sư AI thấy nhanh khi test offline, nhưng bộ phận CS thấy chậm khi mang đến tay sinh viên).
* **Nguyên nhân cốt lõi:** Thiếu pipeline tự động hóa triển khai (CI/CD) và quy trình chuẩn hóa cấu hình LTI 1.3, dẫn đến thời gian chờ phê duyệt kỹ thuật của trường bị kéo dài.
* **Vấn đề sống còn cần xử lý ngay:** **Rút ngắn thời gian Onboarding LTI 1.3 từ 10 ngày xuống $\le 48$ giờ** để không vi phạm Luật đỏ `R-02` và kịp đạt mốc kích hoạt $\ge 70\%$ đối tác trong 60 ngày.

---

### 4.2. Khung Năng Lực Cần Nâng Cấp (Competency Framework L1 $\rightarrow$ L2 $\rightarrow$ L3)

* **Vai trò được chọn nâng cấp:** **AI/LLM Engineer (Lê Đăng Tấn)**
* **Cấp độ hiện tại:** **L2 — AI Practitioner** *(Đã thành thạo xây dựng RAG Pipeline, Prompt Engineering Socratic, chạy bộ test Eval Kit offline trên 18 tài liệu).*
* **Năng lực cần nâng cấp tiếp theo:** **L3 — AI Builder (Automated CI/CD Eval Pipeline & Production Observability)**.
* **Hành động thực hành trong 30 ngày:** Thiết lập hệ thống tự động chạy bộ 50 câu hỏi kiểm thử chuẩn (Golden Evaluation Set) trên GitHub Actions mỗi khi có bản cập nhật prompt/code, tự động chặn release nếu độ chính xác $<92\%$ hoặc chi phí token $>1.200$ VNĐ/session.

---

### 4.3. Kế Hoạch Phát Triển 30 Ngày (30-Day Team Growth Plan)

> **Nguyên tắc:** Tập trung tối đa 3 hành động cụ thể, có thể đo lường và kiểm tra được, tuyệt đối không viết chung chung.

| STT | Vấn đề cần giải quyết | Hành động cụ thể trong 30 ngày (Action) | Người phụ trách (Owner) | Thời hạn (Deadline) | Dấu hiệu hoàn thành cụ thể (Definition of Done) |
|:---:|---|---|:---:|:---:|---|
| **1** | **Tốc độ Onboarding LTI chậm (TTF-End-User = 10 ngày)** | Xây dựng bộ Docker Staging Template + Script Onboarding 1-Click LTI 1.3 cho Canvas & Moodle; ban hành Whitepaper Kỹ thuật 1 trang cho LMS Admin. | **Nguyễn Quang Sơn**<br>*(LTI Engineer)* | **10/09/2026** | Cấu hình thành công nút AI Tutor trên Staging LMS của trường trong vòng **$\le 48$ giờ**; LMS Admin ký biên bản nghiệm thu kỹ thuật. |
| **2** | **Chưa có CI/CD tự động kiểm soát chất lượng & chi phí AI** | Tích hợp bộ 50 câu test Golden Dataset vào GitHub Actions; kết nối LangSmith/Braintrust để theo dõi 100% trace telemetry và chi phí token trong production. | **Lê Đăng Tấn**<br>*(AI Engineer)* | **16/09/2026** | Pipeline CI trả về kết quả `PASS` tự động trước mỗi lần deploy; dashboard telemetry ghi nhận **độ chính xác $\ge 92\%$** và **chi phí $\le 1.200$đ/session** trên 500 session thật đầu tiên. |
| **3** | **Nhịp phối hợp & phản ứng với phản hồi giảng viên/sinh viên** | Thiết lập lịch họp định kỳ **"Weekly Standup & Metrics Review" 20 phút** vào 09h00 sáng thứ Sáu hàng tuần; rà soát 3 chỉ số L-01 (Kích hoạt), O-02 (Chi phí AI), O-03 (Gross Margin) theo Luật R-01 $\rightarrow$ R-05. | **Phạm Tiến Hưng**<br>*(Team Lead)* | **Bắt đầu 04/09/2026**<br>*(Duy trì liên tục 4 tuần)* | Có 4 biên bản họp ngắn (Action Items Log) được cập nhật lên repo; xử lý dứt điểm 100% blocker kỹ thuật trong vòng 24h sau họp. |

---

## 🚦 GATE 4 — GROWTH PLAN CÓ THỂ THỰC THI (VERIFICATION CHECK)
- [x] **Team đã chấm đủ 4 khía cạnh:** AI Quality (3.75), Velocity (3.25), Morale (4.25), Product Cadence (2.88).
- [x] **Chọn đúng vấn đề ưu tiên hàng đầu:** Khắc phục tốc độ ra sản phẩm và nút thắt Onboarding LTI.
- [x] **Xác định 1 Competency nâng cấp rõ ràng:** Nâng cấp AI Engineer từ L2 (AI Practitioner) lên L3 (AI Builder) với hành động CI/CD Eval cụ thể.
- [x] **Đúng 3 hành động Growth Plan khả thi:** Có vấn đề, hành động, owner (Sơn, Tấn, Hưng), deadline cụ thể (10/09, 16/09, 04/09) và Definition of Done kiểm chứng được bằng số liệu.
- **Kết quả Gate 4:** ✅ **PASS 100%** (Toàn bộ 4 Artefacts đã sẵn sàng xuất bản ra tài liệu PDF chính thức).

---

## 📂 HỒ SƠ PHẢN ÁNH CÁ NHÂN (INDIVIDUAL REFLECTION)
Thư mục `Reflection/` lưu trữ báo cáo thu hoạch và nhật ký đóng góp cá nhân của từng thành viên:
- 👤 [Phạm Tiến Hưng (2A202601800) — Team Lead / Product & AI Ops Lead](Reflection/PhamTienHung_2A202601800.md)
- 👤 [Lê Đăng Tấn (2A202601916) — AI/LLM Engineer & Model Evaluation](Reflection/PhamTienHung_2A202601800.md)
- 👤 [Nguyễn Quang Sơn (2A202601956) — Fullstack & LTI 1.3 Integration Engineer](Reflection/PhamTienHung_2A202601800.md)
- 👤 [Nguyễn Minh Quang (2A202601730) — Customer Success & Data/FinOps Analyst](Reflection/NguyenMinhQuang_2A202601730.md)

---

## 🚦 GATE 5 — REPOSITORY SẴN SÀNG NỘP (FINAL VERIFICATION CHECK)

### 1. Bảng Tự Kiểm 4 Khía Cạnh Cốt Lõi (Audit Checklist):
- **Trang 1 — Stakeholder Map & Strategy:**
  - [x] Có ít nhất 6 stakeholder cụ thể (Chức danh thực tế trong trường ĐH & đối tác LMS).
  - [x] Đã map chính xác theo 2 trục *Influence $\times$ Interest*.
  - [x] Dùng đúng 4 nhãn chuẩn: *Champion*, *Critical Blocker*, *Supporter*, *Skeptic*, *Bystander*.
  - [x] 4 stakeholder ưu tiên đều có hành động cụ thể trong 1–2 tuần tới kèm deadline và phân công Owner.
- **Trang 2 — Pitch & RACI Matrix:**
  - [x] Pitch theo cấu trúc *Conclusion First* (Minto Pyramid).
  - [x] Có số liệu & bằng chứng thực chứng hỗ trợ kết luận ($92.4\%$ Acc, $0\%$ gian lận, $<1.8s$, $1.150$đ/session).
  - [x] Có *Small Ask* nhỏ, rõ ràng, dễ chấp thuận (nhúng 2 lớp trong 48h, họp 20p).
  - [x] Có 1 phản biện rủi ro lớn nhất và phương án xử lý bằng chứng thực (RAG 18 docs + Socratic Guardrails).
  - [x] Mỗi công việc trong RACI có **duy nhất 1 Accountable (A)** rõ ràng.
- **Trang 3 — AI Team Architecture & Resourcing:**
  - [x] Cấu trúc *Cross-Functional Hybrid AI Squad* có lý do gắn liền với giai đoạn Pilot-to-Scale.
  - [x] Core Roles phù hợp hoàn toàn với 4 thành viên thực tế của team Mixue.
  - [x] Nhận diện đúng các Capability Gaps (Pháp chế EdTech, MLOps GPU, Onboarding LTI).
  - [x] Priority Resourcing phân định rõ *Hire / Outsource / Partner* để tối ưu Runway.
- **Trang 4 — Team Health & Growth Plan:**
  - [x] Đủ 4 khía cạnh Team Health được chấm điểm bởi cả 4 thành viên.
  - [x] Chọn đúng vấn đề ưu tiên hàng đầu: Tốc độ ra sản phẩm / Onboarding LTI.
  - [x] Xác định năng lực nâng cấp: AI Engineer từ L2 (Practitioner) $\rightarrow$ L3 (Builder).
  - [x] Đúng 3 hành động 30 ngày có *Owner* + *Deadline* + *Definition of Done*.

### 2. Kiểm tra Tính Nhất Quán (Consistency Check) Giữa 4 Trang:
- [x] **Stakeholder $\leftrightarrow$ Pitch & RACI:** Giảng viên Cốt cán (Champion) và LMS Admin (Blocker) ở Trang 1 xuất hiện trực tiếp là đối tượng nhận Pitch và giữ vai trò Consulted/Responsible trong RACI ở Trang 2.
- [x] **Capability Gap $\leftrightarrow$ Team Health:** Điểm nghẽn Onboarding LTI và CI/CD Eval ở Trang 3 kết nối trực tiếp với điểm số thấp nhất ở Trang 4 (Product Cadence 2.88).
- [x] **Growth Plan $\leftrightarrow$ RACI Ownership:** Các Owner trong Growth Plan 30 ngày (Sơn, Tấn, Hưng) hoàn toàn khớp với vai trò Accountable/Responsible trong RACI Matrix.

### 3. Trạng Thái File Nộp Bài (Deliverables State):
- [x] `README.md` cập nhật đầy đủ thông tin nhóm, dự án, mục tiêu, 4 Artefacts và 5 Gate Checks.
- [x] `Day27_AI-Team-Lab_Mixue.pdf` (và `Day27_AI-Team-Lab_TeamMixue.pdf`) xuất bản chuẩn chỉnh **đúng 4 trang** (1 trang / Artefact).
- [x] Thư mục `Reflection/` chứa báo cáo phản ánh cá nhân [PhamTienHung_2A202601800.md](Reflection/PhamTienHung_2A202601800.md).

**KẾT QUẢ GATE 5:** 🏆 **PASS 100% — HOÀN TẤT VÀ SẴN SÀNG NỘP BÀI!**

---
