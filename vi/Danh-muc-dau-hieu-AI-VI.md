# Danh mục dấu hiệu văn AI tiếng Việt — văn học thuật/kỹ thuật (v0.2)

> **Trạng thái:** v0.2 — đã qua rà soát của Đạt ở **cổng G1 (chốt ngày 2026-11-22)** với 5 quyết
> định ghi trong `Van-de-va-cong-phe-duyet_v1.1.md`. Xây từ suy luận + tương đương tiếng Việt
> của bộ 26 mẫu blader/humanizer và khung 6 lớp của Academic Humanizer, kèm các họ dấu hiệu
> riêng của tiếng Việt (Hán-Việt xếp chồng, dịch máy). **Vẫn chưa qua corpus đối chứng thật**
> (chưa có cặp văn AI ↔ văn người đã duyệt để kiểm định tần suất và tỉ lệ báo động giả) —
> các ngưỡng định lượng là mốc tạm đã được Đạt duyệt, sẽ hiệu chuẩn lại bằng số đo ở bench
> Giai đoạn 3 (cổng G3) mới được coi là chốt cuối.
>
> **Phạm vi:** bài báo, báo cáo kỹ thuật, hồ sơ đề xuất/dự thầu tiếng Việt trong lĩnh vực
> kỹ thuật (ví dụ trong file thuộc dầu khí, ăn mòn, vật liệu). Không áp cho văn phổ thông,
> blog, marketing.
>
> **Cách đọc mức độ:**
> - **CHẮC CHẮN** — dấu hiệu rõ ràng, sửa ngay khi gặp (vẫn phải qua bước audit, không sửa lặng lẽ).
> - **GỢI Ý** — chỉ xử lý khi đi kèm dấu hiệu khác trong cùng đoạn, khi mật độ cao bất thường,
>   hoặc khi người duyệt đồng ý; gặp đơn lẻ thì giữ nguyên.
>
> **Quy ước:** mỗi dấu hiệu gồm *mô tả — ví dụ SAI (văn kỹ thuật) → bản sửa — mức độ —
> khi nào KHÔNG áp dụng*. Mã hiệu (L1.x, L2.x) dùng để trích dẫn trong báo cáo thay đổi
> của SKILL-VI. Lớp L3 không phải dấu hiệu mà là danh sách **ngoại lệ phải bảo vệ**:
> gặp các cấu trúc này thì *không sửa*.

---

# LỚP L1 — DẤU HIỆU PHỔ THÔNG

## L1.1 Cấu trúc dàn dựng thay vì nói thẳng

### L1.1.1 "Không chỉ… mà còn…"
Cấu trúc song hành phủ định dùng để thổi phồng một ý bình thường thành "bước ngoặt".
- **SAI:** "Chất ức chế ăn mòn không chỉ giúp giảm tốc độ ăn mòn của thép các-bon trong môi trường CO₂ mà còn góp phần nâng cao tuổi thọ và độ tin cậy của toàn bộ hệ thống đường ống."
- **Sửa:** "Chất ức chế làm giảm tốc độ ăn mòn của thép các-bon trong môi trường CO₂ từ 2,8 xuống 0,4 mm/năm ở liều 25 ppm (Bảng 3)."
- **Mức độ:** CHẮC CHẮN khi xuất hiện ≥ 2 lần trong một đoạn hoặc đi kèm từ thổi phồng; GỢI Ý khi xuất hiện 1 lần.
- **Không áp dụng:** cấu trúc song hành mang hai nội dung kỹ thuật thật, không thể tách (ví dụ nêu hai cơ chế song song có dữ kiện riêng cho từng vế).

### L1.1.2 Câu kết đoạn một dòng gây kịch tính
Câu ngắn đứng cuối đoạn, không thêm thông tin, chỉ "chốt hạ" cảm xúc.
- **SAI:** (đoạn trình bày kết quả thử nghiệm ăn mòn) kết bằng: "Đó mới là yếu tố quyết định độ bền của đường ống."
- **Sửa:** cắt câu kết; để đoạn kết bằng dữ kiện cuối: "…tốc độ ăn mòn tại mối hàn đạt 0,35 mm/năm, thấp hơn giới hạn cho phép 0,4 mm/năm."
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** câu kết là kết luận định lượng hoặc quyết định kỹ thuật thật ("Do đó chọn phương án B.").

### L1.1.3 Câu nghe sâu mà rỗng
Mở đầu bằng khung "Về bản chất…", "Điều quan trọng là…" nhưng nội dung sau đó là hiển nhiên.
- **SAI:** "Về bản chất, điều quan trọng trong quản lý ăn mòn là phải nhìn nhận vấn đề một cách tổng thể."
- **Sửa:** "Quản lý ăn mòn đường ống cần đồng thời kiểm soát ba yếu tố: áp suất riêng phần CO₂, tốc độ dòng và liều chất ức chế."
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** câu định nghĩa thật mở đầu mục định nghĩa (xem L3.7).

### L1.1.4 Mở đầu dàn dựng kiểu hội thoại
"Thành thật mà nói…", "Vấn đề là…", "Phần khó nằm ở chỗ…" — tàn dư giọng chat lọt vào văn viết.
- **SAI:** "Thành thật mà nói, việc lựa chọn vật liệu cho đường ống dẫn khí ẩm là một bài toán không hề đơn giản."
- **Sửa:** "Việc lựa chọn vật liệu cho đường ống dẫn khí ẩm phụ thuộc chủ yếu vào áp suất riêng phần CO₂ và hàm lượng H₂S."
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** văn bản dạng phỏng vấn/hỏi–đáp có quy ước giữ giọng hội thoại.

### L1.1.5 Phản biện giả (cãi với không ai)
Dựng một ý kiến đối lập mơ hồ ("có ý kiến cho rằng…") chỉ để tự phản bác, không nguồn.
- **SAI:** "Có ý kiến cho rằng thép hợp kim thấp không thể dùng trong môi trường chua. Tuy nhiên, quan điểm này chưa hoàn toàn chính xác."
- **Sửa:** nêu nguồn thật hoặc bỏ hẳn: "Theo NACE MR0175/ISO 15156, thép hợp kim thấp vẫn dùng được trong môi trường chua nếu độ cứng không vượt 22 HRC."
- **Mức độ:** CHẮC CHẮN khi không kèm trích dẫn.
- **Không áp dụng:** phản biện có trích dẫn cụ thể — đó là tranh luận khoa học thật, phải giữ.

