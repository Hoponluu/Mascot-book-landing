# Landing sách “Hành trình của Nhân vật thương hiệu”: bàn giao cho Claude Code

Trang một file giới thiệu sách mascot của đội ngũ TELOS. Trang làm 4 việc: giới thiệu sách, cho đọc thử chương 1–2 (PDF lật trang), thu thông tin quan tâm qua Google Form, và dẫn sang dịch vụ TELOS Agency / Academy.

- Trạng thái: **bản dựng đã duyệt bố cục và nội dung (26/11/2026)**. Phần còn lại là hoàn thiện kỹ thuật và đưa lên.
- Tài liệu nội dung và lịch sử quyết định: `docs/Mascot Landing - Cấu trúc nội dung.md`.

## Cấu trúc gói

```
index.html                     Trang chính (HTML + CSS + JS trong 1 file)
assets/
  TELOS_Mascot_DocThu_TrangDoi.pdf   PDF đọc thử (43 trang PDF, dàn trang đôi), 3,5 MB
  img/        Ảnh sách, ảnh đội ngũ, ảnh tác giả, mascot của sách (bm-*), doodle SVG
  mascot/     Mascot TELOS Academy (m01–m16, đã chọn lọc)
  icon/       Icon 3D
docs/         Tài liệu cấu trúc nội dung
```

Mọi ảnh đều đã nén sang webp. Toàn bộ `assets/` (trừ PDF) khoảng 1 MB.

## Chạy thử

```bash
npx serve .        # hoặc: python3 -m http.server 8000
```

Mở `http://localhost:3000` (hoặc `:8000`). **Đừng mở bằng file://**: trình duyệt sẽ chặn pdf.js đọc file PDF.

## Cấu hình (đầu thẻ `<script>` trong index.html)

```js
const CONFIG = {
  FORM_URL: '',            // [CẦN] link Google Form "Đăng ký quan tâm"
  FORM_SOURCE_ENTRY: '',   // [tuỳ chọn] entry.xxxx của câu hỏi ẩn "Nguồn"
  PDF_URL:   'https://cdn.telos.vn/wp-content/uploads/2026/06/TELOS_Mascot_DocThu_TrangDoi.pdf',
  PDF_LOCAL: 'assets/TELOS_Mascot_DocThu_TrangDoi.pdf',
  PDFJS, PDFJS_WORKER, PAGEFLIP  // pdf.js 4.4.168 + StPageFlip 2.0.7 từ jsDelivr
};
```

- **FORM_URL**: các nút có `data-form="…"` (nav, hero, signup, quiz, team, reader-end, fab) tự trỏ tới link này. Khi FORM_URL để trống, các nút cuộn tới `#dang-ky`. Nếu có `FORM_SOURCE_ENTRY`, link được điền sẵn nguồn bấm.
- **PDF**: `cdn.telos.vn` chỉ cho domain telos.vn tải file (CORS). Code tự chọn nguồn: trên `*.telos.vn` thì lấy CDN trước, ở nơi khác thì lấy bản cục bộ trước. Nguồn đầu lỗi thì thử nguồn còn lại.

## Các phần của trang

