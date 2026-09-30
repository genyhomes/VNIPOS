# ☕ Cuccu Café - Hệ Thống Gọi Món Bằng Mã QR & Quản Lý Doanh Thu

Hệ thống chuyên nghiệp dành cho quán cà phê / trà sữa: Khách quét mã QR tại bàn để xem menu và gọi món trực tiếp, đơn hàng đổ ngay về máy tính tại quầy pha chế kèm **chuông báo âm thanh + giọng nói tiếng Việt**, nhân viên xác nhận và ấn thanh toán để **tự động cộng dồn doanh số thời gian thực**.

## Tích hợp tính năng thông báo số dư bằng âm thanh cho nhân viên. Hoàn toàn miễn phí chỉ cần Cài đặt Store Noti là ứng dụng di động của Techcombank dành riêng cho người bán hàng, giúp gửi thông báo giao dịch tiền về tức thì cho chủ cửa hàng và nhân viên. Cũng có thể kết hợp dùng thêm loa thông báo(Đăng ký Miễn phí)

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
- **💳 Tích hợp thanh toán VietQR tại bàn**: Khách có thể quét mã VietQR mang chính xác số tiền đơn hàng để chuyển khoản ngay tại bàn qua ứng dụng ngân hàng bất kỳ.

### 2. 💳 Tích Hợp VietQR Động Theo Số Tiền Hóa Đơn (Nhiều ngân hàng)
- **Thông tin tài khoản thụ hưởng**:
  - Ngân hàng: **Techcombank (TCB - Mã BIN: 970407)**
  - Số tài khoản: **`1903 1255 2xx30`**
  - Tên chủ tài khoản: **`TRAN VAN AAA`**

- **Tự động gắn số tiền**: Mã QR sinh ra tự động điền đúng chính xác 100% số tiền hóa đơn và nội dung chuyển khoản (ví dụ: `CUCCU B3 5`).
- **Quét bằng mọi ứng dụng ngân hàng**: Techcombank, Vietcombank, MB, Momo, BIDV, Agribank, ACB, VPBank... không lo khách nhập nhầm số tiền.
- **Tích hợp cả ở 2 nơi**:
  - Tại quầy thu ngân (`/barista` khi chọn Chuyển khoản QR): hiển thị cho khách tại quầy quét.
  - Tại bàn khách ngồi (`/?table=X` trong hộp thoại theo dõi đơn): khách tự quét thanh toán tại bàn.
  - Có sẵn các nút sao chép nhanh 📋 số tài khoản, số tiền và nội dung.

### 3. 🔐 Đặt Mật Khẩu Bảo Vệ Khu Vực Quản Lý (Ngoại trừ trang khách)
- **Trang khách gọi món (`/`)**: Hoàn toàn mở, khách quét mã QR vào là gọi món ngay, không cần đăng nhập hay nhập bất kỳ mật khẩu nào.
- **Các trang quản trị được bảo vệ 100%**:
  - Màn hình Quầy pha chế (`/barista`)
  - Báo cáo Doanh thu (`/revenue`)
  - In mã QR để bàn (`/qr`)
  - Quản lý Thực đơn (`/menu-manage`)
  - Tất cả các API xem doanh thu, đổi trạng thái món, thanh toán thu tiền.
- **Mật khẩu quản trị**: Khi chạy lần đầu hoặc sau khi Khôi phục dữ liệu gốc (Factory Reset), hệ thống sẽ yêu cầu thiết lập mật khẩu quản trị mới (tối thiểu 4 ký tự) chứ không để mật khẩu mặc định 1234 để đảm bảo an toàn tuyệt đối.
- **Cơ chế xác thực**:
  - Nếu chưa đăng nhập, hệ thống sẽ tự động chuyển hướng đến màn hình **`/login`**.
  - Đăng nhập thành công sẽ lưu phiên làm việc (7 ngày).
  - Có nút **🔑 Đổi MK** để đổi mật khẩu quản trị bất kỳ lúc nào.
  - Có nút **🚪 Đăng xuất** để bảo mật khi rời quầy.