### L1.1.6 Mở bài dựng cảnh "Trong bối cảnh…"
Đoạn mở đầu vẽ bối cảnh thời đại chung chung, không chứa thông tin của chính văn bản.
- **SAI:** "Trong bối cảnh ngành dầu khí đang không ngừng phát triển và hội nhập sâu rộng, vấn đề ăn mòn đường ống ngày càng trở nên cấp thiết hơn bao giờ hết."
- **Sửa:** vào thẳng vấn đề cụ thể: "Đường ống tại mỏ X ghi nhận tốc độ ăn mòn cục bộ tới 3,1 mm/năm tại các vị trí đọng nước, gấp 8 lần giá trị thiết kế."
- **Mức độ:** CHẮC CHẮN ở đoạn mở đầu.
- **Không áp dụng:** phần đặt vấn đề của hồ sơ thầu, nơi bối cảnh dự án là nội dung được yêu cầu (xem chế độ đề xuất trong SKILL-VI).

## L1.2 Nhịp điệu theo công thức

### L1.2.1 Bộ ba cưỡng bức
Ép ý thành đúng ba mục song hành cho "tròn trịa", dù nội dung chỉ có một hoặc hai ý có dữ kiện.
- **SAI:** "Phương pháp bảo vệ ca-tốt mang lại hiệu quả cao, chi phí hợp lý và thi công thuận tiện cho đường ống ngầm."
- **Sửa:** giữ đúng số ý có dữ kiện: "Bảo vệ ca-tốt giữ điện thế thép ở −0,95 V (điện cực so sánh Cu/CuSO₄) và có chi phí vận hành thấp hơn khoảng 40% so với phương án thay đoạn ống."
- **Mức độ:** GỢI Ý; CHẮC CHẮN khi cả ba vế đều là tính từ chung chung không số liệu.
- **Không áp dụng:** liệt kê đúng ba hạng mục thật của nội dung (xem L3.8).

### L1.2.2 Mở đầu câu lặp lại máy móc
Nhiều câu liên tiếp mở đầu bằng cùng một cụm, nhịp đơn điệu kiểu điền mẫu.
- **SAI:** "Kết quả cho thấy tốc độ ăn mòn tăng theo nhiệt độ. Kết quả cho thấy ảnh hưởng của pH là rõ rệt. Kết quả cho thấy lưu lượng dòng có tác động không đáng kể."
- **Sửa:** "Tốc độ ăn mòn tăng theo nhiệt độ và giảm khi pH tăng; lưu lượng dòng ảnh hưởng không đáng kể (Hình 4)."
- **Mức độ:** GỢI Ý; CHẮC CHẮN khi ≥ 3 câu liên tiếp cùng một mở đầu.
- **Không áp dụng:** cấu trúc song hành có chủ ý trong bảng tóm tắt/kết luận từng mục theo mẫu của tạp chí.

### L1.2.3 Gạch ngang dài "—" làm khớp nối vạn năng
Dùng "—" để nối mọi loại quan hệ (giải thích, liệt kê, nhấn mạnh) thay cho dấu câu đúng chức năng. *Yếu khi đứng một mình.*
- **SAI:** "Thép X65 — loại thép được sử dụng rộng rãi trong ngành — cho thấy khả năng chống ăn mòn tốt — đặc biệt trong môi trường CO₂ — khi được xử lý bề mặt đúng cách."
- **Sửa:** "Thép X65 cho thấy khả năng chống ăn mòn tốt trong môi trường CO₂ khi được xử lý bề mặt đúng cách."
- **Mức độ:** GỢI Ý (chỉ xử lý khi mật độ cao hoặc đi kèm dấu hiệu khác).
- **Không áp dụng:** gạch ngang trong khoảng giá trị (0,2–0,5 mm/năm), trong tên gọi ghép đã quy ước, hoặc một lần dùng đúng giọng tác giả.

### L1.2.4 Từ hạn định chồng chất
Xếp nhiều lớp "có thể / có khả năng / được cho là / có xu hướng" trong một câu đến mức câu mất nghĩa.
- **SAI:** "Có thể có khả năng mẫu thép bị cho là có xu hướng xuất hiện ăn mòn điểm trong một số điều kiện nhất định."
- **Sửa:** giữ một lớp hạn định có căn cứ: "Mẫu thép có thể xuất hiện ăn mòn điểm khi hàm lượng clorua vượt 5.000 ppm."
- **Mức độ:** CHẮC CHẮN khi ≥ 3 lớp hạn định trong một câu.
- **Không áp dụng:** hedging có căn cứ dữ kiện (xem L3.1) — chỉ bỏ phần chồng thừa, không bỏ lớp hạn định đúng.

### L1.2.5 Gạch nối xếp chồng kiểu Anh
Nối chuỗi tính từ bằng gạch nối theo cú pháp tiếng Anh, xa lạ với tiếng Việt.
- **SAI:** "lớp phủ epoxy-tăng-cường-sợi-thuỷ-tinh-chất-lượng-cao"
- **Sửa:** "lớp phủ epoxy tăng cường sợi thuỷ tinh chất lượng cao"
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** gạch nối trong từ phiên âm/thuật ngữ đã quy ước (ví dụ "ca-tốt" trong "bảo vệ ca-tốt") và trong ký hiệu, mã hiệu.

### L1.2.6 Câu dài chất mệnh đề
Một câu kéo dài qua nhiều mệnh đề phụ chằng chịt, người đọc phải đọc lại mới nắm được ý chính.
- **SAI:** "Mẫu thép sau khi được lấy từ hiện trường nơi đường ống đã vận hành trong điều kiện áp suất cao và nhiệt độ cao với sự hiện diện đồng thời của CO₂ và H₂S trong thời gian dài được đưa về phòng thí nghiệm để phân tích thành phần hoá học và đánh giá mức độ ăn mòn bằng các phương pháp hiện đại."
- **Sửa:** "Mẫu thép được lấy từ đoạn ống đã vận hành dài ngày ở áp suất và nhiệt độ cao, có đồng thời CO₂ và H₂S. Tại phòng thí nghiệm, mẫu được phân tích thành phần hoá học và đánh giá mức độ ăn mòn."
- **Mức độ:** **CẢNH BÁO + gợi ý sửa** khi câu **dài hơn 40 từ** (ngưỡng Đạt chốt ở G1,
  2026-11-22 — thay ngưỡng ~60 từ của v0.1): khi gắn cờ phải kèm gợi ý tách câu cụ thể,
  không chỉ báo dài; CHẮC CHẮN khi có ≥ 4 mệnh đề phụ. Câu dài do liệt kê điều kiện thử
  nghiệm/thông số (L3.9) chỉ cảnh báo, không tự tách.
- **Không áp dụng:** câu liệt kê điều kiện thử nghiệm mà tách câu làm đứt liên hệ điều kiện–kết quả (xem L3.9).

