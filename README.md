⚠️ PERINGATAN ETIKA & KEAMANAN
1. SELURUH KODE RENTAN DISINI HANYA UNTUK TUJUAN PENDIDIKAN DAN PRAKTIKUM
2. Repositori ini dibuat sepenuhnya untuk tujuan pembelajaran, dan untuk memenuhi UJIAN TENGAH SEMESTER, Mata Kuliah : Keamanan Data dan Informasi.
3. Dilarang Keras menjalankan kode rentan di lingkungan server publik atau non-laboratorium.

# PERBANDINGAN RENTAN vs AMAN
1. Versi Rentan (Vulnerable)
- Prinsip Inti : "Trust by Default" (Percaya secara default).
Metode Implementasi:
- SQLi: Menggunakan String Concatenation (penggabungan langsung input ke query).
- XSS: Menampilkan (echo) input pengguna RAW ke halaman HTML tanpa proses.
- Upload: Menerima file apa pun (termasuk .php) tanpa validasi atau penggantian nama.
- Dampak: Memungkinkan serangan SQL Injection, Cross-Site Scripting (XSS), dan Remote Code Execution (RCE) melalui file yang diunggah.
  
2. Versi Aman (Safe)
- Prinsip Inti: "Validate, Sanitize, and Never Trust" (Validasi, Saring, dan Jangan Pernah Percaya).
- Sikap terhadap Input: Input pengguna selalu diperlakukan sebagai data yang tidak tepercaya dan berpotensi berbahaya.
Metode Implementasi
- SQLi: Menggunakan Prepared Statements (Parameterized Queries), memastikan input hanya ditafsirkan sebagai data.
- XSS: Menerapkan Output Escaping (misalnya htmlspecialchars()) pada semua data sebelum ditampilkan ke browser.
- Upload: Melakukan Validasi ketat (ekstensi, MIME type, ukuran) di sisi server dan menggunakan Penggantian Nama (hashing) pada file.
- Dampak: Memblokir serangan yang memanfaatkan penyalahgunaan data input, menjaga integritas query dan output halaman.

# Topik yang Dianalisis 
Praktikum ini mencakup empat materi :
1. SQL Injection (SQLi)
Fokus: Eksploitasi melalui string concatenation dan mitigasi menggunakan Prepared Statements.
2. Cross-Site Scripting (XSS)
Fokus: Demonstrasi Stored XSS dan pencegahan melalui teknik Output Encoding.
3. Kerentanan File Upload
Fokus: Eksploitasi Remote Code Execution (RCE) melalui upload berkas berbahaya dan mitigasi melalui White-listing dan validasi MIME Type.
4. Broken Access Control (BAC) / Insecure Direct Object Reference (IDOR)
Fokus: Eksploitasi akses data pengguna lain dengan manipulasi ID objek, dan pencegahan melalui Ownership Check di setiap permintaan.
