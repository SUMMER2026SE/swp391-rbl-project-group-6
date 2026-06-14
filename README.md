[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/r92bbHwx)

<div align="center">

# 📋 AI Audit Log — Group 6

### *Nhật ký sử dụng AI minh bạch & có trách nhiệm*

![SWP391](https://img.shields.io/badge/Course-SWP391-blue?style=for-the-badge)
![FPT University](https://img.shields.io/badge/FPT-University-orange?style=for-the-badge)
![Summer 2026](https://img.shields.io/badge/Semester-SUMMER%202026-green?style=for-the-badge)
![Class](https://img.shields.io/badge/Class-SE20A06-red?style=for-the-badge)

</div>

---

## 🎯 Giới thiệu

Repository này là **nhật ký kiểm toán AI (AI Audit Log)** chính thức của nhóm 6 trong môn **Software Development Project (SWP391)** tại FPT University.

Mỗi thành viên trong nhóm sử dụng các file trong repository này để ghi chép **minh bạch**, **có hệ thống** toàn bộ quá trình sử dụng các công cụ AI (ChatGPT, Gemini, Claude, GitHub Copilot, Antigravity, Kiro) trong suốt học kỳ nhằm đảm bảo tính trung thực học thuật.

---

## 👥 Thành viên nhóm

| Họ tên | MSSV | Vai trò | Thư mục Audit |
| :--- | :---: | :--- | :--- |
| [Họ tên của Thi] | [MSSV] | [Vai trò] | [`Thi_Audit/`](./Thi_Audit/) |
| [Họ tên của Trung] | [MSSV] | [Vai trò] | [`Trung_Audit/`](./Trung_Audit/) |
| [Họ tên của Linh] | [MSSV] | [Vai trò] | [`Linh_Audit/`](./Linh_Audit/) |
| [Họ tên của Giang] | [MSSV] | [Vai trò] | [`Giang_Audit/`](./Giang_Audit/) |
| [Họ tên của Huy] | [MSSV] | [Vai trò] | [`Huy_Audit/`](./Huy_Audit/) |

> **Giảng viên hướng dẫn:** HanhNT &nbsp;|&nbsp; **Lớp:** SE20A06 &nbsp;|&nbsp; **Học kỳ:** SUMMER 2026

---

## 🏗️ Dự án

> **Nền tảng SaaS đa thuê (Multi-tenant SaaS Platform)**

Hệ thống quản lý nhà hàng theo mô hình SaaS đa thuê, cho phép nhiều chủ nhà hàng (tenant) vận hành và quản lý toàn bộ hoạt động kinh doanh trên cùng một nền tảng duy nhất.

---

## 📂 Cấu trúc Repository

```
swp391-rbl-project-group-6/
│
├── 📁 Thi_Audit/               # Nhật ký AI của thành viên Thi
│   ├── 📄 REFLECTION.md        # Tổng kết cuối kỳ
│   └── 📁 Weeks/
│       ├── 📄 Week_01.md       # Log AI tuần 1
│       ├── 📄 Week_02.md       # Log AI tuần 2
│       └── ...                 # (Đến Week_10.md)
│
├── 📁 Trung_Audit/             # Nhật ký AI của thành viên Trung
├── 📁 Linh_Audit/              # Nhật ký AI của thành viên Linh
├── 📁 Giang_Audit/             # Nhật ký AI của thành viên Giang
├── 📁 Huy_Audit/               # Nhật ký AI của thành viên Huy
│
├── 📄 .commitlintrc.json       # Luật kiểm tra commit tự động
├── 📄 .husky/commit-msg        # Git hook chặn commit sai chuẩn
├── 📄 COMMIT_CONVENTION.md     # Hướng dẫn quy chuẩn commit
├── 📄 GIT_RULES.md             # Quy tắc sử dụng Git của nhóm
└── 📄 README.md
```

---

## 📝 Quy trình Log Audit theo tuần

Mỗi thành viên mở file `Week_XX.md` tương ứng với tuần đang làm việc và điền vào **3 phần chính**:

| Phần | Nội dung cần ghi |
| :--- | :--- |
| **1. Changelog** | Các task đã hoàn thành trong tuần |
| **2. Nhật ký AI** | Prompt đã dùng, phản hồi của AI, và cách bạn tự cải tiến (Critical Thinking) |
| **3. Minh chứng** | Đường dẫn file code liên quan, ảnh chụp màn hình |

---

## ⚙️ Cài đặt (Bắt buộc sau khi Clone)

Repository này tích hợp sẵn **Husky + Commitlint** để tự động chặn commit không đúng chuẩn. Sau khi clone về, chạy lệnh sau để kích hoạt:

```bash
npm install
```

> Sau lệnh này, Git sẽ tự động kiểm tra cú pháp mỗi lần bạn gõ `git commit`. Commit sai chuẩn sẽ bị từ chối ngay lập tức.

---

## ✍️ Quy chuẩn Commit

Xem chi tiết tại file 📄 [COMMIT_CONVENTION.md](./COMMIT_CONVENTION.md)

```bash
# Cú pháp bắt buộc
<type>(<scope>): <mô tả ngắn>

# Ví dụ hợp lệ
feat(auth): them chuc nang dang nhap google
fix(db): sua loi ket noi database
docs(audit): hoan thanh log tuan 01
```

| `type` | Ý nghĩa |
| :--- | :--- |
| `feat` | Thêm chức năng mới |
| `fix` | Sửa lỗi |
| `docs` | Viết tài liệu / audit log |
| `refactor` | Tái cấu trúc code |
| `chore` | Công việc lặt vặt |

---

<div align="center">

*SWP391 — FPT University — SUMMER 2026*

</div>