### 4. 🖥️ Màn Hình Quầy Pha Chế & POS Thu Ngân (`/barista`)
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
  - Chọn hình thức: **Tiền mặt** (có máy tính tiền thừa) hoặc **Chuyển khoản QR** (mã VietQR động).
  - Bấm **"✓ Đã Thanh Toán & Cộng Doanh Số"** ➜ Chuông tính tiền reo, đơn được lưu vào doanh thu, hiển thị hóa đơn mẫu in nhiệt (khổ 80mm/58mm).

### 5. 📊 Báo Cáo Doanh Thu & Doanh Số Bán Hàng (`/revenue`)
- **Cập nhật tức thì**: Doanh số lập tức nhảy số thời gian thực qua WebSocket.
- **4 Thẻ thống kê KPI trọng yếu**: Doanh thu hôm nay, Số đơn hoàn thành, Giá trị trung bình/đơn (AOV), Số bàn đang phục vụ.
- **Biểu đồ phân bố doanh thu theo khung giờ** (từ 7h sáng đến 22h đêm).
- **Cơ cấu thanh toán**: Tỷ lệ Tiền mặt vs Chuyển khoản VietQR.
- **Top món bán chạy nhất & Lịch sử đơn hàng**: Bộ lọc ngày/bàn, xuất file **Excel / CSV**, in báo cáo A4.

### 6. 🖨️ In Mã QR Để Bàn Sẵn Sàng Sử Dụng (`/qr`)
- Tự động tạo mã QR sắc nét cho từng bàn (Bàn 1 đến Bàn 15 hoặc tùy chỉnh).
- Standee in sẵn logo quán, số bàn, tên Wi-Fi & mật khẩu, vạch cắt kéo để lồng mica.

---

## 🚀 Hướng Dẫn Cài Đặt & Sử Dụng

### Khởi Động & Quản Trị Máy Chủ:
- **Khởi động server**: Nhấp đúp vào **`start-server.bat`** (tự động giải phóng cổng 3000 nếu bị kẹt).
- **Khởi động lại server nhanh**: Nhấp đúp vào **`restart-server.bat`** (tự động tắt tiến trình cũ và khởi động lại ngay).
- **Reset & Khôi phục hệ thống**: Nhấp đúp vào **`reset-server.bat`** (có menu chọn: Khởi động lại, Khôi phục dữ liệu gốc `initialSeed`, Làm mới đơn hàng, Sao lưu JSON, Phục hồi từ file JSON).
- **Sao Lưu & Phục Hồi Dữ Liệu (Backup & Restore)**:
  - **Trên Web**: Vào trang **Cài Đặt** (`/settings`) hoặc bấm nút **`⚡ Thao Tác Server`** trên thanh menu để bấm **"Tải File Sao Lưu (.JSON)"** hoặc chọn file JSON để **"Phục Hồi Dữ Liệu"**.
  - **Qua file lệnh / CLI**: Chạy **`reset-server.bat`** (mục `[4]` Sao lưu, mục `[5]` Phục hồi) hoặc dùng lệnh `node scripts/reset-db.js --backup` / `--restore <file.json>`.
- Hoặc bấm nút **`⚡ Thao Tác Server`** trực tiếp trên thanh menu quản trị của trang web.

### Các Đường Dẫn Truy Cập:

| Mục Đích | Đường Dẫn Trên Máy Tính Quầy | Đường Dẫn Khách Quét (Wi-Fi Quán) | Yêu Cầu Mật Khẩu |
| :--- | :--- | :--- | :--- |
| **Menu khách chọn món** | `http://localhost:3000/?table=1` | `http://<IP_MÁY_TÍNH>:3000/?table=1` | ❌ **Không cần** (Mở tự do) |
| **Đăng nhập quản lý** | `http://localhost:3000/login` | - | Mật khẩu quản trị do quán thiết lập |
| **Quầy pha chế & âm thanh** | `http://localhost:3000/barista` | - | 🔒 **Có** |
| **Quản lý doanh thu** | `http://localhost:3000/revenue` | - | 🔒 **Có** |
| **In mã QR dán bàn** | `http://localhost:3000/qr` | - | 🔒 **Có** |
| **Quản lý thực đơn** | `http://localhost:3000/menu-manage` | - | 🔒 **Chỉ Admin** |
| **Cài đặt quán & ngân hàng** | `http://localhost:3000/settings` | - | 🔒 **Chỉ Admin** |


