---
layout: post
title: "SavEat - Aplikasi Mobile Pengelola Bahan Makanan & Resep Cerdas"
date: 2024-11-08 10:00:00 +0700
categories: [Mobile Development, Android]
tags: [android, java, sqlite, api, mobile-app, food-management, ai-chatbot, gemini-ai, recipe-app]
image:
  path: /assets/img/saveat.jpg
  alt: SavEat - Smart Food Management App
---

## 📱 Tentang SavEat

**SavEat** adalah aplikasi mobile berbasis Android yang dirancang untuk membantu pengguna dalam mengelola stok bahan makanan, mengurangi pemborosan, serta menemukan resep-resep berdasarkan bahan yang tersedia di rumah. Aplikasi ini merupakan solusi praktis untuk mengatasi masalah pemborosan makanan di rumah tangga.

## 🚀 Teknologi yang Digunakan

### Platform & Tools
- **Bahasa Pemrograman**: Java
- **IDE**: Android Studio
- **Database**: SQLite (penyimpanan lokal)

### API Integration
- **TheMealDB API** – Untuk data resep masakan
- **Google Gemini AI** – Untuk fitur asisten AI cerdas melalui chat

### Build Tools
- **Gradle Plugin**:
  - `com.android.application` version 8.1.0
  - `org.jetbrains.kotlin.android` version 1.8.10 (opsional untuk dependensi Kotlin)

## 🎯 Tujuan & Fungsi Utama

SavEat bertujuan untuk:

✅ Membantu pengguna mengelola stok bahan makanan  
✅ Memberikan pengingat masa kedaluwarsa untuk bahan makanan  
✅ Menyediakan rekomendasi resep berdasarkan bahan yang dimiliki pengguna  
✅ Mengurangi pemborosan makanan di rumah tangga  

## ✨ Fitur-fitur Utama

### 1. 🗂️ Manajemen Stok Bahan
- Tambah, edit, dan hapus bahan makanan
- Simpan informasi lengkap: nama, jumlah, satuan, kategori, tanggal kedaluwarsa, dan gambar bahan
- Tampilan yang intuitif dan mudah digunakan

### 2. 📝 Detail Bahan
- Lihat detail bahan termasuk informasi lengkap dan gambar
- Informasi kedaluwarsa yang jelas

### 3. 🔍 Pencarian Resep
- Cari resep berdasarkan bahan makanan yang dimiliki pengguna
- Integrasi dengan TheMealDB API untuk database resep yang luas

### 4. 🏆 Rekomendasi Resep Populer
- Tampilkan resep trending dari API TheMealDB
- Update resep populer secara berkala

### 5. ⭐ Resep Favorit
- Simpan resep ke daftar favorit untuk akses cepat
- Kelola koleksi resep favorit Anda

### 6. 🤖 Asisten AI (Chatbot)
- Gunakan fitur AI chat untuk tips memasak dan rekomendasi resep
- Powered by Google Gemini AI untuk respons yang cerdas dan kontekstual

### 7. 🔔 Notifikasi Kadaluwarsa
- Notifikasi otomatis saat bahan mendekati tanggal kedaluwarsa
- Hindari pemborosan makanan dengan pengingat tepat waktu

### 8. 👤 Manajemen Profil
- Edit informasi profil: nama, email, gender, dan foto profil
- Personalisasi pengalaman pengguna

### 9. 📊 Riwayat Bahan
- Lihat log penggunaan bahan makanan
- Tracking konsumsi bahan untuk perencanaan belanja yang lebih baik

## 📋 Cara Menggunakan Aplikasi

### 1️⃣ Instalasi
Buka Aplikasi SavEat melalui Android Studio atau instal langsung di perangkat Android.

### 2️⃣ Login atau Daftar Akun
- Pengguna baru dapat mendaftar (Sign Up)
- Pengguna lama dapat masuk (Sign In)

### 3️⃣ Navigasi Utama
Setelah login, pengguna akan diarahkan ke halaman **Home** yang menampilkan resep populer.

Gunakan menu navigasi bawah untuk mengakses fitur:
- **Home**: Resep-resep pilihan dan populer
- **Stok**: Lihat dan kelola bahan makanan
- **AI Chat**: Berinteraksi dengan asisten pintar
- **Profil**: Kelola akun, lihat riwayat bahan, dan logout

### 4️⃣ Mengelola Stok
Pada halaman **Stok**, klik tombol **+** untuk menambahkan bahan baru, atau klik bahan yang ada untuk mengedit atau menghapus.

### 5️⃣ Menjelajahi Resep
Klik resep pada halaman utama untuk melihat detail resep lengkap, termasuk:
- Bahan-bahan yang dibutuhkan
- Instruksi memasak step-by-step
- Video tutorial dari YouTube (jika tersedia)

## 🛠️ Developer Notes

> **Catatan Penting untuk Developer:**
{: .prompt-warning }

- Pastikan perangkat memiliki koneksi internet untuk menggunakan fitur API (Resep dan AI Chat)
- SQLite digunakan untuk menyimpan data bahan secara lokal di perangkat
- Fitur AI Chat menggunakan Google Gemini API, pastikan key/akses diatur dengan benar

## 💡 Pembelajaran & Tantangan

Dalam pengembangan SavEat, saya belajar tentang:

- **Integrasi API**: Bekerja dengan multiple API (TheMealDB dan Google Gemini AI)
- **Database Management**: Implementasi SQLite untuk penyimpanan data lokal yang efisien
- **User Experience**: Merancang interface yang intuitif untuk manajemen inventori
- **Notification System**: Implementasi sistem notifikasi untuk pengingat kedaluwarsa
- **Image Handling**: Manajemen gambar dan foto dalam aplikasi mobile

## 🎓 Konteks Proyek

SavEat adalah proyek tugas akademik yang dikembangkan untuk keperluan edukasi dan non-komersial. Proyek ini mendemonstrasikan kemampuan dalam:

- Pengembangan aplikasi Android native
- Integrasi dengan REST API
- Database management dengan SQLite
- Implementasi AI/ML features
- User-centered design thinking

## 🔗 Source Code

Proyek ini dikembangkan sebagai bagian dari pembelajaran Mobile Development.

---

