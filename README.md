# Chặng 4: Build

# 1. Thông tin cá nhân & Đội ngũ

| Thông tin | Nội dung |
|---|---|
| Mã học viên | 2A202602387 |
| Họ và tên | Nguyễn Tiến Phát |
| Tên nhóm | ThreeWhites |
| Số thành viên | 3 |
| Thành viên 1 | Đào Trọng Khang — MHV: 2A202602974 |
| Thành viên 2 | Nguyễn Tiến Phát — MHV: 2A202602387 |
| Thành viên 3 | Đỗ Trọng Bình — MHV: 2A202602855 |
| Case đã chọn | Case A — AI Tutor: Diagnostic Refresher |

# 2. Hypothesis Problem

Khi đang học (trên lớp hoặc trực tuyến) và gặp phần chưa hiểu trong lúc bài giảng vẫn tiếp tục, học viên gặp khó khăn trong việc làm rõ phần đó ngay trong ngữ cảnh bài học vì phải rời luồng bài sang công cụ bên ngoài (chụp màn hình, chuyển tab, tự mô tả lại ngữ cảnh) hoặc ghi lại để xem sau. Quá trình này làm mất thêm thời gian và trì hoãn việc làm rõ, khiến những kiến thức chưa hiểu dần tích tụ, tạo thành các lỗ hổng kiến thức và lâu dài làm chậm tiến độ học các bài tiếp theo.

**Năm thành tố của phát biểu (theo công thức Situation – User – Job – Barrier – Consequence):**

| Thành tố | Nội dung trong Hypothesis Problem |
|---|---|
| **Situation** | Đang học (trên lớp hoặc trực tuyến) và gặp phần chưa hiểu trong lúc bài giảng vẫn tiếp tục. |
| **User** | Học viên. |
| **Job** | Làm rõ phần chưa hiểu ngay trong ngữ cảnh bài học. |
| **Barrier** | Phải rời luồng bài sang công cụ bên ngoài (chụp màn hình, chuyển tab, tự mô tả lại ngữ cảnh) hoặc ghi lại để xem sau. |
| **Consequence** | Mất thêm thời gian, trì hoãn việc làm rõ; kiến thức chưa hiểu tích tụ thành lỗ hổng và làm chậm tiến độ học các bài tiếp theo. |

**Dữ kiện thực tế từ Day 17 làm điểm tựa.** Mỗi dữ kiện là lời tự kể của một người được phỏng vấn trong buổi luyện problem interview, chưa phải validation; nội dung dưới đây được diễn ý, không trích nguyên văn.