*(Địa chỉ IP cụ thể của máy chủ trong mạng Wi-Fi quán sẽ được hệ thống tự động hiển thị trong màn hình console và trang In mã QR).*

---

## 👥 Phân Quyền Người Dùng (Admin & Nhân Viên)

Hệ thống hỗ trợ phân quyền chặt chẽ 2 cấp độ:

### 1. 👑 Quản Trị Viên (`admin`)
- **Quyền hạn**: Toàn quyền quản trị mọi tác vụ trong hệ thống:
  - Xem và quản lý chi tiết doanh thu, doanh số, phương thức thanh toán, biểu đồ giờ cao điểm (`/revenue`).
  - Quản lý danh mục, thêm / sửa / xóa món ăn đồ uống, tải ảnh món (`/menu-manage`).
  - Cài đặt thông tin quán, Wi-Fi, cấu hình tài khoản ngân hàng thụ hưởng VietQR (`/settings`).
  - Quản lý số bàn và in mã QR để bàn (`/qr`).
  - Reset server, làm mới đơn hàng ca bán, sao lưu JSON và phục hồi dữ liệu.
  - Xem và thao tác quầy pha chế (`/barista`).
  - Có thể đổi mật khẩu cho chính mình hoặc đặt lại mật khẩu cho nhân viên.

### 2. ☕ Nhân Viên Pha Chế (`staff` / `nhanvien`)
- **Mật khẩu mặc định**: **`123456`** (Cả trên Local và Hosting).
- **Quyền hạn**: **Chỉ xem và thao tác ở Quầy Pha Chế (`/barista`)**:
  - Xem các đơn hàng đang chờ làm, đang pha chế và đã ra món.
  - Chuyển trạng thái đơn: *Chờ ➜ Đang làm ➜ Đã ra món*.
  - Xác nhận thanh toán đơn hàng tại quầy và hiển thị mã VietQR cho khách quét.
  - Tự động **ẩn các nút menu** *Doanh Thu, In Mã QR, Món, Cài Đặt, Reset Server*.
  - **Đổi mật khẩu**: Nhân viên có thể tự đổi mật khẩu của mình ngay tại quầy Barista qua nút **🔑 Đổi MK** (nhập mật khẩu cũ `123456` và nhập mật khẩu mới).

---

## 📁 Phân Chia 2 Thư Mục Độc Lập: `local/` và `hosting/`

Hệ thống đã được tách riêng thành 2 gói thư mục độc lập để quản lý và triển khai dễ dàng:

```
Cuccu-cafe/
├── local/                  <-- DÀNH CHO MÁY TÍNH CỤC BỘ TẠI QUÁN (Node.js / Python)
│   ├── server.js           (Máy chủ Node.js)
│   ├── server.py           (Máy chủ Python 3 thuần - không cần pip install)
│   ├── start-server.bat    (Chạy Node.js port 3000 chỉ 1 click)
│   ├── start-python.bat    (Chạy Python port 3000 chỉ 1 click)
│   ├── reset-server.bat    (Bảo trì & khôi phục dữ liệu)
│   ├── data/               (Cơ sở dữ liệu db.json)
│   └── public/
│       ├── login.html (Giao diện đăng nhập & thiết lập mật khẩu admin local)
│       └── qr-print.html   (Nhúng qr-print.js:In mã QR 4 bước kèm kết nối Wi-Fi)
│
└── hosting/                <-- DÀNH CHO UPLOAD LÊN WEB HOSTING (PHP 8.0+ & MySQL)
    ├── index.php           (Router chính)
    ├── api.php             (Backend REST APIs)
    ├── db.php              (Lớp kết nối PDO MySQL)
    ├── auth.php            (Phân quyền Admin / Nhân viên)
    ├── vietqr.php          (Tạo mã VietQR chuẩn EMVCo an toàn trên PHP 8.0+)
    ├── schema.sql          (Cấu trúc bảng MySQL)
    ├── .htaccess           (Cấu hình Apache Rewrite)
    └── public/
        ├── login.html      (Giao diện cấu hình Database hosting & Đăng nhập)
        └── qr-print.html   (Nhúng qr-print.js:  In mã QR 3 bước rút gọn)
```

---

