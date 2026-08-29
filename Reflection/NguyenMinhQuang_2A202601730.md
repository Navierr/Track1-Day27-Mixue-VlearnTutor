# Báo Cáo Thu Hoạch Cá Nhân (Individual Reflection) — Day 27: AI Team Lab

- **Học viên:** Nguyễn Minh Quang
- **Mã học viên (MHV):** 2A202601730
- **Nhóm:** Mixue (Track 1)
- **Dự án:** VLearn AI Tutor
- **Vai trò đảm nhiệm:** Customer Success & Data/FinOps Analyst
- **Ngày thực hiện:** 29/08/2026

---

## 🎯 1. TỔNG QUAN VAI TRÒ & NHIỆM VỤ ĐÃ THỰC HIỆN TRONG LAB HÔM NAY

Trong buổi Lab Day 27, với vai trò **Customer Success & Data/FinOps Analyst**, tôi tập trung vào hai trục chính: (1) đảm bảo trải nghiệm của người dùng cuối (giảng viên, sinh viên) được chuyển hóa thành hành động cụ thể, và (2) giám sát các chỉ số chi phí/vận hành để dự án không "chạy nhanh nhưng lỗ vốn". Cùng team Mixue (Phạm Tiến Hưng, Lê Đăng Tấn, Nguyễn Quang Sơn), tôi đã đóng góp trực tiếp vào cả 4 Artefacts và giúp team vượt qua 100% 5 Quality Gates.

### 📌 Các nhiệm vụ cụ thể tôi đã trực tiếp chủ trì và thực hiện:

#### 1. Đóng góp mục tiêu FinOps cho Gate 0 (Scope Alignment)
- Cùng team chốt chỉ tiêu **Trách nhiệm AI & Kiểm soát chi phí**: duy trì chi phí token/embedding $\le 1.200$ VNĐ/session, Gross Margin sau 25% Rev-Share $\ge 58\%$ (Luật `R-04`, `R-05`) — đây là chỉ tiêu tôi trực tiếp chịu trách nhiệm theo dõi trong vận hành.

#### 2. Làm Owner hành động cho Stakeholder ưu tiên số 1 (Phase 1 / Gate 1)
- Trực tiếp phụ trách kế hoạch hành động 1–2 tuần tới với **Giảng viên Cốt cán / Chủ nhiệm Bộ môn** (*Champion, Influence 5/5, Interest 5/5*) — stakeholder có ảnh hưởng và mức độ quan tâm cao nhất trong ma trận:
  > *Bàn giao tài khoản Teacher Analytics Dashboard trước thứ Sáu 04/09/2026, hỗ trợ cấu hình nhúng AI Tutor vào 2 lớp thử nghiệm (120 sinh viên), và tổ chức họp 20 phút vào sáng thứ Ba tuần kế tiếp để đối soát độ chính xác câu trả lời theo rubric Day 20-21.*
- Đây là lần đầu tôi nhận ra vai trò Customer Success không chỉ "hỗ trợ sau khi launch" mà phải **chủ động thiết kế điểm chạm đầu tiên** với người dùng quan trọng nhất.

#### 3. Xây dựng Pitch cá nhân & tham gia RACI Matrix (Phase 2 / Gate 2)
- Soạn bản pitch cá nhân theo góc nhìn Customer Success, nhấn mạnh giá trị dữ liệu cho giảng viên:
  > *"Teacher Dashboard của VLearn sẽ tự động thống kê 5 lỗ hổng kiến thức sinh viên hay gặp nhất mỗi tuần để Thầy/Cô tiết kiệm 50% thời gian chữa bài. Thầy/Cô chỉ cần dành 15 phút xem demo dashboard vào thứ Sáu này."*
- Trong Ma trận RACI 6 công việc cốt lõi, tôi nhận:
  - **Accountable (A)** cho việc **(5) Triển khai Pilot tại 2 Lớp & Onboarding Giảng viên** — chịu trách nhiệm cuối cùng cho việc cài đặt LMS, đào tạo Teacher Dashboard và hỗ trợ khung giờ cao điểm 21h–23h.
  - **Responsible (R)** cho việc **(2) Chuẩn bị Dữ liệu Corpus & Benchmark Eval Dataset** (hỗ trợ Lê Đăng Tấn chuẩn hóa 18 tài liệu, gán nhãn ground-truth) và **(6) Giám sát FinOps & Xử lý Incident** (theo dõi Gross Margin $\ge 58\%$, chi phí $\le 1.200$đ/session, sẵn sàng đề xuất Kill Switch khi vượt trần).

#### 4. Nhận diện Capability Gap & chiến lược Resourcing (Phase 3 / Gate 3)
- Tự đánh giá năng lực hiện tại: phân tích dữ liệu học tập, đối soát chi phí token, tổ chức onboarding cho giảng viên.
- Nhận diện khoảng trống lớn nhất của bản thân: **thiết kế tài liệu đào tạo người dùng hàng loạt (Mass Training Content)** — hiện tại tôi quen hỗ trợ 1-1 nhưng chưa có quy trình chuẩn để scale khi số trường đối tác tăng.
- Đề xuất chiến lược **PARTNER**: hợp tác với Ban cán sự sinh viên và Trợ giảng các khoa để cùng sản xuất video hướng dẫn 60 giây và infographic sử dụng nhanh, thay vì tự làm thủ công từng trường.

