# Đề cương: "Bé chơi Arduino cùng TurboWarp" (bản nháp 6, để duyệt)

Dành cho: bé 6 tuổi học cùng bố mẹ · Mỗi bài 10–15 phút · Lập trình bằng khối TurboWarp, mạch Arduino Uno · Chạy trên web **Ong Nhỏ Code**.

Bộ tài liệu gồm 2 cuốn:
- **Sách học**: trên web, mỗi bài có phần cho bé và phần cho bố mẹ.
- **Bài tập trên web**: bé làm sau mỗi bài; giáo viên xem lại và chấm ngay trên web.

## 1. Sách nguồn

| # | Sách | Giấy phép | Cách dùng |
|---|---|---|---|
| A | **SparkFun Inventor's Kit Experiment Guide v4.1** (SparkFun Electronics) | CC BY-SA 4.0 | **Sách chính**: thí nghiệm, sơ đồ nối dây, lỗi thường gặp. Được dịch và chỉnh sửa |
| B | **ARDX Arduino Experimenter's Guide** (Oomlout) | CC BY-SA | Thêm bài đèn chạy đuổi, bài phát nhạc, và **tấm hình in dán lên breadboard** để biết cắm linh kiện vào đâu. Được dịch và chỉnh sửa |
| + | *Arduino Programming Notebook* (Brian W. Evans) | CC BY-SA 3.0 | Tham khảo cho bố mẹ, không đưa vào phần của bé |

Nguồn tải:
- A: https://learn.sparkfun.com/tutorials/sparkfun-inventors-kit-experiment-guide---v41
- B: https://haseloff.plantsci.cam.ac.uk/resources/Arduino/ARDX-EG-OOML-DD.pdf (bản lưu tại Đại học Cambridge; trang gốc là ardx.org / oomlout.com)

### 1.1 Giấy phép

- Sách A và B đều là **CC BY-SA**. Nội dung CC BY-SA 3.0 được phép phát hành lại theo CC BY-SA 4.0, nên **gộp A và B làm một được**. Toàn bộ sách học và bài tập phát hành theo **CC BY-SA 4.0**.
- *Beginning Arduino* (Michael McRoberts, Apress 2010) chỉ dùng để **đối chiếu danh sách linh kiện** bạn đang có. Sách ghi "All rights reserved", nên không dịch, không chép lời, hình hay code của sách, và không đưa file PDF lên web.
- Không dùng *Arduino Projects Book* (cả lời, hình lẫn ý tưởng), vì giấy phép CC BY-NC-SA của sách này không gộp được với CC BY-SA. Mọi bài học chỉ lấy từ sách A và B, hoặc do mình tự viết.
- Trang "Nguồn tài liệu" trên web sẽ ghi:
  > Phỏng theo *SparkFun Inventor's Kit Experiment Guide v4.1* (SparkFun Electronics, CC BY-SA 4.0) và *ARDX Experimenter's Guide* (Oomlout, CC BY-SA). Nội dung đã được lược bớt, dịch và biên soạn lại cho trẻ 6 tuổi. Phát hành theo CC BY-SA 4.0.

> Cần đối chiếu: tên và thứ tự các thí nghiệm bên dưới lấy theo cấu trúc sách mà mình biết. Từ môi trường làm việc này không mở được các trang tải sách, nên trước khi dịch mình sẽ kiểm tra lại với bản PDF.

## 2. Lộ trình bài học

⭐ = bài chính · ➕ = bài thêm, có thể bỏ qua nếu bé mệt hoặc thiếu linh kiện

