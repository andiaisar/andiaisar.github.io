---
layout: post
title: "Vida View Apartment - Sistem Booking Apartemen Fullstack"
date: 2025-12-20 14:00:00 +0800
categories: [Web Development, Fullstack]
tags: [react, flask, python, fullstack, jwt, mysql, tailwind, zustand, booking-system, apartment]
image:
  path: /assets/img/vida-view.png
  alt: Vida View Apartment Booking System
---

## 🏢 Tentang Vida View Apartment

**Vida View Apartment Website** adalah platform berbasis web yang komprehensif untuk memudahkan proses penyewaan unit apartemen. Sistem ini menghubungkan tiga entitas utama: **Penyewa (Tenant)**, **Pemilik Unit (Owner)**, dan **Administrator** dalam satu ekosistem digital yang terintegrasi.

Proyek ini dirancang untuk menangani alur bisnis apartemen mulai dari pencarian unit, pemesanan (booking), verifikasi pembayaran, hingga pelaporan keuangan bagi pemilik unit.

## 🚀 Teknologi yang Digunakan

Aplikasi ini dikembangkan menggunakan arsitektur **Fullstack** modern dengan pemisahan yang jelas antara frontend dan backend.

### Frontend (Client-Side)
- **Framework**: React.js 18 dengan Vite sebagai build tool yang cepat dan modern
- **Styling**: Tailwind CSS untuk desain responsif dan konsisten
- **State Management**: Zustand untuk manajemen state global yang ringan dan efisien
- **Routing**: React Router DOM untuk navigasi multi-page application
- **HTTP Client**: Axios untuk komunikasi API dengan interceptor authentication

### Backend (Server-Side)
- **Language**: Python 3.x dengan paradigma OOP yang terstruktur
- **Framework**: Flask sebagai RESTful API server
- **ORM**: SQLAlchemy untuk abstraksi database dan query builder
- **Database**: MySQL / SQLite (Kompatibel untuk development dan production)
- **Authentication**: JWT (JSON Web Token) untuk sistem autentikasi stateless dan aman

### Integrasi & Deployment
- **API Architecture**: RESTful API dengan standar HTTP methods (GET, POST, PUT, DELETE)
- **File Upload**: Multer-like handling untuk upload bukti pembayaran dan foto unit
- **CORS**: Konfigurasi Cross-Origin Resource Sharing untuk keamanan API

## 🎯 Fitur Utama

### 1. 👥 Sistem Multi-Role User

Platform ini mendukung tiga level pengguna dengan hak akses yang berbeda:

#### 🏠 Tenant (Penyewa)
- Mencari dan memfilter unit apartemen berdasarkan kriteria (harga, tipe, lantai)
- Melakukan booking dengan pemilihan tanggal check-in dan check-out
- Mengunggah bukti transfer pembayaran secara manual
- Melihat riwayat transaksi dan status booking (*Pending*, *Confirmed*, *Cancelled*)
- Dashboard personal untuk tracking reservasi aktif

#### 🔑 Owner (Pemilik Unit)
- Mendaftarkan dan mengelola unit apartemen yang dimiliki
- Upload galeri foto unit dan deskripsi lengkap fasilitas
- Mengatur ketersediaan unit (available/booked) secara *real-time*
- Dashboard laporan pendapatan dengan grafik visualisasi
- Melihat detail penyewa dan riwayat booking per unit

#### ⚙️ Admin (Administrator)
- Memverifikasi dan mengonfirmasi pembayaran dari tenant
- Manajemen user (CRUD operations untuk tenant dan owner)
- Pengawasan sistem booking secara keseluruhan
- Dashboard statistik: total user, booking aktif, total revenue
- Manajemen promosi dan diskon (jika diimplementasikan)

### 2. 🏠 Manajemen Apartemen & Fasilitas

- **Pencarian Cerdas**: Filter berdasarkan range harga, tipe unit (Studio, 1BR, 2BR), dan lantai
- **Galeri Foto**: Multiple image upload dengan preview dan carousel viewer
- **Detail Lengkap**: Informasi ukuran, fasilitas (AC, WiFi, Kitchen), dan aturan unit
- **Status Real-time**: Indikator ketersediaan unit yang update otomatis saat ada booking baru

