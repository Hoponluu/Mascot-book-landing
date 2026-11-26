# Landing sách Mascot · bản cá nhân tác giả (Nhân Lưu)

> Phiên bản 0.2 · 26/11/2026 · Trạng thái: **đã chốt cụm, đã dựng HTML bản 1** (`mascot-book-landing.html`)
> Trang gốc tham chiếu: https://telos.vn/mascot-book/ (trang của TELOS Agency)
> Bước tiếp theo: bạn chốt các cụm ở mục 3 và trả lời mục 6 → mình dàn ra HTML theo Design System TELOS → bạn đưa qua Claude Code.

---

## 1. Mục tiêu trang (theo thứ tự ưu tiên)

| # | Mục tiêu | Người xem cần làm được | Đo bằng |
|---|---|---|---|
| 1 | Giới thiệu sách | Hiểu trong 5 giây: sách nói về gì, dành cho ai, ai viết | Tỉ lệ cuộn qua hero |
| 2 | Đọc thử 1 chương | Đọc ngay, không tải file, không đăng nhập, đọc tốt trên điện thoại | Số lượt mở trình đọc, % đọc hết chương |
| 3 | Để lại thông tin quan tâm | Bấm 1 nút, điền form ngắn (Google Form) | Số lượt gửi form |
| 4 | Giới thiệu dịch vụ TELOS (phụ) | Biết tác giả đứng sau TELOS Agency / Academy và có lối đi tiếp | Click ra trang dịch vụ |

**Không thuộc phạm vi:** bán sách, thanh toán, đếm ngược ưu đãi, giao hàng (chưa có kế hoạch in ấn).

---

## 2. Đọc trang gốc: giữ gì, bỏ gì

Trang gốc có 15 cụm. Nội dung về sách khá tốt, nhưng trang đang kể theo giọng công ty, CTA lặp nhiều và có vài chỗ hỏng.

| Cụm trên trang gốc | Nhận xét UX | Bản cá nhân |
|---|---|---|
| 1. Banner đếm ngược giảm 20% | Đồng hồ đang về 00, tạo cảm giác ưu đãi giả | **Bỏ** |
| 2. Hero "Hành trình của NHÂN VẬT THƯƠNG HIỆU" + Pre-order | CTA trỏ về /lien-he/, khác các nút còn lại trỏ #preorder | **Giữ, viết lại**: thêm tên tác giả, 2 CTA rõ vai |
| 3. "Công ty nọ có một con Mascot" + 4 thẻ minh hoạ | Mở đầu hay, nhưng dài trước khi người xem biết đây là sách | **Rút gọn**, gộp vào cụm "Vì sao mình viết" |
| 4. "Tại sao chúng tôi viết ra cuốn sách này?" | Giọng "chúng tôi" | **Giữ, đổi giọng** thành lời tác giả |
| 5. Đội ngũ đứng sau | Đội ngũ TELOS Agency | **Chuyển thành** "Về tác giả" + dòng ghi công cộng sự |
| 6. Social post block | Lặp ý cụm 4 và 7 | **Bỏ** |
| 7. Khối quảng bá "cẩm nang đầu tiên tại VN" | Lặp ý | **Gộp** thành 1 câu trong hero hoặc "Bên trong sách" |
| 8. 4 thẻ chủ đề (4 giai đoạn, 3 mức IP, Characterize & Humanize, Quy trình T.E.L.O.S) | Cụm giá trị nhất, nói được sách có gì | **Giữ**, làm thành "Bên trong sách" + mục lục |
| 9. Quiz 11 câu "Linh vật nhà bạn trưởng thành đến đâu?" | Tương tác tốt nhưng dài, đặt giữa trang làm loãng luồng đọc thử | **Tuỳ chọn** (xem mục 6, câu 3) |
| 10. Đọc thử miễn phí (trình xem PDF) | Đang kẹt "Đang tải sách... 0/0", không đọc được | **Làm lại** (mục 4) |
| 11. Mini-game lật thẻ | Vui nhưng không phục vụ mục tiêu nào | **Bỏ** |
| 12. FAQ 3 câu | Có ích | **Giữ, viết lại** theo trạng thái "chưa phát hành" |
| 13. Form pre-order (tên, SĐT, email, địa chỉ) | Không có nút gửi; hỏi địa chỉ khi chưa bán | **Thay** bằng nút dẫn sang Google Form |
| 14. Form đăng ký khóa học Academy | Nhầm form, lệch mục tiêu trang | **Bỏ**; dịch vụ Academy đi vào cụm "TELOS" |
| 15. Footer hotline + Zalo | — | **Giữ**, đổi thành kênh liên hệ cá nhân |

