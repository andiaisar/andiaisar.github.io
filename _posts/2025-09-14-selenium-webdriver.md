---
title: "Pengantar Selenium WebDriver: Automasi Pengujian Web"
date: 2025-10-22 15:05:01 +0800
categories: [Software Testing and Quality Assurance]
tags: [Selenium, WebDriver, Automation Testing, Python, Web Testing]
image: /assets/img/k7.png

---
# Pengantar Selenium WebDriver

Selenium adalah *framework open-source* untuk automasi *browser*. Alat ini digunakan untuk menguji aplikasi web dengan berbagai bahasa pemrograman.

---

## Apa itu Selenium WebDriver?

* **Komponen Inti**: *WebDriver* adalah komponen inti dari Selenium.
* **Fungsi**: Berfungsi sebagai penghubung antara kode kita dengan *browser*.
* **Tugas**: Mengontrol *browser* untuk melakukan aksi seperti klik, *input* teks, navigasi, dan validasi.
* **Dukungan**: Mendukung banyak *browser* seperti Chrome, Firefox, Edge, dan Safari.

### Alur Kerja (Workflow) Selenium WebDriver

1.  **Test Scripts**: Kode pengujian ditulis dalam bahasa pemrograman yang didukung (misalnya Java, Python, C#, PHP).
2.  **WebDriver**: Menerima perintah dari *Test Scripts*.
3.  **Browsers**: *WebDriver* menjalankan perintah pada *browser* yang ditargetkan.

---

## Mengapa Harus Menggunakan Selenium?

Selenium menjadi pilihan populer untuk automasi pengujian web karena beberapa keunggulan:

* **Sifat**: *Open-source* dan gratis.
* **Dukungan Bahasa**: Mendukung banyak bahasa pemrograman, termasuk Python, Java, C#, dan JS.
* **Dukungan Platform**: *Multi-platform* (Windows, macOS, Linux).
* **Integrasi**: Dapat diintegrasikan dengan *framework testing* seperti Pytest, JUnit, atau TestNG.
* **Komunitas**: Memiliki komunitas besar dan dokumentasi yang lengkap.

---

## Contoh Skenario dan Test Case

Presentasi ini menampilkan contoh pengujian untuk aplikasi web SauceDemo:

### Test Scenario
* **TS-001**: Login berhasil di halaman SauceDemo.
* **TS-002**: Login gagal dengan kredensial salah.
* **TS-003**: Menambahkan produk ke keranjang (*cart*).

### Test Case (Contoh)

| ID | Deskripsi | Steps | Expected Result |
| :--- | :--- | :--- | :--- |
| **TC-001** | Login sukses | Input `standard_user` & `secret_sauce` , Klik Login  | Masuk ke *inventory*  |
| **TC-002** | Login gagal | Input *user* salah, Klik Login  | Muncul pesan *error*  |
| **TC-003** | Tambah produk ke *car* | Login sukses → Klik "Add to cart"  | *Cart* bertambah 1  |