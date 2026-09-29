# ☕ Cuccu Café - Hệ Thống Gọi Món Bằng Mã QR & Quản Lý Doanh Thu

Hệ thống chuyên nghiệp dành cho quán cà phê / trà sữa: Khách quét mã QR tại bàn để xem menu và gọi món trực tiếp, đơn hàng đổ ngay về máy tính tại quầy pha chế kèm **chuông báo âm thanh + giọng nói tiếng Việt**, nhân viên xác nhận và ấn thanh toán để **tự động cộng dồn doanh số thời gian thực**.

Tích hợp tính năng thông báo số dư bằng âm thanh cho nhân viên. Hoàn toàn miễn phí

Cài đặt Store Noti là ứng dụng di động của Techcombank dành riêng cho người bán hàng, giúp gửi thông báo giao dịch tiền về tức thì cho chủ cửa hàng và nhân viên. Có thể kết hợp dùng thêm loa thông báo

Tải full code: https://forumviet.com/threads/he-thong-goi-mon-bang-ma-qr-quan-ly-doanh-thu-cho-nha-hang-quan-cafe-mien-phi.6187/
---

## 🌟 Tính Năng Chính

### 1. 📱 Khách Gọi Món Tại Bàn Qua Mã QR (`/` hoặc `/?table=X`)
- **Tự động nhận diện số bàn**: Khách quét mã QR để bàn nào thì hệ thống tự động ghi nhận đúng bàn đó (ví dụ: `/?table=3`).
- **Thực đơn sinh động**: Phân loại theo danh mục: Cà phê đặc sản, Trà trái cây, Trà sữa & Macchiato, Đá xay & Sinh tố, Bánh ngọt & Ăn vặt.
- **Tùy chỉnh món (Topping & Options)**:
  - Chọn Size (Size M tiêu chuẩn, Size L).
  - Chọn mức đường (100%, 70%, 50%, 30%, 0%).
  - Chọn mức đá (100%, 70%, 50%, Không đá).
  - Thêm topping đa dạng (Trân châu đen, Trân châu trắng 3Q, Kem Cheese, Thạch nha đam, Pudding).
  - Ghi chú riêng cho từng món hoặc cho cả đơn hàng.
- **Giỏ hàng tiện lợi**: Tự động tính tổng tiền món + topping theo thời gian thực.
- **Theo dõi tiến độ trực tiếp (Live Tracking)**: Khách xem trực tiếp trạng thái đơn: *Chờ pha chế ➜ Đang pha chế ➜ Đã ra món ➜ Đã thanh toán*.

### 2. 🖥️ Màn Hình Quầy Pha Chế & POS Thu Ngân (`/barista`)
- **Âm thanh thông báo tự động (Web Audio API)**:
  - Chuông ngân trong trẻo âm sắc café cao cấp ngay khi có bàn mới bấm gọi món.
  - Tự động đọc bằng giọng nói tiếng Việt: *"Có đơn hàng mới từ Bàn số 5!"*.
  - Có nút **Thử chuông**, công tắc bật/tắt âm thanh và giọng nói.
- **Quản lý quy trình 3 làn (KDS Workflow)**:
  - 🟡 **Làn 1 - Chờ pha chế**: Đơn mới gửi từ bàn hiển thị nhấp nháy, kèm đồng hồ đếm phút chờ.
  - 🔵 **Làn 2 - Đang làm**: Nhân viên bấm *"Bắt đầu làm"*.
  - 🟢 **Làn 3 - Đã ra món**: Nhân viên bấm *"Hoàn thành & Ra món"*, sẵn sàng thu tiền.
- **Thu ngân & In hóa đơn thanh toán**:
  - Bấm nút **"Thanh toán & Thu tiền"**.
  - Chọn hình thức: **Tiền mặt** (có sẵn máy tính nhập tiền khách đưa, tính tiền thừa/thối lại) hoặc **Chuyển khoản QR**.
  - Bấm **"✓ Đã Thanh Toán & Cộng Doanh Số"** ➜ Chuông tính tiền reo, đơn được lưu vào doanh thu, hiển thị hóa đơn mẫu in nhiệt (khổ 80mm/58mm) để in ra nếu cần.

### 3. 📊 Báo Cáo Doanh Thu & Doanh Số Bán Hàng (`/revenue`)
- **Cập nhật tức thì**: Ngay khi thu ngân ấn thanh toán, doanh số lập tức nhảy số mà không cần tải lại trang.
- **4 Thẻ thống kê KPI trọng yếu**:
  - Tổng doanh thu hôm nay.
  - Số lượng đơn đã thanh toán.
  - Giá trị trung bình trên mỗi đơn (AOV).
  - Số bàn đang phục vụ & số tiền chờ thu.
- **Biểu đồ phân bố doanh thu theo khung giờ** (từ 7h sáng đến 22h đêm).
- **Cơ cấu thanh toán**: Tỷ lệ tiền mặt vs chuyển khoản ngân hàng.
- **Top món bán chạy nhất**: Bảng xếp hạng các món được gọi nhiều nhất quán.
- **Lịch sử giao dịch chi tiết**: Bộ lọc theo ngày, theo bàn, theo trạng thái, tìm kiếm theo mã đơn hoặc món, xuất dữ liệu ra file **Excel / CSV**, in báo cáo A4.

### 4. 🖨️ In Mã QR Để Bàn Sẵn Sàng Sử Dụng (`/qr`)
- Sinh mã QR sắc nét chuẩn mực cho từng bàn (từ Bàn 1 đến Bàn 15 hoặc tùy chỉnh số lượng bàn quán có).
- Thiết kế standee để bàn chuẩn mực: Tên quán, Logo, số bàn nổi bật, tên mạng Wi-Fi và mật khẩu, hướng dẫn khách dùng Camera/Zalo quét.
- Có sẵn đường viền và vạch cắt kéo để in ra giấy A4 hoặc bìa cứng dán lên mica để bàn.

### 5. 📝 Quản Lý Menu Món (`/menu-manage`)
- Bật/tắt trạng thái món nhanh chóng (Còn món 🟢 / Hết món 🔴). Khách quét mã sẽ thấy ngay thông báo hết hàng nếu quán hết nguyên liệu.
- Thêm món mới vào thực đơn với hình ảnh, mô tả, danh mục, giá tiền và nhãn nổi bật.

---

## 🚀 Hướng Dẫn Cài Đặt & Sử Dụng

### Khởi Động Máy Chủ:
Cách 1: Nhấp đúp chuột vào file **`start-server.bat`** trên máy tính quầy.
Cách 2: Mở terminal tại thư mục dự án và chạy:
```bash
npm start
```

### Các Đường Dẫn Truy Cập:

| Mục Đích | Đường Dẫn Trên Máy Tính Quầy | Đường Dẫn Khách Quét (Wi-Fi Quán) |
| :--- | :--- | :--- |
| **Menu khách chọn món** | `http://localhost:3000/?table=1` | `http://<IP_MÁY_TÍNH>:3000/?table=1` |
| **Quầy pha chế & âm thanh** | `http://localhost:3000/barista` | - |
| **Quản lý doanh thu** | `http://localhost:3000/revenue` | - |
| **In mã QR dán bàn** | `http://localhost:3000/qr` | - |
| **Quản lý thực đơn** | `http://localhost:3000/menu-manage` | - |

*(Địa chỉ IP cụ thể của máy chủ trong mạng Wi-Fi quán sẽ được hệ thống tự động hiển thị trong màn hình console và trang In mã QR).*
