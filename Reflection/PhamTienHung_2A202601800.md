# Báo Cáo Thu Hoạch Cá Nhân (Individual Reflection) — Day 27: AI Team Lab

- **Học viên:** Phạm Tiến Hưng
- **Mã học viên (MHV):** 2A202601800
- **Nhóm:** Mixue (Track 1)
- **Dự án:** VLearn AI Tutor
- **Vai trò đảm nhiệm:** Team Lead / Product & AI Ops Lead (Người tổng hợp bài & Quản lý Repository)
- **Ngày thực hiện:** 29/08/2026

---

## 🎯 1. TỔNG QUAN VAI TRÒ & NHIỆM VỤ ĐÃ THỰC HIỆN TRONG LAB HÔM NAY

Trong buổi Lab Day 27, với vai trò là **Trưởng nhóm kiêm Product & AI Ops Lead**, tôi đã dẫn dắt team **Mixue** (gồm 4 thành viên: Phạm Tiến Hưng, Lê Đăng Tấn, Nguyễn Quang Sơn, Nguyễn Minh Quang) hoàn thành trọn vẹn chuỗi quyết định quản trị đội ngũ AI cho dự án **VLearn AI Tutor** và vượt qua 100% 5 Quality Gates.

### 📌 Các nhiệm vụ cụ thể tôi đã trực tiếp chủ trì và thực hiện:

#### 1. Khởi tạo & Điều phối Dự án (Gate 0 - Scope Alignment)
- Khởi tạo và cấu trúc chuẩn hóa GitHub Repository cho cả nhóm.
- Thống nhất mục tiêu 1–3 tháng của team: Đưa VLearn AI Tutor đến sinh viên/giảng viên qua LTI 1.3 LMS, nâng Partner Activation Rate $\ge 70\%$, kiểm soát chi phí token $\le 1.200$ VNĐ/session với độ chính xác sư phạm $\ge 92\%$.
- Thiết lập quy trình làm việc theo Quality Gates (chỉ chuyển phase khi đạt chuẩn tự kiểm).

#### 2. Xây dựng Stakeholder Map & Chiến lược tương tác (Phase 1 / Gate 1)
- Nhận diện và định vị 6 nhóm chức danh bên liên quan cốt lõi trong hệ sinh thái trường đại học trên ma trận $2 \times 2$ (*Influence $\times$ Interest*).
- Trực tiếp xây dựng chiến lược và kế hoạch hành động 1–2 tuần tới đối với **Ban Giám Hiệu / Ban Đào Tạo Trường ĐH** (*Skeptic / Potential Blocker*): Soạn thảo Executive Summary 2 trang chứng minh hiệu quả sư phạm (Acc $\ge 92\%$) và cơ chế Socratic Guardrails chống giải hộ để xin phê duyệt cơ chế triển khai thử nghiệm Sandbox trước thứ Sáu tuần 1.

#### 3. Soạn thảo Pitch "Kết Luận Trước" & Thiết lập RACI Matrix (Phase 2 / Gate 2)
- Trực tiếp xây dựng cấu trúc Executive Pitch gửi tới Hội đồng Thẩm định & Giảng viên theo nguyên lý Kim tự tháp Minto (*Conclusion First $\rightarrow$ 3 Luận điểm $\rightarrow$ Bằng chứng số liệu Day 20-26 $\rightarrow$ Small Ask cụ thể*).
- Xây dựng bản Pitch cá nhân dưới góc độ Product Ops: *"VLearn Tutor giúp Khoa giải bài toán trợ giảng 24/7 với chi phí 0 đồng trong 30 ngày pilot, giúp tăng tỷ lệ sinh viên qua môn thêm 15% nhờ giải đáp đúng điểm nghẽn 21h-23h."*
- Chủ trì phân bổ **Ma trận RACI 6 công việc cốt lõi**, đảm bảo nguyên tắc bất biến: **Mỗi dòng chỉ có duy nhất 1 Accountable (A)**. Trực tiếp nhận trách nhiệm **Accountable (A)** cho:
  - *(1) Xác định Use Case & Thiết kế Socratic Prompt Guardrails.*
  - *(6) Quyết định Release, Giám sát FinOps & Xử lý Incident (Kill Switch).*

#### 4. Thiết kế Cấu trúc AI Team & Chiến lược Resourcing (Phase 3 / Gate 3)
- Lựa chọn mô hình **Cross-Functional Hybrid AI Squad** phù hợp với giai đoạn 0 $\rightarrow$ 1 (Pilot to Scale) giúp loại bỏ độ trễ bàn giao giữa AI, Engineering và Business.
- Phân định rõ 4 Core Roles cho 4 thành viên trong nhóm.
- Nhận diện khoảng trống năng lực cá nhân về *Pháp lý hợp đồng EdTech B2B với trường đại học công lập*, đề xuất chiến lược **PARTNER** tham vấn mạng lưới cố vấn pháp chế của Vườn ươm để chuẩn hóa Hợp đồng Dịch vụ LTI mà không làm phát sinh chi phí cố định.