**Quy tắc CTA cho bản mới:** cả trang chỉ có 2 loại nút, nhãn và đích giữ nguyên ở mọi chỗ.
- Nút chính: **"Đăng ký quan tâm"** → Google Form (mở tab mới).
- Nút phụ: **"Đọc thử chương 1"** → mở trình đọc.

---

## 3. Cấu trúc đề xuất (để chốt)

Luồng: **Biết sách → Thấy bên trong → Đọc thử → Tin người viết → Đăng ký → (Đi tiếp với TELOS)**.

| Mã  | Cụm                                                        | Nội dung chính                                                                                                                                                                | CTA                                               | Chốt?                                                                                                                                                                                              |
| --- | ---------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| S00 | Thanh điều hướng mỏng (dính trên cùng)                     | Tên sách · Về sách · Đọc thử · Tác giả · nút "Đăng ký quan tâm"                                                                                                               | Đăng ký                                           | Y                                                                                                                                                                                                  |
| S01 | Hero                                                       | Ảnh bìa 3D, tên sách, 1 câu hứa hẹn, "Tác giả Nhân Lưu", nhãn trạng thái "Sách đang hoàn thiện · Chưa mở bán"                                                                 | Đọc thử chương 1 (chính) · Đăng ký quan tâm (phụ) | N - đừng focus vào tác giả. Và tác giả vẫn là đội ngũ TELOS chứ không riêng Nhân Lưu (vị trí trung tâm thì ok, nhưng trong thông tin vẫn có 2 tác giả & tập thể)                                   |
| S02 | Sách dành cho ai                                           | 3 thẻ: Designer muốn hiểu quy trình tạo nhân vật · Marketer muốn khai thác mascot lâu dài · Chủ doanh nghiệp coi mascot là tài sản                                            | —                                                 | Y - nhưng ưu tiên chủ doanh nghiệp lên đầu tiên                                                                                                                                                    |
| S03 | Vì sao mình viết cuốn này                                  | Đoạn mở "Công ty nọ có một con Mascot..." rút gọn còn 3–4 câu + 3 câu hỏi tu từ + lời tác giả (giọng "mình")                                                                  | —                                                 | Y - nhưng viết gọn lại theo ngôn ngữ bình thường: "TELOS chúng mình đã thực hành việc sáng tạo mascot, tụi mình viết cái này ra để tổng hợp các kiến thức và hệ thống hóa nó lại cho người đọc..." |
| S04 | Bên trong sách                                             | 4 thẻ ý chính (4 giai đoạn trưởng thành · 3 mức bảo hộ IP · Characterize & Humanize · Quy trình T.E.L.O.S) + mục lục rút gọn có thể mở rộng                                   | Đọc thử chương 1                                  | Y                                                                                                                                                                                                  |
| S05 | **Đọc thử chương 1 và 2**                                  | Đoạn mở đầu chương hiện ngay trên trang, mờ dần ở cuối; nút mở trình đọc toàn chương (chi tiết mục 4)                                                                         | Đọc tiếp toàn chương                              | Y (gợi ý các thư viện có thể gắn pdf vào đọc trực tiếp, mô phỏng lật trang, [link PDF đọc thử](https://cdn.telos.vn/wp-content/uploads/2026/06/TELOS_Mascot_DocThu_TrangDoi.pdf))                  |
| S06 | Về tác giả                                                 | Ảnh, tiểu sử ngắn Nhân Lưu: 9+ năm làm mascot/branding, founder TELOS Agency & TELOS Academy, 3.000 học viên. Dòng ghi công cộng sự (Quỳnh Cao, Quy Trần, đội Creative TELOS) | —                                                 | Y - Các bạn phía sau ghi là "đồng tác giả"                                                                                                                                                         |
| S07 | Đăng ký quan tâm                                           | Nói rõ: miễn phí, không phải đặt mua, nhận được gì (mục 5). 1 nút lớn                                                                                                         | Đăng ký quan tâm                                  | Y                                                                                                                                                                                                  |
| S08 | Quiz "Linh vật nhà bạn trưởng thành đến đâu?" *(tuỳ chọn)* | Rút 11 → 7 câu, hiện kết quả theo 4 giai đoạn của sách, cuối kết quả gợi ý chương liên quan                                                                                   | Đăng ký quan tâm                                  | Y                                                                                                                                                                                                  |
| S09 | Làm việc cùng TELOS (phụ)                                  | 2 thẻ: **TELOS Agency** (thiết kế mascot, branding) · **TELOS Academy** (khóa UI/UX). Mỗi thẻ 1 dòng + 1 link                                                                 | Link ra telos.vn / academy.telos.vn               | Y                                                                                                                                                                                                  |
| S10 | Hỏi đáp                                                    | 4–5 câu (gợi ý mục 5.3)                                                                                                                                                       | —                                                 | Y                                                                                                                                                                                                  |
| S11 | Footer                                                     | Email, Facebook/LinkedIn cá nhân, Zalo, link TELOS                                                                                                                            | —                                                 | Y                                                                                                                                                                                                  |

Gợi ý vị trí mascot TELOS (đã có 16 biểu cảm trong `Nội dung khóa học/Asset/Mascot/`): hero, đầu trình đọc, S07 và hỏi đáp.

---

## 4. Đọc thử: đề xuất UX

### 4.1 So sánh 3 cách

| Cách | Ưu | Nhược |
|---|---|---|
| A. **Chữ HTML trên trang + trình đọc toàn màn hình** *(đề xuất)* | Nhẹ, đọc tốt trên điện thoại, cỡ chữ tự co giãn, Google và AI đọc được (SEO), không kẹt tải | Phải chuyển chương sang HTML (mình làm từ file .docx/.md) |
| B. Trình xem PDF/flipbook như bản gốc | Giữ nguyên dàn trang sách in | Nặng, chữ bé trên điện thoại, đang lỗi không tải được, không SEO |
| C. Bắt để lại email mới gửi chương | Thu nhiều lead | Thêm ma sát ngay bước tạo thiện cảm, người xem thường bỏ đi |

Kết hợp đề xuất: **A làm chính**, có thêm link "Tải bản PDF" trong trình đọc nếu bạn muốn giữ dàn trang. Không chặn bằng email; chỉ đặt lời mời đăng ký ở **cuối chương**, đúng lúc người đọc muốn đọc tiếp.

### 4.2 Cách hoạt động

1. **Trên trang (S05):** tên chương, thời gian đọc ước tính ("~12 phút"), 2–3 đoạn đầu, mờ dần ở cuối. Nút "Đọc tiếp toàn chương".
2. **Trình đọc** mở dạng lớp phủ toàn màn hình (link trực tiếp được `#doc-thu`):
   - Cột chữ 60–70 ký tự/dòng, cỡ 18px, giãn dòng 1.7; ảnh minh hoạ chèn giữa bài.
   - Thanh tiến độ trên cùng, mục lục các phần trong chương (mở được trên mobile).
   - Chỉnh cỡ chữ A−/A+, nút đóng, phím Esc.
   - Nhớ vị trí đang đọc trên máy (đóng mở lại vẫn ở chỗ cũ).
3. **Cuối chương:** khối "Hết chương 1. Muốn đọc tiếp khi sách ra mắt?" + nút "Đăng ký quan tâm" + chia sẻ link chương.
4. **Gắn số liệu:** sự kiện mở trình đọc, 50%, đọc hết, bấm đăng ký từ cuối chương (để biết chương đọc thử có kéo được đăng ký không).

---

## 5. Thu thập thông tin quan tâm

### 5.1 Cách gắn
- Dùng nút dẫn sang **Google Form** (mở tab mới), không nhúng iframe vì form nhúng trên điện thoại hay bị cuộn kép.
- Thêm tham số nguồn vào link để biết người đăng ký bấm từ đâu (hero / cuối chương / quiz). Google Form làm được bằng link điền sẵn 1 câu hỏi ẩn ý "Nguồn".
- Sau khi gửi, trang cảm ơn của Form có link quay về trang sách.

### 5.2 Câu hỏi gợi ý cho Google Form (ngắn, ≤ 1 phút)
| #   | Câu hỏi                                                                                                                                             | Bắt buộc       | Lý do                                    |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- | ---------------------------------------- |
| 1   | Tên của bạn                                                                                                                                         | Có             |                                          |
| 2   | Email                                                                                                                                               | Có             | Kênh báo tin phát hành                   |
| 3   | Số điện thoại / Zalo                                                                                                                                | Không          | Chỉ khi muốn được liên hệ                |
| 4   | Bạn đang là: Designer · Marketer · Chủ doanh nghiệp · Sinh viên · Khác                                                                              | Có             | Biết chân dung người đọc                 |
| 5   | Bạn muốn nhận: Thông báo khi sách phát hành · Chương đọc thử tiếp theo · Tư vấn thiết kế mascot (TELOS Agency) · Thông tin khóa học (TELOS Academy) | Có, chọn nhiều | Gắn mục tiêu phụ mà không cần form riêng |
| 6   | Bạn muốn sách ở dạng: Sách in · Ebook · Cả hai                                                                                                      | Không          | Dữ liệu cho quyết định in ấn             |
| 7   | Mức giá bạn thấy hợp lý cho sách in                                                                                                                 | Không          | Như trên                                 |
| 8   | Điều bạn muốn sách trả lời                                                                                                                          | Bỏ             | Ý tưởng nội dung                         |

Bỏ: địa chỉ giao sách (chưa bán).

### 5.3 Hỏi đáp gợi ý
- Khi nào sách phát hành? → "Đang hoàn thiện, đăng ký để được báo đầu tiên." - Sách đã được viết xong vào 2024, thiết kế xong vào 2025, chưa in và xuất bản chủ yếu là do TELOS ...nghèo và đang tập trung kiếm tiền =))).
- Đăng ký có phải đặt mua không? → Không, chỉ là đăng ký quan tâm, không mất phí.
- Có ebook không? → Đang khảo sát; bạn chọn ở form.
- Sách dành cho ai? → 3 nhóm ở S02.
- Mình muốn làm mascot cho thương hiệu thì liên hệ ai? → TELOS Agency (S09).

