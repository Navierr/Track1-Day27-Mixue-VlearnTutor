# Báo Cáo Thu Hoạch Cá Nhân (Individual Reflection) — Day 27: AI Team Lab

- **Học viên:** Nguyễn Quang Sơn
- **Mã học viên (MHV):** 2A202601956
- **Nhóm:** Mixue (Track 1)
- **Dự án:** VLearn AI Tutor
- **Vai trò đảm nhiệm:** Fullstack & LTI 1.3 Integration Engineer
- **Ngày thực hiện:** 29/08/2026

---

## 🎯 1. TỔNG QUAN VAI TRÒ & NHIỆM VỤ ĐÃ THỰC HIỆN TRONG LAB HÔM NAY

Trong buổi Lab Day 27, với vai trò là **Fullstack & LTI 1.3 Integration Engineer** của team **Mixue**, tôi đã tham gia đầy đủ chuỗi quyết định quản trị đội ngũ AI cho dự án **VLearn AI Tutor** và cùng team vượt qua 100% 5 Quality Gates, đồng thời trực tiếp đảm nhận các nhiệm vụ gắn với mảng kỹ thuật tích hợp LMS.

### 📌 Các nhiệm vụ cụ thể tôi đã trực tiếp thực hiện:

#### 1. Tham gia Định hướng Dự án (Gate 0 - Scope Alignment)
- Cùng team thống nhất mục tiêu 1–3 tháng: đưa VLearn AI Tutor vào vận hành thực tế qua LTI 1.3 trên Canvas/Moodle, rút ngắn `TTF-End-User` (thời gian từ khi cấp quyền đến sinh viên đầu tiên sử dụng) xuống $\le 7$ ngày theo Luật `R-02`.
- Đóng góp góc nhìn kỹ thuật khi team chốt phạm vi: độ trễ phản hồi AI trong widget nhúng phải $< 2s$ và cam kết **Zero-PII retention** — hai ràng buộc sống còn để LMS Admin của trường chấp thuận tích hợp.

#### 2. Đóng góp vào Stakeholder Map (Phase 1 / Gate 1)
- Cung cấp dữ liệu thực tế về **Quản trị viên LMS / Trưởng phòng CNTT Trường** (*Critical Blocker Kỹ thuật — Influence 5/5, Interest 1/5*): rủi ro thực tế nhất là trì hoãn cấp LTI 1.3 Client ID/Deployment ID, kéo dài thẩm định kỹ thuật khiến `TTF-End-User` vượt 14 ngày.
- Nhận quyền **Owner cho hành động de-risk stakeholder này trong 1–2 tuần tới**: gửi Whitepaper "Bảo mật LTI 1.3 & Cam kết Không lưu trữ PII" trước 17h thứ Ba tuần 1, và hẹn lịch hỗ trợ kỹ thuật 1-1 trong 30 phút vào thứ Năm để cấu hình nhúng nút AI hoàn tất trên Staging LMS của trường trong 48h.

#### 3. Đóng góp vào Pitch & RACI Matrix (Phase 2 / Gate 2)
- Soạn pitch cá nhân dưới góc độ kỹ sư tích hợp: *"Tiện ích VLearn nhúng 1-Click trực tiếp vào LMS Canvas/Moodle qua chuẩn LTI 1.3 bảo mật, hoàn toàn không thu thập thông tin định danh sinh viên (Zero-PII). Chúng tôi hỗ trợ kỹ thuật trực tiếp cài đặt xong trong 15 phút."*
- Tham gia chốt **Ma trận RACI 6 công việc cốt lõi** với nguyên tắc mỗi dòng chỉ có duy nhất 1 Accountable. Nhận trách nhiệm:
  - **Accountable (A)** cho *(3) Xây dựng & Tích hợp Tiện ích LTI 1.3 trên LMS* (cấu hình Canvas/Moodle, bảo mật Zero-PII, độ trễ $< 2s$).
  - **Responsible (R)** cho *(4) Kiểm thử Tự động & Calibrate AI Judge Model* và *(6) Quyết định Release, Giám sát FinOps & Xử lý Incident*.
- Đóng góp vào phần xử lý phản biện "AI ảo giác & giải hộ bài": phương án minh bạch 100% với giảng viên qua Teacher Dashboard và cơ chế nhận diện trường hợp sinh viên nhập nguyên đề xin giải hộ.