| Chặng | Bài | Tên cho bé | Bé làm gì | Nguồn |
|---|---|---|---|---|
| **0. Làm quen** | 0.1 ⭐ | Gặp bạn Arduino | Xem tranh: Arduino là "bộ não nhỏ", dây là "đường đi", đèn là "đôi mắt" | Tự viết |
| | 0.2 ⭐ | Mèo biết đi | Ghép khối cho mèo đi trên màn hình | Tự viết |
| | 0.3 ⭐ | Làm lại nhiều lần | Khối `lặp lại`: mèo nhảy 5 lần | Tự viết |
| **1. Ánh sáng** | 1.1 ⭐ | Đèn ơi, sáng lên! | Bật và tắt một đèn LED | A 1A · B CIRC-01 |
| | 1.2 ⭐ | Đèn nháy như tim đập | Đèn nhấp nháy, nhanh hoặc chậm | A 1A · B CIRC-01 |
| | 1.3 ⭐ | Đèn giao thông | 3 đèn đỏ, vàng, xanh bật lần lượt | Tự viết, dựa trên A 1A |
| | 1.4 ➕ | Đèn chạy đuổi | 4 đèn sáng nối đuôi nhau như đoàn tàu | B CIRC-02 (rút từ 8 đèn còn 4) |
| | 1.5 ⭐ | Nút bấm thần kỳ | Giữ nút thì đèn sáng, thả ra thì đèn tắt | B CIRC-07 |
| | 1.6 ⭐ | Núm xoay thần kỳ | Xoay núm thì mèo trên màn hình đi theo | A 1B · B CIRC-08 |
| | 1.7 ⭐ | Đèn ngủ biết tự bật | Che tay lên cảm biến thì đèn sáng | A 1C · B CIRC-09 |
| | 1.8 ⭐ | Đèn cầu vồng | Trộn 3 đèn đỏ, xanh lá, xanh dương thành nhiều màu | A 1D · B CIRC-12 |
| | 1.9 ➕ | Màn hình mặt cười | Bảng đèn 8×8 hiện mặt cười, trái tim, mũi tên; bé vẽ hình trên màn hình máy tính thì bảng đèn hiện theo | Tự viết |
| **2. Âm thanh** | 2.1 ⭐ | Còi kêu bíp bíp | Bấm phím trên máy tính thì còi kêu | A 2A |
| | 2.2 ⭐ | Còi biết hát | Còi phát bài "Kìa con bướm vàng" | B CIRC-06 (đổi bài hát) |
| | 2.3 ⭐ | Chiếc kèn tí hon | Mỗi nút bấm phát một nốt nhạc | A 2B |
| | 2.4 ➕ | Núm chỉnh to nhỏ | Xoay núm thì tiếng còi to lên hoặc nhỏ đi | A 2A (núm chỉnh âm lượng trong mạch còi) |
| | 2.5 ⭐ | Trò chơi bắt chước | Đèn sáng theo thứ tự, bé bấm nút lặp lại (3 bước) | A 2C |
| | 2.6 ➕ | Gõ cửa cốc cốc | Gõ nhẹ lên bàn cạnh miếng piezo thì đèn sáng và mèo trên màn hình chạy ra mở cửa | Tự viết |
| **3. Chuyển động** | 3.1 ⭐ | Cánh tay vẫy chào | Động cơ servo vẫy qua vẫy lại | A 3A · B CIRC-04 |
| | 3.2 ⭐ | Đôi mắt dơi | Cảm biến khoảng cách: tay lại gần thì mèo kêu "meo" | A 3B |
| | 3.3 ⭐ | Chuông báo có khách | Có người lại gần thì còi kêu và đèn nháy | A 3C |
| | 3.4 ➕ | Tay cầm chơi game | Đẩy cần điều khiển (joystick) thì nhân vật trên màn hình chạy theo và servo quay theo | Tự viết |
| **4. Nóng – lạnh** | 4.1 ⭐ | Hôm nay nóng hay lạnh? | Trời nóng hiện mặt trời, trời lạnh hiện người tuyết | A 4B · B CIRC-10 |
| | 4.2 ➕ | Nhiệt kế đèn màu | Nóng thì đèn sáng màu đỏ, mát thì đèn sáng màu xanh | Ghép A 4B với A 1D · B CIRC-10 với CIRC-12 |
| **5. IoT nhí** | 5.1 ⭐ | Mạch nói chuyện với máy tính | Bấm nút trên mạch thì nhân vật trên màn hình nhảy, bấm nút trên màn hình thì đèn trên mạch sáng | Tự viết |
| | 5.2 ➕ | Đèn báo từ máy tính | Bé bấm hình trên màn hình thì đèn trên mạch đổi màu và còi kêu "ting" | Tự viết (dùng mạch A 1D và A 2A) |
| | 5.3 ⭐ | Ngôi nhà thông minh mini | Ghép lại: trời tối thì đèn tự bật, có người đến thì chuông kêu | Tự viết (dùng mạch 1.7 và 3.2) |
| | 5.4 ➕ | Thẻ thần kỳ | Chạm thẻ RFID vào đầu đọc thì màn hình chào đúng tên chủ thẻ, đèn xanh sáng: "Mời vào!" | Tự viết |

