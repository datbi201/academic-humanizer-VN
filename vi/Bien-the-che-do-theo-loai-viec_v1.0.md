# Các biến thể chế độ theo loại việc học thuật — phác thảo v1.0

**Căn cứ:** quyết định **2.5-B tại cổng G1** (Đạt chốt 2026-11-22): bản v1.0 KHÔNG gộp chung các loại đề xuất/văn bản vào một chế độ; Lisa nghiên cứu và lập sẵn các biến thể riêng cho từng loại việc học thuật để tích hợp vào SKILL-VI ở bản sau (sau cổng G3). File này là **bản phác thảo nghiên cứu** — chưa phải quy tắc đang chạy trong SKILL-VI v0.2.
**Ngày lập:** 2026-11-22 · **Người lập:** Lisa.

## Nguyên tắc chung cho mọi biến thể

- Dùng chung lõi không đổi: quy trình audit → viết lại → báo cáo; không đổi số liệu/ký hiệu/trích dẫn; phân loại claim 3 loại; giữ mệnh đề mục đích/nhân quả khi hạ khẳng định (bài học issue #5); danh mục L1/L2/L3 và danh sách trắng thuật ngữ dùng chung.
- Cái khác nhau giữa các biến thể chỉ là 4 thứ: **(i) ai đọc và chấm theo tiêu chí gì, (ii) ngôn ngữ nào phải GIỮ dù ở biến thể khác sẽ bị cắt, (iii) loại khẳng định nào nhạy cảm nhất, (iv) cấu trúc văn bản chuẩn của thể loại**.
- Khi gọi skill, nêu rõ biến thể ngay trong câu lệnh (ví dụ: "áp biến thể BÁO CÁO KỸ THUẬT") — không để model tự đoán thể loại.

---

## Biến thể 1 — BÀI BÁO khoa học (paper mode)

- **Người đọc/chấm:** phản biện và biên tập tạp chí; chấm trên tính đúng, tính mới có chứng cứ, và mức khẳng định khớp dữ kiện.
- **Phải giữ:** hedging có căn cứ (L3.1); bị động trong phương pháp (L3.2); thuật ngữ chuẩn (L3.3); mọi trích dẫn và vị trí Bảng/Hình.
- **Nhạy cảm nhất:** động từ khẳng định quá mức bằng chứng (L2.1 "chứng minh" khi chỉ "cho thấy"); tính từ phóng đại không kèm số (L2.2); khẳng định không neo Bảng/Hình/trích dẫn (L2.3); nhận "đầu tiên/mới nhất" không có rà soát tài liệu (L2.x tương ứng).
- **Cấu trúc cần tôn trọng:** tóm tắt (abstract) nén cao — câu dài do nén thông tin trong abstract chỉ cảnh báo theo L1.2.6, không ép tách như thân bài; phần phương pháp cho phép câu quy trình dài (L3.9).
- **Trạng thái:** đây là chế độ gốc của SKILL-VI hiện hành (các mục ngoài Mục 8) — đã có, không phải việc mới.

## Biến thể 2 — BÁO CÁO KỸ THUẬT (technical report mode)

- **Người đọc/chấm:** chủ đầu tư/đơn vị vận hành và hội đồng nghiệm thu nội bộ; chấm trên tính truy vết được (số liệu nào, phép thử nào, tiêu chuẩn nào) và kết luận dùng được cho quyết định vận hành/bảo trì.
- **Khác bài báo ở chỗ:** ngôn ngữ "khuyến nghị hành động" là nội dung chính đáng, không phải khẳng định khoa học — không hạ mức các câu khuyến nghị có căn cứ sang dạng hedging; ngược lại, kết luận không có số đo/phép thử chống lưng phải gắn cờ mạnh hơn cả ở bài báo.
- **Phải giữ:** bị động quy trình (L3.2) ở mức cao nhất trong các biến thể; tên tiêu chuẩn, mã thiết bị, mã vòng đo (L3.4); bảng số liệu và chú thích bảng/hình nguyên trạng.
- **Nhạy cảm nhất:** kết luận trôi (không neo số liệu); lẫn lộn "quan sát được" với "suy đoán nguyên nhân"; thuật ngữ dịch máy trong mô tả hiện trường (L1.6).
- **Trạng thái:** phác thảo mới — SKILL-VI hiện hành mới nhắc báo cáo kỹ thuật trong phạm vi chung, chưa có mục riêng.

## Biến thể 3 — ĐỀ XUẤT KỸ THUẬT / HỒ SƠ THẦU (proposal mode)

- **Người đọc/chấm:** hội đồng/bên mời thầu; chấm trên tầm nhìn + tính khả thi + bằng chứng năng lực.
- **Phải giữ:** ngôn ngữ tầm nhìn và cam kết phạm vi (đây là biến thể DUY NHẤT mà ngôn ngữ tham vọng là phù hợp và được chờ đợi); số liệu năng lực có thật (dự án đã làm, nhân sự, thiết bị) giữ nguyên từng con số.
- **Nhạy cảm nhất:** khẳng định năng lực không có bằng chứng (khác với khẳng định khoa học không có dữ kiện — ở đây là rủi ro pháp lý/thương mại khi trúng thầu phải thực hiện); sáo rỗng dàn dựng (L1.1, L1.3) vì hội đồng đọc lướt và nhận ra ngay văn mẫu.
- **Trạng thái:** **đã có** — chính là Mục 8 của SKILL-VI hiện hành, và là chế độ đề xuất duy nhất của v1.0 theo quyết định 2.5-B.

## Biến thể 4 — THUYẾT MINH ĐỀ TÀI / ĐỀ XUẤT NGHIÊN CỨU KH&CN (research proposal mode)

- **Người đọc/chấm:** hội đồng khoa học xét duyệt đề tài; chấm trên **tính mới + cơ sở khoa học + tính khả thi của kế hoạch** — khác hẳn hồ sơ thầu (chấm tầm nhìn + năng lực thực hiện dịch vụ).
- **Khác hồ sơ thầu ở chỗ:** phần "tổng quan tình hình nghiên cứu" là nội dung khoa học thật, áp kỷ luật trích dẫn như bài báo; phần "mục tiêu/nội dung nghiên cứu" viết ở thì dự định — khẳng định về kết quả CHƯA có phải giữ nguyên dạng mục tiêu, tuyệt đối không viết lại thành dạng như đã đạt được (đây là lỗi trôi nghĩa ngược chiều với issue #5: nâng khẳng định thay vì hạ).
- **Phải giữ:** hedging khoa học trong phần dự báo kết quả; cấu trúc mục tiêu → nội dung → sản phẩm dự kiến; định mức/số liệu kế hoạch (kinh phí, tiến độ) nguyên trạng như số liệu.
- **Nhạy cảm nhất:** tính mới khẳng định miệng không có đối chiếu tài liệu; mục tiêu viết chung chung không đo được; lẫn giọng hồ sơ thầu (tầm nhìn thương mại) vào thuyết minh khoa học.
- **Trạng thái:** phác thảo mới theo giao việc kèm quyết định 2.5-B — tích hợp vào SKILL-VI ở bản sau G3.

## Biến thể 5 — TRẢ LỜI PHẢN BIỆN (reviewer response mode) — biến thể phụ

- **Người đọc/chấm:** chính phản biện của bài báo; chấm trên sự đầy đủ, tôn trọng và có dẫn chứng trang/dòng cho từng thay đổi.
- **Quy tắc riêng:** giọng lịch sự chuẩn mực không phải "sáo rỗng" — không áp L1.3 cho các câu cảm ơn/tiếp thu mở đầu mỗi mục; mọi câu "chúng tôi đã sửa…" phải neo được vào vị trí sửa thật trong bản thảo, không bịa thay đổi chưa làm.
- **Trạng thái:** SKILL-VI hiện hành đã nhắc trả lời phản biện trong phạm vi dùng; phác thảo này nâng thành biến thể riêng khi tích hợp.

## Biến thể 6 — TÓM TẮT / ABSTRACT song ngữ (abstract mode) — biến thể phụ

- **Đặc thù:** abstract tiếng Anh và bản tóm tắt tiếng Việt của cùng một bài phải khớp nhau từng con số và từng mức khẳng định; humanizer xử lý hai bản riêng rẽ rất dễ làm lệch mức khẳng định giữa hai ngôn ngữ.
- **Quy tắc riêng:** sửa bản nào thì kiểm tra đối chiếu bản còn lại trong cùng lượt; mức khẳng định sau sửa phải tương đương nhau; số liệu so khớp 100% trước khi trả kết quả.
- **Trạng thái:** phác thảo mới.

---

## Lộ trình tích hợp (đề xuất của Lisa, chờ Đạt duyệt khi tới việc)

1. v1.0 (hiện tại): giữ nguyên SKILL-VI với chế độ bài báo/báo cáo chung + Mục 8 hồ sơ thầu; các biến thể 2, 4, 5, 6 ở dạng phác thảo trong file này.
2. Sau cổng G3 (bench đạt): tích hợp biến thể 2 (báo cáo kỹ thuật) và 4 (thuyết minh đề tài) thành mục riêng trong SKILL-VI v0.3, vì đây là hai loại văn Đạt dùng nhiều nhất sau bài báo và hồ sơ thầu.
3. Biến thể 5, 6 tích hợp sau cùng, hoặc tách thành skill con nếu SKILL-VI phình quá dài.

*Hết v1.0.*
