# WPWK — Web Project Workflow Kit

WPWK (Web Project Workflow Kit) adalah template arsitektur dan workflow untuk pengembangan project web yang dikelola dengan mengintegrasikan ChatGPT, Gemini, Anti-Gravity IDE, dan GitHub sebagai Source of Truth.

> **PENTING**: Repositori ini sekarang mendukung dua alur (Mode) utama: **Greenfield Mode** (pembuatan dari nol) dan **Existing Mode** (adopsi project berjalan). Silakan baca file `START_HERE.md` sebelum memulai.

## Struktur Repository
Repositori ini disusun agar terstruktur dan aman saat bekerja sama dengan eksekutor AI:

- `START_HERE.md` - Pintu masuk utama bagi user dan AI untuk memilih mode.
- `WK-Web-Greenfield/` - Workspace untuk mode Greenfield. Di sinilah letak folder `client/` dan `server/` jika Anda memulai aplikasi dari nol.
- `WK-Web-Existing/` - Workspace untuk mode Existing Project. Digunakan jika Anda ingin menempatkan kode project lama Anda untuk mulai diaudit dan dikontrol.
- `docs/` - Pusat kendali dokumentasi dan riwayat.
  - `docs/project/` - Dokumentasi utama project, onboarding, dan aturan workflow.
  - `docs/history/` - Tracker fitur (`CURRENT_STATUS.md`, `FEATURE_HISTORY.md`) dan roadmap.
  - `docs/frontend/` - Area dokumentasi khusus frontend.
  - `docs/backend/` - Area dokumentasi khusus backend.
  - `docs/database/` - Area dokumentasi khusus database.
  - `docs/deployment/` - Area dokumentasi khusus infrastruktur.

## Prinsip Utama
1. **GitHub sebagai Source of Truth**: Semua perubahan diakui hanya yang sudah ter-push ke GitHub.
2. **Pemisahan Peran**:
   - **User**: Pengambil keputusan, reviewer akhir, pelaku commit/push.
   - **Roomchat 00**: Manager Utama (ChatGPT).
   - **Roomchat 01**: Reviewer/Auditor (ChatGPT).
   - **Gemini**: Eksekutor teknis di workspace (Anti-Gravity IDE).
3. **Dual Mode Adoption**: Mendukung pembuatan dari nol (Greenfield) maupun merapikan project lama (Existing).
4. **Batch Gate System**: Pekerjaan dibagi dalam Batch Terkontrol (FXX).

## Status Awal Project
Project WPWK ini berstatus inisialisasi workflow foundation. Detail tracker ada di `docs/history/CURRENT_STATUS.md`.