**Tổng cộng: 28 bài, trong đó 20 bài chính và 8 bài thêm.** Nếu mỗi tuần học 2 bài thì 20 bài chính mất khoảng 2,5 tháng; bài thêm học khi bé thích.

Bốn bài thêm 1.9, 2.6, 3.4, 5.4 được bổ sung vì bộ linh kiện của bạn có bảng đèn 8×8, miếng piezo, cần điều khiển và đầu đọc RFID (xem mục 7).

### Mỗi sách đóng góp gì

| | A: SIK | B: ARDX | Tự viết |
|---|---|---|---|
| Số bài dùng | 15 | 11 (nhiều bài trùng với A; khi trùng, lấy sơ đồ của A và tấm hình dán breadboard của B) | 7 |
| Phần lấy | Thí nghiệm, sơ đồ, lỗi thường gặp | Đèn chạy đuổi, nút bấm, phát nhạc, tấm hình dán breadboard | Làm quen, đèn giao thông, IoT |

## 3. Những phần lược bỏ

| Phần | Lý do bỏ | Thay bằng |
|---|---|---|
| Màn hình LCD (A 4A, 4C) | Bé chưa đọc tốt; nối dây nhiều và dễ sai | Hiện hình trên màn hình TurboWarp |
| Robot (A, chặng 5) | Nhiều linh kiện, dễ nối nhầm, tốn kém | Phần mở rộng cho bé lớn hơn |
| Động cơ DC, relay, transistor, thanh ghi dịch (B CIRC-03, 05, 11) | Cần nguồn điện riêng; mạch khó với bé | Bỏ |
| Lý thuyết điện (định luật Ohm, PWM...) | Quá khó với bé | Một câu ví von trong phần bố mẹ |
| Code C++ | Bé dùng khối TurboWarp | Code gốc chỉ để ở phần bố mẹ, nếu cần |

## 4. Cấu trúc mỗi bài (sách học trên web)

**Phần cho bé** (chữ to, có nút 🔊 đọc to):
1. 👀 **Xem**: một hình minh họa và một câu giới thiệu.
2. 🧩 **Ghép khối**: hình các khối cần dùng, đánh số 1, 2, 3. Bài mẫu đã mở sẵn trong TurboWarp.
3. ▶️ **Thử**: bấm cờ xanh để chạy.
4. ⭐ **Thưởng**: nhận sao và một câu "Thử thêm" nếu bé muốn chơi tiếp.
5. ✏️ **Làm bài tập**: mở phần bài tập của bài, làm xong bấm "Nộp bài".

**Phần cho bố mẹ** (thu gọn, bấm để mở):
- Linh kiện cần chuẩn bị (có ảnh).
- Sơ đồ nối dây, lấy hình từ sách A và chú thích bằng tiếng Việt.
- Tấm hình dán breadboard để in ra (dựa trên sách B).
- Lỗi thường gặp.
- Gợi ý câu hỏi để trò chuyện với bé.
- Ghi nguồn của bài.

## 5. Bài tập trên web (dùng hệ thống của Ong Nhỏ Code)

Bé làm bài tập ngay trên web. Giáo viên xem lại và chấm ở trang **Lớp học → Bài nộp**, giống hệt cách web Ong Nhỏ Code đang làm. Khoá Arduino **dùng lại** đăng nhập, lớp học, máy chấm và trang chấm bài sẵn có, chỉ thêm những phần còn thiếu.

### 5.1 Những gì web Ong Nhỏ Code đã có (dùng lại nguyên)

