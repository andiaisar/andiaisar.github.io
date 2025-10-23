---
title: "Testing Plan (Rencana Pengujian) - Komponen dan Tujuan"
date: 2025-10-22 14:51:39 +0800
categories: [Software Testing and Quality Assurance]
tags: [Testing Plan, Test Strategy, IEEE 829, Software Testing]
image: /assets/img/k3.png
---

# Testing Plan (Rencana Pengujian): Acuan Resmi Proses Pengujian

*Testing Plan* (Rencana Pengujian) adalah dokumen panduan resmi yang menjelaskan bagaimana proses pengujian perangkat lunak akan dilakukan. Dokumen ini berfungsi sebagai acuan resmi bagi tim penguji agar kegiatan pengujian lebih terarah dan konsisten.

---

## Tujuan Testing Plan
Rencana Pengujian bertujuan untuk:
* Menyediakan gambaran yang jelas tentang apa saja yang akan diuji dan bagaimana cara mengujinya.
* Memastikan proses pengujian dapat menemukan sebanyak mungkin kesalahan.
* Menjamin perangkat lunak mencapai kualitas yang dapat diterima pengguna.
* Mengoptimalkan penggunaan waktu, biaya, dan tenaga.
* Memberikan dokumentasi yang bisa dijadikan referensi dan evaluasi pada proyek berikutnya.

---

## Komponen Utama Testing Plan (Berdasarkan IEEE 829-1988)

Standar IEEE 829-1988 mendefinisikan berbagai komponen yang harus ada dalam sebuah dokumen *test plan*.

### I. Identifikasi dan Referensi
1.  **Test Plan Identifier** : Penanda unik (kode/nomor versi) untuk memudahkan pengelolaan dokumen dan revisi.
2.  **References** : Daftar dokumen, standar, atau sumber yang mendukung dan menjamin bahwa *test plan* konsisten dengan dokumen utama proyek.
3.  **Introduction** : Bagian pembuka yang menjelaskan tujuan, ruang lingkup, dan fokus pengujian (*executive summary*).
4.  **Approvals** : Memastikan semua pihak berkepentingan (Manajer Proyek/Pengujian) telah menyetujui ruang lingkup, jadwal, dan sumber daya.

### II. Ruang Lingkup Pengujian
1.  **Test Items** : Komponen, fitur, modul, atau artefak perangkat lunak yang akan diuji (apa saja yang masuk dalam ruang lingkup).
2.  **Features to be Tested** : Fitur atau fungsi yang akan diuji dari sudut pandang pengguna, fokus pada deskripsi penggunaan dan tingkat risiko.
3.  **Features not to be Tested** : Daftar fitur yang dikecualikan dari proses pengujian beserta alasannya (misalnya, fitur sudah stabil atau tidak direncanakan untuk dirilis).
4.  **Software Risk Issues** : Potensi risiko yang dapat muncul dari perangkat lunak maupun proses pengujiannya, yang memerlukan rencana pencegahan dan penanganan.

### III. Strategi dan Kriteria
1.  **Approach** : Mendefinisikan strategi umum yang akan digunakan. Ini mencakup:
    * **Tipe Pengujian**: *Unit, integration, system*, atau *acceptance testing*.
    * **Teknik Pengujian**: *Black-box, white-box,* atau *gray-box*.
    * **Metode Pengujian**: Manual atau otomatis.
2.  **Item Pass/Fail Criteria** : Standar yang jelas dan terukur untuk menentukan apakah suatu *test item* (fitur/modul/test case) telah lulus atau gagal.
    * **Pass Criteria**: Semua *test case* utama berjalan sesuai harapan, tidak ada *bug* kritis ditemukan.
    * **Fail Criteria**: Satu atau lebih *test case* gagal, ditemukan *defect* kritis atau mayor yang menghambat fungsionalitas inti.
3.  **Suspension Criteria and Resumption Requirements**:
    * **Suspension Criteria**: Kondisi di mana pengujian harus dihentikan sementara (misalnya, ditemukan masalah serius yang membuat pengujian tidak produktif).
    * **Resumption Requirements**: Kondisi yang harus dipenuhi sebelum pengujian dapat dilanjutkan kembali (misalnya, masalah telah diperbaiki).

### IV. Sumber Daya dan Jadwal
1.  **Environmental Needs** : Spesifikasi dan konfigurasi lingkungan yang diperlukan agar pengujian dapat dijalankan (meliputi *hardware, software*, data uji, akses, dan pengaturan jaringan).
2.  **Staffing and Training Needs** : Kebutuhan personel (Manajer, *tester*, *developer*) dan kompetensi yang dibutuhkan. Rencana pelatihan singkat memastikan tim siap.
3.  **Responsibilities** : Pembagian tanggung jawab yang jelas untuk koordinasi, penulisan dan eksekusi *test case*, verifikasi perbaikan, dan penetapan jalur eskalasi.
4.  **Schedule** : Garis waktu mulai pengujian, periode eksekusi, sesi *retest*, hingga *sign-off* rilis, beserta *milestone* penting lainnya.

### V. Hasil dan Penutup
1.  **Test Deliverables** : Dokumen, artefak, dan hasil nyata yang dihasilkan selama proses pengujian (misalnya: *test plan, test case, test summary*).
2.  **Remaining Test Tasks** : Daftar pekerjaan pengujian yang masih belum selesai saat laporan status dibuat.
3.  **Glossary** : Menyediakan daftar istilah teknis atau singkatan yang digunakan dalam dokumen beserta definisinya, untuk membantu semua pihak memiliki pemahaman yang sama.

---

*Brief Reference*: Bahan presentasi kelompok 3 (Testing Plan).