### L1.2.7 Từ nối mở đầu câu liên tiếp
Hơn nữa / Bên cạnh đó / Ngoài ra / Thêm vào đó… mở đầu hàng loạt câu liên tiếp thay cho quan hệ logic thật.
- **SAI:** "Hơn nữa, màng ức chế bền ở 80 °C. Bên cạnh đó, nó không ảnh hưởng tới quá trình tách nước. Ngoài ra, chi phí hoá phẩm ở mức chấp nhận được."
- **Sửa:** "Màng ức chế bền ở 80 °C, không ảnh hưởng tới quá trình tách nước, và chi phí hoá phẩm ở mức chấp nhận được."
- **Mức độ:** GỢI Ý; CHẮC CHẮN khi ≥ 3 câu liên tiếp trong một đoạn.
- **Không áp dụng:** từ nối mang quan hệ logic thật và phân biệt được (nguyên nhân–kết quả, tương phản) dùng thưa.

## L1.3 Thổi phồng và mượn uy tín

### L1.3.1 Từ vựng "AI" lạm dụng trong tiếng Việt
Nhóm từ nghe trang trọng nhưng rỗng, xuất hiện với mật độ bất thường: *đi sâu khám phá, tận dụng (khi chỉ là đệm), đóng vai trò, góp phần, bối cảnh, thể hiện, khẳng định vị thế, mở ra hướng đi mới*.
- **SAI:** "Nghiên cứu đi sâu khám phá cơ chế ăn mòn, qua đó tận dụng tối đa tiềm năng của vật liệu trong bối cảnh vận hành khắc nghiệt."
- **Sửa:** "Nghiên cứu xác định cơ chế ăn mòn chủ đạo của thép X65 ở 60 °C và áp suất riêng phần CO₂ bằng 2 bar."
- **Mức độ:** GỢI Ý theo mật độ (đánh dấu khi nhiều từ trong nhóm cùng xuất hiện trong một đoạn).
- **Không áp dụng:** từ dùng đúng nghĩa kỹ thuật cụ thể ("tận dụng nhiệt thải để gia nhiệt dầu") — giữ nguyên.

### L1.3.2 Thổi phồng tầm quan trọng
"đánh dấu bước ngoặt", "mở ra kỷ nguyên mới", "có ý nghĩa vô cùng to lớn", "chưa từng có tiền lệ" gắn cho kết quả thường.
- **SAI:** "Kết quả này đánh dấu một bước ngoặt mang tính cách mạng trong lĩnh vực chống ăn mòn đường ống."
- **Sửa:** "Kết quả này cho phép giảm liều chất ức chế từ 40 xuống 25 ppm mà tốc độ ăn mòn vẫn dưới 0,1 mm/năm."
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** phát biểu tầm nhìn trong hồ sơ đề xuất (xem chế độ L6 trong SKILL-VI) và trường hợp có căn cứ so sánh cụ thể đi kèm.

### L1.3.3 Liên hệ mơ hồ
Khẳng định "có liên quan", "gắn liền với", "chịu tác động của nhiều yếu tố" mà không nêu yếu tố nào, quan hệ gì.
- **SAI:** "Tốc độ ăn mòn có liên quan mật thiết đến nhiều yếu tố khác nhau trong quá trình vận hành."
- **Sửa:** "Tốc độ ăn mòn phụ thuộc vào áp suất riêng phần CO₂, nhiệt độ và tốc độ dòng (Mục 3.2)."
- **Mức độ:** CHẮC CHẮN khi câu đứng một mình và không mang thông tin.
- **Không áp dụng:** câu chuyển đoạn có đoạn sau liệt kê ngay các yếu tố.

### L1.3.4 Đuôi câu nông kiểu "…, qua đó khẳng định…"
Mệnh đề cuối câu chỉ lặp lại ý chính bằng từ trang trọng hơn, giả vờ rút ra hệ quả.
- **SAI:** "Hàm lượng FeCO₃ trong cặn tăng theo thời gian phơi mẫu, qua đó khẳng định vai trò bảo vệ của lớp cặn đối với bề mặt thép."
- **Sửa:** "Hàm lượng FeCO₃ trong cặn tăng theo thời gian phơi mẫu; tốc độ ăn mòn giảm tương ứng từ 1,9 xuống 0,6 mm/năm (Hình 5)."
- **Mức độ:** GỢI Ý.
- **Không áp dụng:** mệnh đề cuối mang hệ quả định lượng hoặc điều kiện áp dụng thật.

### L1.3.5 Ngôn ngữ bán hàng trong văn kỹ thuật
"giải pháp hàng đầu", "đẳng cấp quốc tế", "đáp ứng mọi yêu cầu khắt khe nhất", "ưu việt vượt trội" — giọng quảng cáo trong bài báo/báo cáo.
- **SAI:** "Đây là giải pháp chống ăn mòn tiên tiến hàng đầu với hiệu quả vượt trội, đáp ứng mọi yêu cầu khắt khe nhất của ngành."
- **Sửa:** "Phương án phủ epoxy 3 lớp đạt tuổi thọ thiết kế 25 năm theo ISO 12944 cho môi trường C5."
- **Mức độ:** CHẮC CHẮN trong bài báo và báo cáo kỹ thuật.
- **Không áp dụng:** phần giới thiệu năng lực trong hồ sơ thầu — xử lý theo chế độ đề xuất (L6), không áp lớp này máy móc.

### L1.3.6 Mượn uy tín không nguồn
"Các chuyên gia đều cho rằng…", "Theo nhiều nghiên cứu…", "Thực tiễn đã chứng minh…" mà không có trích dẫn.
- **SAI:** "Các chuyên gia trong ngành đều thừa nhận rằng ăn mòn dưới lớp cách nhiệt là mối nguy hiểm tiềm ẩn lớn nhất đối với nhà máy."
- **Sửa:** gắn nguồn thật: "Theo khảo sát tại các nhà máy lọc dầu của [tác giả, năm], ăn mòn dưới lớp cách nhiệt (CUI) là nguyên nhân của phần lớn sự cố rò rỉ tại các vị trí có cách nhiệt." — không có nguồn thì cắt câu.
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** phát biểu thuộc kiến thức nền chung của ngành và không mang tính khẳng định định lượng.

### L1.3.7 Tránh động từ "là / có"
Vòng vo bằng "đóng vai trò là", "sở hữu", "thực hiện chức năng của" thay cho "là", "có" đơn giản.
- **SAI:** "Lớp cặn FeCO₃ đóng vai trò là một hàng rào bảo vệ sở hữu khả năng ngăn cản quá trình khuếch tán."
- **Sửa:** "Lớp cặn FeCO₃ là hàng rào ngăn khuếch tán ion Fe²⁺ khỏi bề mặt thép."
- **Mức độ:** GỢI Ý.
- **Không áp dụng:** "đóng vai trò" dùng đúng khi nói về chức năng trong hệ thống có nhiều thành phần và cần phân biệt vai trò/chức danh.

