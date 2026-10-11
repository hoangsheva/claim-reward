# Đề cương: "Bé chơi Arduino cùng TurboWarp" (bản nháp 2, để duyệt)

Dành cho: bé 6 tuổi học cùng bố mẹ · Mỗi bài 10–15 phút · Lập trình bằng khối TurboWarp, mạch Arduino Uno.

Bộ tài liệu gồm 2 cuốn:
- **Sách học**: trên web, mỗi bài có phần cho bé và phần cho bố mẹ.
- **Vở bài tập**: in ra giấy, bé làm sau mỗi bài.

## 1. Sách nguồn

| # | Sách | Giấy phép | Cách dùng |
|---|---|---|---|
| A | **SparkFun Inventor's Kit Experiment Guide v4.1** (SparkFun Electronics) | CC BY-SA 4.0 | **Sách chính**: thí nghiệm, sơ đồ nối dây, lỗi thường gặp. Được dịch và chỉnh sửa |
| B | **ARDX Arduino Experimenter's Guide** (Oomlout) | CC BY-SA | Thêm bài đèn chạy đuổi, bài phát nhạc, và **tấm hình in dán lên breadboard** để biết cắm linh kiện vào đâu. Được dịch và chỉnh sửa |
| C | **Arduino Projects Book** (Arduino, đi kèm Arduino Starter Kit) | CC BY-NC-SA 3.0 | **Chỉ lấy ý tưởng dự án**, mình tự viết lại toàn bộ lời và hình (lý do ở mục 1.1) |
| + | *Arduino Programming Notebook* (Brian W. Evans) | CC BY-SA 3.0 | Tham khảo cho bố mẹ, không đưa vào phần của bé |

Nguồn tải:
- A: https://learn.sparkfun.com/tutorials/sparkfun-inventors-kit-experiment-guide---v41
- B: https://haseloff.plantsci.cam.ac.uk/resources/Arduino/ARDX-EG-OOML-DD.pdf (bản lưu tại Đại học Cambridge; trang gốc là ardx.org / oomlout.com)
- C: đi kèm Arduino Starter Kit; cần tìm bản PDF chính thức của Arduino

### 1.1 Gộp các giấy phép thế nào

- Sách A và B đều là **CC BY-SA**. Nội dung CC BY-SA 3.0 được phép phát hành lại theo CC BY-SA 4.0, nên **gộp A và B làm một được**. Toàn bộ sách học và vở bài tập phát hành theo **CC BY-SA 4.0**.
- Sách C là **CC BY-NC-SA** (cấm dùng thương mại). Giấy phép này **không tương thích** với CC BY-SA, nên không thể chép lời hay hình của sách C vào cùng một cuốn với A và B. **Ý tưởng** dự án thì không có bản quyền, nên mình chỉ lấy ý tưởng (ví dụ "bảng điều khiển phi thuyền", "đàn ánh sáng") rồi tự viết lời và tự vẽ hình.
- Trang "Nguồn tài liệu" trên web sẽ ghi:
  > Phỏng theo *SparkFun Inventor's Kit Experiment Guide v4.1* (SparkFun Electronics, CC BY-SA 4.0) và *ARDX Experimenter's Guide* (Oomlout, CC BY-SA). Một số ý tưởng dự án lấy cảm hứng từ *Arduino Projects Book* (Arduino). Nội dung đã được lược bớt, dịch và biên soạn lại cho trẻ 6 tuổi. Phát hành theo CC BY-SA 4.0.

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
| | 1.5 ➕ | Bảng điều khiển phi thuyền | Bấm nút thì đèn xanh tắt, 2 đèn đỏ nháy: "Phi thuyền cất cánh!" | Ý tưởng từ C |
| | 1.6 ⭐ | Núm xoay thần kỳ | Xoay núm thì mèo trên màn hình đi theo | A 1B · B CIRC-08 |
| | 1.7 ⭐ | Đèn ngủ biết tự bật | Che tay lên cảm biến thì đèn sáng | A 1C · B CIRC-09 |
| | 1.8 ⭐ | Đèn cầu vồng | Đèn đổi màu đỏ, xanh lá, xanh dương | A 1D · B CIRC-12 |
| **2. Âm thanh** | 2.1 ⭐ | Còi kêu bíp bíp | Bấm phím trên máy tính thì còi kêu | A 2A |
| | 2.2 ⭐ | Còi biết hát | Còi phát bài "Kìa con bướm vàng" | B CIRC-06 (đổi bài hát) |
| | 2.3 ⭐ | Chiếc kèn tí hon | Mỗi nút bấm phát một nốt nhạc | A 2B · ý tưởng từ C |
| | 2.4 ➕ | Đàn ánh sáng | Đưa tay lên xuống trên cảm biến thì tiếng còi trầm bổng | Ý tưởng từ C |
| | 2.5 ⭐ | Trò chơi bắt chước | Đèn sáng theo thứ tự, bé bấm nút lặp lại (3 bước) | A 2C |
| **3. Chuyển động** | 3.1 ⭐ | Cánh tay vẫy chào | Động cơ servo vẫy qua vẫy lại | A 3A · B CIRC-04 |
| | 3.2 ⭐ | Đôi mắt dơi | Cảm biến khoảng cách: tay lại gần thì mèo kêu "meo" | A 3B |
| | 3.3 ⭐ | Chuông báo có khách | Có người lại gần thì còi kêu và đèn nháy | A 3C |
| **4. Nóng – lạnh** | 4.1 ⭐ | Hôm nay nóng hay lạnh? | Trời nóng hiện mặt trời, trời lạnh hiện người tuyết | A 4B · B CIRC-10 |
| | 4.2 ➕ | Bàn tay ai ấm nhất? | Bé và bố mẹ thay nhau nắm cảm biến; tay càng ấm thì càng nhiều đèn sáng | Ý tưởng từ C |
| **5. IoT nhí** | 5.1 ⭐ | Mạch nói chuyện với máy tính | Bấm nút trên mạch thì nhân vật trên màn hình nhảy, bấm nút trên màn hình thì đèn trên mạch sáng | Tự viết |
| | 5.2 ➕ | Quả cầu tiên tri | Bấm nút thì màn hình hiện câu trả lời vui ("Có!", "Hỏi lại nhé!") | Ý tưởng từ C (thay màn hình LCD bằng TurboWarp) |
| | 5.3 ⭐ | Ngôi nhà thông minh mini | Ghép lại: trời tối thì đèn tự bật, có người đến thì chuông kêu | Tự viết (dùng mạch 1.7 và 3.2) |

