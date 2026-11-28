# NTMIX Pro – Phần mềm Chấm Trắc Nghiệm Trực Tuyến (Web App)

**NTMIX Pro** là ứng dụng web (PWA) hỗ trợ giáo viên chấm bài thi trắc nghiệm nhanh chóng, chính xác ngay trên trình duyệt điện thoại (iOS/Android) và máy tính mà không cần cài đặt phần mềm phức tạp hay phụ thuộc máy chủ xử lý.

* **Tác giả:** Nguyễn Thanh Tùng – Giáo viên Toán, Trường THPT Vinh Xuân, Thành phố Huế.
* **Trải nghiệm trực tiếp:** [https://tungvinhloc.github.io/ntmix/](https://tungvinhloc.github.io/ntmix/)

---

## ✨ Tính năng nổi bật

### 1. Hỗ trợ chuẩn cấu trúc đề thi 3 phần của Bộ GD&ĐT
* **Phần I:** Trắc nghiệm nhiều lựa chọn (A, B, C, D) – tối đa 40 câu. Hỗ trợ câu có nhiều đáp án đúng hoặc câu lỗi đề (tính điểm cho tất cả thí sinh).
* **Phần II:** Trắc nghiệm Đúng/Sai (4 ý a, b, c, d mỗi câu) – tối đa 8 câu. Hỗ trợ 2 chế độ tính điểm:
  * *Theo quy chế BGD:* Đúng 1 ý được 10%, 2 ý được 25%, 3 ý được 50%, 4 ý được 100% điểm tối đa của câu.
  * *Chia đều:* Mỗi ý đúng được 25% điểm của câu.
* **Phần III:** Trắc nghiệm trả lời ngắn (điền số tối đa 4 ký tự gồm chữ số, dấu `-` và dấu `,`) – tối đa 6 câu. Áp dụng quy tắc tô bắt buộc từ trái sang phải.

### 2. Hỗ trợ đa dạng mẫu phiếu trả lời trắc nghiệm
* **Phiếu BGD 2025 CV 1239** (SBD 8 số, Mã đề 4 số, 40 · 8 · 6 câu).
* **Phiếu NTMark_2025** (SBD 8 số, Mã đề 4 số, 40 · 8 · 6 câu).
* **Phiếu TNMaker BGD 2025 (4MĐ)** (SBD 8 số, Mã đề 4 số, 40 · 8 · 6 câu).
* **Phiếu NH (phiếu ngắn)** (STT 2 số, Mã đề 3 số, 12 · 2 · 4 câu).
* Tích hợp sẵn công cụ xem trước và tải tệp PDF/JPG chuẩn khổ A4 để in ấn trực tiếp trong tab **Tải giấy thi**.

### 3. Công nghệ nhận diện quang học (OMR) thông minh
* **Tự động nhận diện & nắn phẳng phối cảnh (Homography):** Xác định chính xác 4 ô vuông định vị ở 4 góc kết hợp các điểm neo giữa mép phiếu để khử méo khi giấy cong hoặc chụp nghiêng.
* **Chấm trực tiếp qua Camera (Live Scan):** Tự động bắt nét, phát âm báo/rung khi nhận đủ 4 góc ổn định, hiển thị điểm tức thì và hỗ trợ chế độ **Chấm liên tiếp** nhiều bài.
* **Chấm hàng loạt từ thư viện ảnh:** Chọn cùng lúc nhiều ảnh bài làm để hệ thống tự động quét và lưu toàn bộ kết quả.
* **Tuỳ chỉnh độ nhạy OMR:** Cho phép tinh chỉnh trực quan *Độ nhạt tối thiểu*, *Mức độ tô tối thiểu*, và *Độ nhạy tẩy xoá* kèm hình minh hoạ trực tiếp.
* **Kiểm soát quy chế nghiêm ngặt:** Tự động chấm `0` điểm và cảnh báo nếu thí sinh tô sai hoặc thiếu mã đề (dễ dàng khôi phục điểm thật sau khi sửa lại mã đề).

### 4. Quản lý Lớp học, Đợt kiểm tra & Thống kê chuyên sâu
* **Quản lý Lớp học:** Tạo lớp, nạp danh sách thí sinh từ file Excel (`.xlsx`, `.xls`, `.csv`), dán nhanh từ bảng tính hoặc nhập tay. Hỗ trợ thao tác nhấn giữ (long-press) để chỉnh sửa/xoá lớp và bài chấm.
* **Tạo bài chấm trực quan:** Tuỳ chỉnh linh hoạt cấu trúc từng phần, thang điểm, hệ điểm và kế thừa dữ liệu từ các đợt chấm trước.
* **Xem lại & Sửa bài:** Hiển thị ảnh phiếu đã khoanh tròn phản hồi (xanh lá: đúng, đỏ: sai, vàng: đáp án đúng), cắt ảnh vùng họ tên viết tay trên phiếu, cho phép sửa đáp án/SBD/Mã đề và tải ảnh bài chấm về máy.
* **Xuất dữ liệu & Thống kê:** Xuất bảng điểm ra file **Excel (`.xlsx`)**, xuất toàn bộ bài chấm thành file **PDF** hoặc nén thành tệp **ZIP**; xem biểu đồ phổ điểm (dạng cột) và biểu đồ xếp loại (dạng tròn) phân tích chi tiết theo từng phần.

---

## 🛠️ Kiến trúc kỹ thuật

* **Kiến trúc Single-File Web App:** Toàn bộ giao diện, logic xử lý ảnh và quản lý trạng thái được đóng gói gọn nhẹ trong tệp `index.html`, dễ dàng triển khai trên GitHub Pages hoặc chạy ngoại tuyến.
* **Xử lý hoàn toàn phía Client (Client-side):**
  * Sử dụng HTML5 `<canvas>` để phân tích kênh màu (tách mực in hồng và nét bút tô), tính toán ma trận biến đổi phối cảnh và vẽ lớp phủ phản hồi.
  * Lưu trữ cấu hình, danh sách lớp, đáp án và điểm số bằng `localStorage`; lưu trữ ảnh bài làm đã chấm bằng `IndexedDB` để đảm bảo tốc độ và quyền riêng tư dữ liệu.
* **Thư viện tích hợp (CDN):**
  * [SheetJS (`xlsx`)](https://sheetjs.com/): Đọc danh sách học sinh, nạp đáp án và xuất bảng điểm Excel.
  * [jsQR](https://github.com/cozmo/jsQR) & [ZXing](https://github.com/zxing-js/library): Quét và giải mã nhanh đáp án các mã đề từ mã QR.
  * [JSZip](https://stuk.github.io/jszip/) & [FileSaver.js](https://github.com/eligrey/FileSaver.js/): Đóng gói và tải xuống hàng loạt ảnh bài chấm.

---

## 📂 Cấu trúc thư mục

```text
ntmix/
├── index.html          # Mã nguồn chính của ứng dụng Web App NTMIX Pro
├── logo-ntmix.png      # Biểu tượng nhận diện ứng dụng
├── huong_dan.pdf       # Tài liệu hướng dẫn sử dụng chi tiết
├── README.md           # Tài liệu giới thiệu dự án
└── assets/             # Thư mục chứa mẫu phiếu trả lời trắc nghiệm (PDF & JPG)
    ├── bgd2025_cv1239.pdf / .jpg
    ├── NTMark_2025.pdf / .jpg
    ├── bgd2025.pdf / .jpg
    └── vx_02.jpg
```

---

## 🚀 Hướng dẫn sử dụng nhanh

1. **In phiếu trắc nghiệm:** Vào mục **Tải giấy thi**, chọn mẫu phiếu phù hợp và tải tệp PDF gốc. In trên khổ giấy **A4** với tỷ lệ **100%** (không chọn *Fit to page / Vừa trang*).
2. **Tạo lớp & Bài chấm:** Vào mục **Lớp học** (hoặc **Cấu hình lần chấm**), bấm nút **`+`** để tạo lớp, nạp danh sách SBD học sinh từ Excel và thiết lập cấu trúc đề/thang điểm.
3. **Nhập đáp án:** Vào mục **Cài đặt đáp án**, quét mã QR, nạp từ file Excel hoặc chạm chọn trực tiếp đáp án cho từng mã đề.
4. **Chấm bài:** Vào mục **Chấm bài**, chọn **Chấm ngay** để quét trực tiếp bằng camera hoặc **Chọn ảnh có sẵn** để chấm hàng loạt.
5. **Xem kết quả & Xuất báo cáo:** Kiểm tra lại bài làm trong mục **Kết quả**, xem biểu đồ phổ điểm tại **Thống kê**, và tải bảng điểm Excel hoặc hồ sơ bài thi PDF về máy.

---

## 📄 Bản quyền & Liên hệ

Dự án được phát triển phục vụ công tác giảng dạy và kiểm tra đánh giá của giáo viên. Mọi ý kiến đóng góp hoặc báo lỗi xin vui lòng tạo **Issue** trực tiếp trên kho lưu trữ này.
