# Đề cương: "Bé chơi Arduino cùng TurboWarp" (bản nháp để duyệt)

Dành cho: bé 6 tuổi học cùng bố mẹ · Mỗi bài 10–15 phút · Lập trình bằng khối TurboWarp, mạch Arduino Uno.

## 1. Sách nguồn

| | Sách gốc chính | Sách tham khảo thêm |
|---|---|---|
| Tên | **SparkFun Inventor's Kit Experiment Guide v4.1** | *Arduino Programming Notebook* (Brian W. Evans) |
| Giấy phép | CC BY-SA 4.0: được **lược bớt, dịch, sửa**, kể cả dùng thương mại | CC BY-SA 3.0 |
| Nguồn | https://learn.sparkfun.com/tutorials/sparkfun-inventors-kit-experiment-guide---v41 | Diễn đàn Arduino |
| Dùng để | Chọn thí nghiệm, sơ đồ nối dây cho bố mẹ | Giải thích thêm cho bố mẹ (không đưa vào phần của bé) |

**Vì sao chọn SIK v4.1:** đây là sách Arduino miễn phí duy nhất tìm được vừa có giấy phép cho phép **dịch và chỉnh sửa**, vừa có hình nối dây màu rõ ràng, đi từ dễ đến khó. Không tìm thấy sách Arduino tiếng Việt miễn phí nào có giấy phép tương tự.

**Ràng buộc của giấy phép CC BY-SA 4.0:**
- Ghi rõ nguồn: "Phỏng theo SparkFun Inventor's Kit Experiment Guide v4.1, SparkFun Electronics, CC BY-SA 4.0".
- Ghi rõ là đã lược bớt và dịch.
- Phần nội dung phỏng theo cũng phải phát hành theo **CC BY-SA 4.0**.

**Thay đổi so với sách gốc:**
- Sách gốc lập trình bằng code C++ (Arduino IDE) → bé dùng **khối TurboWarp tiếng Việt**. Code gốc chỉ để ở phần bố mẹ, nếu cần.
- Bỏ phần lý thuyết điện (định luật Ohm, PWM, ...) ra khỏi phần của bé; bố mẹ vẫn được giải thích ngắn gọn.
- Bỏ màn hình LCD và robot (lý do ở mục 3).
- Thêm chặng "Làm quen" (không cần mạch) và chặng "IoT nhí" do mình tự viết.

> Cần đối chiếu: tên và thứ tự các mạch bên dưới lấy theo cấu trúc SIK v4.x mà mình biết. Từ môi trường làm việc này không mở được trang SparkFun, nên khi bạn duyệt xong, mình sẽ kiểm tra lại với bản PDF.

## 2. Lộ trình bài học

| Chặng | Bài | Tên cho bé | Bé làm gì | Nguồn |
|---|---|---|---|---|
| 0. Làm quen | 0.1 | Gặp bạn Arduino | Xem tranh: Arduino là "bộ não nhỏ", dây là "đường đi", đèn là "đôi mắt" | Tự viết |
| | 0.2 | Mèo biết đi | Ghép khối cho chú mèo đi trên màn hình | Tự viết |
| | 0.3 | Làm lại nhiều lần | Khối `lặp lại`: mèo nhảy 5 lần | Tự viết |
| 1. Ánh sáng | 1.1 | Đèn ơi, sáng lên! | Bật và tắt một đèn LED | SIK 1A |
| | 1.2 | Đèn nháy như tim đập | Đèn nhấp nháy, nhanh hoặc chậm | SIK 1A |
| | 1.3 | Núm xoay thần kỳ | Xoay núm thì mèo trên màn hình đi theo | SIK 1B |
| | 1.4 | Đèn ngủ biết tự bật | Che tay lên cảm biến thì đèn sáng | SIK 1C |
| | 1.5 | Đèn cầu vồng | Đèn đổi màu đỏ, xanh lá, xanh dương | SIK 1D |
| 2. Âm thanh | 2.1 | Còi kêu bíp bíp | Bấm phím trên máy tính thì còi kêu | SIK 2A |
| | 2.2 | Chiếc kèn tí hon | Mỗi nút bấm phát một nốt nhạc | SIK 2B |
| | 2.3 | Trò chơi bắt chước | Đèn sáng theo thứ tự, bé bấm nút lặp lại (bản đơn giản 3 bước) | SIK 2C |
| 3. Chuyển động | 3.1 | Cánh tay vẫy chào | Động cơ servo vẫy qua vẫy lại | SIK 3A |
| | 3.2 | Đôi mắt dơi | Cảm biến khoảng cách: tay lại gần thì mèo kêu "meo" | SIK 3B |
| | 3.3 | Chuông báo có khách | Có người lại gần thì còi kêu và đèn nháy | SIK 3C |
| 4. Nóng – lạnh | 4.1 | Hôm nay nóng hay lạnh? | Cảm biến nhiệt độ: trời nóng hiện mặt trời, trời lạnh hiện người tuyết | SIK 4B |
| 5. IoT nhí | 5.1 | Mạch nói chuyện với máy tính | Bấm nút trên mạch thì nhân vật trên màn hình nhảy, bấm nút trên màn hình thì đèn trên mạch sáng | Tự viết |
| | 5.2 | Ngôi nhà thông minh mini | Ghép lại: trời tối thì đèn tự bật, có người đến thì chuông kêu | Tự viết (dùng mạch 1C và 3B) |

