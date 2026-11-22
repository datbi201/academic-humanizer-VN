---
name: academic-humanizer-vi
version: 0.2.0
description: |
  Biên tập văn học thuật và kỹ thuật tiếng Việt do AI hỗ trợ soạn (bài báo, luận văn, báo cáo
  kỹ thuật) và hồ sơ đề xuất / dự thầu: loại bỏ các dấu hiệu văn AI tiếng Việt, giữ nguyên mọi
  số liệu, kết quả, ký hiệu và trích dẫn, và khớp mức khẳng định với bằng chứng (ở chế độ đề
  xuất: khớp tham vọng với tính khả thi). Không bao giờ thay đổi một con số, một kết quả hay
  một trích dẫn, và không dùng để né tránh việc khai báo sử dụng AI. Dùng khi biên tập văn
  học thuật/kỹ thuật tiếng Việt hoặc hồ sơ đề xuất tiếng Việt.
license: MIT
compatibility: claude-code codex
---

# Academic Humanizer — bản tiếng Việt (SKILL-VI v0.2)

> **Ghi công:** Skill này diễn sinh từ **academic-humanizer** của AIScientists-Dev
> (https://github.com/AIScientists-Dev/academic-humanizer, giấy phép MIT), bộ khung đến lượt
> nó kế thừa từ **humanizer** của blader (https://github.com/blader/humanizer, giấy phép MIT).
> Khung quy trình và kỷ luật khẳng định ↔ bằng chứng được giữ từ bản gốc; toàn bộ danh mục
> dấu hiệu được xây mới cho tiếng Việt. Bản v0.2 đã **qua cổng G1** (Đạt chốt 5 quyết định
> ngày 2026-11-22, ghi trong `Van-de-va-cong-phe-duyet_v1.1.md`): giữ tên skill
> `academic-humanizer-vi`; L1.6.4 giữ mức GỢI Ý xét từng câu; **câu dài hơn 40 từ phải
> CẢNH BÁO + kèm gợi ý tách câu**; thuật ngữ tra theo danh sách trắng đi kèm
> `Danh-sach-trang-thuat-ngu_v1.0.md` trước khi áp L2.14. Chưa qua kiểm định bằng corpus
> đối chứng (việc đó thuộc Giai đoạn 3, cổng G3).

## Khi nào dùng

Biên tập hoặc rà soát văn xuôi học thuật/kỹ thuật tiếng Việt: các mục của bài báo, tóm tắt,
phần trả lời phản biện, tổng quan tài liệu, chương báo cáo kỹ thuật, và **hồ sơ đề xuất /
dự thầu** (áp dụng thêm Mục 8 — chế độ đề xuất). **Không** dùng cho blog, marketing, bài viết
cá nhân; **không bao giờ** chèn ý kiến cá nhân, giọng hài hước hay "cá tính" ngôi thứ nhất
vào bản thảo. Với văn kỹ thuật, giọng *trung tính và chính xác* chính là giọng người.

Một lưu ý về chế độ đề xuất: văn hồ sơ thầu có giọng riêng — nó được đánh giá trên tầm nhìn
và tính khả thi, nên ngôn ngữ tham vọng mà các lớp của bài báo sẽ cắt tỉa lại là *phù hợp và
được chờ đợi* ở đó. Với phát biểu tầm nhìn, áp dụng Mục 8, không áp dụng mức cắt tỉa khắt
khe của các lớp bài báo.

## Nguyên tắc cốt lõi

Văn học thuật tiếng Việt đã có sẵn một giọng người đúng chuẩn: trung tính, chính xác, ngôi
tác giả nhất quán, mọi khẳng định đều neo vào bằng chứng của nó. Công việc gồm hai phần:
(1) gỡ các *dấu hiệu văn AI* mà không làm văn bản trở nên suồng sã, và (2) thực thi kỷ luật
mà humanizer phổ thông bỏ qua: **mọi khẳng định phải xứng với con số, bảng, hình hoặc trích
dẫn của nó, và không động từ nào được mạnh hơn bằng chứng của nó.**

Danh mục dấu hiệu đầy đủ nằm ở file đi kèm **`Danh-muc-dau-hieu-AI-VI.md`** (bản hiện hành v0.2) (cùng thư
mục với file này): Lớp L1 — dấu hiệu phổ thông (mã L1.1–L1.6), Lớp L2 — dấu hiệu học thuật
(mã L2.1–L2.14), Lớp L3 — ngoại lệ phải bảo vệ (mã L3.1–L3.11). Mọi trích dẫn dấu hiệu
trong quy trình và báo cáo đều dùng mã của danh mục đó.

## 1. Nguyên tắc cứng (không thương lượng)

1. **Không bao giờ thay đổi, thêm, bớt hay làm tròn một con số, kết quả, ký hiệu, công thức
   hay trích dẫn nào.** Thiếu số để chống lưng cho khẳng định → gắn cờ cho tác giả, không tự điền.
2. **Giữ nguyên dấu thập phân tiếng Việt:** `12,5` vẫn là `12,5`. Không đổi sang `12.5`,
   không đổi đơn vị, không gộp khoảng giá trị thành số trung bình.
3. **Không đổi thuật ngữ đã chuẩn hoá và tên riêng kỹ thuật:** thuật ngữ chuẩn ngành
   (L3.3), tên tiêu chuẩn (API 5L, ASTM G31, NACE MR0175/ISO 15156…), mác thép, ký hiệu hoá
   học giữ verbatim (L3.4).
4. **Hạ khẳng định thì phải giữ nguyên ý đồ của câu** — mục đích, liên hệ nhân quả và điều
   kiện đi kèm không được rơi rụng (quy tắc chi tiết ở Mục 3).
5. **Không sửa các ngoại lệ ở Lớp L3.** Nghi ngờ một cấu trúc thuộc L3 → ghi câu hỏi vào
   báo cáo, không tự ý sửa.
6. **Giữ cấu trúc và độ phủ nội dung của bản gốc:** bản gốc có bao nhiêu đoạn, bản sửa có
   bấy nhiêu; không tóm tắt, không lược bỏ mục nào.
7. **Không bịa:** không bịa số liệu, kết quả sơ bộ, năng lực đơn vị, đối tác, thư giới thiệu
   hay tài liệu tham khảo — ở cả chế độ bài báo lẫn chế độ đề xuất.

## 2. Phân loại khẳng định trước khi sửa

Trước khi động vào bất kỳ câu nào mang tính khẳng định, phân loại nó vào **một** trong ba
loại sau. Chỉ loại thứ nhất mới được đối chiếu mức khẳng định với bằng chứng.

| Loại khẳng định | Dấu hiệu nhận biết | Cách xử lý |
|---|---|---|
| **Kết quả đo / kết quả nghiên cứu** | Nêu điều đã quan sát, đo, tính được ("tốc độ ăn mòn đạt…", "kết quả cho thấy…") | Đối chiếu với bằng chứng (số, Bảng, Hình, trích dẫn). Động từ mạnh hơn bằng chứng → hạ mức theo Mục 4. |
| **Giả thuyết / diễn giải** | Nêu cơ chế hoặc cách hiểu còn đang bàn ("có thể do…", "cơ chế được cho là…") | Giữ nguyên mức hạn định (hedging) vốn có — đó là L3.1. Chỉ sửa văn phong, không đổi mức chắc chắn theo cả hai chiều. |
| **Mục tiêu / kế hoạch** | Nêu điều *sẽ* làm hoặc *nhằm* đạt được ("dự kiến…", "nhằm giảm…", "mục tiêu của đề tài là…") | **Giữ nguyên ý đồ và mức cam kết.** Không hạ thành khẳng định yếu, không viết lại thành kết quả. Chỉ sửa sáo rỗng thuần văn phong. |

## 3. Quy tắc giữ ý đồ khi hạ khẳng định (bài học issue #5 / PR #7 của bản gốc)

Khi một khẳng định thuộc loại *kết quả* bị hạ mức vì bằng chứng yếu hơn động từ, bản sửa
thường mắc lỗi **trôi nghĩa**: làm mềm động từ nhưng đồng thời cắt mất mệnh đề chỉ *mục
đích* ("nhằm…", "để…") hoặc *liên hệ nhân quả/điều kiện* ("do đó…", "khi… thì…") của câu —
câu sau sửa nói ít hơn (và khác) câu gốc. Đây là lỗi đã được người dùng báo cáo ở bản gốc
tiếng Anh (issue #5) và đã có PR #7 sửa theo đúng hướng này.

Quy tắc bắt buộc:
- Trước khi sửa, tách câu thành: **khẳng định chính + mệnh đề mục đích + quan hệ nhân
  quả/điều kiện**. Sau khi sửa, đối chiếu lại đủ ba thành phần.
- Chỉ thay **động từ/mức khẳng định**; mệnh đề mục đích và quan hệ logic giữ nguyên văn.
- Mọi lần hạ khẳng định đều ghi riêng vào phần "Đổi mức khẳng định" của báo cáo (Mục 5).

**Ví dụ:**
- *Câu gốc:* "Chúng tôi dự kiến phủ epoxy cho đoạn ống ngầm nhằm giảm tốc độ ăn mòn bên
  ngoài; hiệu quả thực tế của lớp phủ trong điều kiện đất ngập mặn chưa được đo."
- *Bản sửa SAI (trôi nghĩa):* "Hiệu quả của lớp phủ epoxy trong điều kiện đất ngập mặn
  chưa được đo." — mất mục tiêu "nhằm giảm tốc độ ăn mòn bên ngoài", và mất phân loại
  "dự kiến" (kế hoạch bị biến thành như kết quả âm tính).
- *Xử lý ĐÚNG:* câu này thuộc loại *mục tiêu/kế hoạch* — giữ nguyên toàn bộ, không hạ
  khẳng định; nếu cần, chỉ sửa văn phong ở vế khác.
- *Ví dụ hạ khẳng định đúng cách:* gốc — "Kết quả chứng minh lớp phủ epoxy ngăn chặn hoàn
  toàn ăn mòn bên ngoài." → sửa — "Kết quả cho thấy lớp phủ epoxy làm giảm rõ rệt ăn mòn
  bên ngoài trong 12 tháng theo dõi tại đoạn ống ngầm X (Bảng 4)." Động từ hạ từ "chứng
  minh… hoàn toàn" xuống "cho thấy… làm giảm rõ rệt", đồng thời gắn phạm vi và bằng chứng —
  không cắt bất kỳ quan hệ logic nào của câu gốc.

## 4. Kỷ luật khẳng định ↔ bằng chứng (cho khẳng định loại kết quả)

Với mỗi khẳng định thực nghiệm, kiểm tra hai điều: (a) nó có được chống lưng bởi một con
số, hình, bảng hoặc trích dẫn trong văn bản không; (b) động từ có khớp với độ mạnh của
bằng chứng đó không. Áp dụng các dấu hiệu L2.1–L2.4 và L2.13 của danh mục:

- **Khẳng định không có bằng chứng** → gắn neo bằng chứng có sẵn trong văn bản (Bảng/Hình/
  mục), hoặc hạ mức khẳng định; nếu văn bản hoàn toàn không có số → gắn cờ cho tác giả.
- **Động từ mạnh hơn bằng chứng** → hạ mức ("chứng minh" → "cho thấy"; "hoàn toàn" → nêu
  phạm vi điều kiện thực tế).
- **Mức độ mơ hồ** ("đáng kể", "vượt trội", "tương đối cao") → thay bằng con số hoặc
  khoảng giá trị có nguồn (Bảng/Hình cụ thể); ưu tiên khoảng giá trị hơn một số trung bình
  đơn lẻ khi phương pháp tính trung bình không được nêu.
- **So sánh** → dẫn đầu bằng đối chứng mạnh nhất đang được dùng trong ngành/dự án, nêu tên
  đối chứng; không so với "phương pháp thông thường" vô danh.

## 5. Quy trình làm việc (bắt buộc theo thứ tự)

1. **Đọc:** đọc toàn văn bản và văn mẫu của tác giả (nếu có); xác định loại tài liệu (bài
   báo / báo cáo / hồ sơ đề xuất) và nơi nộp. Nếu là hồ sơ đề xuất, bật chế độ ở Mục 8.
2. **Audit (chưa sửa):** liệt kê mọi dấu hiệu phát hiện được — mã danh mục, vị trí, trích
   câu gốc, hướng sửa dự kiến — cùng trạng thái bằng chứng của từng khẳng định loại kết
   quả, và phân loại khẳng định theo Mục 2. Trình danh sách audit trước khi viết lại nếu
   người dùng yêu cầu, hoặc giữ để đối chiếu ở bước báo cáo.
3. **Viết lại:** giữ nguyên cấu trúc và nội dung; gỡ dấu hiệu theo danh mục; hạ các khẳng
   định quá mức theo Mục 3–4; giữ nguyên hedging hợp lệ và toàn bộ Lớp L3.
4. **Báo cáo:** trả bản sạch kèm báo cáo thay đổi gồm **hai phần tách bạch**:
   - **A. Sửa văn phong:** liệt kê theo mã danh mục (ví dụ: L1.1.1, L1.6.2, L2.11) — câu
     gốc → câu sửa.
   - **B. Đổi mức khẳng định:** liệt kê riêng từng câu bị hạ/tăng mức khẳng định — câu
     gốc → câu sửa → loại khẳng định → bằng chứng căn cứ. Không gộp chung với phần A.
   - Cuối báo cáo, xác nhận rõ: *"Không số liệu, ký hiệu, công thức hay trích dẫn nào bị
     thay đổi."* Nếu có khẳng định bị gắn cờ vì thiếu bằng chứng, liệt kê ở cuối báo cáo.

## 6. Các lớp quy tắc (tóm tắt — chi tiết ở file danh mục)

- **Lớp L1 — Dấu hiệu phổ thông:** cấu trúc dàn dựng (L1.1), nhịp điệu theo công thức
  (L1.2), thổi phồng và mượn uy tín (L1.3), định dạng theo công thức (L1.4), tàn dư chat và
  bản nháp (L1.5), dịch máy/tiếng Anh hoá (L1.6). Gỡ theo mức độ CHẮC CHẮN/GỢI Ý ghi trong
  danh mục.
- **Lớp L2 — Dấu hiệu học thuật:** trọng tâm là mức khẳng định vượt bằng chứng (L2.1–L2.4),
  các mẫu sáo rỗng riêng của văn học thuật (L2.5–L2.10, L2.12) và hai họ riêng của tiếng
  Việt: Hán-Việt xếp chồng (L2.11) và chèn tiếng Anh trang trí (L2.14).
- **Lớp L3 — Ngoại lệ phải bảo vệ:** hedging có căn cứ, bị động quy phạm, thuật ngữ chuẩn,
  tên tiêu chuẩn/ký hiệu, số liệu và dấu thập phân, định dạng trích dẫn, câu định nghĩa,
  liệt kê đúng số lượng thật, câu dài do thông số, ngôi tác giả, ngôn ngữ cam kết trong hồ
  sơ thầu. **Không sửa** — xem Mục 1, nguyên tắc cứng số 5.

## 7. Giọng văn và nơi nộp

Nếu tác giả cung cấp bài báo/báo cáo đã được duyệt trước đây, đọc một mẫu trước và ghi lại:
nhịp câu, thói quen dùng từ nối, mức độ và vị trí hedging, cách mở đầu các mục, ký hiệu,
các cụm từ quen dùng — rồi khớp theo. Khớp cả giọng của nơi nộp (tạp chí chuyên ngành:
súc tích, kết quả đi trước; báo cáo cho chủ đầu tư: đầy đủ căn cứ, thận trọng về cam kết).
Khi không có văn mẫu, mặc định là văn xuôi sạch, chính xác, đúng chuẩn nơi nộp — không phải
giọng suồng sã, nhiều ý kiến cá nhân của humanizer phổ thông.

## 8. Chế độ đề xuất / hồ sơ dự thầu

Hồ sơ đề xuất không phải bài báo. Nó được chấm trên **tầm nhìn cộng tính khả thi**, không
phải kết quả đã hoàn thành. Ngôn ngữ tham vọng mà các lớp bài báo cắt tỉa ("mục tiêu dài
hạn", "tiên phong", "nền tảng cho…") là *phù hợp* ở đây, với điều kiện có kế hoạch và căn
cứ khả thi chống lưng. Vì vậy ở chế độ này **không làm phẳng tầm nhìn**; thay vào đó thực
thi kỷ luật tương ứng: **khẳng định ↔ tính khả thi**.

### 8.1 Trọng tâm nằm ở những trang đầu
Hội đồng/bên mời thầu hình thành đánh giá từ phần mở đầu rồi đọc lướt phần còn lại để xác
nhận. Dồn sức biên tập vào: trang tóm tắt đề xuất, phần mở đầu phương án kỹ thuật (vấn đề →
khoảng trống → cách tiếp cận → các hạng mục công việc → hiệu quả mang lại), và mục tiêu/
phạm vi. Sau vài trang đầu, người đọc phải đã nắm được: vì sao việc này quan trọng (cụ thể),
thiếu gì hiện nay, ý tưởng cốt lõi trong một câu, các hạng mục công việc rõ ràng, và kết
quả cam kết.

### 8.2 Các lỗi yếu riêng của hồ sơ đề xuất cần sửa
- **Tầm quan trọng mơ hồ.** "Đây là vấn đề cấp thiết, có ý nghĩa thực tiễn lớn lao." →
  nêu hậu quả cụ thể nếu không làm: "Nếu không đánh giá lại, tốc độ ăn mòn tại đoạn ống X
  đang vượt giá trị thiết kế 8 lần mà chưa có căn cứ để quyết định thay ống hay tăng liều
  ức chế."
- **Hạng mục viết theo công cụ thay vì câu hỏi/kết quả.** "Hạng mục 2: Áp dụng phần mềm
  mô phỏng ăn mòn." → "Hạng mục 2: Xác định mác thép đáp ứng tuổi thọ 20 năm ở điều kiện
  giếng X bằng mô phỏng ăn mòn, đối chứng với dữ liệu vận hành 5 năm."
- **Hạng mục domino.** Các hạng mục sau sụp đổ nếu hạng mục đầu thất bại. *Sửa:* diễn đạt
  các hạng mục song song, độc lập về giá trị; nơi có phụ thuộc thật, nêu phương án dự phòng.
- **Tham vọng không có chân đứng khả thi.** Mỗi cam kết lớn cần một căn cứ: dữ kiện sơ bộ,
  công trình đã công bố, kinh nghiệm dự án tương tự, nhân sự chủ chốt, đối tác. *Sửa:* gắn
  căn cứ ngay cạnh cam kết. Không có căn cứ → gắn cờ cho tác giả, **không bịa** (Mục 1.7).
- **Phần năng lực/đào tạo/phổ biến kết quả viết mẫu.** "Đơn vị có đội ngũ giàu kinh
  nghiệm…" → cụ thể hoá: số lượng, tên dự án tương tự, thiết bị/phần mềm có thật mà đơn vị
  cung cấp.
- **Cam kết trung tâm bị hedging hoá.** Cam kết chính của hồ sơ (phạm vi, tiến độ, sản
  phẩm bàn giao) là cam kết có thể kiểm chứng, không phải "sẽ cố gắng xem xét khả năng…".
  Hedging đúng chỗ của nó là ở phần phân tích rủi ro và diễn giải kỹ thuật.

### 8.3 Giữ và phát huy (thủ pháp của hồ sơ được chọn)
- **Khung tầm nhìn:** mục tiêu dài hạn nêu sớm, hồ sơ này là một bước có nguyên tắc hướng
  tới nó.
- **Nhãn dẫn chạy đầu dòng để dễ đọc lướt:** **Mục tiêu:**, **Cách tiếp cận:**, **Sản phẩm
  bàn giao:** — người chấm đọc lướt; cấu trúc nhìn thấy được sẽ giành thêm thời gian đọc.
- **Một ví dụ/đối tượng chạy xuyên suốt** (ví dụ một đoạn ống, một giếng điển hình) để
  phương án trừu tượng trở nên cụ thể và nhất quán giữa các hạng mục.
- **Neo phương án mới vào căn cứ kinh điển có tên:** tiêu chuẩn, phương pháp đã được công
  nhận mà phương án mở rộng — tín hiệu của sự chặt chẽ.
- **Hồ sơ năng lực thật đặt sớm như bằng chứng khả thi:** dự án tương tự đã làm, công bố,
  đối tác — chỉ dùng hồ sơ *thật do đơn vị cung cấp*; không bịa kinh nghiệm, đối tác, thư giới thiệu.

### 8.4 Khẳng định ↔ tính khả thi (tương ứng Mục 4 ở chế độ đề xuất)
Với mỗi hạng mục và kết quả hứa hẹn, kiểm tra: tham vọng có được chống lưng bởi phương
tiện đáng tin không — dữ kiện sơ bộ, phương pháp đã có, căn cứ tiêu chuẩn, nhân sự/đối tác
có thật, hoặc lộ trình giảm rủi ro theo giai đoạn? Có → giữ nguyên động từ tham vọng.
Không → gắn căn cứ còn thiếu vào, hoặc thu hẹp khẳng định về mức kế hoạch thực sự chống
lưng được. Nếu căn cứ không tồn tại, gắn cờ cho tác giả thay vì che lấp.

## 9. Đầu ra

Trả về: (1) bản văn đã biên tập; (2) báo cáo thay đổi theo Mục 5.4 — tách bạch *sửa văn
phong* (theo mã danh mục) và *đổi mức khẳng định* (kèm loại khẳng định và căn cứ); (3) dòng
xác nhận toàn vẹn số liệu/trích dẫn; (4) danh sách các khẳng định bị gắn cờ chờ tác giả bổ
sung bằng chứng (nếu có).

## 10. Đạo đức và khai báo

Skill này là công cụ biên tập vì sự rõ ràng và đúng mực của văn bản. Nó **không** được thiết
kế để né máy dò AI, không tạo ra kết quả nghiên cứu, không bịa dữ kiện, và **không miễn trừ
nghĩa vụ khai báo việc sử dụng AI** của tác giả: luôn tuân thủ chính sách khai báo của tạp
chí, hội đồng hoặc bên mời thầu nơi văn bản được nộp.

---

*Ghi công và giấy phép: SKILL-VI v0.2 diễn sinh từ academic-humanizer (AIScientists-Dev,
MIT) và humanizer (blader, MIT). Phần diễn sinh này được phát hành theo giấy phép MIT,
kèm giữ nguyên ghi công tác giả gốc theo điều kiện của giấy phép. Danh mục đi kèm:
`Danh-muc-dau-hieu-AI-VI.md` (v0.2) và `Danh-sach-trang-thuat-ngu_v1.0.md`.*
