# 🍽️ XFoodi - Hệ Thống Quản Lý Đặt Bàn & Gọi Món QR Multi-Tenant

XFoodi là nền tảng quản lý nhà hàng đa doanh nghiệp (Multi-tenant) hiện đại, hỗ trợ toàn diện từ đặt bàn trực tuyến, gọi món qua mã QR tại bàn, quản lý bếp theo thời gian thực (real-time) cho đến phân tích báo cáo và trợ lý ảo AI hỗ trợ thực khách.

---

## 🚀 Tính Năng Nổi Bật

### 1. Kiến Trúc Đa Doanh Nghiệp (Multi-Tenant Architecture)
* Mỗi nhà hàng đăng ký trên hệ thống sở hữu phân vùng cơ sở dữ liệu riêng biệt, đảm bảo an toàn thông tin và hiệu năng vận hành.
* Quản lý phân quyền chặt chẽ giữa **Quản trị hệ thống (Platform Admin)**, **Chủ nhà hàng (Restaurant Owner)**, **Nhân viên (Staff)** và **Khách hàng (Customer)**.

### 2. Đặt Bàn Trực Tuyến & Cọc Giữ Chỗ Tự Động
* Cho phép khách hàng vãng lai (Guest) hoặc đã đăng nhập đặt bàn nhanh chóng.
* Hệ thống bắt buộc đặt cọc với mức phí linh hoạt cấu hình theo số lượng chỗ ngồi của từng loại bàn (ví dụ: bàn 4 người, bàn 8 người, bàn tiệc lớn).
* Tích hợp cổng thanh toán trực tuyến **VNPAY**.
* Tự động gửi email xác nhận đặt bàn kèm thông tin chi tiết và mã nhận bàn cho khách hàng.

### 3. Gọi Món Tại Bàn Qua Mã QR (QR-Code Ordering)
* Khách hàng quét mã QR tại bàn để xem thực đơn số và gọi món trực tiếp.
* Giỏ hàng tự động đồng bộ và tính toán chi phí theo thời gian thực.
* Hỗ trợ thanh toán tại bàn hoặc thanh toán sau tại quầy.

### 4. Màn Hình Bếp Thời Gian Thực (Live Kitchen Monitor)
* Kết nối thông suốt qua **SignalR/WebSockets** giữa thực khách và nhà bếp.
* Đơn hàng từ bàn ăn được gửi ngay lập tức tới bếp mà không cần tải lại trang.
* Đầu bếp có thể cập nhật trạng thái đơn hàng (Đang chế biến, Đã xong) và tự động đồng bộ trạng thái thanh toán.

### 5. Bảng Điều Khiển & Phân Tích Thông Minh (Analytics Dashboard)
* Thống kê doanh thu, số lượng đơn hàng, món ăn bán chạy nhất theo dạng biểu đồ trực quan.
* Quản lý phản hồi/đánh giá (Feedback) từ khách hàng.
* Quản lý nhân viên, bàn ăn, sơ đồ tầng và phân phối khu vực phục vụ.

### 6. Trợ Lý Ảo AI (AI Smart Assistant)
* Tích hợp Chatbot AI thông minh hỗ trợ khách hàng tìm kiếm món ăn, đề xuất thực đơn dựa trên sở thích và giải đáp thông tin nhà hàng.

---

## 🛠️ Công Nghệ Sử Dụng

| Phân hệ | Công nghệ |
| :--- | :--- |
| **Frontend** | Next.js (App Router), React, TypeScript, Axios, Day.js |
| **Backend** | Node.js, Express, TypeScript, Prisma ORM, PostgreSQL / MySQL |
| **Real-time & Socket** | SignalR / WebSockets |
| **Thanh toán** | VNPAY API |
| **Gửi Mail** | Nodemailer / SendGrid |
| **Thiết kế & Giao diện** | CSS Variables (Glassmorphism, Dark/Light Mode, Responsive) |

---

## 📂 Cấu Trúc Thư Mục Dự Án

```text
swp391-rbl-project-group-6/
├── XFOODI-BE/          # Mã nguồn Backend (API Service & Database)
│   ├── prisma/         # Prisma Schema & Database Migrations
│   ├── src/            # Thư mục code logic chính (Controllers, Routes, Services)
│   └── package.json
└── XFOODI-FE/          # Mã nguồn Frontend (Next.js Application)
    ├── app/            # Next.js App Router (Pages & API routes)
    ├── components/     # Các UI Components dùng chung (Dashboard, Layout, UI)
    ├── lib/            # Services, Contexts, Hooks, i18n
    └── package.json
```

---

## ⚙️ Hướng Dẫn Cài Đặt

### 1. Cấu hình Biến Môi Trường (Environment Variables)

#### Backend (`XFOODI-BE/.env`):
```env
PORT=3001
DATABASE_URL="postgresql://user:password@localhost:5432/xfoodi_db"
JWT_SECRET="your-jwt-secret-key"
EMAIL_HOST="smtp.gmail.com"
EMAIL_PORT=587
EMAIL_USER="your-email@gmail.com"
EMAIL_PASS="your-email-app-password"
VNP_TMNCODE="your-vnpay-tmncode"
VNP_HASHSECRET="your-vnpay-hashsecret"
VNP_URL="https://sandbox.vnpayment.vn/paymentv2/vpcpay.html"
```

#### Frontend (`XFOODI-FE/.env.local`):
```env
NEXT_PUBLIC_API_URL="http://localhost:3001/api"
NEXT_PUBLIC_SOCKET_URL="http://localhost:3001"
```

### 2. Khởi Chạy Backend

```bash
cd XFOODI-BE
pnpm install
npx prisma db push
pnpm run dev
```

### 3. Khởi Chạy Frontend

```bash
cd XFOODI-FE
pnpm install
pnpm run dev
```

Ứng dụng sẽ khả dụng tại địa chỉ: `http://localhost:3000` (Frontend) và `http://localhost:3001` (Backend).

---

## 👥 Thành Viên Nhóm (Group 6)
Dự án được phát triển và hoàn thiện bởi các thành viên thuộc Nhóm 6 môn học SWP391.