**Tổng cộng: 24 bài, trong đó 19 bài chính và 5 bài thêm.** Nếu mỗi tuần học 2 bài thì mất khoảng 2,5–3 tháng.

### Mỗi sách đóng góp gì

| | A: SIK | B: ARDX | C: Projects Book | Tự viết |
|---|---|---|---|---|
| Số bài | 14 | 8 (trùng phần lớn với A) | 6 ý tưởng | 7 |
| Phần lấy | Thí nghiệm, sơ đồ, lỗi thường gặp | Đèn chạy đuổi, phát nhạc, tấm hình dán breadboard | Ý tưởng các dự án vui | Làm quen, đèn giao thông, IoT |

## 3. Những phần lược bỏ

| Phần | Lý do bỏ | Thay bằng |
|---|---|---|
| Màn hình LCD (A 4A, 4C; C: Crystal Ball) | Bé chưa đọc tốt; nối dây nhiều và dễ sai | Hiện hình trên màn hình TurboWarp |
| Robot (A, chặng 5) | Nhiều linh kiện, dễ nối nhầm, tốn kém | Phần mở rộng cho bé lớn hơn |
| Động cơ DC, relay, transistor, thanh ghi dịch (B; C: chong chóng, zoetrope) | Cần nguồn điện riêng; mạch khó với bé | Bỏ |
| Lý thuyết điện (định luật Ohm, PWM...) | Quá khó với bé | Một câu ví von trong phần bố mẹ |
| Code C++ | Bé dùng khối TurboWarp | Code gốc chỉ để ở phần bố mẹ, nếu cần |

## 4. Cấu trúc mỗi bài (sách học trên web)

**Phần cho bé** (chữ to, có nút 🔊 đọc to):
1. 👀 **Xem**: một hình minh họa và một câu giới thiệu.
2. 🧩 **Ghép khối**: hình các khối cần dùng, đánh số 1, 2, 3. Bài mẫu đã mở sẵn trong TurboWarp.
3. ▶️ **Thử**: bấm cờ xanh để chạy.
4. ⭐ **Thưởng**: nhận sao và một câu "Thử thêm" nếu bé muốn chơi tiếp.
5. ✏️ **Làm vở bài tập**: trang tương ứng trong vở.

**Phần cho bố mẹ** (thu gọn, bấm để mở):
- Linh kiện cần chuẩn bị (có ảnh).
- Sơ đồ nối dây, lấy hình từ sách A và chú thích bằng tiếng Việt.
- Tấm hình dán breadboard để in ra (dựa trên sách B).
- Lỗi thường gặp.
- Gợi ý câu hỏi để trò chuyện với bé.
- Ghi nguồn của bài.

## 5. Vở bài tập "Bé chơi Arduino"

Vở gồm các trang khổ A4, in đen trắng được, có chỗ cho bé tô màu. Mỗi bài có 1 trang bài tập. Cuối mỗi chặng có 1 trang ôn tập và 1 **huy hiệu** để cắt ra. Mỗi bài tập dành cho bé chỉ cần **tô, nối, khoanh, dán hoặc vẽ**, không cần viết chữ.

### 5.1 Các dạng bài tập