**Tổng cộng: 17 bài.** Nếu mỗi tuần học 2 bài thì mất khoảng 2 tháng.

## 3. Những phần lược bỏ khỏi sách gốc

| Phần của SIK | Lý do bỏ | Thay bằng |
|---|---|---|
| 4A: Màn hình LCD | Bé 6 tuổi chưa đọc tốt; nối dây LCD nhiều và dễ sai | Hiện hình trên màn hình TurboWarp |
| 4C: Trò chơi đoán chữ trên LCD | Như trên | Bỏ |
| Chặng 5: Robot (động cơ, mạch điều khiển, pin) | Nhiều linh kiện, dễ nối nhầm, tốn kém | Để thành **phần mở rộng** cho bé lớn hơn |
| Phần lý thuyết điện | Quá khó với bé | Một câu ví von trong phần bố mẹ |

## 4. Cấu trúc mỗi bài

**Phần cho bé** (chữ to, có nút 🔊 đọc to):
1. 👀 **Xem**: một hình minh họa và một câu giới thiệu.
2. 🧩 **Ghép khối**: hình các khối cần dùng, đánh số 1, 2, 3. Bài mẫu đã mở sẵn trong TurboWarp.
3. ▶️ **Thử**: bấm cờ xanh để chạy.
4. ⭐ **Thưởng**: nhận sao và một câu "Thử thêm" nếu bé muốn chơi tiếp.

**Phần cho bố mẹ** (thu gọn, bấm để mở):
- Linh kiện cần chuẩn bị (có ảnh).
- Sơ đồ nối dây, lấy hình từ SIK và chú thích bằng tiếng Việt.
- Lỗi thường gặp (ví dụ: LED cắm ngược chân).
- Gợi ý câu hỏi để trò chuyện với bé.
- Ghi nguồn: "Phỏng theo SIK v4.1, mạch 1A".

## 5. Bài mẫu (để bạn duyệt giọng văn)

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
- Nối dây: chân dài của LED nối vào chân số 13 qua điện trở, chân ngắn nối vào GND (theo hình SIK mạch 1A).
- Đèn không sáng? Thử cắm ngược LED lại. LED chỉ sáng khi cắm đúng chiều.
- Gợi ý hỏi bé: "Ngoài đèn ra, còn cái gì cứ bật tắt liên tục nữa?" (đèn giao thông, đèn xe cứu thương...)

## 6. Linh kiện cần mua

Có hai lựa chọn: mua bộ SparkFun Inventor's Kit, hoặc một **bộ Arduino Uno Starter Kit** phổ thông bán ở Việt Nam. Bộ phổ thông cần có:

- Arduino Uno R3 và cáp USB, breadboard, dây nối
- Đèn LED đỏ, vàng, xanh và 1 đèn LED RGB; điện trở 330Ω
- 3–4 nút bấm, 1 biến trở (núm xoay), 1 quang trở và 1 điện trở 10kΩ
- 1 còi buzzer, 1 servo SG90, 1 cảm biến siêu âm HC-SR04
- 1 cảm biến nhiệt độ (TMP36 như trong SIK, hoặc thay bằng DHT11)

## 7. An toàn

- Chỉ cấp điện bằng cáp USB nối máy tính (5V, an toàn). **Không bao giờ** nối mạch vào ổ điện.
- Linh kiện nhỏ, chân LED nhọn: bố mẹ ngồi cùng bé và cất linh kiện sau mỗi buổi học.
- Bố mẹ nối dây, bé lập trình và quan sát. Khi bé quen rồi, bé có thể tự cắm dây theo hình với bố mẹ kiểm tra lại.

## 8. Cần bạn duyệt

1. Danh sách 17 bài và những phần lược bỏ có ổn không?
2. Giọng văn của bài mẫu 1.2 có phù hợp không (cách xưng hô "con", độ dài câu)?
3. Có bỏ hẳn chặng Robot không, hay giữ làm phần mở rộng?
4. Cảm biến nhiệt độ dùng **TMP36** (như sách gốc) hay **DHT11** (phổ biến ở Việt Nam)?
