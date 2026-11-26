---
name: "len-camp-search"
description: "Lên chiến dịch Google Ads Search từ khóa thương hiệu (brand) cho dự án affiliate/ref link trong các tài khoản P7 Group, với mẫu quảng cáo đạt Ad strength Excellent."
---

# Lên Camp Search (từ khóa thương hiệu)

Dùng khi người dùng yêu cầu "lên chiến dịch tìm kiếm" cho một dự án/thương hiệu vào một tài khoản Google Ads con trong MCC "Admin - P7 Group Company Limited". Thao tác bằng Claude in Chrome trên tab Google Ads người dùng đang mở.

## Đầu vào cần có (hỏi nếu thiếu)
- Tên dự án / thương hiệu (vd: Checkr)
- Tài khoản đích: tên + Customer ID (vd: P7 Group 015 – 730-885-4299)
- Link ref (affiliate) – sẽ gắn ở **Final URL cấp từ khóa**
- **CPC tối đa – luôn do người dùng đưa theo từng dự án** (vd: 2k = 2.000₫). Nếu thiếu thì hỏi, không tự đặt, không tự đề xuất mức CPC.

## Cấu hình chuẩn (đã học từ camp Upwork – P7 Group 014; không cần đọc lại camp mẫu)
| Mục | Giá trị |
|---|---|
| Tên chiến dịch | Tên thương hiệu (vd: `Checkr`) |
| Loại | Search |
| Mạng | Google Search + Search Partners. **Bỏ tick Display Network** |
| Vị trí | Mặc định: "Enter another location" → để trống phần target (= tất cả quốc gia), **Exclude: Vietnam (country)**. Nếu người dùng chỉ định quốc gia (vd Australia, Indonesia): "Enter another location" → gõ từng nước → bấm **Include** ở dòng "… country" (không exclude Vietnam). Layout xê dịch sau mỗi lần thêm, chụp lại trước khi click ô tìm kiếm tiếp |
| Ngôn ngữ | Không có mục riêng – để mặc định |
| Đấu thầu | Focus **Clicks** (Maximize clicks), tick "Set a maximum CPC bid limit" = CPC người dùng đưa |
| Ngân sách | **7.000.000.000₫/ngày** (Average daily budget, custom) |
| Mục tiêu | Page view (bắt buộc chọn 1 goal) |
| AI Max | Bỏ qua – để mặc định (tắt), bấm Next ngay, không cần kiểm tra |
| Ad rotation | Optimize (mặc định) |
| Ad group | `Ad group 1` |
| Từ khóa | **Chỉ 1 từ khóa đối sánh chính xác**: `[tenthuonghieu]`. Không thêm phrase/broad, không thêm từ khóa mở rộng |
| Từ khóa phủ định | Danh sách từ gần giống / tương tự tên thương hiệu (xem bước 2) |
| Final URL quảng cáo | Trang chủ thương hiệu (vd: https://checkr.com) |
| Final URL từ khóa | **Link ref** |

## Quy trình

### 1. Nghiên cứu (trước khi vào Google Ads)
- WebFetch link ref để xem nó redirect về đâu (thường là trang signup của thương hiệu).
- WebFetch trang chủ + trang pricing + sitemap/menu để lấy số liệu thật (số khách hàng, giá gói, tính năng, tích hợp, phạm vi quốc gia) và **danh sách trang con thật của dự án** để chọn sitelink.
- Chỉ dùng claim có trên website chính thức. Không viết "Official Site" (đây là affiliate); dùng `Brand.com` thay thế.

### 2. Tìm từ khóa phủ định (từ gần giống / tương tự)
Mục đích: từ khóa exact vẫn khớp "close variants" (sai chính tả, gần giống), nên cần chặn các từ trông/nghe giống tên thương hiệu nhưng là thứ khác.
- Liệt kê biến thể gần giống tên thương hiệu: thêm/bớt/đổi 1 chữ cái, viết tách, đồng âm, số nhiều (vd Checkr → `checker`, `checkers`, `check r`, `chekr`, `checkrs`, `cheker`…).
- Tìm thương hiệu/sản phẩm/từ thông dụng khác có tên giống: WebSearch tên thương hiệu và các biến thể, xem gợi ý tìm kiếm, kết quả không thuộc thương hiệu (app, game, công ty khác, từ điển…).
- Giữ lại biến thể mà người tìm có thể vẫn muốn đúng thương hiệu (vd lỗi gõ rất phổ biến của chính tên đó) – nếu không chắc, liệt kê cho người dùng duyệt.
- Thêm vào chiến dịch dạng **negative exact** `[...]` (hoặc phrase "..." với cụm chắc chắn không liên quan). Không phủ định chính tên thương hiệu.
- Sau khi publish: Keywords → **Negative keywords** → + → chọn cấp Campaign → dán danh sách → Save.

### 3. Soạn nội dung quảng cáo (kiểm tra độ dài bằng Python trước khi nhập)
- **15 headline** (≤30 ký tự), không trùng nhau, có từ khóa thương hiệu ở nhiều headline: `Brand.com`, `Brand + sản phẩm chính`, lợi ích, giá "From $X", social proof, "No Contracts…", tích hợp, CTA ("Get Started With Brand"), phạm vi.
- **4 description** (≤90 ký tự), mỗi cái có lợi ích + số liệu + CTA.
- **Display path**: KHÔNG điền – bỏ qua, để trống 2 ô path (ô này hay không nhận nhập liệu và không cần để đạt Ad strength Excellent).
- **Business name**: tên thương hiệu (khớp domain URL).
- **Sitelink – tùy theo từng dự án**: chọn 4–6 trang con thật, phù hợp với hành động mà link ref nhắm tới (thường là đăng ký/mua). Ưu tiên: pricing/gói, sản phẩm/tính năng chính, use case/đối tượng, đăng ký (dùng link ref), liên hệ sales/enterprise. **Tránh** trang dành cho người không phải khách mục tiêu (login, hỗ trợ khách hàng cũ, trang cho ứng viên/người dùng cuối, careers). Text ≤25, mô tả ≤35, **mỗi sitelink một URL khác nhau**. Nếu dự án không rõ nên chọn trang nào, liệt kê đề xuất cho người dùng duyệt.
- **8 callout** (≤25).
- **Structured snippet**: header phù hợp (`Service catalog`, `Types`, `Brands`…), 4–6 giá trị ≤25 ký tự.
- **Price asset** (nếu dự án có bảng giá công khai): Type phù hợp (vd `Service tiers`), tiền tệ của site, qualifier `From`, 3–4 mục (header ≤25, mô tả ≤25). Xoá các mục thừa (form mặc định có 5).

### 4. Logo và hình ảnh (bắt buộc – tự lấy từ website chính thức)
Người dùng đã cho phép sẵn: **tự lấy logo và ảnh trên website chính thức của thương hiệu** để đúng nhận diện, không cần hỏi lại. Chỉ lấy từ domain chính thức của thương hiệu (và CDN ảnh mà trang đó dùng), không lấy từ site bên thứ ba.

**Tìm nguồn logo (theo thứ tự):**
1. Trang press / media kit / brand assets của thương hiệu (WebSearch `brand press kit logo site:domain`).
2. Logo trong header website: thường là SVG inline hoặc `<img>` – mở website bằng Chrome (tab mới), dùng `javascript_tool` lấy `outerHTML` của SVG/`src` của ảnh logo trong `header`.
3. `apple-touch-icon` / favicon lớn / `og:image` (WebFetch hoặc `javascript_tool` đọc thẻ `<link>`/`<meta>`).

**Chuẩn bị file (Python/PIL, cairosvg cho SVG) trong scratchpad:**
- **Business logo**: vuông 1:1, 1200×1200 (tối thiểu 128×128), logo căn giữa, padding ~15%, nền trắng hoặc màu thương hiệu. Ưu tiên biểu tượng (icon) nếu wordmark quá dài.
- **Images** (3–4 ảnh): lấy ảnh hero/sản phẩm/og:image trên website; xuất ngang 1.91:1 (1200×628) và vuông 1:1 (1200×1200), thêm dọc 4:5 (960×1200) nếu đủ nội dung; <5MB; không chữ đè lớn, không viền, không mờ. Nếu website không có ảnh phù hợp thì chỉ thêm logo và báo người dùng.
- Luôn `Read` lại file PNG đã xuất để nhìn kiểm tra trước khi tải lên.

**Nếu môi trường cloud không tải được file** (proxy chặn domain, curl 403): không tìm cách vòng qua proxy. Thay vào đó dùng Chrome: mở logo/ảnh trên website, `computer` zoom vùng logo (nền sạch) → dùng `upload_image` với screenshot ID đó vào ô tải logo/ảnh của Google Ads (screenshot ID hết hạn sau vài phút – chụp ngay trước khi tải). Nếu vẫn không được thì báo người dùng và xin file.

**Gắn vào quảng cáo:** trong ad editor mục **Business logo** (+ Business logo) và **Images** (More asset types). Dùng `find` lấy ref ô input file rồi `file_upload` (không bấm nút mở hộp chọn file) → crop theo khung Google → Save. Nếu chiến dịch đã publish: Assets → + → Business logo / Image → cấp Campaign.
- Lưu ý: business name/logo cần Google duyệt (tài khoản xác minh dưới tên "P7 Group Company Limited"); báo người dùng nếu asset chờ duyệt/bị từ chối.

### 5. Tạo chiến dịch
1. Account switcher → chọn tài khoản đích → **+ New campaign**.
2. Objective: **Create a campaign without guidance** → Continue → type **Search** (có thể đang chọn sẵn Display, click lại Search) → đặt tên + nhập URL trang chủ bằng `form_input` (giao diện mới không còn ô tick "Website visits", chỉ có ô URL) → Continue; danh sách goal hiện bên dưới, cuộn xuống chọn Page view.
3. Goal: chọn **Page view**. Ở "Turn on enhanced conversions" **bỏ tick** (nút đổi thành "Continue", tránh tự đồng ý điều khoản dữ liệu).
4. Bidding: Clicks → tick max CPC → nhập CPC người dùng đưa.
5. Campaign settings: bỏ Display; Locations như bảng trên; More settings giữ mặc định.
6. **AI Max: bỏ qua** – bấm **Next** ngay (mặc định đã tắt), không cuộn/kiểm tra.
7. **Keyword and asset generation: bỏ qua** – bấm **Skip** ngay, không điền Final URL, không Generate.
8. Keywords and ads: **bỏ qua phần "Get keyword suggestions (optional)"** (không điền Final URL/products, không bấm Get keyword suggestions) – nhập thẳng đúng 1 từ khóa `[brand]` vào ô "Enter keywords"; bỏ qua gợi ý "Add more keywords"; bỏ qua path (để trống), điền 15 headline (nút "+ Headline" thêm ô, lấy ref bằng `read_page` vùng Headlines), 4 description, business name, **business logo, images**, sitelinks, callouts, structured snippet, prices. Mục tiêu: **Ad strength = Excellent**.
9. Budget: Set custom budget = 7.000.000.000 (`find` lấy ref ô budget, ctrl+a rồi gõ).
10. Review → kiểm tra lại (Locations có loại trừ Vietnam, CPC đúng; dòng "Asset optimization … turned on" ở trang Review là hiển thị sai, bỏ qua) → **Publish campaign** (người dùng đã yêu cầu lên camp = đồng ý publish; nếu chưa rõ thì hỏi trước).
11. Bỏ qua trang "Set up with a Google Tag".

### 6. Sau khi publish (bắt buộc)
- **Gắn link ref vào Final URL từ khóa**: campaign → Audiences, keywords, and content → **Keywords** → hover ô Final URL của `[brand]` → `find` nút "Edit this Final URL" → nhập link ref → **Save**. Zoom kiểm tra cột Final URL hiển thị đúng link.
- **Thêm từ khóa phủ định** (danh sách ở bước 2) ở tab Negative keywords, cấp Campaign.
- Kiểm tra Assets: logo/ảnh/sitelink đã gắn vào campaign, không bị từ chối.

## Lưu ý kỹ thuật (bổ sung từ lần chạy Ploy AI)
- Ad strength đạt Excellent chỉ với 15 headline + 4 description + 6 sitelink; logo/ảnh không bắt buộc để đạt Excellent nhưng vẫn nên thêm.
- `javascript_tool` có thể bị chặn ("Cookie/query string data") khi trang có URL kèm query → dùng screenshot/zoom. `zoom` chỉ ra ảnh rất nhỏ (~115px) nên KHÔNG đủ làm logo (tối thiểu 128px); cần xin người dùng file logo sớm, ngay khi bắt đầu nếu cloud không tải được site (curl 403).
- Tab trong form sitelink bị nhảy qua nút "?" → không dùng Tab, điền từng ô bằng ref/toạ độ. Mở sitelink 2–6 bằng click header; ref ô của sitelink kế tiếp lệch +78.
- Callout: bấm "Add callout text" 4 lần (mỗi lần nút dịch ~58px) rồi điền bằng toạ độ. Price asset: xoá các mục trống bằng thùng rác từ dưới lên.
- Bước Locations: chọn "Enter another location" xong layout xê dịch, chụp lại trước khi gõ Vietnam; EU political ads bị bỏ chọn khi đổi layout → chọn lại "No".
- Sau Publish, vào tài khoản đích bằng account switcher (mục Recent), mở campaign → Keywords/Negative keywords. Negative keywords gõ nhiều dòng bằng ký tự xuống dòng trong một lệnh type.
- Hộp thoại "Confirm it's you" có thể xuất hiện ở bước Review: dừng, nhờ người dùng tự xác minh; sau đó bản nháp vẫn còn, bấm Publish tiếp.

## Lưu ý kỹ thuật (bổ sung từ lần chạy Emergent, Hunter 001)
- Thiếu tài khoản đích thì hỏi trước (tài khoản có thể thuộc nhóm MCC khác như "Hunter 01"; chọn trong account picker bằng `find` + click ref).
- Ô Enter keywords được điền sẵn ~25 từ khóa gợi ý: dùng `form_input` ghi đè thành đúng `[brand]`.
- Sau Skip ở Keyword and asset generation có thể bật panel "Ask Advisor", đóng bằng dấu X.
- Headline: form có sẵn 8 ô, bấm "+ Headline" 7 lần rồi `read_page` với ref_id vùng Headlines để lấy 15 ref. Description cũng có gợi ý sẵn, ghi đè bằng `form_input`.
- Sitelink: ref các ô tăng +33 mỗi sitelink (text, desc1 +7, desc2 +16, URL +23). Nếu `form_input` báo lỗi ngay sau khi mở sitelink mới, gọi lại từng lệnh riêng (không dùng batch).
- Callout: bấm "Add callout text" 4 lần, `find` 8 ref rồi `form_input`, Save rồi Apply.
- Price asset: Type "Product tiers" (SaaS có gói) hoặc "Service tiers"; Qualifier From; mỗi mục đơn vị "Per month"; ref ô header của mục 2+ không ổn định, dùng click toạ độ + `type`. Xoá mục trống từ dưới lên, chụp lại vì layout dịch.
- Structured snippet: "More asset types" → Structured snippets → header "Service catalog" (cuộn danh sách) → "Add value" 2 lần để đủ 5 giá trị → Create → Save.
- Business name/logo bị khoá sau "Get access" (cần xác minh nhà quảng cáo): bỏ qua, gửi file logo cho người dùng.
- Sau Publish nếu Overview báo "Your account cannot show ads / Payment method is missing": không tự nhập thanh toán, báo người dùng bổ sung billing.
- Dấu cảnh báo cam ở mục Bidding trong sidebar có thể còn hiển thị dù cài đặt đã đúng; kiểm tra bước Bidding rồi bỏ qua.
- Final URL từ khóa: link ref có query nên `javascript_tool` bị chặn; click "Edit this Final URL" rồi `type` thẳng vào ô đang focus.

## Lưu ý kỹ thuật (gốc)
- Nếu hiện hộp thoại **"Confirm it's you"** (xác minh danh tính) hoặc "Changes failed to save": dừng lại, nhờ người dùng tự bấm Confirm/xác minh, không tự đăng nhập.
- Ô textarea trống: `ctrl+a` có thể gõ ra chữ "a". Khi cần xoá textarea, dùng `ctrl+End` + BackSpace nhiều lần rồi gõ lại; luôn zoom kiểm tra bộ đếm ký tự.
- Layout wizard hay xê dịch sau mỗi thao tác → ưu tiên `find`/ref thay vì toạ độ cố định, chụp màn hình sau mỗi batch.
- Dùng `browser_batch` để gom nhiều thao tác; không bấm nút có thể bật dialog chặn.
- Sau cùng báo cáo: cấu hình đã lên, nội dung quảng cáo, Ad strength, link ref đã gắn, danh sách phủ định, logo/ảnh, và các điểm cần người dùng quyết.

## Mẹo tiết kiệm thời gian & token
- Làm nghiên cứu + soạn toàn bộ nội dung (headline, description, sitelink, callout, snippet, price, phủ định) và kiểm tra độ dài bằng **một** lệnh Python **trước** khi mở Google Ads.
- Gom thao tác bằng `browser_batch`; chụp màn hình ở scale 0.5–0.6, chỉ chụp full khi cần đọc chữ nhỏ; dùng `zoom` để kiểm tra vùng nhỏ.
- Lấy ref ô nhập bằng `find`/`read_page` (filter interactive, ref vùng) thay vì đoán toạ độ; khi thêm nhiều ô (headline, callout) bấm nút "+" nhiều lần trong một batch rồi đọc ref một lần.
- **Không đọc campaign mẫu** (Upwork hay bất kỳ camp nào khác) – cấu hình chuẩn ở trên đã được học một lần, dùng thẳng. Mọi cải tiến đi qua phần "Tự tối ưu skill" bên dưới.

## Tự tối ưu skill sau mỗi lần làm (bắt buộc, cuối mỗi lần chạy)
Sau khi báo cáo kết quả chiến dịch, tự rà lại lần chạy vừa xong và đề xuất cập nhật skill:
1. Ghi nhận: bước nào tốn nhiều lượt gọi tool/thời gian, chỗ nào thao tác sai phải làm lại, giao diện Google Ads có gì thay đổi, lỗi/hộp thoại mới gặp, và góp ý người dùng đưa ra trong lần này.
2. Đọc SKILL.md hiện tại, viết bản cập nhật **đầy đủ** (giữ mọi nội dung còn đúng): rút gọn bước thừa, thêm cách làm nhanh hơn/ít token hơn (ref, selector, thứ tự batch), sửa hướng dẫn lỗi thời, thêm lưu ý mới.
3. Gọi `propose_skills` (kind `improvement`, target `len-camp-search`) để người dùng duyệt – không tự sửa file skill trên đĩa.
4. Trong câu trả lời, tóm tắt ngắn 2–4 điểm đã thay đổi và (nếu có) 1 đề xuất tối ưu thêm cho chiến dịch/quy trình để người dùng quyết.
5. Nếu lần chạy suôn sẻ, không có gì đáng sửa thì nói rõ "skill không cần cập nhật" thay vì đề xuất cho có.
