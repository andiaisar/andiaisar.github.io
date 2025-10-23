---
title: "Test Scenario, Test Case, dan Bug Report: Elemen Kunci Pengujian"
date: 2025-10-22 14:55:01 +0800
categories: [Software Testing and Quality Assurance]
tags: [Test Scenario, Test Case, Bug Report, Severity, Priority]
image: /assets/img/k4.png
---

# Test Scenario, Test Case, dan Bug Report

*Test scenario, test case*, dan *bug report* adalah tiga elemen penting yang saling melengkapi dalam proses pengujian perangkat lunak untuk memastikan aplikasi berjalan sesuai harapan dan bebas dari kesalahan.

---

## 1. Test Scenario

*Test Scenario* adalah gambaran umum apa yang diuji untuk memastikan fungsi aplikasi sesuai kebutuhan. Ini menjawab pertanyaan: **"APA YANG HARUS DIUJI?"**.

### Template Sederhana Test Scenario
* **ID Scenario**: Nomor unik skenario.
* **Deskripsi**: Ringkasan skenario pengujian.
* **Modul/Fitur**: Modul atau fitur yang diuji.

### Contoh (Aplikasi BMI)
| ID Scenario | Deskripsi | Modul/Fitur yang diuji |
| :--- | :--- | :--- |
| **TS001** | Periksa fungsi *slider input* | *Slider input* berat dan tinggi badan  |
| **TS002** | Periksa hasil perhitungan dan klasifikasi BMI | Perhitungan dan klasifikasi BMI  |
| **TS003** | Periksa fungsi penyimpanan *history* BMI | *History* BMI  |

---

## 2. Test Case

*Test Case* adalah langkah detail pengujian, termasuk *input*, proses, dan hasil yang diharapkan. Ini menjawab pertanyaan: **"BAGAIMANA MELAKUKAN PENGUJIAN?"**.

### Komponen Test Case
* **ID Test Case**: Nomor unik *test case*.
* **Deskripsi**: Ringkasan singkat tentang pengujian.
* **Precondition**: Kondisi awal sebelum pengujian.
* **Test Steps**: Langkah-langkah detail pengujian.
* **Test Data**: Data yang digunakan untuk pengujian.
* **Expected Result**: Hasil yang diharapkan sesuai *requirement*.
* **Actual Result**: Hasil aktual yang muncul setelah pengujian.
* **Status**: Lulus/Gagal (*Pass/Fail*).

### Contoh (Test Case untuk TS002 - Verifikasi Perhitungan)
| ID Test Case | Test Steps | Test Data | Expected Result |
| :--- | :--- | :--- | :--- |
| **TC003** | 1. Masukkan tinggi 170cm 2. Masukkan berat 65kg | Tinggi = 170, Berat = 65 | Hasil BMI seharusnya 22.49. |

---

## 3. Bug Report

*Bug Report* adalah laporan formal kesalahan/masalah pada sistem. Laporan ini berisi detail masalah, cara mereproduksi, dan hasil aktual.

### Klasifikasi Bug
#### A. Bug Severity (Ukuran Dampak pada Fungsi Software) 
1.  **Critical**: Menyebabkan kegagalan total pada sistem atau fungsionalitas utama. Aplikasi tidak dapat digunakan, atau data menjadi rusak.
2.  **Major (High)**: Menyebabkan fungsionalitas utama tidak bekerja dengan benar, tetapi tidak menyebabkan sistem *crash* total.
3.  **Minor (Medium)**: Tidak memengaruhi fungsionalitas utama, tetapi dapat menyebabkan ketidaknyamanan bagi pengguna.
4.  **Low**: Tidak mengakibatkan kerusakan pada sistem.

#### B. Bug Priority (Ukuran Urgensi Perbaikan) 
1.  **P1 - Urgent/Critical**: Paling mendesak untuk diperbaiki.
2.  **P2 - High**: Penting dan harus diperbaiki secepatnya karena memengaruhi banyak pengguna, tetapi tidak se-mendesak P1.
3.  **P3 - Medium**: Dapat diperbaiki di siklus rilis berikutnya, tidak memengaruhi fungsionalitas inti.
4.  **P4 - Low**: Minor atau kosmetik, bisa diperbaiki kapan saja.

### Contoh Format Bug Report
| Field | Detail (Contoh) |
| :--- | :--- |
| **Bug Title** | Perhitungan BMI salah saat input berat 60kg dan tinggi 170cm  |
| **Bug ID** | BMI-001  |
| **Step to reproduce** | Masukkan Berat = 60, Tinggi = 170, Klik tombol "Hitung"  |
| **Actual result** | Hasil BMI = 12.5  |
| **Expected result** | Hasil BMI seharusnya = 20.8  |
| **Severity** | Major (High)  |
| **Priority** | P2 - High  |

---

## Cara Terbaik Menghindari Bug

Cara terbaik untuk menghindari *bug* adalah dengan menerapkan praktik terbaik di seluruh siklus pengembangan, tidak hanya saat pengujian.

1.  **Pahami Persyaratan**: Pastikan semua persyaratan dipahami dengan jelas oleh seluruh tim.
2.  **Unit Testing**: Lakukan pengujian unit untuk mendeteksi *bug* di tahap awal pengembangan.
3.  **Code Review**: Minta pengembang lain meninjau kode untuk menemukan kesalahan.
4.  **Rencana Pengujian**: Buat *test plan* yang komprehensif.
5.  **Pengujian Otomatis**: Manfaatkan *automation testing* untuk deteksi *bug* yang lebih cepat.
6.  **Kolaborasi Tim**: Tingkatkan komunikasi dan kolaborasi antara pengembang dan penguji.