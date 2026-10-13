# Prototype Feedback Note — Day 18 · Chặng 6

**Họ tên người phỏng vấn:** Nguyễn Tiến Phát · **Mã học viên:** 2A202602387  
**Tester:** Khuê · Người dùng bên ngoài nhóm  
**Bối cảnh kiểm thử:** Học slide bài giảng nhưng chưa hiểu một số nội dung trong bài, thao tác hệ thống để xem các cách giải quyết giúp người học hiểu ngay được nội dung đó để tiếp tục theo dõi bài giảng.

Đây là bản ghi cá nhân cho phiên kiểm thử do Nguyễn Tiến Phát điều phối, trong đó Khuê trải nghiệm đủ ba phương án A/B/C. Ghi chép gốc của người phỏng vấn dùng nhãn **O1 = Phát = Option A**, **O2 = Bình = Option C**, **O3 = Khang = Option B**. Các phản hồi của tester dưới đây là diễn ý từ ghi chép, không phải trích dẫn nguyên văn.

## 1. Bối cảnh và phạm vi phiên kiểm thử

**Câu hỏi xác thực bối cảnh:** Chưa ghi nhận nội dung câu hỏi đã đặt cho Khuê, cũng như câu trả lời, nghề nghiệp hoặc tình huống học tập gần đây của tester. Nhiệm vụ mẫu được giao, thứ tự trải nghiệm A/B/C và thời lượng thực tế của từng phương án cũng chưa được ghi lại trong ghi chép.

| Phương án | Prototype được thử | Cơ chế hỗ trợ |
|---|---|---|
| **Option A — Phát (O1)** | [prototype_phat](prototypes/prototype_phat/prototype/option-a.html) | Người học bấm vào thuật ngữ trên slide Double Diamond để mở pop-up giải thích ngay bên dưới thuật ngữ đó. |
| **Option B — Khang (O3)** | [prototype_khang](prototypes/prototype_khang.html) | Hệ thống chủ động hiển thị câu hỏi kiểm tra mức độ hiểu; người học chọn khó khăn hoặc xác nhận đã hiểu. |
| **Option C — Bình (O2)** | [prototype-c2-region.html](prototypes/prototype_binh/prototype-c2-region.html) | Người học tự chọn phần nội dung cần hỏi, có thể nhập thêm câu hỏi rồi yêu cầu AI giải thích. Chưa ghi nhận Khuê dùng biến thể C1, C2 hay C3; nhóm dùng C2 làm đại diện của Option C. |

**Lưu ý phạm vi:** Ba phương án so sánh là bản của Phát, Khang và Bình; không phải ba biến thể C1/C2/C3. Cả ba prototype dùng lời giải thích dựng sẵn, không gọi mô hình AI thật.

## 2. Ghi nhận phản hồi cá nhân

