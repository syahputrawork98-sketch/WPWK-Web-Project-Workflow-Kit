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

## Safety Rules
- Jangan menyimpan credential/secret di repository (gunakan file `.env.example` sebagai panduan).
- Jangan men-generate kode ekstensif di luar scope instruksi.
- Eksekutor dilarang melakukan `git commit` dan `git push`.
