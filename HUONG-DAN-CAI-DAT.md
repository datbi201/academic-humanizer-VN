# Academic Humanizer (EN) + Academic Humanizer VI — Hướng dẫn cài đặt

Bộ hai skill biên tập văn học thuật cho AI agent (Claude Code, OpenAI Codex, Google
Antigravity…), giúp loại bỏ "văn AI", giữ nguyên mọi số liệu/trích dẫn và khớp mức khẳng
định với bằng chứng:

- **`academic-humanizer`** — bản tiếng Anh (gốc của AIScientists-Dev, bản 0.3.3).
- **`academic-humanizer-vi`** — bản tiếng Việt (v0.3): danh mục 49 dấu hiệu văn AI tiếng
  Việt, danh sách trắng thuật ngữ kỹ thuật và Hóa–Y–Sinh, biến thể theo loại văn bản
  (bài báo, báo cáo, hồ sơ thầu, thuyết minh đề tài, trả lời phản biện, abstract) và theo
  lĩnh vực (Hóa học / Y học / Sinh học).

Kho mã nguồn (mở, giấy phép MIT): https://github.com/datbi201/academic-humanizer-VN

> Lưu ý gõ đúng tên repo có đuôi **-VN**: `datbi201/academic-humanizer-VN`. Thiếu đuôi này
> GitHub sẽ báo lỗi xác thực khó hiểu ("Authentication failed").

## Cách 1 — Cài bằng một lệnh (khuyên dùng)

Cần máy đã có **Node.js** (để chạy `npx`). Mở terminal và chạy lệnh tương ứng với agent
bạn dùng. Cờ `-g` = cài cho mọi dự án; `-y` = không hỏi lại.

**Claude Code:**
```
npx skills add datbi201/academic-humanizer-VN --skill academic-humanizer-vi -a claude-code -g -y
```

**OpenAI Codex:**
```
npx skills add datbi201/academic-humanizer-VN --skill academic-humanizer-vi -a codex -g -y
```

**Google Antigravity:**
```
npx skills add datbi201/academic-humanizer-VN --skill academic-humanizer-vi -a antigravity -g -y
```

Muốn cài luôn bản tiếng Anh, thêm `--skill academic-humanizer` vào lệnh trên (hoặc chạy
lại lệnh với `--skill academic-humanizer`). Muốn cài cho cả ba agent trong một lần chạy,
liệt kê cả ba: `-a claude-code -a codex -a antigravity`.

Sau khi cài xong, **mở phiên agent mới** rồi dùng bình thường, ví dụ: "Dùng academic
humanizer rà soát đoạn tóm tắt này" hoặc "Biên tập đoạn văn tiếng Việt này theo skill
academic-humanizer-vi, loại văn bản: bài báo, lĩnh vực: hóa học".

**Cập nhật lên bản mới:** chạy `npx skills update` (một lần cho mỗi máy), rồi mở phiên mới.

## Cách 2 — Cài thủ công (khi mạng công ty chặn git/npx)

1. Mở trang repo ở trên bằng trình duyệt → nút **Code** → **Download ZIP** → giải nén.
2. Tạo thư mục skill theo đúng tên, trong thư mục skills của agent:
   - Claude Code: `%USERPROFILE%\.claude\skills\`
   - Codex: `%USERPROFILE%\.codex\skills\`
   - Antigravity: `%USERPROFILE%\.gemini\antigravity\skills\`
3. Bản tiếng Việt: tạo thư mục con `academic-humanizer-vi` và chép **toàn bộ nội dung thư
   mục `vi\`** trong file ZIP vào đó (phải đủ 6 file — SKILL.md và 5 file đi kèm; skill
   tiếng Việt cần các file đi kèm để tra thuật ngữ và áp biến thể).
4. Bản tiếng Anh: tạo thư mục con `academic-humanizer` và chép file `SKILL.md` ở thư mục
   gốc của file ZIP vào đó.
5. Mở phiên agent mới để skill được nạp.

Cập nhật thủ công: tải lại ZIP mới và chép đè như trên.

## Ghi công & giấy phép

Giấy phép MIT. Bản tiếng Anh diễn sinh từ academic-humanizer của AIScientists-Dev
(https://github.com/AIScientists-Dev/academic-humanizer), kế thừa humanizer của blader
(https://github.com/blader/humanizer). Bản tiếng Việt do nhóm tác giả của repo
datbi201/academic-humanizer-VN xây dựng mới trên cùng khung kỷ luật khẳng định ↔ bằng
chứng. Skill này hỗ trợ biên tập văn bản, **không** dùng để né tránh việc khai báo sử
dụng AI khi nơi đăng yêu cầu khai báo.