| Tiêu điểm quan sát hành vi | Ghi chép chi tiết hành vi thực tế (Fact-First) |
|---|---|
| **First Action — Hành động đầu tiên** | **Chưa ghi nhận** Khuê bấm hoặc nhìn vào đâu đầu tiên ở từng bản. Với A, Khuê nhận xét bản này tiện và dễ sử dụng; chưa ghi lại thao tác đầu tiên hay thuật ngữ nào được bấm đầu tiên. |
| **Hesitation — Điểm do dự hoặc hiểu sai** | **A:** Khuê muốn so sánh hai phần lý thuyết nhưng chưa thực hiện được trong bản này; đồng thời muốn tra lý thuyết hoặc yêu cầu ví dụ theo ý muốn. **B:** Khuê thấy thông báo gây phiền khi đang đọc nội dung và một số phần trong bản demo còn khó hiểu. **C:** Chưa ghi nhận điểm do dự cụ thể. |
| **Evidence Checking — Minh chứng được đọc hay bỏ qua** | **Chưa ghi nhận** Khuê có đối chiếu lời giải thích với slide, đọc cảnh báo hay kiểm tra nguồn hay không. Về thiết kế: pop-up của A chỉ hiển thị lời giải thích dựng sẵn, không có nguồn trích dẫn hay chỉ báo độ tin cậy; việc thiếu các thành phần này không cho biết Khuê có cần đến chúng hay không. |
| **Control & Recovery — Sửa sai hoặc lấy lại quyền kiểm soát** | **Chưa ghi nhận** Khuê dùng nút đóng, phím Escape hoặc chọn thuật ngữ khác trong A. Về thiết kế: A cho đóng pop-up hoặc đổi thuật ngữ nhưng không có ô nhập câu hỏi, không sửa được yêu cầu và không chọn được hai nội dung cùng lúc; vì vậy A không có đường điều chỉnh tương ứng với nhu cầu so sánh hai phần lý thuyết mà Khuê nêu. |
| **Selected Option — Phương án được lựa chọn** | **Option C — bản của Bình.** Chưa ghi nhận Khuê dùng biến thể C1, C2 hay C3. |
| **Trade-offs — Lý do chọn và đánh đổi chấp nhận** | Theo phản hồi được người phỏng vấn thuật lại, Khuê chọn bản của Bình vì cho rằng cơ chế này khắc phục hạn chế của A về việc hỏi theo nhu cầu; bản này linh hoạt hơn và khá trực quan, dễ dùng. Khuê nhận xét A tiện và dễ sử dụng nhưng không đủ để đáp ứng việc so sánh lý thuyết và hỏi theo ý muốn; B có thể hữu ích khi gặp lý thuyết chưa hiểu nhưng sẽ gây phiền nếu thông báo ngắt lúc đang đọc. Khuê góp ý hoàn thiện phần LLM để bản demo trở thành công cụ hữu ích hơn. **Chưa ghi nhận** Khuê chấp nhận đánh đổi gì khi chọn C, ví dụ thêm thao tác chọn nội dung. |
| **Counter-evidence — Dữ kiện đi ngược kỳ vọng** | (1) Option A — bản tôi phụ trách — được Khuê nhận xét tiện và dễ dùng nhưng không được chọn; sự dễ dùng không đủ để thắng khả năng hỏi linh hoạt. (2) Nhu cầu so sánh hai phần lý thuyết mà Khuê nêu cho thấy giả định "giải thích theo từng thuật ngữ là đủ" của A chưa đúng với ít nhất một tester. (3) Khuê chọn C vì tính linh hoạt, trong khi bản C hiện tại chưa chứng minh xử lý được việc so sánh hai phần lý thuyết; lựa chọn này một phần dựa trên kỳ vọng về LLM chưa được xây dựng. |

## 3. Bóc tách 4 tầng tư duy

### 1. OBSERVED — Quan sát khách quan

- Khuê trải nghiệm đủ ba bản. Ghi chép của tôi dùng nhãn O1 (A), O2 (C), O3 (B).
- **A:** Khuê nhận xét tiện và dễ sử dụng. Khuê muốn so sánh hai phần lý thuyết nhưng chưa làm được trong bản này, và muốn tra lý thuyết hoặc yêu cầu ví dụ theo ý muốn.
- **B:** Khuê nhận xét cơ chế hữu ích khi gặp lý thuyết chưa hiểu, nếu bỏ qua được vấn đề gây gián đoạn. Thông báo gây phiền khi đang đọc; một số phần trong demo còn khó hiểu.
- **C:** Khuê đánh giá khá trực quan, dễ dùng, linh hoạt hơn A và chọn bản của Bình. Khuê góp ý hoàn thiện phần LLM.
- **Chưa ghi nhận:** câu trả lời cho câu hỏi bối cảnh, hành động đầu tiên ở từng bản, điểm dừng cụ thể, thao tác đóng hoặc đổi thuật ngữ, việc đối chiếu minh chứng, thời lượng từng bản và biến thể C mà Khuê dùng. Không có câu nói nguyên văn của tester được lưu trong bản này.

### 2. INTERPRETED — Diễn giải của người làm sản phẩm