| Nguồn Day 17 | Dữ kiện | Ủng hộ hay thử thách Hypothesis |
|---|---|---|
| P01 do Bình phỏng vấn — [Interview Record](https://github.com/dotrongbinhf/Track1_Day17_2A202602855_DoTrongBinh/blob/main/interview/notes.md) | Khi học trên lớp và bài giảng vẫn tiếp tục, P01 thường chỉ ghi lại để xem sau; chỉ tra cứu bằng ChatGPT hoặc Claude khi có thời gian. P01 nói nếu phải mang bài tập về làm thì không còn thời gian tìm hiểu sâu phần đó; sau một câu hỏi gợi ý của người phỏng vấn, P01 nói thêm là ngại hỏi bạn vì sợ làm phiền. | **Ủng hộ** Situation và Barrier (bài giảng vẫn tiếp tục, ghi lại để xem sau, không có thời gian tra cứu ngay). Hậu quả mới ở mức tự báo cáo có điều kiện, chưa có sự kiện cụ thể. |
| P1 do tôi phỏng vấn — [Practice Note](https://github.com/phatnguyen2004s/Track1-Day17-2A202602387-NguyenTienPhat/blob/main/03-interview/practice-note.md) | Khi gặp phần chưa hiểu, P1 tra Google (có AI hỗ trợ) và tự đánh giá là nhanh, không quá mất thời gian. P1 thường phải tra lại cùng một kiến thức khoảng 2–3 lần mới nhớ, đôi khi quên luôn; không kể hậu quả nào với việc học. Chưa nêu rõ đây là trên lớp hay tự học. | **Thử thách** Barrier "mất thêm thời gian" và Consequence "lỗ hổng tích tụ": ít nhất một người xử lý nhanh và không thấy phiền. Đồng thời gợi ra một hướng ngoài giả thuyết: kiến thức không đọng lại nên phải tra lặp. |

Dữ kiện Day 17 của Khang chưa được đưa vào bộ bài này. Hai dữ kiện trên đều từ một người, chưa có sự kiện cụ thể kèm ngày và bài học, nên Hypothesis là điểm tựa để thiết kế và thử nghiệm, không phải bài toán đã được kiểm chứng hay giải quyết.

**Ẩn số chưa biết:**

1. **Về vấn đề (từ mâu thuẫn Day 17):** khi bài giảng vẫn tiếp tục, việc ghi lại để xem sau có thật sự khiến kiến thức chưa hiểu tích tụ thành lỗ hổng không, hay người học vẫn tra lại nhanh sau đó và không chịu hậu quả đáng kể như P1 của tôi?
2. **Về giải pháp (cần giải mã bằng ba prototype):** người học muốn tự khởi phát hỗ trợ hay để hệ thống gợi hỏi, và mức công sức thao tác họ chấp nhận khi muốn hỏi đúng phần mình chưa hiểu. Ba option A/B/C được thiết kế để kiểm thử ẩn số này.

# 3. Three Solution Options

Ba phương án cùng giải quyết tình huống người học chưa hiểu nội dung slide và cần được làm rõ ngay trong luồng học. Nhóm sử dụng slide Double Diamond “Evidence về problem không phải evidence về solution” làm bối cảnh chung. Các phương án khác nhau ở thời điểm hỗ trợ, cách xác định phần chưa hiểu và quyền quyết định của người học.

## Option A — Giải thích thuật ngữ ngay trên slide

**Người phụ trách:** Nguyễn Tiến Phát — MHV: 2A202602387  
**Prototype:** [prototype_phat — Option A](prototypes/prototype_phat/prototype/option-a.html) · [Hướng dẫn và checklist](prototypes/prototype_phat/README.md)  
**Link trải nghiệm công khai:** <https://phatnguyen2004s.github.io/Track1_Day18_2A202602387_NguyenTienPhat/prototypes/prototype_phat/prototype/option-a.html>

- **Cơ chế và luồng tương tác:** Người học hover vào thuật ngữ trên slide để thấy dấu hiệu tương tác, sau đó bấm vào thuật ngữ. Một pop-up xuất hiện cạnh phần vừa chọn, hiển thị nội dung giải thích tương ứng. Người học đọc, đóng pop-up hoặc bấm thuật ngữ khác rồi tiếp tục học.
- **Vai trò Người–AI:** Người học chủ động quyết định khi nào cần hỗ trợ và thuật ngữ nào cần làm rõ. Vai trò AI được mô phỏng bằng việc cung cấp lời giải thích theo thuật ngữ đã bấm; hệ thống không tự chen vào luồng học.
- **Quyền kiểm soát:** Có thể đóng pop-up bằng nút đóng, phím Escape hoặc bấm ra ngoài; chọn thuật ngữ khác để đổi nội dung giải thích. Bản hiện tại không có luồng nhập câu hỏi tự do hay chỉnh sửa yêu cầu trong pop-up.
- **Lợi ích kỳ vọng và đánh đổi:** Ít thao tác, giải thích gần nội dung gốc, phù hợp với nhu cầu tra cứu nhanh. Đổi lại, người học chỉ hỏi được qua các thuật ngữ đã gắn tương tác, chưa chọn tùy ý một vùng ảnh, bảng hoặc đặt câu hỏi chuyên sâu.

**Phạm vi Option A hiện tại:** Có 40 phần tử bấm được trên slide Double Diamond (tiêu đề cột, dòng trong cột, nhãn trong sơ đồ và hai từ khóa trong tiêu đề); hai slide tiếp theo không có thuật ngữ bấm được. Lời giải thích là nội dung dựng sẵn, chọn theo giai đoạn hoặc viên kim cương mà thuật ngữ thuộc về, nên nhiều thuật ngữ cùng mở một đoạn giải thích. Chưa có AI thật, chưa có câu hỏi tự do và chưa so sánh được hai nội dung. Nút **Bắt đầu lại** của người điều phối (`?facilitator=1`) chỉ đóng pop-up; muốn về slide đầu cần tải lại trang.

## Option B — Kiểm tra mức độ hiểu và hỗ trợ chủ động (Guided Check)

**Người phụ trách:** Đào Trọng Khang — MHV: 2A202602974  
**Prototype:** [prototype_khang — Option B3](prototypes/prototype_khang.html)  
**Link trải nghiệm công khai:** <https://phatnguyen2004s.github.io/Track1_Day18_2A202602387_NguyenTienPhat/prototypes/prototype_khang.html>

- **Cơ chế và luồng tương tác:** Sau khi người học bắt đầu và ở lại slide Double Diamond đủ thời gian, hệ thống tự mở hộp thoại hỏi đã hiểu slide chưa. Người học chọn “Tôi đã hiểu, tiếp tục” hoặc chọn một trong ba khó khăn: hai viên kim cương, mối liên hệ giữa bốn giai đoạn, hay Divergence/Convergence. Với lựa chọn chưa hiểu, hệ thống hiển thị giải thích chung, ví dụ, ý chính và phần trả lời theo khó khăn đã chọn.
- **Vai trò Người–AI:** Hệ thống chủ động xác định thời điểm hỏi từ tín hiệu thời gian ở lại slide. Người học xác nhận mức độ hiểu và chọn vấn đề cần làm rõ; thời gian ở lại không được coi là kết luận chắc chắn rằng họ chưa hiểu.
- **Quyền kiểm soát:** Người học có thể xác nhận đã hiểu, chọn khó khăn, tiếp tục sang slide sau hoặc quay lại trang bắt đầu. Sau lời giải thích, nút **Đã hiểu / Chưa hiểu** cho phép quay về slide hoặc mở lại câu hỏi kiểm tra. Bản hiện tại chưa có ô nhập câu hỏi tự do.
- **Lợi ích kỳ vọng và đánh đổi:** Có thể hỗ trợ người học chưa chủ động hỏi và giảm công sức mô tả khó khăn. Đổi lại, câu hỏi tự xuất hiện có thể ngắt luồng đọc; tín hiệu thời gian có thể không phản ánh đúng nhu cầu và các lựa chọn có sẵn chưa bao quát mọi thắc mắc.

**Chi tiết cần đồng bộ trong prototype:** Mã hiện kích hoạt hộp thoại sau khoảng **8 giây**, trong khi thông báo trên giao diện nói **hơn 15 giây**. Đây là cơ chế mô phỏng bằng bộ đếm thời gian, chưa phải AI chẩn đoán khó khăn thực tế.

## Option C — Giải thích phần nội dung do người học khoanh chọn (C2)

**Người phụ trách:** Đỗ Trọng Bình — MHV: 2A202602855  
**Prototype dùng kiểm thử:** [prototype_binh — C2](prototypes/prototype_binh/prototype-c2-region.html)  
**Link trải nghiệm công khai:** <https://phatnguyen2004s.github.io/Track1_Day18_2A202602387_NguyenTienPhat/prototypes/prototype_binh/prototype-c2-region.html>

- **Cơ chế và luồng tương tác:** Người học kéo chuột khoanh vùng sơ đồ cần làm rõ hoặc dùng nút chọn vùng nhanh. Panel trợ lý hiển thị ảnh preview để kiểm tra phần đã chọn. Người học có thể để trống câu hỏi để nhận giải thích chung, hoặc nhập thêm yêu cầu như hỏi ví dụ, hỏi sâu về một giai đoạn rồi gửi yêu cầu giải thích.
- **Vai trò Người–AI:** Người học quyết định thời điểm hỏi, phạm vi nội dung và trọng tâm câu hỏi. Vai trò AI là giải thích theo phần được chọn và ngữ cảnh bài học; trong prototype, phản hồi này được mô phỏng bằng nội dung dựng sẵn.
- **Quyền kiểm soát:** Có các thao tác **Chọn lại**, **Giải thích lại**, **Sửa yêu cầu**, **Đổi phần chọn**, **Hủy kết quả** và **Đối chiếu sơ đồ và Chosen opportunity**. Người học quyết định tiếp tục bài học khi đã hiểu.
- **Lợi ích kỳ vọng và đánh đổi:** Hướng tới việc hỏi đúng phần đang vướng, kể cả nội dung trực quan, đồng thời cho phép điều chỉnh câu hỏi. Đổi lại, người học phải tự khoanh đúng vùng và đọc nhiều lựa chọn hơn. Phiên thử với Duyên phát hiện hạn chế không chọn được hết phần ảnh mong muốn, cần sửa và kiểm thử lại.

**Phạm vi C2 hiện tại:** Chọn ảnh được mô phỏng bằng cách cắt vùng từ SVG của sơ đồ; chưa chụp toàn bộ slide, chưa OCR hay phân tích ảnh thật. C1 (chọn văn bản) và C3 (chọn khối) là các biến thể khác của Option C, không phải Option A và B của nhóm.

# 4. Đóng góp cụ thể của tôi trong sản phẩm nhóm:

- **Dựng Option A:** Tôi chịu trách nhiệm chính xây dựng prototype Option A — giải thích thuật ngữ ngay trên slide. Tôi dựng lớp tương tác riêng của Option A (`option-a.html`) trên khung trang học dùng chung có slide Double Diamond và hai slide tiếp theo: thuật ngữ bấm được, pop-up giải thích đặt cạnh thuật ngữ, và việc chọn đoạn giải thích dựng sẵn theo thuật ngữ đã bấm. Tôi cũng viết [hướng dẫn và checklist kiểm thử cho Option A](prototypes/prototype_phat/README.md), ghi rõ phạm vi và các giới hạn hiện có.
- **Xây dựng bối cảnh chung:** Tôi cùng các thành viên thảo luận để thống nhất bối cảnh người học gặp phần chưa hiểu khi học slide, xây dựng Hypothesis Problem và đề xuất ba phương án A/B/C để giải quyết vấn đề.
- **Tham gia Human–AI Decision Table:** Ban đầu, mỗi thành viên tự điền phần tương ứng với option mình phụ trách; tôi điền phần Option A. Sau đó, cả nhóm trao đổi, góp ý và chỉnh sửa phần của nhau để hoàn thiện bảng chung.
- **Dẫn dắt một phiên kiểm thử:** Tôi điều phối **Khuê, một tester ngoài nhóm**, thử đủ ba phương án A/B/C và ghi chép bằng nhãn O1/O2/O3. Bản ghi cá nhân là [prototype-feedback-note.md](prototype-feedback-note.md); ghi chép này là một trong ba nguồn của [Group Feedback Synthesis](group-feedback-synthesis.md).
- **Hỗ trợ đồng đội:** Tôi tham gia trao đổi ý tưởng, góp ý cho phần Human–AI Decision Table của Khang và Bình, đồng thời tiếp nhận góp ý của hai bạn để chỉnh sửa phần Option A của mình.

# 5. Dữ liệu kiểm thử & Bài học:

## Dữ kiện từ phiên kiểm thử do tôi dẫn dắt

Tôi điều phối **Khuê, một tester ngoài nhóm**, trải nghiệm đủ ba phương án A/B/C. Các dữ kiện dưới đây được tổng hợp từ ghi chép, không phải trích dẫn nguyên văn:

- **Option A (bản của tôi):** Khuê nhận xét bản này tiện và dễ sử dụng, nhưng muốn so sánh hai phần lý thuyết và muốn tra lý thuyết hoặc yêu cầu ví dụ theo ý muốn; hai việc này chưa làm được trong A.
- **Option B:** Khuê thấy cơ chế hữu ích khi gặp lý thuyết chưa hiểu, nếu bỏ qua được vấn đề gây gián đoạn. Thông báo gây phiền khi đang đọc và một số phần trong demo còn khó hiểu.
- **Option C:** Khuê đánh giá bản của Bình khá trực quan, dễ dùng và linh hoạt hơn, đồng thời góp ý hoàn thiện phần LLM.
- **Lựa chọn và đánh đổi:** Khuê chọn **C — bản của Bình** vì cơ chế này khắc phục hạn chế của A về việc hỏi theo nhu cầu. Chưa ghi nhận Khuê chấp nhận đánh đổi cụ thể nào khi chọn C.

Chi tiết được ghi trong [Prototype Feedback Note cá nhân](prototype-feedback-note.md). Các mục như hành động đầu tiên, điểm do dự cụ thể, việc đối chiếu minh chứng và thao tác đóng hoặc đổi thuật ngữ **chưa được ghi nhận**, nên không được suy diễn thêm.

## Tổng hợp ba phiên kiểm thử của nhóm

| Người điều phối | Tester | Option được chọn | Phản hồi nổi bật |
|---|---|---|---|
| Đào Trọng Khang | Linh | **B — bản của Khang** | Đánh giá câu hỏi, ghi chú và ví dụ của B dễ theo dõi, nhưng thông báo xuất hiện sớm. Với C, gặp khó khăn ban đầu khi kéo thả và thấy việc tự nhập câu hỏi tăng công sức. |
| Đỗ Trọng Bình | Duyên | **C2 — bản của Bình** | Muốn chủ động chọn đúng phần cần hỏi và điều chỉnh trọng tâm; chấp nhận thao tác khoanh vùng nhưng phát hiện lỗi không chọn được hết ảnh. |
| Nguyễn Tiến Phát | Khuê | **C — bản của Bình** | Thấy A tiện và dễ dùng nhưng thiếu khả năng so sánh lý thuyết, hỏi theo ý muốn. Chọn C vì linh hoạt hơn, khá trực quan; góp ý hoàn thiện LLM. Nhận xét B có thể hữu ích nhưng gây phiền khi đang đọc và còn khó hiểu trong demo. |

Theo [Group Feedback Synthesis](group-feedback-synthesis.md), **2/3 tester — Duyên và Khuê — chọn bản của Bình**. Nhóm quyết định phát triển tiếp **Option C2**, dựa trên lựa chọn này và các tín hiệu tích cực về quyền chủ động, khả năng hỏi đúng trọng tâm. Phản hồi của Linh được giữ làm dữ kiện đối trọng để cải thiện thao tác của C2.

## Quy luật lặp lại và mâu thuẫn, nhìn từ Option A

| Dữ kiện | Linh | Duyên | Khuê | Nhận xét |
|---|---|---|---|---|
| Dễ bắt đầu với A | Nhanh hiểu cách dùng | Nhận ra phần chữ tương tác khi hover, không có thắc mắc đáng kể | Tiện và dễ sử dụng | **Lặp lại ở 3/3 tester** |
| Chọn A | Không (chọn B) | Không (chọn C2) | Không (chọn C) | **0/3 chọn A** |
| Thiếu khả năng hỏi theo ý muốn | — | Muốn tự khoanh đúng phần cần hỏi, kể cả ảnh hoặc bảng | Muốn so sánh lý thuyết, hỏi ví dụ | Hai tester chọn C với lý do liên quan đến việc chủ động hỏi |
| Độ chính xác nội dung A | Một số nội dung lý thuyết chưa chính xác | Chưa ghi nhận | Chưa ghi nhận | Chỉ một tester nêu; cần rà soát |

**Mâu thuẫn đáng chú ý:** Cả ba tester đều dễ dùng A nhưng không ai chọn A. Linh ưu tiên B (câu hỏi dễ nắm bắt, ghi chú và ví dụ rõ) và thấy việc tự nhập câu hỏi ở C tăng công sức, trong khi Duyên và Khuê ưu tiên C vì tự chọn nội dung và hỏi linh hoạt — hai ưu tiên kéo về hai hướng ngược nhau (ít công sức so với nhiều quyền kiểm soát).

**Bài học rút ra:**

- **Dễ dùng chưa đủ để được chọn.** A thắng ở chỗ dễ bắt đầu nhưng thua ở khả năng hỏi theo ý muốn; thiết kế cần cân bằng công sức thao tác với quyền chủ động của người học.
- **Giải thích gắn với thuật ngữ có giới hạn.** Cơ chế bấm thuật ngữ trả lời tốt câu hỏi "cái này là gì", nhưng không có đường cho câu hỏi dạng so sánh, quan hệ hoặc ví dụ theo ý muốn như Khuê nêu.
- **Nội dung dựng sẵn cần rà soát độ chính xác.** Một tester nhận xét lý thuyết trong A chưa chính xác; với công cụ học tập, nội dung sai làm giảm niềm tin hơn việc thiếu tính năng.
- **Lựa chọn của người dùng chưa phải bằng chứng học tốt hơn.** Việc Khuê chọn C phản ánh ưu tiên khi thử, chưa chứng minh C giúp hiểu bài hoặc nhớ lâu hơn.

## DECIDED — Next Change

**Next Change duy nhất nhóm chốt cho vòng tiếp theo: sửa phạm vi khoanh vùng và ảnh preview của C2 để người học chọn được toàn bộ phần ảnh mong muốn, rồi kiểm thử lại.**

- **Dữ kiện dẫn tới quyết định:** Duyên chọn C2 vì muốn tự khoanh đúng phần cần hỏi, kể cả ảnh hoặc bảng, nhưng phát hiện không chọn được hết phần ảnh mong muốn. Lỗi này làm mất đúng giá trị mà người dùng chọn C2 vì nó.
- **Cách quan sát khi thử lại:** người học có tự khoanh đúng vùng không, ảnh preview có khớp phần đã khoanh không, số lần phải chọn lại; kiểm tra ở mép ảnh, toàn ảnh và các kích thước cửa sổ.
- **Hướng thử sau Next Change, chưa phải quyết định:** giảm công sức thao tác (gợi ý nhanh), chia nhỏ lời giải thích, hoàn thiện LLM. Từ phiên Khuê, tôi đề xuất thêm luồng chọn hai nội dung để hỏi so sánh lý thuyết; và rà soát nội dung giải thích của Option A theo nhận xét của Linh. Chi tiết trong [Group Feedback Synthesis](group-feedback-synthesis.md) và [Feedback Note cá nhân](prototype-feedback-note.md).

Đây là kế hoạch cho vòng tiếp theo, chưa phải thay đổi đã hoàn thành.

## STILL UNPROVEN — Những ẩn số còn lại

- Nền Day 17 còn mỏng: hai buổi phỏng vấn đã dẫn ở mục 2 đều từ một người, một bên ủng hộ và một bên thử thách giả thuyết, chưa có sự kiện cụ thể; chưa biết vấn đề đủ lớn để đáng giải quyết ở quy mô người học.
- Ba tester chưa đủ để khái quát ưu tiên C2 cho toàn bộ người học; chưa có số liệu chứng minh hiểu bài, ghi nhớ hoặc tiết kiệm thời gian tốt hơn A/B.
- Nhu cầu so sánh hai phần lý thuyết mới ghi nhận ở Khuê; chưa biết người học khác có cần không, và luồng chọn hai nội dung có được dùng thành công không.
- Chưa biết phần nội dung nào của A bị đánh giá chưa chính xác và A sau khi sửa có thay đổi lựa chọn của người học không.
- Chưa biết người học nhận ra thuật ngữ bấm được ra sao khi không có hover, ví dụ trên màn hình cảm ứng.
- Chưa ghi nhận Khuê có đối chiếu minh chứng hoặc dùng cách đóng, đổi thuật ngữ trong A hay không.
- Prototype dùng phản hồi dựng sẵn; độ chính xác của LLM thật khi xử lý ảnh, bảng, câu hỏi tự do và so sánh lý thuyết vẫn cần kiểm thử riêng.

# 6. AI Support Log

- **Công cụ AI sử dụng:** Claude (Claude Code) xuyên suốt: ở các bước trước khi dựng prototype Option A và lên ý tưởng, và ở bước này để đọc tài liệu cùng mã prototype trong repo của nhóm, kiểm tra hành vi của Option A bằng cách chạy mã, rồi soạn bản nháp bộ bài nộp cá nhân.
- **Khâu AI hỗ trợ hiệu quả:** Tổng hợp dữ kiện từ ba phiên kiểm thử của nhóm, đối chiếu mô tả Option A với mã nguồn, kiểm tra nhanh hành vi pop-up và sắp xếp nội dung theo cấu trúc bài tập.
- **Phần tôi tự chỉnh sửa:** AI suy ra từ repo rằng tôi dựng khung trang học dùng chung; tôi xác nhận không đúng và loại khỏi mục 4. AI để nhiều ô "chưa ghi nhận" trong Feedback Note; tôi xác nhận không còn ghi chép gốc nên giữ nguyên, không để AI suy diễn thêm hành vi của Khuê. Khi đối chiếu hướng dẫn nộp bài, AI chỉ ra yêu cầu đúng một Next Change; tôi quyết định Next Change của nhóm là sửa vùng chọn ảnh của C2. Các đầu ra của AI được xem là bản nháp để tôi kiểm tra trước khi dùng. Chi tiết xem [ai-support-log.md](ai-support-log.md).
