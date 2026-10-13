# Prototype Links — Day 18 · Ba micro-prototype A/B/C

**Nhóm:** ThreeWhites · **Bối cảnh:** Hỗ trợ người học làm rõ nội dung slide Double Diamond ngay trong bài học.

| Option | Người phụ trách | Link công khai (mở trực tiếp trên trình duyệt) | Tương tác chính |
|---|---|---|---|
| **A — Giải thích thuật ngữ tại chỗ** | Nguyễn Tiến Phát | <https://phatnguyen2004s.github.io/Track1_Day18_2A202602387_NguyenTienPhat/prototypes/prototype_phat/prototype/option-a.html> | Hover để nhận biết thuật ngữ tương tác, bấm để mở pop-up giải thích. |
| **B — Guided Check** | Đào Trọng Khang | <https://phatnguyen2004s.github.io/Track1_Day18_2A202602387_NguyenTienPhat/prototypes/prototype_khang.html> | Bấm Bắt đầu, chờ câu hỏi tự xuất hiện rồi chọn mức độ hiểu hoặc khó khăn. |
| **C — Khoanh vùng nội dung (C2)** | Đỗ Trọng Bình | <https://phatnguyen2004s.github.io/Track1_Day18_2A202602387_NguyenTienPhat/prototypes/prototype_binh/prototype-c2-region.html> | Kéo chọn vùng sơ đồ, xem preview, nhập câu hỏi nếu cần và gửi yêu cầu giải thích. |

Link tương đối trong repo (dùng khi tải thư mục về máy): [Option A](prototypes/prototype_phat/prototype/option-a.html) · [Option B3](prototypes/prototype_khang.html) · [Option C2](prototypes/prototype_binh/prototype-c2-region.html).

Ba link trên trỏ tới các bản A/B/C trong bộ bài nộp của nhóm; theo hồ sơ nhóm, đây là các bản được dùng trong phiên kiểm thử của Bình. Chưa ghi lại phiên bản tệp chính xác mà Khuê dùng trong phiên do Phát điều phối. **C1/C2/C3 đều thuộc Option C**; chỉ C2 được chọn làm đại diện C trong bộ ba này.

## Cách truy cập và chạy

1. Tải hoặc giữ nguyên toàn bộ thư mục bài nộp để các đường dẫn tương đối hoạt động.
2. Mở file HTML tương ứng bằng **Chrome hoặc Edge**. Nếu bấm link trong IDE chỉ mở mã nguồn, dùng chức năng **Open with** để mở file bằng trình duyệt.
3. Với **Option A**, giữ `option-a.html`, `common.css`, `common.js` và `content.js` trong cùng thư mục `prototypes/prototype_phat/prototype/`; không gửi riêng file HTML. **Option B và C2** là các file HTML tự chứa mã giao diện và tương tác.

Không cần backend hay API để thử các luồng chính. Cả ba sử dụng lời giải thích dựng sẵn. Option A có tham chiếu Google Fonts; khi không tải được font, trình duyệt dùng font dự phòng.

**Đưa Option A về trạng thái ban đầu giữa hai lượt thử:** tải lại trang (F5) để về slide 5. Nút **Bắt đầu lại** (thêm `?facilitator=1` vào URL) chỉ đóng pop-up, không đổi slide. Chi tiết trong [hướng dẫn Option A](prototypes/prototype_phat/README.md).

**Trạng thái truy cập:** Repo là public và ba link trên chạy qua GitHub Pages, không cần đăng nhập. Ngày 13/10/2026, cả ba link được mở bằng trình duyệt: Option A (hover, bấm thuật ngữ, đóng bằng Escape), Option B (bấm Bắt đầu, hộp thoại tự mở sau khoảng 8 giây, chọn khó khăn, về trang bắt đầu) và Option C2 (kéo chọn vùng, gửi yêu cầu, hiển thị các nút Giải thích lại, Sửa yêu cầu, Đổi phần chọn, Hủy kết quả, Đối chiếu); không có lỗi trong console. Nên dùng cửa sổ rộng từ 1280 px, ở màn hẹp bố cục của C2 bị cắt.

## Tài liệu liên quan

- [Thiết kế ba option và Human–AI Decision Table](three-option-design-sheet.md)
- [Prototype Feedback Note cá nhân của Phát](prototype-feedback-note.md)
- [Group Feedback Synthesis](group-feedback-synthesis.md)
- [Hướng dẫn và checklist Option A](prototypes/prototype_phat/README.md)
- [Hướng dẫn và checklist Option C](prototypes/prototype_binh/README.md)