## L1.4 Định dạng theo công thức

### L1.4.1 In đậm trang trí đầu câu
"**Nhãn:**" mở đầu câu/đoạn trong thân bài, sau đó lặp lại chính nhãn đó.
- **SAI:** "**Tốc độ ăn mòn:** Tốc độ ăn mòn của mẫu tăng nhanh sau 72 giờ phơi."
- **Sửa:** "Tốc độ ăn mòn của mẫu tăng nhanh sau 72 giờ phơi."
- **Mức độ:** CHẮC CHẮN trong thân bài.
- **Không áp dụng:** in đậm là quy định trình bày của mẫu tài liệu/tạp chí (đề mục, nhãn trường trong biểu mẫu, nhãn Bảng/Hình).

### L1.4.2 Tiêu đề, nhãn trang trí bằng ký hiệu
Emoji, mũi tên, ký hiệu trang trí chèn vào tiêu đề và nhãn bước.
- **SAI:** "🚀 Kết quả thử nghiệm:" / "➤ Bước 1: Chuẩn bị mẫu"
- **Sửa:** "Kết quả thử nghiệm:" / "Bước 1: Chuẩn bị mẫu."
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** ký hiệu kỹ thuật có nghĩa quy ước (⚠ trong cảnh báo an toàn theo mẫu tài liệu HSE).

### L1.4.3 Lạm dụng ngoặc kép cho thuật ngữ thông thường
Đặt mọi thuật ngữ quen thuộc vào ngoặc kép khiến văn bản lốm đốm và gợi ý nghĩa bóng không có thật.
- **SAI:** "Hiện tượng "ăn mòn" xảy ra tại "vùng hàn" khiến "tuổi thọ" của ống giảm rõ rệt."
- **Sửa:** "Ăn mòn tại vùng hàn làm giảm rõ rệt tuổi thọ của ống."
- **Mức độ:** GỢI Ý.
- **Không áp dụng:** ngoặc kép đúng quy ước — trích nguyên văn, thuật ngữ mới được định nghĩa lần đầu, tên gọi quy ước nội bộ.

### L1.4.4 Lạm dụng gạch đầu dòng trong thân bài
Mọi ý diễn giải đều bị chặt thành gạch đầu dòng, mất mạch lập luận của văn xuôi.
- **SAI:** đoạn phân tích nguyên nhân hư hỏng trình bày thành 6 gạch đầu dòng rời rạc, mỗi dòng một mẩu ý.
- **Sửa:** chuyển phần diễn giải thành văn xuôi có quan hệ nguyên nhân–kết quả; chỉ giữ danh sách cho liệt kê thật (thông số, bước quy trình, danh mục thiết bị).
- **Mức độ:** GỢI Ý.
- **Không áp dụng:** danh sách là định dạng đúng của nội dung (quy trình thao tác, bảng thông số dạng liệt kê theo mẫu).

## L1.5 Tàn dư chat và bản nháp

### L1.5.1 Tàn dư chatbot
Câu chào, câu mời, lời chúc của giao diện chat lọt nguyên vào văn bản: "Dưới đây là…", "Hy vọng hữu ích!", "Bạn có muốn tôi… không?"
- **SAI:** "Dưới đây là phân tích về cơ chế ăn mòn CO₂. Hy vọng nội dung này hữu ích cho bạn!"
- **Sửa:** cắt toàn bộ khung, bắt đầu thẳng vào nội dung: "Cơ chế ăn mòn CO₂ gồm ba giai đoạn…"
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** không có ngoại lệ trong văn học thuật/kỹ thuật.

### L1.5.2 Câu thoái thác giới hạn kiến thức
"Dù dữ liệu còn hạn chế, có vẻ như…", "Tính đến thời điểm hiện tại…" — thoái thác thay cho việc nói rõ thiếu dữ kiện gì.
- **SAI:** "Mặc dù dữ liệu còn hạn chế, có vẻ như thép 13Cr là lựa chọn phù hợp trong trường hợp này."
- **Sửa:** "Dữ kiện hiện có (hai đợt khảo sát 2023–2024) chưa đủ để kết luận; cần bổ sung kết quả thử nghiệm ngâm mẫu trước khi chọn thép 13Cr."
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** phần "hạn chế của nghiên cứu" viết đúng chuẩn — nêu cụ thể hạn chế và ảnh hưởng của nó (đó là nội dung khoa học, phải giữ).

### L1.5.3 Câu đầu lặp lại tiêu đề
Câu mở đầu mục chỉ nhắc lại tiêu đề mục bằng một khẳng định chung chung.
- **SAI:** Mục "3.2. Ảnh hưởng của nhiệt độ" mở đầu: "Nhiệt độ có ảnh hưởng quan trọng đến tốc độ ăn mòn."
- **Sửa:** vào thẳng dữ kiện: "Khi nhiệt độ tăng từ 40 lên 80 °C, tốc độ ăn mòn tăng từ 0,8 lên 2,3 mm/năm."
- **Mức độ:** GỢI Ý.
- **Không áp dụng:** câu mở đầu là câu chủ đề mang thông tin mới (không chỉ lặp tiêu đề).

### L1.5.4 Viết về tài liệu thay vì về chủ đề
Câu meta kể về chính văn bản ("Phần này sẽ phân tích…", "Bảng dưới đây trình bày…" lặp ở mọi bảng) thay vì nói về đối tượng.
- **SAI:** "Phần này sẽ đi sâu phân tích ảnh hưởng của pH đến quá trình ăn mòn." và mọi bảng đều mở bằng "Bảng dưới đây trình bày kết quả…"
- **Sửa:** "pH quyết định dạng cặn cacbonat hình thành trên bề mặt thép, qua đó quyết định mức độ bảo vệ của lớp cặn."
- **Mức độ:** GỢI Ý.
- **Không áp dụng:** câu dẫn bảng/hình theo quy ước của tạp chí, dùng thưa và không lặp máy móc; mục lục và phần giới thiệu cấu trúc báo cáo theo mẫu bắt buộc.

### L1.5.5 Kết luận mẫu rỗng
Kết luận mở bằng "Tóm lại, có thể khẳng định rằng…" rồi lặp lại tầm quan trọng chung chung, không có kết quả cụ thể.
- **SAI:** "Tóm lại, có thể khẳng định rằng ăn mòn là vấn đề quan trọng cần được quan tâm đúng mức trong vận hành đường ống."
- **Sửa:** "Ở điều kiện giếng X, thép các-bon L80 kết hợp chất ức chế liều 25 ppm đáp ứng tuổi thọ thiết kế 20 năm; phương án thép 13Cr là không cần thiết."
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** câu tóm tắt có chứa kết quả/khuyến nghị cụ thể — chỉ bỏ khung mở đầu sáo rỗng.

