# AI Support Log — Day 18

**Họ và tên:** Nguyễn Tiến Phát  
**Mã học viên:** 2A202602387  
**Nhóm:** ThreeWhites  
**Phần phụ trách:** Option A — Giải thích thuật ngữ ngay trên slide.

## 1. Công cụ và mục đích sử dụng

Tôi sử dụng **Claude (Claude Code)** xuyên suốt: ở các bước trước để hỗ trợ dựng prototype Option A và lên ý tưởng, và ở bước này để đọc tài liệu cùng mã prototype trong repo của nhóm, kiểm tra hành vi của Option A bằng cách chạy mã, rồi soạn bản nháp bộ bài nộp cá nhân. Tôi không dùng công cụ AI nào khác. AI hỗ trợ tạo bản nháp; tôi và nhóm quyết định bối cảnh, phương án thiết kế và nội dung cuối cùng.

Nhật ký này được tổng hợp theo các công việc đã thực hiện, không ghi thời gian hoặc prompt nguyên văn khi chưa có dữ liệu lưu lại.

## 2. Nhật ký ứng dụng AI

| Công việc | AI đã hỗ trợ | Phần tôi và nhóm thực hiện |
|---|---|---|
| **Dựng Option A và lên ý tưởng** | Hỗ trợ dựng prototype Option A và gợi ý hướng giải pháp ở mức tham khảo. | Tôi cùng nhóm thảo luận bối cảnh, thống nhất Hypothesis Problem và ba phương án A/B/C; tôi quyết định cơ chế Option A (bấm thuật ngữ, pop-up cạnh nội dung) và rà soát đầu ra của AI trước khi dùng. |
| **Soạn bộ bài nộp cá nhân** | Đọc repo của nhóm (README, Three Option Design Sheet, Group Feedback Synthesis, Feedback Note của Bình, mã ba prototype) và dựng bản nháp README, Feedback Note, AI Support Log theo cấu trúc bài tập. | Tôi cung cấp vai trò của mình (Option A, phiên kiểm thử với Khuê) và yêu cầu dựa trên thông tin đã làm chung với nhóm; tôi rà soát để nội dung phản ánh đúng công việc và dữ kiện thực tế của mình. |
| **Đối chiếu Option A với mã nguồn** | Đọc `option-a.html`, `common.js`, `content.js`; chạy prototype trong trình duyệt bằng cách giả lập sự kiện để xác nhận số thuật ngữ bấm được, nội dung hiển thị theo từng thuật ngữ, các cách đóng pop-up, trạng thái ở slide 6/7 và hành vi nút Bắt đầu lại. | Tôi dùng kết quả để mô tả phạm vi và giới hạn thật của Option A, thay vì mô tả theo ý định thiết kế. |
| **Phân loại dữ kiện phiên kiểm thử** | Sắp xếp dữ kiện về phiên của Khuê vào bảng Feedback Note và bốn tầng Observed, Interpreted, Decided — Next Change, Still Unproven. | Dữ kiện về Khuê lấy từ ghi chép của tôi đã được nhóm tổng hợp trong Group Feedback Synthesis. Các mục không có dữ liệu được ghi là **chưa ghi nhận**; lời tester được diễn ý, không trình bày như trích dẫn nguyên văn. |
| **Viết hướng dẫn Option A** | Soạn bảng thuật ngữ → nội dung, checklist thủ công và danh sách giới hạn cho [prototypes/prototype_phat/README.md](prototypes/prototype_phat/README.md). | Tôi rà soát bảng và checklist với prototype; các hiệu ứng hover và bố cục pop-up chưa được kiểm tra bằng chuột thật. |

## 3. Khâu AI hỗ trợ hiệu quả

- **Đọc và đối chiếu mã:** Giúp phát hiện các giới hạn của Option A mà mô tả thiết kế chưa nêu, ví dụ nút Bắt đầu lại chỉ đóng pop-up và nhiều thuật ngữ cùng mở một đoạn giải thích.
- **Tổng hợp dữ kiện:** Gom ghi chép rải rác của ba phiên thành bảng đối chiếu theo từng option và từng tester.
- **Cấu trúc tài liệu:** Sắp xếp nội dung theo các mục bài tập yêu cầu và giữ cách ghi "chưa ghi nhận" cho dữ kiện còn thiếu.

## 4. Những điểm tôi tự chỉnh sửa và vấn đề còn cần xử lý

**Phần đã tự chỉnh sửa (các sai sót của AI tôi đã xử lý):**

- AI suy ra từ repo rằng tôi dựng khung trang học dùng chung. Tôi xác nhận không đúng, nên mục "Đóng góp cụ thể" chỉ ghi phần tôi thực sự làm là lớp tương tác của Option A.
- AI để nhiều ô "chưa ghi nhận" trong Feedback Note vì repo không có dữ liệu. Tôi xác nhận không còn ghi chép gốc về phiên với Khuê và giữ nguyên các ô đó, không để AI suy diễn hành vi của tester.
- Khi đối chiếu với hướng dẫn nộp bài, AI chỉ ra bản tổng hợp nhóm liệt kê bốn thay đổi ưu tiên trong khi yêu cầu là đúng một Next Change. Tôi quyết định Next Change của nhóm là sửa vùng chọn ảnh của C2 và chuyển các mục còn lại thành hướng thử tiếp.
- Hướng dẫn yêu cầu Hypothesis gắn với dữ kiện Day 17. Tôi xác nhận không có dữ kiện này để bổ sung, nên bộ bài ghi rõ là chưa ghi nhận thay vì để AI bịa.

Tôi chưa ghi lại ví dụ nguyên văn trước–sau cho từng câu đã sửa.

**Vấn đề được phát hiện ở Option A:**

- Nút **Bắt đầu lại** của người điều phối (`?facilitator=1`) chỉ đóng pop-up; không đưa trang về slide đầu. Giữa hai lượt thử cần tải lại trang. Chưa sửa mã.
- Lời giải thích dựng sẵn theo giai đoạn chứ không theo từng thuật ngữ; Linh cũng nhận xét một số nội dung lý thuyết chưa chính xác. Chưa xác định chính xác đoạn nào bị nhận xét, cần rà soát nội dung với bài giảng.

**Điểm cần phân biệt khi đọc kết quả:** Prototype dùng câu trả lời dựng sẵn, chưa tích hợp AI thật. Việc Khuê chọn C phản ánh ưu tiên trong một phiên thử, chưa đủ để kết luận AI thật sẽ giải thích chính xác hoặc cải thiện hiệu quả học tập lâu dài.

## 5. Vai trò và trách nhiệm cá nhân

Việc xây dựng **Human–AI Decision Table** được thực hiện bằng cách mỗi thành viên tự điền phần option mình phụ trách, sau đó cùng trao đổi, góp ý và chỉnh sửa cho nhau. Tôi phụ trách phần Option A.

Dữ liệu kiểm thử xuất phát từ phiên tôi trực tiếp điều phối với Khuê. AI hỗ trợ tổ chức và diễn đạt lại ghi chép; các hành vi chưa có dữ liệu được ghi là **chưa ghi nhận**.