---

## 6. Cần bạn chốt

1. **Tên sách và tác giả hiển thị:** giữ "Hành trình của Nhân vật thương hiệu"? Hero ghi "Nhân Lưu" một mình, còn cộng sự ghi ở S06 — ổn không?
2. **Giọng văn:** "mình" hay "tôi"?
3. **Quiz S08:** giữ (rút còn 7 câu), bỏ, hay để phiên bản sau?
4. **Nội dung chương 1:** bạn có file .docx/.md/PDF không? Chương có nhiều hình không?
5. **Link Google Form** (hoặc mình soạn sẵn bộ câu hỏi để bạn tạo).
6. **Nơi đăng:** trang này đặt ở đâu (web cá nhân, subdomain, hay trong WordPress TELOS)? Ảnh hưởng tới việc có header/footer riêng hay không.
7. **Ảnh:** dùng lại ảnh bìa và minh hoạ trên trang gốc được không? Ảnh chân dung của bạn?

---

## 7. Bước tiếp theo
1. Bạn đánh dấu ☐ ở mục 3 và trả lời mục 6.
2. Mình dàn `mascot-book-landing.html` (1 file, theo Design System TELOS: màu, Be Vietnam Pro, component Button/Tag/Card/Mascot), chữ còn thiếu để `[CẦN BỔ SUNG]`.
3. Bạn đưa qua Claude Code để hoàn thiện và gắn vào nơi đăng.