#### 4. Tham gia Thiết kế Cấu trúc AI Team (Phase 3 / Gate 3)
- Cùng team lựa chọn mô hình **Cross-Functional Hybrid AI Squad** phù hợp giai đoạn Pilot-to-Scale.
- Trung thực khai báo khoảng trống năng lực cá nhân: **tiêu chuẩn bảo mật IMS Global LTI 1.3 chuyên sâu và cấu hình Single Sign-On (SSO) phức tạp**.
- Đề xuất và được team chấp thuận chiến lược **OUTSOURCE TOOLING**: tận dụng thư viện mã nguồn mở chuẩn `pylti1.3` và tài liệu kỹ thuật của Canvas/Moodle thay vì tự xây từ đầu hoặc tuyển nhân sự chuyên sâu — bảo vệ Runway của dự án.

#### 5. Đánh giá Team Health & Cam kết Growth Plan (Phase 4 / Gate 4)
- Tham gia tự chấm điểm Team Health 4 khía cạnh: Chất lượng AI (3.5), Tiến độ (3.5), Tinh thần (4.0), Tốc độ ra sản phẩm (3.0).
- Cùng team xác định nguyên nhân gốc rễ của điểm thấp nhất (Product Cadence 2.88): thiếu pipeline tự động hóa triển khai (CI/CD) và quy trình chuẩn hóa cấu hình LTI 1.3 khiến thời gian chờ phê duyệt kỹ thuật của trường kéo dài đến 10 ngày.
- **Nhận làm Owner cho Hành động số 1 — ưu tiên số một của Growth Plan 30 ngày** (deadline **10/09/2026**): xây dựng bộ Docker Staging Template + Script Onboarding 1-Click LTI 1.3 cho Canvas & Moodle, ban hành Whitepaper Kỹ thuật 1 trang cho LMS Admin. Definition of Done: cấu hình thành công nút AI Tutor trên Staging LMS của trường trong vòng $\le 48$ giờ và LMS Admin ký biên bản nghiệm thu kỹ thuật.

#### 6. Hỗ trợ Tổng hợp Deliverables
- Rà soát phần nội dung kỹ thuật LTI 1.3 (Zero-PII, độ trễ, quy trình cài đặt) trong README.md và tài liệu PDF 4 trang trước khi team xuất bản.

---

## 💡 2. BÀI HỌC KINH NGHIỆM & THU HOẠCH CÁ NHÂN (KEY TAKEAWAYS)

1. **Blocker lớn nhất thường không phải code mà là con người:** Nút thắt thật sự của dự án không nằm ở việc viết plugin LTI, mà ở khâu thuyết phục và thẩm định của LMS Admin — người có Influence 5/5 nhưng Interest chỉ 1/5. Bài học: với stakeholder kiểu này, tài liệu chuẩn hóa ngắn gọn + hỗ trợ trực tiếp 1-1 hiệu quả hơn nhiều so với gửi yêu cầu rồi chờ.
2. **Chuẩn mở (pylti1.3) > Tự xây từ đầu:** Ở giai đoạn startup, tôi nhận ra rằng cố gắng tự triển khai toàn bộ đặc tả LTI 1.3 (OIDC login, JWKS, deep linking) là một rủi ro tiến độ không cần thiết. Dùng thư viện chuẩn IMS giúp giảm thời gian tích hợp và tăng độ tin cậy bảo mật khi được trường thẩm định.
3. **Zero-PII là lợi thế đàm phán, không chỉ là nghĩa vụ:** Việc thiết kế hệ thống không lưu trữ thông tin định danh sinh viên từ đầu giúp chuyển cuộc đàm phán bảo mật từ "xin phép thu thập dữ liệu" sang "cam kết không thu thập" — mức độ tín nhiệm hoàn toàn khác khi đối mặt với Trưởng phòng CNTT.
4. **RACI giúp kỹ sư tập trung đúng chỗ:** Khi biết rõ mình chỉ Accountable cho duy nhất mục (3) nhưng Responsible ở 2 mục khác, tôi dễ dàng ưu tiên thời gian cho việc tích hợp LTI thay vì bị kéo vào quá nhiều mảng cùng lúc.

---

## 📈 3. CAM KẾT HÀNH ĐỘNG CÁ NHÂN TRONG 30 NGÀY TỚI
- [ ] Hoàn thành Docker Staging Template + Script Onboarding 1-Click LTI 1.3 cho Canvas & Moodle trước ngày **10/09/2026**.
- [ ] Gửi Whitepaper "Bảo mật LTI 1.3 & Cam kết Không lưu trữ PII" cho LMS Admin của trường đối tác trước 17h thứ Ba tuần 1 (01/09/2026), và hoàn thành buổi cấu hình Staging trong $\le 48$ giờ kể từ khi được cấp quyền.
- [ ] Đạt Definition of Done: LMS Admin ký biên bản nghiệm thu kỹ thuật, đưa `TTF-End-User` thực tế xuống $\le 48$ giờ (thay vì 10 ngày như hiện tại).

---
*Xác nhận của học viên: Nguyễn Quang Sơn (2A202601956)*
