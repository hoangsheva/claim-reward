# Đề cương: "Bé chơi Arduino cùng TurboWarp" (bản nháp 4, để duyệt)

Dành cho: bé 6 tuổi học cùng bố mẹ · Mỗi bài 10–15 phút · Lập trình bằng khối TurboWarp, mạch Arduino Uno.

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
| | 1.8 ⭐ | Đèn cầu vồng | Đèn đổi màu đỏ, xanh lá, xanh dương | A 1D · B CIRC-12 |
| **2. Âm thanh** | 2.1 ⭐ | Còi kêu bíp bíp | Bấm phím trên máy tính thì còi kêu | A 2A |
| | 2.2 ⭐ | Còi biết hát | Còi phát bài "Kìa con bướm vàng" | B CIRC-06 (đổi bài hát) |
| | 2.3 ⭐ | Chiếc kèn tí hon | Mỗi nút bấm phát một nốt nhạc | A 2B |
| | 2.4 ➕ | Núm chỉnh to nhỏ | Xoay núm thì tiếng còi to lên hoặc nhỏ đi | A 2A (núm chỉnh âm lượng trong mạch còi) |
| | 2.5 ⭐ | Trò chơi bắt chước | Đèn sáng theo thứ tự, bé bấm nút lặp lại (3 bước) | A 2C |
| **3. Chuyển động** | 3.1 ⭐ | Cánh tay vẫy chào | Động cơ servo vẫy qua vẫy lại | A 3A · B CIRC-04 |
| | 3.2 ⭐ | Đôi mắt dơi | Cảm biến khoảng cách: tay lại gần thì mèo kêu "meo" | A 3B |
| | 3.3 ⭐ | Chuông báo có khách | Có người lại gần thì còi kêu và đèn nháy | A 3C |
| **4. Nóng – lạnh** | 4.1 ⭐ | Hôm nay nóng hay lạnh? | Trời nóng hiện mặt trời, trời lạnh hiện người tuyết | A 4B · B CIRC-10 |
| | 4.2 ➕ | Nhiệt kế đèn màu | Nóng thì đèn sáng màu đỏ, mát thì đèn sáng màu xanh | Ghép A 4B với A 1D · B CIRC-10 với CIRC-12 |
| **5. IoT nhí** | 5.1 ⭐ | Mạch nói chuyện với máy tính | Bấm nút trên mạch thì nhân vật trên màn hình nhảy, bấm nút trên màn hình thì đèn trên mạch sáng | Tự viết |
| | 5.2 ➕ | Đèn báo từ máy tính | Bé bấm hình trên màn hình thì đèn trên mạch đổi màu và còi kêu "ting" | Tự viết (dùng mạch A 1D và A 2A) |
| | 5.3 ⭐ | Ngôi nhà thông minh mini | Ghép lại: trời tối thì đèn tự bật, có người đến thì chuông kêu | Tự viết (dùng mạch 1.7 và 3.2) |

**Tổng cộng: 24 bài, trong đó 20 bài chính và 4 bài thêm.** Nếu mỗi tuần học 2 bài thì mất khoảng 2,5–3 tháng.

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

## 5. Bài tập trên web "Bé chơi Arduino"

Bài tập làm **ngay trên web**, không in ra giấy. Bé làm bài trên máy tính hoặc máy tính bảng; giáo viên (hoặc bố mẹ) xem lại bài làm và chấm trên cùng trang web, theo cách web TurboWarp của bạn đang làm.

### 5.1 Ai làm gì

| Vai trò | Làm gì trên web |
|---|---|
| 👧 **Bé** | Vào lớp bằng **ảnh đại diện + mã lớp**, không cần gõ mật khẩu. Làm bài, bấm "Nộp bài", xem sao và lời khen của cô |
| 👩‍🏫 **Giáo viên** | Tạo lớp, thêm bé, xem bài nộp, chấm sao và nhận xét, xem tiến độ cả lớp |
| 👨‍👩‍👧 **Bố mẹ** (tuỳ chọn) | Xem bài làm và nhận xét của cô dành cho con mình |

### 5.2 Các dạng bài tập và cách chấm

Mỗi bài học có 3–4 câu bài tập, làm trong khoảng 5 phút. Bé chỉ cần **chạm, kéo thả, tô hoặc vẽ**, không cần gõ chữ. Mỗi câu đều có nút 🔊 đọc đề.