---

## 8. Kết quả chốt (26/11/2026)

| Mục | Chốt |
|---|---|
| Tác giả | Không đặt tác giả ở hero. Tác giả: **Nhân Lưu** (ở giữa) và **Quỳnh Cao**. Đồng tác giả: **Quy Trần**, đội Creative và đội Account TELOS |
| Giọng văn | “TELOS chúng mình / tụi mình”, gọi người đọc là “bạn” |
| S02 | Chủ doanh nghiệp đứng đầu, thẻ lớn |
| S05 | Đọc thử **chương 1 và 2** bằng PDF lật trang (file `TELOS_Mascot_DocThu_TrangDoi.pdf`) |
| S08 Quiz | Giữ đủ **11 câu** như trang gốc. Kết quả hiện trong popup: “Mascot của bạn đạt X/11 tiêu chí” + 2 lựa chọn **Tự tay nâng cấp** (Google Form) và **Đột phá cùng chuyên gia** (telos.vn/lien-he). Mức: 0–3 sơ khai · 4–6 có vài ứng dụng/nền tảng · 7–9 có hệ thống, đầu tư bài bản · 10–11 tiềm năng rất lớn, còn vài điểm nghẽn |
| Form | Bỏ câu 8. Còn 7 câu |
| Hỏi đáp | Câu “Khi nào phát hành”: viết xong 2024, thiết kế xong 2025, chưa in vì TELOS đang tập trung kiếm tiền |
| Ảnh tác giả | Cập nhật sau |

