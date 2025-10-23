---
title: "Pengantar Unit Testing: Kunci Coding Bebas Bug"
date: 2025-10-22 14:58:39 +0800
categories: [Software Testing and Quality Assurance]
tags: [Unit Testing, TDD, AAA Pattern, JUnit, Pytest, Code Quality]
image: /assets/img/k5.png
---

# Unit Testing: Fondasi Pengujian Perangkat Lunak

Unit testing adalah salah satu jenis pengujian perangkat lunak (*software*) yang berfokus pada pengujian unit-unit terkecil dalam sebuah sistem perangkat lunak. Unit testing umumnya merupakan pengujian paling awal yang dilakukan oleh *developer* sebelum pengujian lain, seperti *integration test* atau *end-to-end test*.

Secara hirarki pengujian, *unit testing* berada di dasar piramida, menjadikannya pengujian yang paling cepat (*faster*) dan paling murah (*cheaper*) dibandingkan *Integration* dan *E2E*.

---

## Pentingnya Unit Testing

Unit testing membantu memastikan keandalan, kualitas, dan kemudahan pemeliharaan kode yang kita tulis.

1.  **Mendeteksi Bug Lebih Awal**: Mengidentifikasi *bug* di tahap awal pengembangan.
2.  **Menghemat Waktu dan Biaya**: Lebih murah untuk memperbaiki *bug* di tahap unit testing daripada di tahap akhir.
3.  **Mempermudah Perubahan dan Refactoring**: Memberikan jaring pengaman saat kode diubah atau diperbaiki.
4.  **Memberikan Dokumentasi Kode yang Hidup**: Test case berfungsi sebagai contoh penggunaan yang jelas untuk fungsionalitas kode.
5.  **Meningkatkan Kualitas Kode**: Mendorong penulisan kode yang lebih modular dan mudah diuji.
6.  **Meningkatkan Kepercayaan Diri**: Meningkatkan keyakinan *developer* saat melakukan perubahan kode.

---

## Pola Dasar: Arrange, Act, Assert (AAA)

Pendekatan populer dalam penulisan *unit test* yang membagi setiap tes menjadi tiga bagian utama:

1.  **ARRANGE**: Menyiapkan kondisi awal tes (*Setup the code to test*).
2.  **ACT**: Menjalankan fungsi atau metode yang akan diuji (*Perform the action you want to test*).
3.  **ASSERT**: Memverifikasi bahwa hasil dari tindakan yang dilakukan sesuai dengan ekspektasi (*Check if the result matches your expectation*).

---

## Framework Unit Testing Populer

Tiga *framework* paling populer di ekosistemnya masing-masing:

| Framework | Bahasa | Kapan Digunakan | Keunggulan |
| :--- | :--- | :--- | :--- |
| **JUNIT 5** | Java | Bekerja dengan Java atau bahasa berbasis JVM (Kotlin, Scala). | Integrasi Penuh, Ekosistem yang Matang, Struktur Berbasis Anotasi. |
| **JEST** | JavaScript | Menggunakan React, Node.js, TypeScript, atau *framework frontend* modern. | Konfigurasi Minimal (*Zero-Config*), *Batteries-Included*, Fitur *Snapshot Testing*. |
| **PYTEST** | Python | Proyek Python apapun (skrip sederhana, aplikasi web, *data science*). | Sintaks Sederhana & *Boilerplate* Rendah, *Fixtures* yang Sangat Kuat, Pelaporan *Error* yang Detail. |

---

## Contoh Live Coding (Konsep)

**Studi Kasus 1: Bank Account (Junit 5/Java)** 
* **Test: `testDeposit`**:
    * *Act*: `account.deposit(100);` 
    * *Assert*: Memastikan saldo saat ini sama dengan 100 (`assertEquals(100, account.getBalance());`) 
* **Test: `testWithdrawInsufficientFunds`**:
    * *Assert*: Memastikan bahwa ketika penarikan lebih besar dari saldo, `IllegalArgumentException` terlempar (`assertThrows(IllegalArgumentException.class, ...)` ) dan pesan error sesuai.

**Studi Kasus 2: Shopping Cart (Pytest/Python)** 
* **Test: `test_add_overflow`**:
    * *Act*: Mencoba menambahkan item melebihi batas maksimum 5.
    * *Assert*: Memastikan `OverflowError` terlempar (`pytest.raises(OverflowError):`).