| Có sẵn | Dùng cho khoá Arduino thế nào |
|---|---|
| Đăng nhập bằng **mã lớp + mật mã 4 hình**, in thẻ đăng nhập | Bé 6 tuổi đăng nhập như hiện nay |
| 3 vai trò: quản trị, giáo viên, học sinh | Giữ nguyên |
| TurboWarp nhúng trong trang bài học; tự lưu sau mỗi 45 giây | Thêm các khối Arduino vào đúng trình soạn thảo này |
| Thẻ *Bài học / Bài tập / Trang sách* | *Trang sách* hiện trang gốc của SIK hoặc ARDX cho bố mẹ và giáo viên |
| Nút 🔊 **Nghe đọc**, hình khối lệnh đúng màu, nút 💡 **Gợi ý** chỉ trực tiếp trên Scratch | Dùng cho mọi bài Arduino |
| Câu **trắc nghiệm** chấm ngay | Dạng "Đoán xem" (đáp án là hình 🐇 / 🐢) |
| Bài **thực hành**: kiểm tra bé đã dùng đúng loại khối chưa | Kiểm tra bé đã dùng khối `bật đèn`, `chờ`, `liên tục`... chưa |
| Giáo viên **mở bài nộp trong Scratch**, cho điểm 0–100 và nhận xét; sao của bài tự tính từ điểm | Giữ nguyên, thêm phần chấm nhanh (mục 5.3) |
| **Gói nội dung soạn sẵn** (`content/packs/`) và lời giải mẫu | Viết khoá Arduino theo đúng mẫu này |

### 5.2 Các dạng bài tập

| Dạng | Bé làm gì | Chấm | Trạng thái |
|---|---|---|---|
| 🤔 **Đoán xem** | Chạm vào một hình (🐇 hay 🐢, 💡 hay 🔊) | Tự động | ✅ Có sẵn (trắc nghiệm) |
| 🚀 **Thực hành trên mạch** | Ghép khối trong TurboWarp, chạy trên Arduino, bấm "Nộp bài" | Tự động kiểm tra khối + giáo viên chấm thêm | ✅ Có sẵn (thực hành) |
| 🔍 **Sửa lỗi** | Dự án có lỗi đã mở sẵn (ví dụ thiếu khối `tắt đèn`), bé sửa lại | Tự động kiểm tra khối + giáo viên | ✅ Có sẵn (giống bài "Sửa lỗi!" trong gói Lập trình sáng tạo) |
| 🧩 **Xếp khối** | Kéo các thẻ khối vào đúng thứ tự, ngay trong tab Bài tập | Tự động | 🆕 Cần thêm |
| 🔗 **Nối hình** | Kéo đường nối "còi" với 🔊, "đèn" với 💡 | Tự động | 🆕 Cần thêm |
| 🎨 **Tô màu** | Chạm vào đèn để tô màu | Tự động | 🆕 Cần thêm |
| 🖍️ **Vẽ ý tưởng** | Vẽ bằng ngón tay hoặc chuột | Giáo viên chấm | 🆕 Cần thêm |
| 📷 **Chụp ảnh mạch** | Bố mẹ chụp ảnh hoặc quay video ngắn mạch đang chạy, đính kèm khi nộp | Giáo viên chấm | 🆕 Cần thêm |
| 🎤 **Kể cho cô nghe** | Ghi âm tối đa 30 giây | Giáo viên chấm | 🆕 Cần thêm |

Khi bé làm sai câu chấm tự động, web nói "Gần đúng rồi, con thử lại nhé!". Điểm được giữ ở lần làm tốt nhất, như web đang làm.

### 5.3 Thêm vào trang chấm bài của giáo viên

| Thêm | Lý do |
|---|---|
| **Hộp bài cần chấm** cho cả lớp, chấm xong tự chuyển sang bài tiếp theo | Hiện phải mở từng học sinh |
| Xem hình vẽ, ảnh/video mạch, nghe ghi âm ngay trong bảng bài nộp | Các dạng bài mới |
| Nút chấm nhanh **⭐ / ⭐⭐ / ⭐⭐⭐** (tương ứng 50 / 80 / 100 điểm) bên cạnh ô điểm | Bé 6 tuổi hiểu sao hơn hiểu điểm |
| Câu khen mẫu bấm chọn nhanh, và **ghi âm lời khen** | Bé chưa đọc được nhận xét |
| Nút **Cho làm lại** kèm gợi ý | Bé sửa bài theo lời cô |
| Thống kê câu nhiều bé làm sai | Giáo viên giảng lại |

### 5.4 Phần thưởng

- Sao của mỗi bài tính tự động như web đang làm. Xong mỗi chặng được 1 **huy hiệu**: "Bé làm quen", "Bé ánh sáng", "Bé âm nhạc", "Bé chuyển động", "Bé nóng lạnh", "Kỹ sư IoT nhí".
- Xong cả khoá được **giấy khen "Kỹ sư nhí"** để in.
- Không có bảng xếp hạng giữa các bé.

### 5.5 Câu hỏi mẫu: Bài 1.2 "Đèn nháy như tim đập"