## L1.6 Dịch máy / tiếng Anh hoá (translationese)

### L1.6.1 "được trang bị với"
Dịch sát "equipped with" — tiếng Việt không nói "trang bị với".
- **SAI:** "Đường ống được trang bị với hệ thống giám sát ăn mòn trực tuyến."
- **Sửa:** "Đường ống được lắp hệ thống giám sát ăn mòn trực tuyến."
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** không có ngoại lệ; đây là lỗi diễn đạt thuần tuý.

### L1.6.2 "dựa trên cơ sở của"
Dịch chồng "based on the basis of" — hai lớp "dựa/cơ sở" cùng nghĩa.
- **SAI:** "Dựa trên cơ sở của các kết quả thử nghiệm, nhóm tác giả đề xuất thay đổi chế độ vận hành."
- **Sửa:** "Dựa trên kết quả thử nghiệm, nhóm tác giả đề xuất thay đổi chế độ vận hành."
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** "cơ sở" là danh từ có nghĩa riêng trong câu ("cơ sở dữ liệu", "cơ sở lý thuyết của phương pháp").

### L1.6.3 Chủ ngữ "nó / điều này" thừa mở câu
Dịch sát đại từ "it/this" của tiếng Anh khiến câu nào cũng mở bằng "Nó…", "Điều này…".
- **SAI:** "Ăn mòn điểm là dạng hư hỏng nguy hiểm. Nó thường khởi phát tại các tạp chất sunfua. Điều này khiến việc phát hiện sớm trở nên khó khăn."
- **Sửa:** "Ăn mòn điểm thường khởi phát tại các tạp chất sunfua nên khó phát hiện sớm."
- **Mức độ:** GỢI Ý.
- **Không áp dụng:** "điều này" chỉ đúng một mệnh đề ngay trước trong lập luận chặt chẽ, dùng thưa.

### L1.6.4 Bị động "được / bị" ở nơi tiếng Việt dùng chủ động
Dịch sát cấu trúc bị động tiếng Anh, kể cả khi tác nhân có mặt ngay trong câu ("bởi…").
- **SAI:** "Áp suất thử được tăng lên một cách từ từ bởi kỹ thuật viên cho đến khi đạt giá trị yêu cầu."
- **Sửa:** "Kỹ thuật viên tăng áp suất thử từ từ đến giá trị yêu cầu."
- **Mức độ:** GỢI Ý.
- **Không áp dụng:** bị động hợp lệ trong văn quy phạm/quy trình khi tác nhân không quan trọng (xem L3.2) — đây là ranh giới phải xét từng câu, không sửa hàng loạt.

### L1.6.5 "một cách" + tính từ (dịch trạng từ -ly)
Mọi trạng từ đều thành "một cách + tính từ", nặng nề và đơn điệu.
- **SAI:** "Hệ thống vận hành một cách ổn định và quá trình ăn mòn diễn ra một cách đồng đều trên toàn bộ bề mặt."
- **Sửa:** "Hệ thống vận hành ổn định và ăn mòn diễn ra đồng đều trên toàn bộ bề mặt."
- **Mức độ:** CHẮC CHẮN khi ≥ 2 lần trong một đoạn; GỢI Ý khi 1 lần.
- **Không áp dụng:** "một cách" mang nghĩa phương thức thật ("đo một cách gián tiếp", "kiểm tra một cách định kỳ" — trường hợp sau vẫn nên xét rút thành "định kỳ kiểm tra").

### L1.6.6 "thông qua việc" và cụm giới từ dịch máy
"thông qua việc + danh từ hoá", "trong quá trình của + …" — vòng vo thay cho giới từ/cách diễn đạt trực tiếp.
- **SAI:** "Độ kín của mặt bích được kiểm tra thông qua việc thử áp bằng khí nitơ trong quá trình của đợt bảo dưỡng."
- **Sửa:** "Độ kín của mặt bích được kiểm tra bằng thử áp khí nitơ trong đợt bảo dưỡng."
- **Mức độ:** GỢI Ý.
- **Không áp dụng:** "thông qua" dùng đúng nghĩa kênh/phương tiện ("truyền dữ liệu thông qua mạng SCADA").

---

# LỚP L2 — DẤU HIỆU RIÊNG CHO VĂN HỌC THUẬT / KỸ THUẬT

> Lớp này là phần khác biệt cốt lõi so với humanizer phổ thông: vấn đề không chỉ là
> "nghe giống AI" mà là **mức khẳng định vượt quá bằng chứng**. Với các dấu hiệu thuộc
> nhóm khẳng định (L2.1–L2.4, L2.9), người biên tập *không tự bịa số liệu để lấp vào*:
> nếu văn bản không có số, gắn cờ báo tác giả ở bước báo cáo.

## L2.1 Động từ khẳng định quá mức bằng chứng
"chứng minh", "khẳng định chắc chắn", "đảm bảo", "cho thấy một cách rõ ràng và không thể chối cãi" dùng cho kết quả thực nghiệm có phạm vi hẹp.
- **SAI:** "Kết quả thử nghiệm chứng minh rằng chất ức chế X là hiệu quả nhất cho mọi điều kiện vận hành."
- **Sửa:** "Kết quả thử nghiệm cho thấy chất ức chế X đạt hiệu quả bảo vệ 92% ở 60 °C và áp suất riêng phần CO₂ bằng 2 bar, cao nhất trong ba loại được khảo sát."
- **Mức độ:** CHẮC CHẮN (cờ đỏ bắt buộc rà soát ở bước audit).
- **Không áp dụng:** "chứng minh" trong toán học/lý thuyết (chứng minh định lý); khẳng định có kiểm định đầy đủ và quy ước của tạp chí cho phép — dù vậy vẫn ưu tiên "cho thấy".

## L2.2 "Đáng kể / rõ rệt" không kèm số hoặc kiểm định
Từ chỉ mức độ đứng thay cho con số; người đọc không biết "đáng kể" là bao nhiêu.
- **SAI:** "Tốc độ ăn mòn giảm đáng kể khi tăng liều chất ức chế."
- **Sửa:** "Tốc độ ăn mòn giảm từ 2,8 xuống 0,9 mm/năm khi liều chất ức chế tăng từ 10 lên 25 ppm."
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** câu dẫn ý có đoạn/bảng ngay sau trình bày số liệu; "có ý nghĩa thống kê" khi đi kèm tên kiểm định và giá trị p.