### 3. 📅 Sistem Booking & Pembayaran

#### Alur Booking
1. **Pencarian Unit**: Tenant memilih unit yang diinginkan dari listing page
2. **Pemilihan Tanggal**: Date picker untuk check-in dan check-out dengan validasi minimal stay
3. **Konfirmasi Booking**: Review detail booking (total harga, durasi, biaya tambahan)
4. **Upload Bukti Bayar**: Form upload gambar bukti transfer dengan preview
5. **Menunggu Verifikasi**: Status booking berubah menjadi *Pending* hingga admin verifikasi
6. **Notifikasi**: Sistem memberikan feedback status (*Confirmed* atau *Rejected*)

#### Fitur Pembayaran
- Upload manual bukti transfer (format: JPG, PNG, PDF)
- Preview gambar sebelum submit
- History bukti pembayaran yang tersimpan
- Admin panel untuk approve/reject payment dengan catatan

### 4. 📊 Dashboard & Laporan

#### Admin Dashboard
- **Total Users**: Statistik user terdaftar (Tenant, Owner, Admin)
- **Active Bookings**: Jumlah booking yang sedang berjalan
- **Total Revenue**: Kalkulasi pendapatan dengan grafik trend bulanan
- **Recent Activities**: Log aktivitas terbaru (booking baru, payment verified)

#### Owner Dashboard
- **Unit Performance**: Statistik occupancy rate per unit
- **Financial Report**: Laporan pendapatan kotor dan bersih
- **Booking Calendar**: Visualisasi kalender booking untuk setiap unit
- **Tenant Reviews**: (Optional) Rating dan review dari penyewa

#### Export & Reporting
- **Format Export**: Download laporan dalam format PDF atau Excel (CSV)
- **Date Range Filter**: Laporan custom berdasarkan periode tertentu
- **Detailed Breakdown**: Rincian transaksi per unit, per owner, atau per tenant

## 📂 Struktur Proyek

```bash
vida-view-apartment-website/
├── backend/                    # Server-side Logic (Flask)
│   ├── routes/                 # API Endpoints
│   │   ├── auth.py             # Login, Register, JWT Refresh
│   │   ├── apartments.py       # CRUD Apartments (Owner)
│   │   ├── bookings.py         # Booking Management
│   │   ├── payments.py         # Payment Verification (Admin)
│   │   └── users.py            # User Management (Admin)
│   ├── uploads/                # File Storage
│   │   ├── apartments/         # Foto unit apartemen
│   │   └── payments/           # Bukti transfer pembayaran
│   ├── app.py                  # Entry point Flask application
│   ├── models.py               # SQLAlchemy Models (User, Apartment, Booking)
│   ├── config.py               # Database & JWT Configuration
│   └── requirements.txt        # Python Dependencies
│
├── frontend/                   # Client-side Logic (React + Vite)
│   ├── src/
│   │   ├── api/                # Axios Configuration & API Calls
│   │   │   ├── axios.js        # Base Axios instance with JWT interceptor
│   │   │   └── endpoints.js    # API endpoint constants
│   │   ├── components/         # Reusable UI Components
│   │   │   ├── Navbar.jsx      # Navigation bar dengan role detection
│   │   │   ├── ApartmentCard.jsx # Card component untuk listing
│   │   │   ├── BookingForm.jsx # Form pemesanan dengan validasi
│   │   │   └── ImageUpload.jsx # Component upload dengan preview
│   │   ├── pages/              # Pages per Role
│   │   │   ├── auth/           # Login & Register
│   │   │   ├── admin/          # Admin Dashboard & Management
│   │   │   ├── owner/          # Owner Unit Management
│   │   │   └── tenant/         # Tenant Booking & History
│   │   ├── stores/             # Zustand Global State
│   │   │   ├── authStore.js    # Authentication state
│   │   │   └── apartmentStore.js # Apartment data caching
│   │   └── utils/              # Helper Functions
│   │       ├── formatters.js   # Date & Currency formatters
│   │       └── validators.js   # Form validation helpers
│   ├── vite.config.js          # Vite Configuration
│   └── package.json            # NPM Dependencies
│
└── database/                   # Database Schema & Sample Data
    ├── vidaview_schema.sql     # Complete Database Schema
    ├── sample_data.sql         # Dummy data untuk testing
    └── ERD_VidaView.png        # Entity Relationship Diagram
```