| Dạng | Bé làm gì trên web | Cách chấm |
|---|---|---|
| 🎨 **Tô màu** | Chạm vào đèn để tô màu (ví dụ tô đèn giao thông đúng thứ tự) | **Tự động** |
| 🔗 **Nối hình** | Kéo đường nối "còi" với 🔊, "đèn" với 💡 | **Tự động** |
| 🧩 **Xếp khối** | Kéo các khối lệnh vào đúng thứ tự | **Tự động** |
| 🤔 **Đoán xem** | Chạm vào một hình, ví dụ 🐇 hay 🐢 | **Tự động** |
| 🔍 **Tìm chỗ sai** | Chạm vào khối bị sai hoặc bị thiếu | **Tự động** |
| 🖍️ **Vẽ ý tưởng** | Vẽ bằng ngón tay hoặc chuột lên khung vẽ | **Giáo viên chấm** |
| 🎤 **Kể cho cô nghe** | Bấm nút ghi âm (tối đa 30 giây) để kể về sản phẩm của mình | **Giáo viên chấm** |
| 🚀 **Nộp dự án TurboWarp** | Bấm "Nộp bài" ngay trong trình soạn thảo; có thể kèm ảnh hoặc video ngắn chụp mạch đang chạy | **Giáo viên chấm** |

**Chấm tự động:**
- Bé làm sai: web nói nhẹ nhàng "Gần đúng rồi, con thử lại nhé!" và cho làm lại, không trừ điểm.
- Web ghi lại số lần bé thử, để giáo viên biết câu nào bé thấy khó.

**Giáo viên chấm:**
- Cho 1–3 ⭐ và một lời nhận xét. Có sẵn các câu khen mẫu để bấm chọn nhanh, ví dụ "Con vẽ đẹp quá!" hay "Đèn nháy đúng rồi!".
- Có thể ghi âm lời khen, vì bé chưa đọc được.
- Có thể bấm "Cho làm lại" kèm gợi ý.

### 5.3 Trang của giáo viên

| Màn hình | Nội dung |
|---|---|
| **Lớp học** | Danh sách các bé; bảng tiến độ mỗi bé × mỗi bài, có màu ✅ đã xong, 🟡 chờ chấm, ⬜ chưa làm |
| **Hộp bài cần chấm** | Các bài vẽ, ghi âm và dự án đang chờ, xếp theo thời gian nộp. Chấm xong thì tự chuyển sang bài tiếp theo |
| **Xem bài một bé** | Toàn bộ bài làm của bé: đáp án, số lần thử, hình vẽ, ghi âm, mở dự án TurboWarp để chạy thử |
| **Thống kê** | Câu nào nhiều bé làm sai, để giáo viên giảng lại |
| **Xuất báo cáo** | Tải bảng điểm cả lớp (CSV hoặc Excel) |

### 5.4 Phần thưởng

- Mỗi bài xong được ⭐. Xong mỗi chặng được 1 **huy hiệu**: "Bé làm quen", "Bé ánh sáng", "Bé âm nhạc", "Bé chuyển động", "Bé nóng lạnh", "Kỹ sư IoT nhí".
- Xong cả khoá học được **giấy khen "Kỹ sư nhí"** để in ra.
- Không có bảng xếp hạng giữa các bé, để bé không bị so sánh với bạn.

### 5.5 Câu hỏi mẫu: Bài 1.2 "Đèn nháy như tim đập"

| Câu | Dạng | Đề (đọc to) | Đáp án / Cách chấm |
|---|---|---|---|
| 1 | 🎨 Tô màu | "Con chạm để tô đỏ những đèn đang **sáng** nhé!" (4 đèn có chữ sáng, tắt, sáng, tắt) | Đèn 1 và 3 · tự động |
| 2 | 🧩 Xếp khối | "Con kéo các khối vào trong vòng lặp để đèn nháy nhé!" | `bật đèn` → `chờ 1 giây` → `tắt đèn` → `chờ 1 giây` · tự động |
| 3 | 🤔 Đoán xem | "Đổi *chờ 1 giây* thành *chờ 0.2 giây*, đèn nháy giống bạn nào?" | 🐇 Thỏ · tự động |
| 4 | 🖍️ Vẽ | "Con vẽ một thứ cũng nhấp nháy mà con biết nhé!" | Giáo viên chấm sao và nhận xét |
| 5 | 🚀 Dự án | "Con nộp chương trình đèn nháy của con cho cô nhé!" (tuỳ chọn: chụp ảnh đèn đang sáng) | Giáo viên mở dự án chạy thử, chấm sao |