| Dạng | Ví dụ | Bé luyện được gì |
|---|---|---|
| 🎨 **Tô màu** | Tô đèn giao thông đúng thứ tự đỏ, vàng, xanh | Nhận biết linh kiện, thứ tự |
| 🔗 **Nối hình** | Nối "còi" với "🔊", "đèn" với "💡", "núm xoay" với "🔄" | Linh kiện nào làm việc gì |
| ✂️ **Cắt dán khối** | Cắt các khối lệnh in sẵn và dán đúng thứ tự | Trình tự chương trình |
| 🤔 **Đoán xem** | "Đổi `chờ 1 giây` thành `chờ 3 giây`, đèn nháy như 🐇 hay như 🐢?" Bé khoanh hình | Dự đoán kết quả |
| 🔍 **Tìm chỗ sai** | Chương trình thiếu khối `tắt đèn`; bé khoanh chỗ cần sửa | Tìm lỗi chương trình |
| 🖍️ **Vẽ ý tưởng** | "Con muốn làm đèn ngủ cho ai?" Bé vẽ ra | Sáng tạo |
| ⭐ **Dán sao** | Bảng 24 ô; bé dán hoặc tô một sao sau mỗi bài | Tạo động lực |

### 5.2 Các trang trong vở

| Trang | Nội dung |
|---|---|
| Bìa | Tên bé, ảnh bé (dán vào) |
| Gặp gỡ các bạn linh kiện | Trang hình các linh kiện, mỗi bạn có một cái tên vui: "bạn Đèn", "bạn Còi", "bạn Núm Xoay"... |
| Bài 0.1 → 5.3 | 24 trang bài tập, mỗi bài 1 trang |
| Ôn tập chặng 0 → 5 | 6 trang, trộn các dạng bài |
| Huy hiệu | 6 huy hiệu để cắt: "Bé làm quen", "Bé ánh sáng", "Bé âm nhạc", "Bé chuyển động", "Bé nóng lạnh", "Kỹ sư IoT nhí" |
| Bảng sao | 24 ô |
| Cuối vở | "Giấy khen Kỹ sư nhí" để bố mẹ trao cho bé |

**Tổng cộng khoảng 40 trang.** Vở sẽ có trên web dạng PDF để tải, in được từng trang hoặc in cả cuốn.

### 5.3 Trang mẫu: Bài 1.2 "Đèn nháy như tim đập"

```
┌─────────────────────────────────────────────┐
│  Bài 1.2  Đèn nháy như tim đập 💓    ☆ ☆ ☆   │
├─────────────────────────────────────────────┤
│ 1. 🎨 Tô màu đỏ cho đèn đang SÁNG:            │
│        ( )      ( )      ( )      ( )       │
│       sáng     tắt     sáng     tắt         │
├─────────────────────────────────────────────┤
│ 2. ✂️ Cắt các khối ở cuối trang, dán vào     │
│    đúng thứ tự để đèn nháy:                  │
│    [ 🚩 khi bấm cờ xanh ]                    │
│    [ 🔁 liên tục ┐                           │
│    │  [ ...... ]                             │
│    │  [ ...... ]                             │
│    │  [ ...... ]                             │
│    │  [ ...... ]                             │
│    └─────────────┘                           │
├─────────────────────────────────────────────┤
│ 3. 🤔 Đổi "chờ 1 giây" thành "chờ 0.2 giây". │
│    Đèn nháy giống bạn nào? Khoanh tròn:      │
│          🐇 Thỏ             🐢 Rùa           │
├─────────────────────────────────────────────┤
│ 4. 🖍️ Vẽ một thứ cũng nhấp nháy mà con biết: │
│    ┌───────────────────────┐                 │
│    │                       │                 │
│    └───────────────────────┘                 │
├ ✂ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ┤
│ [💡 bật đèn] [⏱️ chờ 1 giây]                 │
│ [💡 tắt đèn] [⏱️ chờ 1 giây]                 │
└─────────────────────────────────────────────┘
Đáp án cho bố mẹ: bật đèn → chờ → tắt đèn → chờ · Thỏ 🐇
```

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
- Vở bài tập có phần cắt dán: dùng kéo an toàn cho trẻ em.
- Bố mẹ nối dây, bé lập trình và quan sát. Khi bé quen rồi, bé có thể tự cắm dây theo tấm hình dán breadboard, bố mẹ kiểm tra lại.

## 9. Cần bạn duyệt

1. Danh sách 24 bài (19 bài chính và 5 bài thêm) có ổn không?
2. Có đồng ý cách xử lý sách C (chỉ lấy ý tưởng, tự viết lại) không?
3. Vở bài tập: các dạng bài và trang mẫu 1.2 có phù hợp không? Vở in đen trắng hay in màu?
4. Giọng văn của bài mẫu 1.2 có phù hợp không (cách xưng hô "con", độ dài câu)?
5. Cảm biến nhiệt độ dùng **TMP36** hay **DHT11**?