- Khuê coi trọng khả năng hỏi theo ý muốn, gồm so sánh và xin ví dụ, hơn là chỉ cần thao tác nhanh. Với tester này, "tiện" là điều kiện cần chứ chưa phải lý do chọn.
- Là người làm Option A, tôi cho rằng giới hạn của A nằm ở cơ chế: người học chỉ hỏi được qua các thuật ngữ đã gắn sẵn và nhận lời giải thích đã dựng sẵn cho từng thuật ngữ, nên câu hỏi dạng quan hệ hoặc so sánh không có đường hỏi. Đây là nhận định sau phiên thử, cần kiểm tra thêm với người học khác.
- Nhận xét của Khuê về B (hữu ích nhưng gây phiền khi đang đọc) cùng hướng với phản hồi của Linh về thông báo xuất hiện sớm. Hai trên ba tester nhắc đến việc gián đoạn có thể là tín hiệu lặp lại về thời điểm can thiệp, nhưng chưa đủ để kết luận.
- Việc Khuê chọn C có thể dựa vào kỳ vọng rằng bản này, khi hoàn thiện LLM, sẽ làm được điều A chưa làm được. Đây là suy đoán, chưa có dữ liệu xác nhận.

### 3. DECIDED — NEXT CHANGE

**Next Change nhóm chốt cho vòng tiếp theo: sửa phạm vi khoanh vùng và ảnh preview của C2** (xem [group-feedback-synthesis.md](group-feedback-synthesis.md), mục 5). Phiên của Khuê không gặp lỗi này; tôi ủng hộ quyết định vì lỗi do Duyên phát hiện làm mất đúng giá trị mà người dùng chọn C2 vì nó, và vì nó chặn việc đánh giá các cải tiến khác của C2.

**Điều riêng từ phiên Khuê — đề xuất thử tiếp, không phải Next Change:** thử bổ sung luồng chọn phần nội dung thứ hai trong Option C để hỏi so sánh hai phần lý thuyết. Đề xuất xuất phát từ nhu cầu Khuê nêu khi trải nghiệm A, phù hợp với hướng "hoàn thiện LLM và thử so sánh lý thuyết" trong danh sách hướng thử của nhóm, và chỉ thực hiện sau khi Next Change trên được xác minh.

1. Cho phép người học chọn thêm một phần nội dung thứ hai (ví dụ hai giai đoạn, hoặc hai loại evidence) rồi hỏi so sánh; giữ ô câu hỏi là tùy chọn.
2. Phản hồi dựng sẵn cho trường hợp so sánh: nêu điểm giống và khác ngắn gọn, ví dụ Discover so với Define, trước khi mở rộng thêm.
3. Khi chưa chọn đủ hai phần hoặc thiếu ngữ cảnh, yêu cầu người học chọn thêm thay vì trả lời chắc chắn.
4. Ở lượt thử tiếp theo, ghi lại cụ thể: tester có tự tìm cách chọn phần thứ hai không, mất bao nhiêu thao tác, có đọc phần so sánh không và câu trả lời có đúng trọng tâm không.

**Ghi chú liên quan, cũng chưa phải quyết định:** (a) rà soát nội dung giải thích của A, vì Linh nhận xét một số nội dung lý thuyết chưa chính xác; (b) cân nhắc đưa thao tác bấm thuật ngữ của A làm lối vào nhanh ít công sức trong C, vì cả ba tester đều dùng được A dễ dàng trong khi Linh gặp khó khăn với kéo thả ở C. Cả hai cần thử thêm.

### 4. STILL UNPROVEN — Điều vẫn chưa thể chứng minh

- Nhu cầu so sánh hai phần lý thuyết mới được ghi nhận ở một trong ba tester (Khuê); chưa biết người học khác có cần không.
- Chưa biết luồng chọn hai nội dung có được người học tự tìm ra và dùng thành công, hoặc có giúp hiểu bài tốt hơn không.
- Chưa biết Khuê có vẫn chọn C nếu gặp khó khăn thao tác như Linh khi kéo thả hoặc tự nhập câu hỏi.
- Chưa biết phần nội dung nào của A bị đánh giá chưa chính xác và A sau khi sửa có thay đổi lựa chọn của người học hay không.
- Chưa biết người học có nhận ra thuật ngữ bấm được khi không có thao tác hover, ví dụ trên màn hình cảm ứng; A dùng hover để gợi ý tương tác.
- Hành vi kiểm tra minh chứng, đóng pop-up và đổi thuật ngữ của Khuê chưa được ghi nhận nên chưa thể kết luận.
- Độ chính xác của AI thật trên câu hỏi tự do và so sánh vẫn cần kiểm thử riêng, vì cả ba prototype dùng phản hồi dựng sẵn.
