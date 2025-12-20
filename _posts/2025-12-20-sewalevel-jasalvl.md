---
layout: post
title: "SEWALEVEL x JASALVL - Kalkulator & Layanan Leveling Growtopia Terintegrasi"
date: 2025-12-20 10:00:00 +0800
categories: [Web Development, Laravel]
tags: [laravel, php, tailwind, growtopia, calculator, web-app, fullstack]
image:
  path: /assets/img/sewaLevel.png
  alt: SEWALEVEL - Growtopia Leveling Calculator
---

## 🎮 Tentang SEWALEVEL x JASALVL

**SEWALEVEL x JASALVL** adalah aplikasi web berbasis Laravel yang dirancang khusus untuk komunitas pemain game **Growtopia**. Aplikasi ini berfungsi sebagai kalkulator cerdas untuk menghitung kebutuhan pengalaman (XP), estimasi biaya, dan waktu yang diperlukan untuk menaikkan level karakter dalam game. Selain itu, platform ini juga menjembatani pengguna dengan layanan jasa joki level yang terpercaya.

## 🚀 Teknologi yang Digunakan

### Framework & Language
- **Backend Framework**: Laravel 11
- **Bahasa Pemrograman**: PHP 8.2, JavaScript
- **Styling**: Tailwind CSS (Custom UI dengan Dark/Light Mode)
- **Templating**: Blade Engine

### Library & Tools
- **Composer**: Dependency management
- **FontAwesome**: Ikon antarmuka
- **Google Fonts**: Tipografi (Roboto & Press Start 2P)
- **Vite**: Build tool untuk aset frontend

## 🎯 Tujuan & Fungsi Utama

Aplikasi ini dibuat untuk memecahkan masalah pemain Growtopia yang kesulitan memperkirakan biaya leveling. Tujuannya adalah:

✅ Memberikan perhitungan XP yang akurat dari level saat ini ke level target  
✅ Mengoptimalkan pembelian "Pack" (Supreme, Mega, Premium, Regular) agar efisien  
✅ Transparansi estimasi harga (dalam mata uang game: WL, DL, BGL) dan durasi pengerjaan  

## ✨ Fitur-fitur Utama

### 1. 🧮 Kalkulator Level Cerdas
- Input fleksibel untuk **Current Level** (Level Saat Ini) dan **Target Level**.
- Opsi input **Current XP** untuk hasil perhitungan yang presisi hingga digit terakhir.
- Validasi input otomatis untuk mencegah kesalahan data (Min level 1, Max 125).

### 2. 📦 Algoritma Rekomendasi Pack
- Sistem secara otomatis menghitung kombinasi item terbaik (Supreme Pack, Mega Pack, dll) yang harus dibeli pemain.
- **Faster Method**: Opsi toggle untuk memprioritaskan metode tercepat menggunakan pack level tinggi.

### 3. 💰 Estimasi Biaya & Waktu Real-time
- Konversi otomatis total harga ke satuan mata uang game (World Lock, Diamond Lock, Blue Gem Lock) dengan visualisasi sprite.
- Kalkulasi estimasi waktu pengerjaan (Jam & Menit) berdasarkan jumlah pack.

### 4. 🌗 Tampilan Responsif & Tema
- **Dark Mode & Light Mode**: Dukungan tema visual yang dapat diganti sesuai kenyamanan mata pengguna.
- Efek visual interaktif (Glow effect, Card hover 3D) menggunakan CSS modern.
- Desain responsif yang optimal untuk Desktop dan Mobile.

### 5. 🎵 Pemutar Musik Latar
- Fitur pemutar audio terintegrasi dengan kontrol volume dan tombol play/pause.
- Menambah pengalaman pengguna (UX) yang imersif saat menggunakan kalkulator.

### 6. 🔐 Sistem Autentikasi & Role
- Fitur Login dan Register untuk pengguna.
- Integrasi Dashboard Admin (berdasarkan struktur controller) untuk mengelola layanan.
- Tombol akses cepat ke komunitas Discord.

## 📋 Cara Menggunakan Aplikasi

### 1️⃣ Akses Website
Buka halaman utama SEWALEVEL. Pengguna akan disambut dengan antarmuka kalkulator.

### 2️⃣ Masukkan Data Level
- Isi kolom **Current Level** (contoh: 50).
- (Opsional) Isi **Current XP** jika ingin akurasi tinggi.
- Isi **Target Level** yang diinginkan (contoh: 125).

### 3️⃣ Lihat Hasil Perhitungan
Sistem akan langsung menampilkan:
- Total XP yang dibutuhkan.
- Daftar belanja (Rekomendasi Pack).
- Total harga dan durasi.

### 4️⃣ Kustomisasi
- Aktifkan tombol **"Faster Method"** jika ingin hasil lebih cepat (mempengaruhi rekomendasi pack).
- Gunakan toggle tema di navigasi atas untuk mengubah tampilan gelap/terang.

## 🛠️ Developer Notes

> **Catatan Pengembangan:**
{: .prompt-info }

- **Logika Perhitungan**: Menggunakan rumus progresi level Growtopia `50 * (level^2 + 2)` untuk menentukan base XP.
- **Frontend Logic**: Sebagian besar logika interaktif (perhitungan instan saat mengetik) ditangani oleh Vanilla JavaScript di sisi klien untuk performa yang cepat tanpa reload halaman.
- **Asset Management**: Menggunakan sprite sheet untuk ikon mata uang (WL/DL/BGL) guna menghemat request HTTP.

## 💡 Pembelajaran & Tantangan

Dalam pengembangan proyek ini, fokus utama adalah:

- **Algoritma Optimasi**: Membuat logika loop yang efisien untuk menentukan kombinasi pack termurah vs tercepat.
- **UI/UX Design**: Menciptakan antarmuka yang "gaming-friendly" dengan efek neon dan font pixel art, namun tetap bersih dan mudah digunakan.
- **Laravel 11**: Implementasi struktur folder dan fitur terbaru dari framework Laravel versi 11.

## 🔗 Source Code

Proyek ini bersifat open-source dan dapat dikembangkan lebih lanjut.