## 💻 1. Hướng Dẫn Sử Dụng Thư Mục `local/` (Chạy Tại Quán)- Khách phải dùng chung wifi với máy chủ

### Khởi động máy chủ:
- **Chạy bằng Node.js**: Nhấp đúp vào file `local/start-server.bat`.
- **Chạy bằng Python**: Nhấp đúp vào file `local/start-python.bat`.
- Cả hai máy chủ đều lắng nghe trên cổng `3000`:
  - Khách gọi món: `http://localhost:3000/?table=1` (hoặc qua IP nội bộ Wi-Fi).
  - Đăng nhập: `http://localhost:3000/login.html`.
  - Quầy pha chế: `http://localhost:3000/barista`.

### Mật khẩu & Phân quyền trên Local:
- Mật khẩu mặc định của user/nhân viên: **`123456`**.
- Đổi mật khẩu nhân viên: Nhân viên bấm **🔑 Đổi MK** tại màn hình `/barista` để đổi mật khẩu của mình.
- **Quy trình Reset hệ thống trên Local**:
  - Khi Admin bấm **Reset Server (Khôi phục dữ liệu gốc)**: Hệ thống đặt lại mật khẩu admin về rỗng, đặt lại mật khẩu user về `123456`, xóa session và chuyển hướng ngay về **`login.html`**.
  - Tại `login.html`, màn hình sẽ yêu cầu Admin tạo mật khẩu quản trị mới trước khi bắt đầu sử dụng.

---

## 🌐 2. Hướng Dẫn Sử Dụng Thư Mục `hosting/` (Upload Hosting cPanel) - Khách hàng kết nối bât kỳ mạng nào đều được - cần có tên miền

### Tính tương thích PHP:
- **Hỗ trợ đầy đủ PHP 8.0, 8.1, 8.2, 8.3+**:
  - Không sử dụng các hàm deprecated.
  - Module `vietqr.php` sử dụng thuật toán xóa dấu tiếng Việt bằng Regex thuần chuẩn UTF-8, hoàn toàn **không phụ thuộc vào extension `iconv`**, loại bỏ 100% lỗi runtime/warning trên PHP 8.0.
  - Đã bổ sung endpoint tải ảnh QR chuyển khoản `/api/settings/vietqr/download` trực tiếp từ server.
  - Tự động fallback ảnh QR nội bộ khi khách hàng có cài Adblock Plus hoặc bị mạng chặn CDN.

### Triển khai lên Hosting:
1. Nén toàn bộ nội dung trong thư mục `hosting/` thành file `.zip`.
2. Tải lên thư mục gốc của domain (thường là `public_html` trên cPanel hoặc thư mục con `/cuccu/`).
3. Tạo 1 Database MySQL và 1 User MySQL trên cPanel, gán quyền *ALL PRIVILEGES*.
4. Mở trình duyệt truy cập: `http://domain-cua-ban.com/login` (hoặc `http://domain-cua-ban.com/cuccu/login`).
5. Giao diện **`login.html`** sẽ hiện ra form thiết lập CSDL:
   - Nhập thông số Database: Host, Port, Tên CSDL, User, Pass.
   - Nhập mật khẩu quản trị Admin mới.
   - Bấm **"Khởi Tạo CSDL & Bắt Đầu Sử Dụng"**: Hệ thống sẽ tự động tạo bảng, tạo tài khoản Admin và Staff (`123456`), tạo file `config.php` và đăng nhập.

### Quy trình Reset hệ thống trên Hosting:
- Khi Admin bấm **Reset Server (Khôi phục dữ liệu gốc)**:
  - Hệ thống thực thi lệnh **DROP TOÀN BỘ CÁC BẢNG** trong CSDL MySQL (`orders`, `order_items`, `events`, `sessions`, `options`, `menu`, `categories`, `tables`, `settings`, `users`).
  - Xóa sạch session và chuyển hướng ngay về **`login.html`**.
  - Tại `login.html`, hệ thống phát hiện CSDL trống và hiển thị lại form cấu hình/tạo bảng để cài đặt lại từ đầu.





Tải full code: https://forumviet.com/threads/he-thong-goi-mon-bang-ma-qr-quan-ly-doanh-thu-cho-nha-hang-quan-cafe-mien-phi.6187/