| ID | Section | Ghi chú kỹ thuật |
|---|---|---|
| S00 | Nav cố định | Icon mascot, menu, nút đăng ký, thanh tiến độ cuộn. Chữ trắng khi ở hero (`.nav.dark`), nền sáng sau khi cuộn qua (`.nav.solid`) |
| S01 | Hero | Cao 100svh, nền indigo, vòng tròn hồng, ảnh sách. Khối chữ nghiêng -3°. Khi cuộn: nội dung lùi chậm (×0.42) và mờ dần |
| S02 | Sách dành cho ai | Margin-top âm, bo góc trên, phủ lên hero. Chủ doanh nghiệp là thẻ lớn |
| S03 | Vì sao viết sách | Nền sky, bong bóng thoại, dải 4 ảnh intro trượt ngang (`data-sx`) |
| S04 | Bên trong sách | Scrollytelling 4 chặng: cột trái sticky, mascot đổi và lớn dần theo IntersectionObserver. 4 thẻ ý chính có mascot ló đầu, mục lục 7 chương dạng `<details>` |
| S05 | Đọc thử | pdf.js render + StPageFlip lật trang. **Tự tải khi cuộn gần tới** (rootMargin 600px). Trang PDF ngang được cắt làm 2 trang sách. Render dần (trang hiện tại −2/+5). Có toàn màn hình, phím ← →, Esc, trang cuối mời đăng ký |
| S06 | Đội ngũ | Phong cách giấy note: thẻ TELOS Agency + ảnh tập thể, thẻ “New Post”, câu trích + ảnh talk |
| S06b | Tác giả chấp bút | Nhân Lưu (giữa), Quỳnh Cao (tác giả), Quy Trần (đồng tác giả), đội Creative / Account. Chỉ số: 9+, 50+, 6, 3.000+ (count-up) |
| S07 | Đăng ký quan tâm | Khối hồng, nút sang Google Form |
| S08 | Quiz 11 câu | Kết quả hiện trong `<dialog>`: “đạt X/11 tiêu chí”, 4 mức (0–3, 4–6, 7–9, 10–11), 2 lựa chọn: Tự tay nâng cấp (Form) và Đột phá cùng chuyên gia (telos.vn/lien-he) |
| S09 | Làm việc cùng TELOS | 2 thẻ Agency / Academy |
| S10 | Hỏi đáp | `<details>` |
| S11 | Footer | hello@telos.vn, facebook.com/TELOSVN, Zalo 0949 165 064 |

Nút nổi ở mobile (`.fab`) tự ẩn khi đang ở khu đăng ký hoặc đang đọc sách.

## Design system

Trang theo **TELOS Design System (landing 2026)**. Token nằm ở `:root` đầu file CSS:
- Màu: indigo `#251776`, pink `#EF4A82`, sky `#40B0E0`, yellow `#FFC945`.
- Font: Be Vietnam Pro 400–900.
- Easing duy nhất: `cubic-bezier(.16,1,.3,1)`.
- Thành phần: kicker + H2 hai dòng, selection box kiểu Figma (`.sel`), thẻ có icon 3D lú khỏi mép (`.card.pop`).

`prefers-reduced-motion: reduce` sẽ tắt toàn bộ animation, parallax và hiệu ứng lật.

## Theo dõi sự kiện

Trang đẩy vào `window.dataLayer` các sự kiện: `form_click` {source}, `read_open`, `read_50`, `read_end`, `read_error`, `quiz_start`, `quiz_done` {score}, `agency_click`. Gắn GTM/GA4 là nhận được.

## Việc còn lại

- [ ] Điền `CONFIG.FORM_URL` (và `FORM_SOURCE_ENTRY` nếu muốn biết nguồn bấm).
- [ ] Chọn nơi đăng:
  - **Trang riêng** (subdomain): giữ nguyên nav/footer.
  - **Trong WordPress TELOS** (Elementor): bỏ nav/footer riêng, thêm tiền tố class (vd `mb-`), gói CSS dưới một id gốc, chừa chỗ cho header sticky của site, đưa ảnh lên Media Library.
- [ ] Thêm `og:image`, favicon, `link rel="canonical"`. Cân nhắc thêm JSON-LD `Book`.
- [ ] Gắn GTM/GA4.
- [ ] Cân nhắc tự host pdf.js và page-flip, thay vì tải từ jsDelivr, nếu cần chạy offline hoặc không muốn phụ thuộc CDN ngoài.
- [ ] QA cuối: Safari iOS (sticky, `<dialog>`, `100svh`), Android Chrome, kiểm tra tốc độ tải PDF trên 4G.

## Nguồn

- Trang gốc tham chiếu: https://telos.vn/mascot-book/
- Nội dung mục lục, 4 chặng, 3 mức IP, 5 tiêu chí: trích từ PDF đọc thử.
- Mascot `m01–m16`: nhân vật TELOS Academy. Ảnh `bm-*` và ảnh sách: từ trang mascot-book gốc của TELOS.