#### 5. Tham gia chấm điểm Team Health & xác định vấn đề ưu tiên (Phase 4 / Gate 4)
- Tự chấm điểm 4 khía cạnh Team Health dưới góc nhìn Customer Success & FinOps: Chất lượng AI (3.5), Tiến độ (3.0), Tinh thần team (4.5), **Tốc độ ra sản phẩm (2.5) — điểm tôi chấm thấp nhất trong cả 4 thành viên**.
- Lý do tôi chấm thấp nhất ở Product Cadence: tôi là người trực tiếp tiếp xúc sinh viên/giảng viên nên cảm nhận rõ nhất độ trễ **10 ngày** từ lúc code/prompt sửa xong đến khi thực sự đến tay người dùng — khoảng cách giữa "xong ở máy AI Engineer" và "xong ở tay End-User" chính là gap tôi phải cảnh báo cho team.
- Góp ý xác định nguyên nhân gốc rễ: thiếu pipeline CI/CD và quy trình chuẩn hóa LTI 1.3 khiến thời gian chờ phê duyệt kỹ thuật của trường kéo dài, ảnh hưởng trực tiếp đến trải nghiệm Customer Success.

#### 6. Đóng góp dữ liệu FinOps cho Sản phẩm Đầu ra (Final Deliverables)
- Cung cấp số liệu chi phí vận hành (~1.150 VNĐ/session, thấp hơn trần 1.200đ) và cơ sở tính Gross Margin để đưa vào phần bằng chứng (Hard Evidence) của bản Pitch trong [README.md](../README.md).

---

## 💡 2. BÀI HỌC KINH NGHIỆM & THU HOẠCH CÁ NHÂN (KEY TAKEAWAYS)

1. **Customer Success trong sản phẩm AI = "phiên dịch" dữ liệu thành hành động, không chỉ là hỗ trợ:**
   - Teacher Analytics Dashboard chỉ có giá trị khi nó giúp giảng viên tiết kiệm thời gian thật (50% thời gian chữa bài), chứ không phải chỉ là bảng số liệu đẹp. Bài học là mọi tính năng CS đưa ra phải gắn với một "small ask" hoặc lợi ích đo lường được.
2. **FinOps là trách nhiệm chung, không phải việc riêng của kỹ sư AI:**
   - Trước lab, tôi nghĩ chi phí token là việc của AI Engineer. Sau khi làm RACI, tôi nhận ra Customer Success là người *cảm nhận sớm nhất* khi chi phí tăng (qua volume session thực tế), nên phải là người đồng sở hữu (Responsible) chỉ số Gross Margin và có quyền đề xuất Kill Switch.
3. **Khoảng cách giữa "Velocity nội bộ" và "Cadence thực tế đến người dùng" là rủi ro dễ bị bỏ qua:**
   - Kỹ sư AI thấy tiến độ nhanh vì test offline nhanh, nhưng người dùng (giảng viên/sinh viên) chỉ thấy chậm vì họ chờ 10 ngày mới được dùng thật. Việc chấm điểm Team Health độc lập theo từng vai trò giúp lộ ra bất đồng này thay vì để nó âm thầm tích tụ.
4. **Đào tạo diện rộng cần "sản phẩm hóa" thay vì làm thủ công từng trường hợp:**
   - Nếu tiếp tục hỗ trợ 1-1 như hiện tại, tôi sẽ không thể scale khi Partner Activation Rate tăng lên $\ge 70\%$ số trường. Video 60 giây + infographic là hướng đi bắt buộc để không trở thành nút thắt cổ chai của chính team.

---

## 📈 3. CAM KẾT HÀNH ĐỘNG CÁ NHÂN TRONG 30 NGÀY TỚI

- [ ] Hoàn tất bàn giao tài khoản Teacher Analytics Dashboard cho Giảng viên Cốt cán và cấu hình xong AI Tutor trên 2 lớp thử nghiệm (120 sinh viên) trước **04/09/2026**.
- [ ] Tổ chức buổi hướng dẫn trực tuyến 30 phút cho Ban cán sự lớp vào tối **06/09/2026** (Chủ Nhật tuần 1) và thu thập đủ **100 lượt đánh giá mini-eval** đầu tiên từ sinh viên.
- [ ] Phối hợp Ban cán sự sinh viên/Trợ giảng sản xuất bộ video hướng dẫn 60 giây + infographic onboarding trước cuối tháng 9/2026 để chuẩn bị nhân rộng sang các trường đối tác tiếp theo.
- [ ] Theo dõi hàng tuần chi phí token/session và Gross Margin trên Operating Dashboard, báo cáo tại buổi "Weekly Standup & Metrics Review" (từ 04/09/2026), đảm bảo duy trì $\le 1.200$ VNĐ/session và Gross Margin $\ge 58\%$; chủ động cảnh báo team nếu có dấu hiệu vượt trần.

---
*Xác nhận của học viên: Nguyễn Minh Quang (2A202601730)*
