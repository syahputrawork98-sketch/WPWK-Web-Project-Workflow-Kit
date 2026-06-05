# Working System

Sistem kerja WebPWK dirancang untuk keamanan, konsistensi, dan keteraturan.

## Prinsip Utama
1. **GitHub sebagai Source of Truth**.
2. **Tidak ada AI yang boleh commit/push**.
3. **Review sebelum dan sesudah eksekusi**.

## Peran
- **User**: Pemilik project. Menyetujui rencana, memindahkan instruksi antar room, melakukan commit dan push.
- **Roomchat 00**: Manager Utama (ChatGPT). Merencanakan fitur, membuat instruksi untuk Gemini.
- **Roomchat 01**: Reviewer (ChatGPT). Mengaudit rencana (Batch Gate) dan hasil eksekusi.
- **Gemini Anti-Gravity**: Eksekutor. Menulis kode/dokumentasi di workspace lokal Anti-Gravity IDE.
- **Anti-Gravity IDE**: Workspace nyata tempat eksekusi dan validasi dilakukan.

## Pre-Batch Mode vs Batch Execution
- **Pre-Batch Mode**: Fase perencanaan di Room 00 dan audit di Room 01. Belum ada kode yang ditulis.
- **Batch Execution**: Fase pengerjaan nyata di Anti-Gravity IDE oleh Gemini.

## Ukuran Batch
- **Small Batch**: 1–3 file, satu area, risiko rendah.
- **Medium Batch**: 4–8 file, satu sampai dua area, risiko sedang.
- **Large Batch**: Lebih dari 8 file. Wajib dipecah menjadi batch yang lebih kecil.

## Scope Area
Pembagian area kerja dalam project:
- `docs`
- `frontend`
- `backend`
- `database`
- `deployment`
- `content`
- `design`

## Batch Gate
Mekanisme validasi (checkpoint) sebelum instruksi dari Room 00 dieksekusi oleh Gemini. Harus disetujui (APPROVED) oleh Room 01 (atau User).

## Feature Batch Naming Policy
- `F00` = workflow/setup awal
- `F01` = project foundation
- `F02` = frontend core
- `F03` = backend/API
- `F04` = database
- `F05` = deployment/domain
- `FXX-CP` = checkpoint dokumentasi

## Definition of Done
Setiap batch dianggap selesai jika:
1. Kriteria penerimaan dari instruksi terpenuhi.
2. Tidak ada error/bug yang diketahui.
3. Dokumentasi (terutama `CURRENT_STATUS.md` dan feature file) sudah diperbarui.
4. Laporan eksekutor sudah diserahkan.
5. User telah me-review, commit, dan push ke repository.

## Adaptasi Template dan Kedalaman Dokumentasi

WebPWK adalah template yang harus disesuaikan dengan kebutuhan project turunan. File seperti `README.md` dan `FEATURES.md` di project turunan wajib diubah untuk mencerminkan project nyata.

### Aturan Adaptasi README.md
README project turunan sebaiknya berisi:
- Nama project dan deskripsi singkat
- Kenapa project dibuat & target pengguna
- Fitur utama & teknologi yang digunakan
- Struktur folder & cara menjalankan local development
- Status project & catatan deployment jika ada

### Aturan Adaptasi FEATURES.md
FEATURES project turunan sebaiknya berisi daftar fitur nyata:
- Fitur public user, customer/login, admin
- Fitur backend/API & database
- Fitur deployment
- Status fitur: Planned, In Progress, Completed, Partial, Blocked, HOLD

### Jenis Project Turunan (Project Type)
1. **Static / Landing Page**: Cocok untuk web tanpa backend.
2. **Frontend-only Dynamic Website**: Cocok untuk web dinamis dengan API eksternal/BaaS.
3. **Fullstack Single Role**: Cocok untuk aplikasi dengan satu jenis user (misal CMS admin saja atau user saja).
4. **Fullstack Multi Role**: Cocok untuk aplikasi dengan beberapa jenis hak akses.
5. **Fullstack Multi Role + Admin CMS**: Cocok untuk sistem kompleks dengan manajemen penuh.

### Kedalaman Dokumentasi (Documentation Depth)
Kedalaman dokumentasi mengikuti kompleksitas project:
- **Static / Landing Page**: README wajib disesuaikan. FEATURES berisi fitur section/halaman. Frontend docs ringan. Backend/Database docs tidak wajib.
- **Frontend-only Dynamic**: README disesuaikan. FEATURES berisi fitur web. Frontend docs wajib. Backend/Database docs hanya jika ada integrasi eksternal.
- **Fullstack Single Role**: README disesuaikan. FEATURES berisi fitur front & back. Frontend & Backend docs wajib. Database docs wajib jika ada. Role matrix tidak wajib (cukup role utama).
- **Fullstack Multi Role**: README disesuaikan. FEATURES berisi fitur per role. Semua docs wajib. Role matrix, API contract, dan database ownership wajib.
- **Fullstack Multi Role + Admin CMS**: Semua dokumentasi wajib. Role & permission matrix, API contract, database ownership, dan admin feature tracker wajib. Checkpoint dokumentasi lebih sering.

### Documentation Debt / Docs Later
Kerja teknis boleh mendahului dokumentasi detail, tetapi harus dicatat sebagai **Documentation Debt**.
Gunakan Documentation Debt ketika:
- Client sudah berubah tapi docs/frontend belum diupdate.
- Server/backend sudah berubah tapi docs/backend belum diupdate.
- Database/schema sudah berubah tapi docs/database belum diupdate.
- README/FEATURES belum disesuaikan setelah project berubah.

Documentation Debt wajib diselesaikan melalui eksekusi **FXX-CP — Documentation Checkpoint**.

## Safety Rules
- Jangan menyimpan credential/secret di repository (gunakan file `.env.example` sebagai panduan).
- Jangan men-generate kode ekstensif di luar scope instruksi.
- Eksekutor dilarang melakukan `git commit` dan `git push`.