| Câu | Dạng | Đề (đọc to) | Đáp án / Cách chấm |
|---|---|---|---|
| 1 | 🎨 Tô màu | "Con chạm để tô đỏ những đèn đang **sáng** nhé!" (4 đèn: sáng, tắt, sáng, tắt) | Đèn 1 và 3 · tự động |
| 2 | 🧩 Xếp khối | "Con kéo các khối vào trong vòng lặp để đèn nháy nhé!" | `bật đèn` → `chờ 1 giây` → `tắt đèn` → `chờ 1 giây` · tự động |
| 3 | 🤔 Đoán xem | "Đổi *chờ 1 giây* thành *chờ 0.2 giây*, đèn nháy giống bạn nào?" | 🐇 Thỏ · tự động |
| 4 | 🚀 Thực hành | "Con làm đèn nháy trên mạch rồi nộp cho cô nhé!" (kèm ảnh mạch nếu muốn) | Kiểm tra có khối cờ xanh, `liên tục`, `bật đèn`, `tắt đèn`, `chờ` · giáo viên chấm thêm |
| 5 | 🖍️ Vẽ | "Con vẽ một thứ cũng nhấp nháy mà con biết nhé!" | Giáo viên chấm sao |

### 5.6 Bảo vệ dữ liệu của trẻ

- Giữ như web đang làm: bé chỉ có tên gọi, con vật đại diện và mật mã hình.
- Ảnh, video và ghi âm chỉ giáo viên của lớp xem được. Có tuỳ chọn tự xoá sau khi kết thúc khoá học.
- Nhắc bố mẹ chỉ chụp mạch, **không chụp mặt bé**.

## 6. Bài mẫu trong sách học (để bạn duyệt giọng văn)

### Bài 1.2: Đèn nháy như tim đập 💓

**👀 Xem**
> Tim của con đập "thình thịch, thình thịch". Hôm nay mình dạy đèn đập giống trái tim nhé!

**🧩 Ghép khối**
1. Kéo khối 🚩 `khi bấm cờ xanh`
2. Kéo khối 🔁 `liên tục`
3. Bỏ vào trong: 💡 `bật đèn`, rồi ⏱️ `chờ 1 giây`
4. Bỏ tiếp: 💡 `tắt đèn`, rồi ⏱️ `chờ 1 giây`

**▶️ Thử**
> Bấm cờ xanh. Đèn có nháy không con?

**⭐ Thử thêm**
> Đổi số `1` thành `0.2`. Đèn nháy nhanh hay chậm hơn? Tim lúc con chạy nhảy cũng đập nhanh như thế đấy!

**Phần cho bố mẹ**
- Cần: Arduino Uno, cáp USB, 1 đèn LED, 1 điện trở 150–330Ω, breadboard, 2 dây nối.
- Nối dây: chân dài của LED nối vào chân số 13 qua điện trở, chân ngắn nối vào GND (theo hình mạch 1A trong sách A). In tấm hình dán breadboard (dựa trên CIRC-01 trong sách B), đặt lên breadboard rồi cắm theo hình.
- Đèn không sáng? Thử cắm ngược LED lại. LED chỉ sáng khi cắm đúng chiều.
- Gợi ý hỏi bé: "Ngoài đèn ra, còn cái gì cứ bật tắt liên tục nữa?" (đèn giao thông, đèn xe cứu thương...)

## 7. Linh kiện: đối chiếu với bộ của bạn

Bạn có các linh kiện giống trong sách *Beginning Arduino* (Apress). Bảng dưới so từng bài với linh kiện trong sách đó.

✅ = có trong sách · ❓ = sách có nhắc đến nhưng cần bạn xác nhận đã có · 🔁 = khác linh kiện trong SIK/ARDX, khối lệnh và hướng dẫn nối dây sẽ viết theo linh kiện của bạn