## L2.3 Tính từ phóng đại không neo số liệu
"vượt trội", "đột phá", "ưu việt", "ấn tượng" gắn cho vật liệu/phương pháp mà không có chênh lệch định lượng.
- **SAI:** "Vật liệu mới thể hiện khả năng chống ăn mòn vượt trội và đột phá so với thép thông thường."
- **Sửa:** "Ở cùng điều kiện thử nghiệm, tốc độ ăn mòn của vật liệu mới là 0,12 mm/năm, bằng 1/6 so với thép các-bon (0,74 mm/năm)."
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** phần tầm nhìn của hồ sơ đề xuất (chế độ L6) — và ngay cả ở đó, tính từ phóng đại phải đi kèm cam kết/kế hoạch cụ thể.

## L2.4 Khẳng định không neo vào Bảng / Hình / trích dẫn
Kết luận định lượng hoặc so sánh được nêu trơn, không chỉ ra bằng chứng nằm ở đâu trong văn bản.
- **SAI:** "Ăn mòn tại vùng ảnh hưởng nhiệt của mối hàn nghiêm trọng hơn hẳn vùng kim loại cơ bản."
- **Sửa:** "Ăn mòn tại vùng ảnh hưởng nhiệt của mối hàn cao hơn 1,8 lần so với vùng kim loại cơ bản (Bảng 5, Hình 7)."
- **Mức độ:** CHẮC CHẮN — dưới dạng *cờ báo cáo*: nếu văn bản không có số, ghi vào báo cáo thay đổi để tác giả bổ sung, tuyệt đối không tự điền số.
- **Không áp dụng:** khẳng định là kiến thức nền được trích dẫn ở câu/bối cảnh liền trước.

## L2.5 Cường điệu tính mới
"lần đầu tiên", "hoàn toàn mới", "chưa từng có", "theo hiểu biết của chúng tôi" dùng lặp lại hoặc không kiểm chứng được.
- **SAI:** "Đây là lần đầu tiên trên thế giới một phương pháp hoàn toàn mới được đề xuất để đánh giá ăn mòn đường ống."
- **Sửa:** "Phương pháp đề xuất khác với [12] ở chỗ dùng đồng thời tín hiệu điện thế và dòng ăn mòn để xác định thời điểm màng ức chế mất hiệu lực."
- **Mức độ:** GỢI Ý; CHẮC CHẮN khi lặp ≥ 2 lần trong một mục hoặc khi khẳng định "đầu tiên" không có rà soát tài liệu đi kèm.
- **Không áp dụng:** tuyên bố tính mới có rà soát tài liệu hệ thống chứng minh và là yêu cầu của tạp chí.

## L2.6 Phạm vi mơ hồ thay cho liệt kê
"toàn diện", "hàng loạt", "vô số", "đa dạng", "nhiều loại khác nhau" đứng thay cho danh sách cụ thể vốn có thể liệt kê.
- **SAI:** "Nghiên cứu tiến hành khảo sát toàn diện trên hàng loạt loại thép khác nhau."
- **Sửa:** "Nghiên cứu khảo sát bốn mác thép: X52, X65, L80 và 13Cr."
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** phạm vi thật sự không liệt kê được (khảo sát hiện trường diện rộng) — khi đó nêu tiêu chí chọn mẫu thay cho danh sách.

## L2.7 Hedging mơ hồ thay cho con số
"tương đối cao", "khá lớn", "ở mức độ nhất định", "phần nào" — mơ hồ giả vờ thận trọng, khác hẳn hedging có căn cứ.
- **SAI:** "Tốc độ ăn mòn ở mức tương đối cao và khá nhạy với nhiệt độ."
- **Sửa:** "Tốc độ ăn mòn đạt 1,6–2,1 mm/năm và tăng khoảng gấp đôi khi nhiệt độ tăng từ 50 lên 70 °C."
- **Mức độ:** GỢI Ý.
- **Không áp dụng:** hedging chỉ xu hướng chưa lượng hoá được và văn bản nói rõ lý do chưa lượng hoá (xem L3.1).

## L2.8 Khung nhấn mạnh sáo rỗng kiểu học thuật
"Cần nhấn mạnh rằng…", "Đáng lưu ý là…", "Điều quan trọng cần chỉ ra là…" — khung đệm không thêm thông tin; câu sau nó phải tự đứng được.
- **SAI:** "Cần nhấn mạnh rằng, đáng lưu ý là, tốc độ ăn mòn tăng mạnh khi xuất hiện H₂S trong dòng khí."
- **Sửa:** "Tốc độ ăn mòn tăng từ 0,5 lên 1,7 mm/năm khi H₂S xuất hiện trong dòng khí."
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** nhấn mạnh an toàn theo mẫu tài liệu vận hành/HSE, nơi câu cảnh báo được quy định phải nổi bật.

## L2.9 Đổ trích dẫn (citation dumping)
Một khẳng định chung chung gánh cả chùm trích dẫn [3, 7, 9, 12, 15] mà không nói nguồn nào nói gì.
- **SAI:** "Nhiều phương pháp đánh giá ăn mòn đã được đề xuất [3, 7, 9, 12, 15]."
- **Sửa:** "Phương pháp gần nhất với nghiên cứu này là của [7], dùng điện trở phân cực tuyến tính; điểm khác biệt của chúng tôi là hiệu chuẩn theo hàm lượng Fe²⁺ trong dung dịch."
- **Mức độ:** GỢI Ý.
- **Không áp dụng:** câu tổng quan có bảng tổng hợp tài liệu đi kèm phân loại từng nguồn ngay sau đó.

## L2.10 Danh sách đóng góp sáo rỗng
Mục đóng góp lặp lại tóm tắt bằng từ chung chung: "phương pháp mới", "thực nghiệm toàn diện", "kết quả tốt".
- **SAI:** "Đóng góp của bài báo: (1) đề xuất mô hình mới; (2) tiến hành thực nghiệm toàn diện; (3) thu được kết quả tốt."
- **Sửa:** "(1) Xây dựng mô hình dự báo tốc độ ăn mòn CO₂ với sai số ±15% trên 214 điểm dữ liệu hiện trường; (2) xác định ngưỡng áp suất riêng phần CO₂ bằng 3 bar, tại đó cơ chế chuyển từ ăn mòn đều sang ăn mòn cục bộ."
- **Mức độ:** CHẮC CHẮN.
- **Không áp dụng:** mẫu hồ sơ/tạp chí quy định cấu trúc đóng góp riêng — vẫn phải điền kết quả cụ thể vào từng mục.