### 5.6 Bảo vệ dữ liệu của trẻ

- Chỉ lưu **tên gọi ở nhà hoặc biệt danh** và ảnh đại diện hoạt hình, không cần họ tên đầy đủ, ngày sinh hay ảnh thật.
- Chỉ giáo viên của lớp và bố mẹ của bé xem được bài làm của bé. Không có trang công khai.
- Ảnh, video và ghi âm của bé tự xoá sau khi kết thúc khoá học (thời gian lưu do bạn quyết định).
- Bố mẹ có thể yêu cầu xoá toàn bộ dữ liệu của con.

### 5.7 Phần kỹ thuật (phụ thuộc web hiện tại của bạn)

Phần chấm bài cần nơi lưu dữ liệu và tài khoản giáo viên. Mình sẽ **dùng lại hệ thống đang có trong web TurboWarp của bạn** (đăng nhập, lớp học, nộp và chấm bài), chỉ thêm các dạng bài tập mới. Vì vậy mình cần xem mã nguồn web đó trước khi làm.

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
- Cần: Arduino Uno, cáp USB, 1 đèn LED, 1 điện trở 330Ω, breadboard, 2 dây nối.
- Nối dây: chân dài của LED nối vào chân số 13 qua điện trở, chân ngắn nối vào GND (theo hình mạch 1A trong sách A). In tấm hình dán breadboard (dựa trên CIRC-01 trong sách B), đặt lên breadboard rồi cắm theo hình.
- Đèn không sáng? Thử cắm ngược LED lại. LED chỉ sáng khi cắm đúng chiều.
- Gợi ý hỏi bé: "Ngoài đèn ra, còn cái gì cứ bật tắt liên tục nữa?" (đèn giao thông, đèn xe cứu thương...)

## 7. Linh kiện cần mua

Có hai lựa chọn: mua bộ SparkFun Inventor's Kit, hoặc một **bộ Arduino Uno Starter Kit** phổ thông bán ở Việt Nam. Bộ phổ thông cần có:

- Arduino Uno R3 và cáp USB, breadboard, dây nối
- 6 đèn LED (2 đỏ, 2 vàng, 2 xanh) và 1 đèn LED RGB; điện trở 330Ω
- 4 nút bấm, 1 biến trở (núm xoay), 1 quang trở và 1 điện trở 10kΩ
- 1 còi buzzer, 1 servo SG90, 1 cảm biến siêu âm HC-SR04
- 1 cảm biến nhiệt độ (TMP36 như trong sách A và B, hoặc thay bằng DHT11)

## 8. An toàn

- Chỉ cấp điện bằng cáp USB nối máy tính (5V, an toàn). **Không bao giờ** nối mạch vào ổ điện.
- Linh kiện nhỏ, chân LED nhọn: bố mẹ ngồi cùng bé và cất linh kiện sau mỗi buổi học.
- Giới hạn thời gian dùng màn hình: mỗi buổi chỉ 1 bài học và bài tập của bài đó (khoảng 20 phút).
- Bố mẹ nối dây, bé lập trình và quan sát. Khi bé quen rồi, bé có thể tự cắm dây theo tấm hình dán breadboard, bố mẹ kiểm tra lại.

## 9. Cần bạn duyệt

1. Danh sách 24 bài (20 bài chính và 4 bài thêm) có ổn không?
2. Bài tập trên web: các dạng bài, cách chấm và câu hỏi mẫu 1.2 có phù hợp không? Có cần ghi âm và chụp ảnh mạch không?
3. Giọng văn của bài mẫu 1.2 có phù hợp không (cách xưng hô "con", độ dài câu)?
4. Cảm biến nhiệt độ dùng **TMP36** hay **DHT11**?
5. Web TurboWarp của bạn nằm ở repo GitHub nào, và đang lưu bài nộp ở đâu (Firebase, Supabase, máy chủ riêng...)?