| Bài | Linh kiện dùng | Trong bộ của bạn | Ghi chú |
|---|---|---|---|
| Mọi bài | Arduino Uno, cáp USB, breadboard, dây nối, điện trở | ✅ | Sách dùng breadboard 840 lỗ |
| 1.1–1.4 | Đèn LED đỏ, vàng, xanh lá (10 đèn đỏ cho đèn chạy đuổi) | ✅ | Đèn chạy đuổi rút còn 4 đèn |
| 1.5, 2.3, 2.5, 5.1 | Nút bấm | ✅ | Cần 3–4 nút. Sách chỉ dùng 1 nút, cần xác nhận số lượng |
| 1.6 | Biến trở (núm xoay) 4,7kΩ hoặc 10kΩ | ✅ | |
| 1.7, 5.3 | Quang trở + điện trở 10kΩ | ✅ | |
| 1.8, 4.2, 5.2 | 3 đèn LED đỏ, xanh lá, xanh dương | ✅ 🔁 | SIK dùng 1 đèn RGB; bộ của bạn dùng 3 đèn rời (đèn RGB 4 chân là ❓). Khối lệnh `đèn màu (đỏ)` dùng được cho cả hai |
| 1.9 | Bảng đèn 8×8 | ❓ 🔁 | Sách nối bảng đèn qua IC MAX7219 trên breadboard. Nếu bạn có **module 8×8 có sẵn MAX7219** (5 chân) thì bé dùng dễ hơn nhiều |
| 2.1–2.5 | Còi piezo | ✅ | Piezo phát được nốt nhạc |
| 2.4 | Còi piezo + biến trở | ✅ | |
| 2.6 | Miếng piezo + điện trở 1MΩ | ✅ | Dùng chính miếng piezo làm cảm biến gõ |
| 3.1 | Servo nhỏ (2 cái) | ✅ | |
| 3.2, 3.3, 5.3 | Cảm biến khoảng cách **LV-MaxSonar EZ3** | ✅ 🔁 | SIK dùng HC-SR04. MaxSonar cho số đo trực tiếp, dễ nối hơn. Chương trình nạp cho mạch hỗ trợ cả hai loại |
| 3.4 | Joystick 2 trục (hoặc 2 biến trở) | ❓ | |
| 4.1, 4.2 | Cảm biến nhiệt độ **DS18B20** | ✅ 🔁 | Thay cho TMP36/DHT11. Không phải chỉnh, đo chính xác. Sách còn có LM335 nhưng phải chỉnh bằng biến trở nên không dùng |
| 5.4 | Đầu đọc RFID **ID-12** + thẻ 125kHz | ❓ | Đầu đọc ID-12 cần bo ra chân (breakout) |

### Linh kiện trong bộ của bạn nhưng không dùng cho bé 6 tuổi

| Linh kiện | Lý do |
|---|---|
| Động cơ DC, transistor TIP120, IC L293D, motor shield, động cơ bước, nguồn ngoài 12V | Cần nguồn điện riêng, dòng điện lớn, dễ nóng; để dành cho bé lớn hơn |
| Màn hình LCD 16×2, LCD đồ hoạ 128×64, màn hình 7 đoạn | Bé chưa đọc tốt; nối nhiều dây. Thay bằng hình trên màn hình TurboWarp |
| IC thanh ghi dịch 74HC595 | Mạch phức tạp |
| Thẻ nhớ SD, đồng hồ DS1307, cảm biến áp suất SCP1000, màn cảm ứng Nintendo DS, Arduino Mega | Khó với bé, hoặc không cần cho các bài này |
| Ethernet shield | Phần IoT làm qua cáp USB và TurboWarp là đủ cho bé 6 tuổi. Có thể dùng sau cho phần mở rộng "IoT thật" (gửi dữ liệu lên mạng) |

### Chương trình nạp cho mạch (firmware)

Bố mẹ hoặc giáo viên nạp **một lần** bằng Arduino IDE. Chương trình này hiểu tất cả linh kiện trong bảng trên (đèn, nút, biến trở, quang trở, piezo, servo, MaxSonar, DS18B20, bảng đèn MAX7219, joystick, RFID ID-12). Cần cài thêm 2 thư viện miễn phí trong Arduino IDE: **OneWire** và **DallasTemperature** (cho DS18B20).

## 8. An toàn

- Chỉ cấp điện bằng cáp USB nối máy tính (5V, an toàn). **Không bao giờ** nối mạch vào ổ điện.
- Linh kiện nhỏ, chân LED nhọn: bố mẹ ngồi cùng bé và cất linh kiện sau mỗi buổi học.
- Giới hạn thời gian dùng màn hình: mỗi buổi chỉ 1 bài học và bài tập của bài đó (khoảng 20 phút).
- Bố mẹ nối dây, bé lập trình và quan sát. Khi bé quen rồi, bé có thể tự cắm dây theo tấm hình dán breadboard, bố mẹ kiểm tra lại.