## 9. HTML bản 1: ghi chú bàn giao cho Claude Code

**File:** `mascot-book-landing.html` + thư mục `assets/` (mascot TELOS Academy và icon 3D, đã chuyển webp, tổng khoảng 550 KB). Thư mục `_tmp/` là file nháp, xoá được.

**Design system:** token màu, Be Vietnam Pro, kicker, H2 hai dòng, selection box Figma, thẻ có icon lú ra khỏi mép, vòng tròn indigo + blob hồng ở hero, easing `cubic-bezier(.16,1,.3,1)`.

**Hiệu ứng đã dùng**
- Parallax nhẹ (`data-speed`) cho các lớp ở hero và bong bóng thoại ở S03.
- **S04 “4 chặng”**: cột trái dính khi cuộn, mascot đổi theo từng chặng và lớn dần (02 → 16 → 05 → 08), thanh tiến độ 4 nấc. Tắt JS vẫn đọc được 4 chặng.
- Reveal khi cuộn, selection box vẽ dần, số đếm, mascot nhún. Tắt hết khi `prefers-reduced-motion`.

**Trình đọc thử (S05)**
- Thư viện: **pdf.js 4.4** (render PDF) + **StPageFlip 2.0.7** (lật trang, MIT), tải từ jsDelivr **chỉ khi người dùng bấm “Mở sách”**, để trang chính nhẹ.
- PDF trang đôi được tự cắt làm 2 trang sách. Trang dọc giữ nguyên, trang đầu dọc được coi là bìa.
- Tải dần: chỉ render trang đang xem ±5 trang (`disableAutoFetch`).
- Desktop xem 2 trang, điện thoại 1 trang. Có nút trước/sau, phím ← →, toàn màn hình (Esc để thoát), mở PDF tab mới.
- Cuối sách thêm 2 trang: “Phía sau còn” (chương 3–7) và “Hết phần đọc thử” + nút Đăng ký.
- Lỗi tải thì hiện nút mở PDF trong tab mới.
- Các thư viện khác có thể thay: DearFlip (plugin WordPress, có bản free), 3D FlipBook (trả phí), turn.js (cũ, cần jQuery).

**Việc còn lại**
- [ ] `CONFIG.FORM_URL`: link Google Form. Tuỳ chọn `CONFIG.FORM_SOURCE_ENTRY` để ghi nguồn bấm (nav / hero / signup / quiz / reader-end / fab).
- [ ] **CORS cho PDF**: pdf.js tải file bằng fetch, nên `cdn.telos.vn` phải trả header `Access-Control-Allow-Origin` cho domain đặt trang (và cho phép Range). Cách khác: đặt file PDF cùng domain với trang.
- [ ] Ảnh bìa thật thay cho bìa vẽ bằng CSS (`.book3d` ở hero và nút “Mở sách”).
- [ ] Ảnh 3 tác giả (`assets/author/…`), đang để chữ viết tắt.
- [ ] Số dự án mascot đã làm (S06), email và Facebook/LinkedIn ở footer.
- [ ] 1 câu chuẩn từ sách cho thẻ “Characterize & Humanize”.
- [ ] og:image, favicon, canonical, gắn GA/GTM (trang đã đẩy sự kiện vào `dataLayer`: `form_click`, `read_open`, `read_50`, `read_end`, `read_error`, `quiz_start`, `quiz_done`, `agency_click`).
- [ ] Chọn nơi đăng. Nếu đưa vào WordPress TELOS: bỏ nav/footer riêng, thêm tiền tố class, chừa chỗ cho header của site (xem playbook rebrand showcase).

**Nguồn nội dung:** mục lục, 4 chặng, 3 mức IP, 5 tiêu chí lấy từ file PDF đọc thử. Chặng 2 (Ambassador) chưa có tên tiếng Việt chính thức trong sách, đang tạm viết “Làm nhân viên của thương hiệu”.

## 10. Vòng sửa 26/11 (lần 2)