#### 5. Đánh giá Team Health & Xây dựng Growth Plan 30 ngày (Phase 4 / Gate 4)
- Tham gia tự chấm điểm Team Health 4 khía cạnh: Chất lượng AI (4.0), Tiến độ (3.5), Tinh thần (4.5), Tốc độ ra sản phẩm (3.0).
- Cùng team phân tích nguyên nhân gốc rễ khiến Tốc độ ra sản phẩm thấp nhất ($2.88/5$) do thời gian Onboarding LTI bị nghẽn ở khâu thẩm định IT trường.
- Đảm nhận làm **Owner cho Hành động số 3 trong Growth Plan 30 ngày**: Thiết lập và chủ trì lịch họp định kỳ *"Weekly Standup & Metrics Review" 20 phút* vào 09h00 sáng thứ Sáu hàng tuần (từ 04/09/2026), rà soát 3 chỉ số L-01, O-02, O-03 và 5 Luật vận hành `R-01` $\rightarrow$ `R-05`.

#### 6. Tổng hợp Sản phẩm Đầu ra & Xuất bản Tài liệu (Final Deliverables)
- Tổng hợp, biên tập và hoàn thiện toàn bộ nội dung trong file [README.md](file:///e:/Classroom/Code/Codelabs/Track1-Day27-Mixue-VlearnTutor/README.md).
- Lập trình và kiểm thử script [export_pdf.py](file:///e:/Classroom/Code/Codelabs/Track1-Day27-Mixue-VlearnTutor/export_pdf.py) xuất bản thành công tài liệu [Day27_AI-Team-Lab_TeamMixue.pdf](file:///e:/Classroom/Code/Codelabs/Track1-Day27-Mixue-VlearnTutor/Day27_AI-Team-Lab_TeamMixue.pdf) đúng chuẩn **tối đa 4 trang** (mỗi trang trình bày 1 Artefact chuyên nghiệp, trực quan).

---

## 💡 2. BÀI HỌC KINH NGHIỆM & THU HOẠCH CÁ NHÂN (KEY TAKEAWAYS)

1. **Tư duy Quản trị AI khác biệt với Phần mềm truyền thống:** 
   - Quản trị AI không chỉ là quản lý tiến độ viết code, mà là quản trị **độ bất định (uncertainty)** về chất lượng mô hình, chi phí token biến đổi (FinOps) và rủi ro đạo đức/sư phạm (Responsible AI Guardrails).
2. **Sức mạnh của Cấu trúc "Kết Luận Trước" (Conclusion First):** 
   - Khi làm việc với các bên liên quan cấp cao (Ban Giám Hiệu, Trưởng Khoa), việc đi thẳng vào đề xuất giá trị và số liệu thực chứng (`92.4% accuracy`, `0% gian lận`, `1.150đ/session`) tạo ra sức thuyết phục vượt trội so với việc giải thích kỹ thuật RAG phức tạp.
3. **Tính rõ ràng trong Phân quyền (Single Accountability in RACI):**
   - Bài học lớn nhất là triệt tiêu tâm lý "ai cũng tưởng người khác làm". Việc gán đúng 1 người chịu trách nhiệm cuối cùng (A) cho mỗi đầu việc giúp cả team phản ứng tức thì khi có sự cố kỹ thuật hoặc chi phí API vượt trần.
4. **Tối ưu hóa nguồn lực cho Startup AI giai đoạn đầu:**
   - Thay vì vội vã tuyển dụng (Hire) tốn kém gây rủi ro cho Runway, chiến lược linh hoạt kết hợp giữa **Partner** (Giảng viên làm cố vấn sư phạm) và **SaaS Tooling** (LangSmith, Model Routing) là chìa khóa sống còn để dự án đi nhanh và bền vững.

---

## 📈 3. CAM KẾT HÀNH ĐỘNG CÁ NHÂN TRONG 30 NGÀY TỚI
- [ ] Chủ trì đúng giờ và nghiêm túc 4 buổi họp Weekly Standup vào các ngày 04/09, 11/09, 18/09 và 25/09/2026.
- [ ] Hoàn thành bản Executive Summary và gửi tới Văn phòng Ban Giám Hiệu trước ngày 04/09/2026.
- [ ] Giám sát chặt chẽ các chỉ số kinh tế trên Operating Dashboard để duy trì Gross Margin $\ge 58\%$ và chi phí AI $\le 1.200$ VNĐ/session.

---
*Xác nhận của học viên: Phạm Tiến Hưng (2A202601800)*
