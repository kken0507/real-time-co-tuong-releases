# Real-Time Cờ Tướng

Cờ tướng thời gian thực, đấu với máy. Mỗi quân có một **thanh hành động**; chỉ quân nào đầy thanh (100%) mới được đi. Thanh tự đầy theo thời gian, nên trong lúc bạn suy nghĩ, quân đối phương vẫn có thể đi. Giao diện kiểu arcade cổ điển: nền đen, màu xanh lá và cam (trong phần cài đặt, chọn «Cổ điển» để dùng màu gỗ truyền thống).

**Kho này chỉ dùng để phát hành bản dựng (tệp chạy và bản chơi trên trình duyệt). Không có mã nguồn.**

## Chơi
- **Trình duyệt**: https://kken0507.github.io/real-time-co-tuong-releases/ (máy tính và điện thoại; lần đầu tải khoảng 10 MB).
- **Linux / Windows**: vào [Releases](../../releases), tải `real-time-co-tuong-linux-x86_64-<phiên bản>.tar.gz` hoặc `real-time-co-tuong-windows-x86_64-<phiên bản>.zip`, giải nén rồi chạy tệp thực thi (đối chiếu bằng `SHA256SUMS`).
  - Linux: sau khi giải nén, tệp đã có quyền thực thi (nếu chưa, chạy `chmod +x`).
  - Windows: tệp chưa được ký số, nên SmartScreen có thể hiện cảnh báo (chọn «Thông tin khác» → «Vẫn chạy»). Tệp exe và cửa sổ trò chơi dùng biểu tượng của trò chơi.
- **Android**: tải `real-time-co-tuong-android-<phiên bản>.apk` (arm64) ở [Releases](../../releases) và cài vào máy. Trò chơi không có trên Google Play, nên cần cho phép «cài ứng dụng từ nguồn không xác định». Để cập nhật, chỉ cần cài APK mới đè lên (chữ ký giống nhau nên dữ liệu và cài đặt được giữ nguyên). Hỗ trợ tay cầm (Bluetooth và tích hợp) và cảm ứng.

## Cách chơi
- Quân cam (Cam) là máy, quân xanh (Xanh) là bạn. Nước đi theo luật cờ tướng (Mã bị cản chân, Tượng bị chẹn mắt, Pháo nhảy qua quân, cung điện, Tốt qua sông). **Ăn được Tướng là thắng**; không bắt buộc phải tránh chiếu. Nước đi làm hai Tướng đối mặt nhau (lộ mặt tướng) bị cấm với cả hai bên.
- Thời gian đầy thanh (tốc độ ×1): Tướng 8 giây / Sĩ 5 / Tượng 6 / Xe 7 / Mã 4 / Pháo 6 / Tốt 3. Trong cài đặt có thể đổi tốc độ (×0,5 đến ×2). Quân vừa đi sẽ về 0%.
- **WAIT** (mặc định): chọn một quân của bạn đã đầy thanh thì thời gian và máy đều dừng. **ACTIVE**: thời gian luôn chạy. Máy có ba mức: dễ, vừa, khó.
- Màn hình: chọn quân sẽ hiện các điểm có thể đến (nét đứt = có thể ăn; đỏ đậm = bị quân đầy thanh của đối phương nhắm tới). Mục «Cách chơi» trong trò chơi cũng có giải thích.

## Điều khiển
| | Cảm ứng / chuột | Bàn phím | Tay cầm |
|---|---|---|---|
| Chọn quân, đi quân | Bấm quân, bấm ô đến | Phím mũi tên để di con trỏ, Enter / Space | Phím điều hướng hoặc cần trái để di con trỏ, A |
| Chuyển giữa các quân đi được | Bấm một mục trong danh sách thanh (hàng hoặc ô) | Q / E | L1 / R1 |
| Bỏ chọn | Bấm vào chỗ trống | Esc | B |
| Tạm dừng | «Tạm dừng» | P | Start |
| Bàn cờ ⇄ bảng điều khiển | — | F2 (Shift+Tab cũng sang bảng) | Select |

- Quân đi được = quân của bạn đã đầy thanh và có nước đi. Khi chuyển qua lại, tâm ngắm di chuyển đến quân đó và quân đó được chọn.
- Khi tạm dừng, quân, thanh và lựa chọn bị đóng băng (con trỏ, xem danh sách và cài đặt vẫn dùng được).
- Ở bảng điều khiển, dùng phím điều hướng để di chuyển giữa các nút và bấm A để chọn (đổi tab bằng trái/phải). Hộp thoại kết thúc ván: A / Start để sang ván mới.
- Hướng màn hình theo thiết bị (khi nằm ngang, bàn cờ ở bên trái hoặc phải, đổi trong cài đặt).

## Kiểm tra chữ ký (Android)
Dấu vân tay SHA-256 của chứng chỉ ký APK:

```
24:17:8D:C7:BD:5A:86:8E:E5:DF:66:AE:05:6F:88:5E:28:9E:17:5F:CD:D6:7D:8E:FA:4C:30:B8:75:DC:A3:DE
```
Có thể đối chiếu với kết quả của `apksigner verify --print-certs real-time-co-tuong-android-<phiên bản>.apk`.

## Hiệu năng (đo trên máy thật)
Retroid Pocket 5 (Android 13): CPU khoảng 4%, bộ nhớ (PSS) khoảng 180–200 MB. Galaxy Note 8 (Android 9): CPU khoảng 22–30%, PSS khoảng 290 MB (máy đời cũ). Dung lượng tệp phát hành (trước khi giải nén): Linux khoảng 29 MB, Windows khoảng 39 MB, bản trình duyệt khoảng 11 MB (lần đầu tải khoảng 10 MB).

## Hạn chế đã biết
- **Windows mới chỉ được kiểm tra bằng Wine** (chưa kiểm tra điều khiển, FPS và bộ nhớ trên Windows thật).
- Bản Android mới được kiểm tra trên hai máy dùng Qualcomm (Adreno): Galaxy Note 8 và Retroid Pocket 5. Các GPU khác chưa được kiểm tra.
- Trò chơi hiển thị bằng tiếng Việt.
- Các tập lệnh nằm trong bản phát hành dưới dạng đã biên dịch của Godot (chuỗi token nén). Không có mã nguồn dạng văn bản thuần.

## Giấy phép
- **Điều khoản sử dụng trò chơi** (© 2026 kken0507): chơi miễn phí. Nếu giữ nguyên bản gốc (không chỉnh sửa), miễn phí, và kèm theo `LICENSE.txt` và `LICENSES.txt`, bạn được sao chép và chia sẻ cho người khác (chia sẻ liên kết tải chính thức cũng được tự do). Cần có sự đồng ý bằng văn bản nếu muốn chỉnh sửa, dịch hoặc tạo bản phát sinh; bán, cho thuê hoặc dùng cho mục đích thương mại (kể cả kiếm tiền bằng quảng cáo); dịch ngược hoặc tách lấy tài nguyên; xóa hoặc sửa thông tin bản quyền. Luật chơi cờ tướng truyền thống không bị hạn chế. **Bản chính có hiệu lực pháp lý là tiếng Anh: `LICENSE.txt`.**
- Trò chơi được làm bằng Godot Engine (MIT) và chứa một phần (subset) phông Noto (SIL Open Font License 1.1). Nội dung giấy phép nằm trong `LICENSES.txt` đi kèm mỗi bản phát hành (cũng đặt ở thư mục gốc của kho này và ở Releases; bản Android là APK nên không thể kèm tệp). Bản Android còn chứa AndroidX và thư viện chuẩn Kotlin (Apache License 2.0).
