---
title: "API Testing: Pengujian Antarmuka Pemrograman Aplikasi"
date: 2025-10-22 15:02:05 +0800
categories: [Software Testing and Quality Assurance]
tags: [API Testing, Postman, SOAPUI, Request, Response]
image: /assets/img/k6.png
---

# API Testing: Memastikan Fungsionalitas Inti Sistem

**API Testing** adalah proses pengujian yang dilakukan pada *Application Programming Interface* (API) untuk memastikan bahwa API berfungsi sesuai dengan spesifikasi[cite: 181]. Pengujian ini memastikan API dapat menangani berbagai skenario dengan benar dan menghasilkan *output* yang benar ketika menerima *input* tertentu.

---

## Keunggulan (Pentingnya) API Testing

Pengujian API adalah pondasi penting bagi integrasi antar sistem yang lancar  dan memiliki beberapa keunggulan:

* **Keandalan Sistem**: Meningkatkan keandalan sistem dengan mendeteksi *bug* sejak awal.
* **Keamanan**: Menjamin keamanan API dari akses tidak sah dan potensi celah keamanan.
* **Performa**: Mengukur performa API di bawah beban untuk stabilitas aplikasi.
* **Akselerasi Pengembangan**: Mempercepat siklus pengembangan melalui otomatisasi pengujian.

---

## Anatomi Request dan Response API

### 1. Anatomi Request API
*Request* adalah permintaan yang dikirimkan dari klien ke server untuk mengakses atau memanipulasi data melalui API.

* **Method (HTTP Verb)**: Menentukan aksi yang ingin dilakukan, seperti `GET`, `POST`, `PUT`, atau `DELETE`.
* **URL (Uniform Resource Locator)**: Alamat dari *resource* yang ingin diakses atau dimodifikasi.

### 2. Anatomi Response API
*Response* adalah balasan yang diberikan oleh server setelah memproses *request*.

* **Status Code**: Kode numerik untuk menandakan hasil eksekusi, misalnya:
    * **200 (OK)** 
    * **404 (Not Found)** 
    * **401 (Unauthorized)** 

---

## Tools API Testing Populer

### 1. Postman
Postman adalah salah satu *tool* API *testing* yang populer karena *user-friendly* dan mendukung berbagai metode HTTP.

**Fitur Utama Postman:**
* Kirim *request* HTTP (`GET, POST, PUT, DELETE`, dll).
* Kelola *environment* dan *Variables*.
* *Testing* dan *Automation*.
* *Collection* dan Dokumentasi API.

### 2. SOAPUI
SOAPUI sangat kuat untuk **SOAP API** (yang berbasis XML) dan cocok untuk *enterprise testing* dengan skenario kompleks.

**Fitur Utama SOAPUI:**
* Mendukung **SOAP** dan **REST API**.
* Bisa membuat *functional testing, security testing*, dan *load testing*.
* Mendukung *data-driven testing* (import data dari Excel atau database).