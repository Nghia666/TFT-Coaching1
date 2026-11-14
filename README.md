# TFT Coach Android 0.4

## Tạo APK tự động bằng GitHub Actions (không cần cài Android Studio)
1. Tải ZIP dự án này và giải nén.
2. Tạo một repository GitHub mới, ví dụ `TFTCoachAndroid`.
3. Đưa toàn bộ nội dung thư mục đã giải nén lên repository (giữ nguyên thư mục `.github`).
4. Mở tab **Actions** của repository.
5. Chọn workflow **Build TFT Coach APK** rồi bấm **Run workflow** (hoặc đợi workflow chạy sau khi push lên nhánh `main`).
6. Khi chạy thành công, mở lần chạy đó, kéo xuống **Artifacts**, tải `TFTCoach-debug-apk`.
7. Giải nén artifact và cài `app-debug.apk` trên điện thoại Android. Nếu Android hỏi, cho phép cài ứng dụng từ nguồn bạn vừa dùng.

## Tạo APK bằng Android Studio
1. Mở thư mục dự án trong Android Studio.
2. Đồng bộ Gradle; cần internet để tải plugin và thư viện.
3. Chọn **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
4. APK debug thường nằm tại `app/build/outputs/apk/debug/app-debug.apk`.

## Quyền cần cấp khi chạy
- Quyền hiển thị trên ứng dụng khác để hiện cửa sổ nổi.
- Chấp thuận hộp thoại Android khi bắt đầu chia sẻ màn hình.
- Có thể dừng quan sát từ cửa sổ nổi hoặc thu hồi quyền hệ thống.

## Giới hạn
Đây là prototype 0.4. Mã nguồn chưa được biên dịch và kiểm thử trên thiết bị thật trong môi trường tạo dự án này. OCR chỉ đọc văn bản; có thể đọc nhầm số và không nhận diện đáng tin cậy chân dung tướng, sao, trang bị, vị trí đội hình hoặc biểu tượng lõi. Hãy xác nhận gợi ý OCR trước khi áp dụng. OCR xử lý trên thiết bị; dự án không có mã tải ảnh màn hình lên máy chủ.

Workflow GitHub Actions tạo APK debug để thử nghiệm, không phải bản phát hành đã kiểm định.