## L2.11 Hán-Việt xếp chồng, danh từ hoá nặng
Chuỗi "tiến hành thực hiện việc…", "sự + danh từ + của…", "nhằm mục đích…" khiến câu nặng và mờ tác nhân.
- **SAI:** "Nhóm nghiên cứu tiến hành thực hiện việc kiểm tra đánh giá sự gia tăng của tốc độ ăn mòn trong quá trình vận hành của đường ống."
- **Sửa:** "Nhóm nghiên cứu kiểm tra tốc độ ăn mòn của đường ống tăng trong quá trình vận hành."
- **Mức độ:** CHẮC CHẮN theo mật độ (≥ 2 cụm xếp chồng trong một câu).
- **Không áp dụng:** thuật ngữ Hán-Việt đã chuẩn hoá và không có tương đương thuần Việt tương đương về nghĩa ("thử nghiệm", "đánh giá rủi ro", "ăn mòn điện hoá") — giữ nguyên, xem L3.3.

## L2.12 Mở bài học thuật theo mẫu
"Trong những năm gần đây, X ngày càng thu hút sự quan tâm của các nhà khoa học…" — mở đầu bài báo bằng câu thời sự chung thay cho khoảng trống tri thức.
- **SAI:** "Trong những năm gần đây, ăn mòn đường ống dầu khí ngày càng thu hút sự quan tâm của nhiều nhà khoa học trong và ngoài nước."
- **Sửa:** "Các mô hình dự báo ăn mòn CO₂ hiện hành chưa tính đến ảnh hưởng của lớp cặn FeCO₃ ở nhiệt độ trên 90 °C — khoảng trống mà nghiên cứu này xử lý."
- **Mức độ:** CHẮC CHẮN ở đoạn mở đầu bài báo/báo cáo.
- **Không áp dụng:** bài tổng quan (review) có mục đích điểm lại diễn biến lĩnh vực — khi đó câu thời sự phải kèm mốc và trích dẫn cụ thể.

## L2.13 So sánh với đối chứng yếu hoặc không nêu tên
"cao hơn hẳn phương pháp thông thường", "tốt hơn các phương pháp hiện có" — chọn đối chứng mờ để thắng dễ.
- **SAI:** "Mô hình đề xuất cho độ chính xác cao hơn hẳn các phương pháp thông thường."
- **Sửa:** "So với mô hình de Waard–Milliams — đối chứng đang dùng tại mỏ X — mô hình đề xuất giảm sai số dự báo từ 38% xuống 17%."
- **Mức độ:** GỢI Ý (dạng cờ báo cáo khi không xác định được đối chứng trong văn bản).
- **Không áp dụng:** so sánh với giới hạn quy định của tiêu chuẩn (ví dụ "thấp hơn giới hạn 0,4 mm/năm theo tiêu chuẩn dự án") — đó là đối chứng có tên và có căn cứ.

## L2.14 Chèn tiếng Anh trang trí khi đã có thuật ngữ Việt chuẩn
Trộn từ tiếng Anh phổ thông (approach, performance, innovative…) vào câu tiếng Việt dù có tương đương chuẩn, làm văn bản lai tạp không nhất quán.
- **SAI:** "Approach của nghiên cứu mang tính innovative, tập trung đánh giá performance của vật liệu trong môi trường sour service."
- **Sửa:** "Nghiên cứu tiếp cận theo hướng đánh giá tính năng vận hành của vật liệu trong môi trường chua (sour service)."
- **Mức độ:** GỢI Ý.
- **Không áp dụng:** thuật ngữ tiếng Anh đã quy ước quốc tế và được giới chuyên môn dùng nguyên dạng (pitting, SSC, sour service) — giữ nguyên và dùng nhất quán trong toàn văn bản; xem L3.3. **Danh sách bảo vệ chốt cứng nằm ở file đi kèm `Danh-sach-trang-thuat-ngu_v1.0.md`** (quyết định 2.3-A, cổng G1): thuật ngữ có trong danh sách trắng thì không gắn cờ, ngoài danh sách mới xét L2.14.

---

# LỚP L3 — NGOẠI LỆ PHẢI BẢO VỆ (KHÔNG SỬA)

> Các cấu trúc dưới đây *trông giống* dấu hiệu AI nhưng là quy ước đúng của văn học
> thuật/kỹ thuật tiếng Việt. Humanizer phổ thông thường "sửa" hỏng chúng. Nguyên tắc:
> **gặp thì giữ nguyên**; nếu nghi ngờ, ghi vào báo cáo dạng câu hỏi cho tác giả, không tự sửa.

## L3.1 Hedging có căn cứ dữ kiện
"có thể", "có xu hướng", "gợi ý rằng", "nhất quán với", "chưa loại trừ khả năng" — khi dữ kiện thật sự chưa cho phép kết luận mạnh hơn.
- **Giữ nguyên:** "Kết quả gợi ý rằng màng ức chế mất hiệu lực ở nhiệt độ trên 90 °C; kết luận này cần kiểm chứng thêm ở điều kiện dòng chảy thực tế."
- **Lỗi phải tránh:** nâng "gợi ý rằng" thành "chứng minh" để văn "mạnh" hơn — đó là bịa mức khẳng định (xem L2.1).

## L3.2 Bị động hợp lệ trong văn quy phạm và quy trình
Câu bị động khi tác nhân không quan trọng, hoặc khi văn bản là quy trình/quy định áp cho mọi người thực hiện.
- **Giữ nguyên:** "Mẫu được gia công theo ASTM E8 và được thử kéo ở tốc độ biến dạng 0,005 s⁻¹." / "Đường ống được thử áp ở 1,5 lần áp suất thiết kế trước khi đưa vào vận hành."
- **Lỗi phải tránh:** ép mọi câu quy trình thành chủ động, làm sai thể loại văn bản và đôi khi sai trách nhiệm pháp lý của quy trình.

## L3.3 Thuật ngữ chuẩn ngành và thuật ngữ quy ước quốc tế
Thuật ngữ đã chuẩn hoá trong ngành dầu khí/ăn mòn/vật liệu: *ăn mòn điểm (pitting), ăn mòn rãnh, nứt dưới ứng suất trong môi trường sunfua (SSC), ăn mòn "ngọt" do CO₂, ăn mòn "chua" do H₂S, vùng ảnh hưởng nhiệt (HAZ), bảo vệ ca-tốt*. **Danh sách trắng đầy đủ (ngành rộng + ngành hẹp) nằm ở file đi kèm `Danh-sach-trang-thuat-ngu_v1.0.md`** — khi biên tập, tra danh sách đó trước khi quyết định giữ/sửa một thuật ngữ tiếng Anh.
- **Giữ nguyên:** dùng đúng dạng thuật ngữ đã chọn từ đầu văn bản, nhất quán đến cuối; không "diễn giải lại" bằng từ đồng nghĩa cho đỡ lặp.
- **Lỗi phải tránh:** thay thuật ngữ bằng cách nói vòng (ví dụ đổi "ăn mòn điểm" thành "hiện tượng ăn mòn tạo lỗ nhỏ") khiến văn bản mất tính tra cứu và sai nghĩa chuyên môn.

