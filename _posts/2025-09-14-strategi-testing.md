---
title: "Strategi dan Klasifikasi Software Testing"
date: 2023-10-22 11:23:54
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/img/k1.png
---

# Strategi Testing Perangkat Lunak

*Testing* adalah proses penting dalam *Software Development Life Cycle* (SDLC) untuk menemukan cacat (*bug*) dan memastikan perangkat lunak memenuhi persyaratan fungsional dan non-fungsional.

---

## Tujuan Utama Testing

- Menemukan kesalahan atau cacat (*bug*) dalam sistem sebelum rilis.
- Melakukan **Verifikasi dan Validasi** terhadap persyaratan.
- Mengurangi resiko kegagalan dan meningkatkan kepercayaan *stakeholder*.
- Menjamin keamanan dan meningkatkan Pengalaman Pengguna.

---

## Software Testing Life Cycle (STLC) — Fase Kunci

1.  **Test Planning**: Membuat strategi, mengidentifikasi lingkungan, memperkirakan waktu dan biaya, serta menyusun rencana testing.
2.  **Test Design**: Mengidentifikasi dan menulis *test case*, menyiapkan data dan skenario pengujian, serta memperbarui **Requirement Traceability Matrix**.
3.  **Test Eksekusi**: Melaksanakan pengujian (Unit, Integration, System, Acceptance testing).
4.  **Pelaporan & Analisis**: Merangkumm hasil, mengidentifikasi *bug* dan isu teknis, mengevaluasi kualitas, dan memberikan rekomendasi perbaikan.

---

## Klasifikasi Software Testing Berdasarkan Abstraksi

- **Unit Testing**: Menguji komponen kode terkecil (fungsi/metode) secara terpisah.
- **Integration Testing**: Menguji interaksi dan komunikasi antar unit atau modul.
- **System Testing**: Menguji sistem secara keseluruhan (holistik) terhadap semua persyaratan fungsional dan non-fungsional.
- **Acceptance Testing**: Pengujian final dari perspektif pengguna akhir (*end-user*) atau klien untuk validasi dan persetujuan.

---

## Klasifikasi Lainnya

### Berdasarkan Fungsi
- **Functional Testing**: Memverifikasi fitur sesuai spesifikasi (misalnya, verifikasi fungsi login, validasi transaksi pembayaran).
- **Non-Fungsional Testing**: Menguji aspek performa, keamanan, dan reliabilitas (bagaimana sistem bekerja), bukan fungsi spesifiknya.

### Berdasarkan Domain (Contoh Non-Fungsional)
- **Performance Testing**: Menguji kinerja dari segi kecepatan dan stabilitas di bawah beban tertentu.
- **Security Testing**: Mengidentifikasi celah keamanan (misalnya, kerentanan terhadap SQL injection atau XSS).
- **Usability Testing**: Mengevaluasi kemudahan penggunaan sistem oleh pengguna akhir.

### Berdasarkan Struktur
- **Black-Box Testing**: Pengujian tanpa mengetahui struktur internal/kode program. Fokus pada input dan output sistem.
- **White-Box Testing**: Pengujian dengan mengetahui struktur internal dan kode program. Fokus pada alur logika dan *coverage* kode.

---

## Kesimpulan

**Testing** adalah tahapan yang sangat penting dalam pengembangan *software* untuk menghasilkan *software* yang berkualitas baik, bebas dari *bugs*, dan disukai oleh pengguna.

---

*Rujukan Singkat*: Materi Presentasi Kelompok 1, Sistem Informasi 2023.