## 9. Kế hoạch kỹ thuật trên Ong Nhỏ Code

### 9.1 Các khối Arduino trong TurboWarp

- Viết một **extension TurboWarp** tên "Arduino", các khối có tên tiếng Việt: `kết nối mạch`, `bật đèn chân (13)`, `tắt đèn chân (13)`, `đèn màu (đỏ)`, `còi kêu nốt (Đô) trong (0.5) giây`, `servo quay tới (90) độ`, `nút chân (2) được bấm?`, `độ sáng`, `núm xoay`, `khoảng cách (cm)`, `nhiệt độ (°C)`.
- Extension nói chuyện với mạch qua **Web Serial** (cáp USB). Arduino chạy một **chương trình nạp sẵn**: bố mẹ hoặc giáo viên nạp một lần bằng Arduino IDE, sau đó không phải nạp lại.
- Trang bài học đã điều khiển được TurboWarp qua `window.vm` (iframe cùng tên miền), nên **không cần build lại TurboWarp**: trang bài học tự nạp extension khi mở bài Arduino.
- Máy chấm khối hiện tại **dùng được luôn** với khối Arduino, vì mỗi khối có mã riêng (ví dụ `arduino_ledOn`).
- **Chế độ không có mạch**: nếu chưa cắm Arduino, sân khấu hiện một mạch ảo (đèn, còi, nút) để bé vẫn làm bài được.
- Giới hạn: Web Serial chỉ chạy trên **Chrome hoặc Edge trên máy tính**, cần HTTPS khi đưa lên mạng (`localhost` thì không cần). Máy tính bảng chỉ dùng được chế độ mạch ảo.

### 9.2 Nội dung khoá học

- Viết khoá Arduino thành **gói nội dung** trong `content/packs/` theo đúng mẫu các gói hiện có: bài giảng, bước, khối `[[...]]`, câu hỏi, bài thực hành, dự án khởi đầu và lời giải mẫu.
- Thêm thẻ **"Arduino"** trên *Bản đồ học*, cạnh *Bài học / Dự án trò chơi / Luyện thi*, để khoá Arduino không lẫn với các bài Scratch.
- Khoá Arduino **không phụ thuộc vào việc nạp PDF**. Nếu quản trị nạp thêm PDF SIK hoặc ARDX, thẻ *Trang sách* sẽ hiện trang gốc tương ứng.
- Thêm trang **"Nguồn tài liệu"** ghi nguồn CC BY-SA 4.0.

### 9.3 Phần cần thêm vào máy chủ

- Các dạng bài mới: xếp khối, nối hình, tô màu (chấm tự động); vẽ, ảnh/video, ghi âm (giáo viên chấm).
- Nơi lưu file vẽ, ảnh và ghi âm trong `data/`, có kiểm tra quyền như file `.sb3` hiện nay.
- Hộp bài cần chấm, chấm nhanh bằng sao, lời khen mẫu và ghi âm lời khen.
- Huy hiệu theo chặng, giấy khen.

### 9.4 Thứ tự làm

1. Extension Arduino, chương trình cho mạch và chế độ mạch ảo.
2. Bài mẫu 1.2 hoàn chỉnh (bài giảng, bài tập, chấm) để bạn chạy thử.
3. Các dạng bài tập mới và phần chấm của giáo viên.
4. Viết đủ 28 bài, dịch dần theo từng chặng để bạn duyệt.

## 10. Cần bạn duyệt

1. Danh sách 28 bài (20 bài chính và 8 bài thêm) có ổn không?
2. Bài tập trên web: các dạng bài mới (xếp khối, nối hình, tô màu, vẽ, ảnh mạch, ghi âm) và phần chấm thêm cho giáo viên ở mục 5 có cần hết không?
3. Giọng văn của bài mẫu 1.2 có phù hợp không (cách xưng hô "con", độ dài câu)?
4. Bảng linh kiện ở mục 7: bạn có đủ những linh kiện đánh ❓ không (đèn RGB 4 chân, bảng đèn 8×8 loại có sẵn mạch MAX7219, joystick, đầu đọc RFID)?
5. Kế hoạch kỹ thuật ở mục 9 (thẻ "Arduino" riêng trên bản đồ học, chế độ mạch ảo, thứ tự làm) có ổn không?