## L3.4 Tên tiêu chuẩn, mác thép, ký hiệu và công thức
Tên tiêu chuẩn (API 5L, API RP 14E, ASTM A106, ASTM G31, NACE MR0175/ISO 15156), mác thép (X65, L80, 13Cr), ký hiệu hoá học (CO₂, H₂S, Fe²⁺), đơn vị (mm/năm, ppm, bar) và mọi công thức.
- **Giữ nguyên:** chép verbatim, kể cả cách viết hoa và khoảng trắng trong mã hiệu.
- **Lỗi phải tránh:** "Việt hoá" tên tiêu chuẩn, đổi đơn vị, hay viết lại công thức dưới dạng chữ.

## L3.5 Số liệu và dấu thập phân tiếng Việt
Mọi con số giữ nguyên giá trị và cách viết; dấu thập phân tiếng Việt là dấu phẩy.
- **Giữ nguyên:** "12,5 mm/năm" vẫn là "12,5 mm/năm" sau khi sửa — không đổi thành "12.5", không làm tròn, không đổi dạng phân số/phần trăm nếu bản gốc không đổi.
- **Lỗi phải tránh:** làm tròn số cho "gọn câu", gộp khoảng giá trị thành một số trung bình không có căn cứ.

## L3.6 Trích dẫn theo quy định của tạp chí / đề cương
Định dạng trích dẫn [12], (Nguyễn Văn A và nnk., 2020) và danh mục tài liệu tham khảo theo mẫu của nơi nộp.
- **Giữ nguyên:** không đổi kiểu trích dẫn, không thêm/bớt nguồn, không di chuyển vị trí trích dẫn khỏi khẳng định mà nó chống lưng.
- **Lỗi phải tránh:** gộp nhiều trích dẫn về một chỗ cho "gọn" (phá vỡ quan hệ khẳng định ↔ bằng chứng, xem L2.9 theo chiều ngược lại).

## L3.7 Câu định nghĩa và câu phân loại chuẩn
Câu mở đầu bằng "X là…" trong mục định nghĩa, phân loại cơ chế, mô tả cấu tạo — thể loại yêu cầu sự trang trọng và chính xác, không phải "câu sâu mà rỗng".
- **Giữ nguyên:** "Ăn mòn điện hoá là quá trình phá huỷ kim loại do tác dụng của dòng điện sinh ra trong pin ăn mòn tại bề mặt tiếp xúc với môi trường điện ly."
- **Lỗi phải tránh:** áp L1.1.3 vào câu định nghĩa — phân biệt bằng tiêu chí: định nghĩa có nội dung phân biệt được với khái niệm lân cận thì giữ.

## L3.8 Liệt kê đúng số lượng thật (kể cả đúng ba ý)
Danh sách ba (hoặc bất kỳ số lượng nào) khi nội dung thật có đúng ngần ấy hạng mục.
- **Giữ nguyên:** "Ba cơ chế ăn mòn chủ đạo tại mỏ X là ăn mòn CO₂, ăn mòn H₂S và ăn mòn do oxy hoà tan xâm nhập."
- **Lỗi phải tránh:** áp L1.2.1 máy móc — cắt bớt hoặc thêm hạng mục làm sai nội dung kỹ thuật.

## L3.9 Câu dài do mật độ thông số kỹ thuật
Câu liệt kê đầy đủ điều kiện thử nghiệm (nhiệt độ, áp suất, môi trường, thời gian) mà tách câu sẽ làm đứt liên hệ điều kiện–kết quả hoặc gây hiểu nhầm phạm vi áp dụng.
- **Giữ nguyên:** "Thử nghiệm ngâm mẫu được tiến hành trong dung dịch NaCl 3,5% bão hoà CO₂ ở 60 °C, áp suất riêng phần CO₂ bằng 2 bar, tốc độ khuấy 500 vòng/phút, trong 168 giờ."
- **Lỗi phải tránh:** áp L1.2.6 máy móc; nếu câu thật sự khó đọc, chỉ được đề xuất tách ở bước báo cáo, kèm bản tách mẫu để tác giả duyệt.

## L3.10 Ngôi tác giả đã chọn ("chúng tôi" / "nhóm nghiên cứu")
Ngôi xưng nhất quán theo quy ước của tạp chí và thói quen tác giả là một phần của giọng văn học thuật tiếng Việt.
- **Giữ nguyên:** văn bản dùng "chúng tôi" thì giữ "chúng tôi" từ đầu đến cuối; không đổi sang bị động hàng loạt để "tránh ngôi".
- **Lỗi phải tránh:** trộn lẫn ngôi xưng giữa các đoạn sau khi sửa — kiểm tra nhất quán là một hạng mục trong bước báo cáo.

## L3.11 Ngôn ngữ tầm nhìn và cam kết trong hồ sơ đề xuất / dự thầu
Phát biểu tầm nhìn, mục tiêu dài hạn và cam kết phạm vi/thời hạn trong hồ sơ thầu là nội dung có giá trị hợp đồng, không phải "thổi phồng".
- **Giữ nguyên:** "Đơn vị cam kết hoàn thành khảo sát và báo cáo đánh giá ăn mòn trong 45 ngày kể từ ngày ký hợp đồng."
- **Lỗi phải tránh:** áp L1.3.2/L2.3 để làm mềm cam kết — sửa cam kết là sửa nghĩa vụ pháp lý. Phần này xử lý theo chế độ đề xuất riêng (L6 trong SKILL-VI): chỉ sửa sáo rỗng không mang cam kết và khẳng định năng lực vô căn cứ.

---

## Tổng kết v0.2

| Lớp | Nội dung | Số mục |
|---|---|---|
| L1.1 | Cấu trúc dàn dựng | 6 |
| L1.2 | Nhịp điệu theo công thức | 7 |
| L1.3 | Thổi phồng và mượn uy tín | 7 |
| L1.4 | Định dạng theo công thức | 4 |
| L1.5 | Tàn dư chat và bản nháp | 5 |
| L1.6 | Dịch máy / tiếng Anh hoá | 6 |
| **L1** | **Dấu hiệu phổ thông** | **35** |
| **L2** | **Dấu hiệu học thuật** | **14** |
| **Tổng dấu hiệu** | | **49** |
| **L3** | **Ngoại lệ phải bảo vệ (không sửa)** | **11** |

*Việc cần làm tiếp (ngoài phạm vi v0.2): đối chứng danh mục này với corpus văn AI ↔
văn người thật (phần còn lại của Giai đoạn 1), đo tỉ lệ báo động giả trên văn người sạch
và hiệu chuẩn lại các ngưỡng định lượng ở bench Giai đoạn 3 (cổng G3). Mức độ
CHẮC CHẮN/GỢI Ý đã được Đạt chốt ở cổng G1 ngày 2026-11-22.*
