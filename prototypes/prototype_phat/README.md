# VLearn — Prototype Option A: Giải thích thuật ngữ tại chỗ

Người phụ trách: Nguyễn Tiến Phát — MHV 2A202602387 · Nhóm ThreeWhites

Mở [prototype/option-a.html](prototype/option-a.html) bằng Chrome hoặc Edge. Giữ nguyên `option-a.html`, `common.css`, `common.js` và `content.js` trong cùng thư mục `prototype/`; không gửi riêng file HTML. Không cần backend, API hay thư viện. Có tham chiếu Google Fonts; khi không tải được font, trình duyệt dùng font dự phòng. Khuyến nghị cửa sổ rộng từ 1280 px.

| File | Vai trò |
|---|---|
| [prototype/option-a.html](prototype/option-a.html) | Option A: lớp tương tác bấm thuật ngữ và pop-up giải thích. |
| [prototype/common-context.html](prototype/common-context.html) | Màn hình bối cảnh chung, chưa có lớp tương tác của Option A. |
| [prototype/common.js](prototype/common.js), [prototype/common.css](prototype/common.css) | Khung trang học mô phỏng, ba slide (trang 5, 6, 7) và điều hướng giữa các slide. |
| [prototype/content.js](prototype/content.js) | Nội dung giải thích Double Diamond dựng sẵn (canned output), tách theo đoạn. |

Tham số URL: `?facilitator=1` hiện nút **Bắt đầu lại** ở góc dưới trái dành cho người điều phối. `?ai=off` ẩn hai điểm vào AI có sẵn của nền tảng.

## Ba trạng thái và phạm vi

1. **Bối cảnh chung:** trang học "Day 18+19 Design the Experiment" ở slide 5/23 **Evidence về problem không phải evidence về solution**, có sơ đồ Double Diamond và bốn cột Discover, Define, Develop, Deliver. Nút **Đặt câu hỏi với AI** trên thanh trên và nút sparkle trên slide là điểm vào AI có sẵn của nền tảng; trong prototype này chúng chỉ hiển thị, không mở gì.
2. **Tương tác then chốt:** đưa chuột vào một thuật ngữ trên slide, thuật ngữ được làm nổi bật (nền vàng với tiêu đề và các dòng trong cột, gạch chân với nhãn trong sơ đồ), rồi bấm. Pop-up xuất hiện ngay dưới thuật ngữ, lật lên trên nếu hết chỗ phía dưới.
3. **Kết quả và quyết định:** đọc lời giải thích, đóng pop-up hoặc bấm thuật ngữ khác, rồi tiếp tục học bằng nút chuyển trang ở thanh công cụ (5 → 6 → 7).

## Thuật ngữ nào bấm được và hiện nội dung gì

Chỉ slide Double Diamond (trang 5) có thuật ngữ bấm được. Trang 6 và 7 không có lớp tương tác và pop-up tự đóng khi chuyển trang. Có 40 phần tử bấm được: 4 tiêu đề cột, 16 dòng trong cột, 18 nhãn trong sơ đồ và hai từ khóa **problem**, **solution** trong tiêu đề. Hai nhãn **Time** và **Alternatives** bị loại khỏi danh sách.

Nội dung được chọn bằng cách khớp chữ của thuật ngữ với các đoạn trong `content.js`:

| Thuật ngữ đã bấm | Nội dung hiển thị |
|---|---|
| DISCOVER, discover, Problem interview, Past story, Behavior & workaround, Quan sát context | Discover – Khám phá |
| DEFINE, define, Synthesis note, Pain pattern, Chọn opportunity, Learning Question, Chosen opportunity | Define – Xác định |
| DEVELOP, develop, Diverge cơ chế, Standard / ++ / Wild, Micro-prototype, Multi-option A/B/C | Develop – Phát triển |
| DELIVER, deliver, Prototype interview, Quan sát behavior, Compare trade-off, Next iteration, Next | Deliver – Kiểm chứng |
| Finding the PROBLEM (và DAY 17), Pain, problem | Viên kim cương 1 – Tìm đúng vấn đề |
| Finding the SOLUTION (và DAY 18), solution | Viên kim cương 2 – Tìm đúng giải pháp |
| Divergence, Convergence | Hai cách tư duy: Divergence – Mở rộng, Convergence – Thu hẹp |

Thuật ngữ không khớp ý nào sẽ hiển thị phần tổng quan Double Diamond. Cơ chế này mô phỏng việc AI chọn lời giải thích theo thuật ngữ; không có AI thật và không gọi mạng.

## Quyền kiểm soát

- Đóng pop-up bằng nút **×**, phím **Escape**, hoặc bấm ra ngoài pop-up.
- Bấm lại đúng thuật ngữ đang mở để đóng; bấm thuật ngữ khác để đổi nội dung.
- Pop-up cũng đóng khi đổi kích thước cửa sổ, cuộn trang hoặc chuyển slide.
- Không có ô nhập câu hỏi, không sửa yêu cầu và không chọn hai nội dung cùng lúc.

## Checklist kiểm thử thủ công

- Mở `option-a.html` → slide 5/23 hiển thị, chưa có pop-up. Người học tự đọc và thao tác, người điều phối không giải thích hộ giao diện.
- Đưa chuột vào một dòng trong cột → nền vàng nhạt; vào một nhãn trong sơ đồ → gạch chân.
- Bấm **DISCOVER** → pop-up Discover dưới tiêu đề cột. Bấm lại đúng thuật ngữ → pop-up đóng.
- Bấm **Chosen opportunity** rồi **Next iteration** → nội dung đổi từ Define sang Deliver.
- Bấm **Divergence** → pop-up hiển thị hai cách tư duy.
- Đóng pop-up bằng **×**, **Escape** và bấm ra ngoài; thử từng cách.
- Bấm **Trang sau** → slide 6, rồi 7: không còn thuật ngữ bấm được, pop-up không còn.
- Thêm `?facilitator=1`, bấm **Bắt đầu lại** → pop-up đóng. Để quay về slide 5 từ slide 6 hoặc 7, tải lại trang (F5).

## Giới hạn hiện tại

- **Reset chưa đầy đủ:** nút **Bắt đầu lại** (`?facilitator=1`) chỉ đóng pop-up; không đưa trang về slide 5. Cần tải lại trang giữa hai lượt thử.
- **Độ chi tiết của giải thích:** nội dung theo giai đoạn chứ không theo từng thuật ngữ. Bốn dòng trong cột DISCOVER cùng mở một đoạn Discover; Standard / ++ / Wild hay Learning Question chưa có định nghĩa riêng.
- **Hover:** gợi ý thuật ngữ bấm được dựa vào hover bằng chuột; màn hình cảm ứng không có hover.
- **Phạm vi nội dung:** chỉ có lời giải thích cho slide Double Diamond; câu hỏi tự do, so sánh hai phần lý thuyết và hỏi ví dụ theo ý muốn chưa được hỗ trợ.
- **Điểm vào AI có sẵn:** nút "Đặt câu hỏi với AI" và nút sparkle chưa có hành vi.

## Trạng thái kiểm tra

Logic mở và đóng pop-up, nội dung theo từng thuật ngữ, trạng thái trên slide 6/7 và nút Bắt đầu lại đã được kiểm tra bằng cách chạy mã trong trình duyệt (giả lập sự kiện bấm). Hiệu ứng hover, vị trí và bố cục pop-up chưa được kiểm tra bằng thao tác chuột thật; cần chạy checklist trên Chrome hoặc Edge trước khi giao cho tester.
