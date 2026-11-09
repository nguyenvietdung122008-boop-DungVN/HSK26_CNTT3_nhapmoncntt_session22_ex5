###  BÁO CÁO SỰ CỐ NỘI BỘ (BUG REPORT)
1. **Context (Ngữ cảnh / Môi trường):**   * Hệ điều hành: [Ví dụ: Windows 11 / Ubuntu 22.04 / macOS]   * Công cụ/Phiên bản: [Ví dụ: Docker v24.0.5, Python 3.10]   * Trạng thái trước khi lỗi: [Ví dụ: Đang chạy lệnh `docker compose up` cho dự án A]
2. **Expected (Mong đợi):**   * Hệ thống/Container phải khởi động thành công và mở port `8000` mà không báo lỗi.
3. **Actual (Thực tế):**   * Lỗi gì xảy ra? [Ví dụ: Container bị dừng đột ngột và báo lỗi xung đột cổng mạng (Port conflict).]
4. **Log / Error Message (Dữ liệu lỗi chi tiết):**   * Dán đoạn code lỗi nguyên bản (không chụp ảnh màn hình đoạn text log):
   ```text
   Error response from daemon: driver failed programming external connectivity on endpoint web_app: Bind for 0.0.0.0:8000 failed: port is already allocated

---

### Phần 2: Quy trình 3 bước tra cứu bắt buộc (Self-Service 80%)

Để giảm tải cho người hỗ trợ (Lead/Senior) và rèn luyện tư duy tự xử lý vấn đề, mọi thành viên phải tuân thủ nghiêm ngặt **3 bước tự xử lý** sau trước khi được phép gửi Bug Report ở trên:

#### Bước 1: Googling chủ động (Tìm kiếm chính xác bằng từ khóa lỗi)
*   **Hành động:** Copy nguyên văn đoạn mã lỗi cốt lõi (hoặc thông điệp lỗi trong file Log) tra cứu trên Google.
*   **Mẹo:** Đặt lỗi trong dấu ngoặc kép (Ví dụ: `"port is already allocated" docker`) để tìm kiếm chính xác các bài viết có cùng lỗi trên StackOverflow hoặc GitHub Issues.

#### Bước 2: Community Search (Tìm kiếm trong lịch sử nhóm hoặc cộng đồng)
*   **Hành động:** 
    *   Tìm kiếm trong thanh tìm kiếm của nhóm chat nội bộ (Slack/Discord/Zalo) xem đã có ai gặp lỗi này trong tuần qua chưa và giải pháp là gì.
    *   Kiểm tra kho tài liệu Wiki / README của dự án xem phần *"Troubleshooting"* đã đề cập đến lỗi này chưa.

#### Bước 3: AI Translation & Analysis (Dùng AI phân tích và dịch nghĩa lỗi)
*   **Hành động:** Nếu thông báo lỗi quá khó hiểu hoặc bằng tiếng Anh chuyên sâu, hãy đưa vào AI kèm câu lệnh:
    > *"Giải thích cho tôi lỗi này nguyên nhân do đâu bằng tiếng Việt ngắn gọn và đưa ra 2 cách khắc phục an toàn nhất."*
*   **Mục tiêu:** Hiểu rõ bản chất vấn đề (ví dụ: hiểu rằng cổng `8000` đang bị một tiến trình khác chiếm dụng) thay vì chỉ làm theo máy móc.

---

*Quy trình này khi được áp dụng đồng bộ sẽ giúp nh