## 🔐 Fitur Keamanan

- **JWT Authentication**: Token-based authentication dengan refresh token mechanism
- **Password Hashing**: Bcrypt untuk enkripsi password di database
- **Role-Based Access Control (RBAC)**: Middleware authorization berdasarkan user role
- **Input Validation**: Server-side validation untuk mencegah SQL injection dan XSS
- **CORS Policy**: Whitelist origin untuk mencegah unauthorized access
- **File Upload Security**: Validasi tipe file dan size limit untuk upload

## 💻 Instalasi & Menjalankan Aplikasi

### Prerequisites
- Python 3.8+
- Node.js 16+ & npm
- MySQL Server (atau SQLite untuk development)

### Setup Backend

```bash
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

Backend akan berjalan di `http://localhost:5000`

### Setup Frontend

```bash
cd frontend
npm install
npm run dev
```

Frontend akan berjalan di `http://localhost:5173`

### Database Setup

```bash
mysql -u root -p < database/vidaview_schema.sql
mysql -u root -p vidaview_db < database/sample_data.sql
```

## 🎨 Highlights Pengembangan

### Teknologi Frontend Modern
Penggunaan React 18 dengan Vite memberikan performa *Hot Module Replacement (HMR)* yang sangat cepat selama development. Zustand dipilih sebagai state management karena lebih ringan dibanding Redux, cocok untuk aplikasi skala menengah.

### RESTful API dengan Flask
Flask dipilih karena kesederhanaannya dalam membangun API, namun tetap powerful dengan ekosistem library Python yang mature (SQLAlchemy, JWT, dll).

### Responsive Design
Tailwind CSS memudahkan pembuatan desain responsif dengan utility classes. Setiap halaman telah dioptimasi untuk tampilan mobile, tablet, dan desktop.

## 📈 Pengembangan Selanjutnya

- [ ] Integrasi payment gateway (Midtrans, Xendit) untuk pembayaran otomatis
- [ ] Sistem notifikasi real-time menggunakan WebSocket (Socket.io)
- [ ] Fitur chat antara tenant dan owner
- [ ] Calendar booking yang lebih interaktif (Google Calendar-like)
- [ ] Review & rating system untuk unit apartemen
- [ ] Dashboard analytics dengan Chart.js atau Recharts
- [ ] Email notification untuk booking confirmation

## 🔗 Repository & Demo

> **Status Proyek**: Production-ready (Private Repository)
{: .prompt-tip }

Proyek ini mencerminkan kemampuan fullstack development dengan pemahaman mendalam tentang arsitektur client-server, database design, dan best practices dalam web development.

---

## 💡 Pembelajaran & Tantangan

### Tantangan Utama
1. **Sinkronisasi Status Booking**: Menangani race condition saat multiple user booking unit yang sama secara bersamaan
2. **File Upload Handling**: Implementasi secure file upload dengan validasi di backend dan preview di frontend
3. **JWT Refresh Token**: Implementasi mekanisme refresh token agar user tidak logout setiap kali access token expired

### Key Takeaways
- Pentingnya memisahkan logic business di backend dan presentation di frontend
- Database normalization untuk menghindari redundansi data
- State management yang efisien untuk mengurangi unnecessary re-render di React
- Security first mindset dalam setiap fitur yang diimplementasikan

---

*Proyek ini dikembangkan sebagai bagian dari portfolio web development dengan fokus pada fullstack architecture, modern frontend framework (React), dan Python backend ecosystem.*
