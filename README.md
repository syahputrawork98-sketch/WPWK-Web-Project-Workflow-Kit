# WebPWK — Web Project Workflow Kit

WebPWK adalah template workflow untuk project web yang dikelola dengan mengintegrasikan ChatGPT, Gemini, Anti-Gravity IDE, dan GitHub sebagai Source of Truth. 

## Struktur Repository

Repository ini menggunakan struktur dokumentasi terpusat di dalam folder `docs/` untuk mengelola workflow, riwayat, dan panduan.

- `docs/project/` - Dokumentasi utama project, onboarding, dan riwayat.
- `docs/frontend/` - Dokumentasi khusus area frontend.
- `docs/backend/` - Dokumentasi khusus area backend.
- `docs/database/` - Dokumentasi khusus area database.
- `docs/deployment/` - Dokumentasi khusus area deployment.

## Prinsip Utama

1. **GitHub sebagai Source of Truth**: Semua perubahan yang diakui hanya yang sudah masuk ke GitHub.
2. **Pemisahan Peran**:
   - **User**: Owner project, pengambil keputusan final, satu-satunya yang boleh commit/push.
   - **Roomchat 00**: Manager Utama di ChatGPT.com.
   - **Roomchat 01**: Reviewer / Auditor.
   - **Gemini Anti-Gravity**: Eksekutor teknis di Anti-Gravity IDE.
3. **Batch System**: Pengerjaan dibagi menjadi Feature Batch (FXX) dan Execution Batch.

## Cara Menggunakan Template Ini

1. Clone repository ini untuk memulai project web baru.
2. Setup ChatGPT Project dengan panduan di `docs/project/onboarding/CHATGPT_PROJECT_INSTRUCTIONS.md`.
3. Mulai inisiasi Room 00 dan Room 01 sesuai prompt yang tersedia.
4. Update `CURRENT_STATUS.md` untuk mencerminkan project baru.
5. Jalankan Feature Batch pertama.

## Status Awal Project

Project WebPWK saat ini sedang dalam tahap inisialisasi workflow foundation (Batch F00). Detail status dapat dilihat di `docs/project/history/CURRENT_STATUS.md`.