- Thanh trên cùng chỉ còn icon mascot (`assets/img/mascot-nav.webp`).
- Hero dùng ảnh sách gốc (`book-hero.webp`). Chữ gọn lại: nhãn “Một cuốn sách về hành trình của” + chữ lớn “NHÂN VẬT THƯƠNG HIỆU”, cả khối nghiêng -3°.
- Bỏ nhãn “Đọc trước tiên”. Kicker S03 đổi thành “Vì sao chúng mình viết cuốn sách này?”, đoạn 2 viết theo lời bạn. Thêm dải 4 ảnh intro của trang gốc, trượt ngang theo cuộn.
- Mục lục có thêm ảnh sách mở.
- Thêm section **Đội ngũ nào đã đứng sau những trang sách này?** theo phong cách giấy note của trang gốc: thẻ TELOS Agency + ảnh tập thể, thẻ “New Post”, câu trích + ảnh talk. Sau đó mới tới **Tác giả chấp bút** với ảnh thật. Số dự án: 50+.
- Footer: hello@telos.vn, facebook.com/TELOSVN.
- Ảnh dùng trên trang nằm trong `assets/img/` (đã nén webp, khoảng 500 KB). Thư mục `assets/Image/` là ảnh gốc; `assets/Image/bìa sách_files/` là file lưu từ trang cũ (JS/CSS), trang mới không dùng.

**Trình đọc thử: vì sao chưa hiện trên trang**
- Thư viện không lỗi: trang gốc dùng đúng pdf.js + StPageFlip, và trên telos.vn sách tải bình thường (86 trang).
- Nguyên nhân 1: bản trước bắt bấm “Mở sách” mới tải. Bản này **tự mở khi cuộn gần tới**.
- Nguyên nhân 2: `cdn.telos.vn` chỉ cho domain telos.vn tải file PDF (CORS). Mở trang từ máy, từ file:// hoặc domain khác thì bị chặn (đã kiểm tra trên trình duyệt: từ telos.vn tải được, từ domain khác bị chặn).
- Cách xử lý trong code: chạy trên *.telos.vn thì dùng file CDN; ở nơi khác dùng file cục bộ `assets/TELOS_Mascot_DocThu_TrangDoi.pdf` (3,5 MB), lỗi thì thử nguồn còn lại.
- [x] Tải file PDF đọc thử về, đặt vào `assets/` (43 trang PDF: bìa + 41 trang đôi + bìa sau → 84 trang sách). Đã test lật trang với file thật.
- [ ] Xem thử qua server cục bộ (`npx serve` hoặc Live Server), vì mở trực tiếp bằng file:// thì trình duyệt chặn đọc file PDF.

## 11. Vòng sửa 26/11 (lần 3)

- Hero cao đủ 1 màn hình, nền indigo đậm có lưới chấm, vòng tròn chuyển hồng (chấm phụ chuyển xanh sky). Menu chuyển chữ trắng khi còn ở hero.
- Khi cuộn xuống, chữ và ảnh ở hero lùi chậm rồi mờ dần, section “Sách dành cho ai” (bo góc trên) trượt lên phủ hero.
- Nền xanh của chữ “NHÂN VẬT” cao hơn, không còn cắt vào dấu.
- Thêm mascot của sách (`assets/img/bm-*.webp`) vào các block nội dung: mascot loa ở đầu “Bên trong sách”, 4 mascot thò đầu trên 4 thẻ (áo choàng · kính lúp · cầm hoa · cầm cọ), mascot giáo viên trên mục lục. Popup quiz dùng hình mascot gõ laptop như trang gốc.
- Bỏ ghi chú đỏ ở thẻ Characterize & Humanize.

## Lịch sử
| Ngày | Thay đổi |
|---|---|
| 26/11/2026 | Tạo tài liệu: đọc trang gốc, đề xuất cấu trúc 12 cụm, UX đọc thử, bộ câu hỏi Google Form |
| 26/11/2026 | Chốt cụm (mục 8). Dựng HTML bản 1 kèm trình đọc PDF lật trang, quiz, scrollytelling 4 chặng (mục 9) |
| 26/11/2026 | Quiz đổi sang 11 câu, kết quả hiện popup 4 mức với 2 lựa chọn tự nâng cấp / chuyên gia |
| 26/11/2026 | Vòng sửa 2: nav, hero ảnh sách gốc, section Đội ngũ, ảnh tác giả, footer, trình đọc tự tải + PDF cục bộ |
| 26/11/2026 | Gắn PDF thật vào trình đọc, khu đọc thử rộng toàn khung, bỏ ghi chú Google Form |
| 26/11/2026 | Vòng sửa 3: hero tối 100% màn hình + parallax reveal, thêm mascot trang trí khối nội dung sách |
