# WK-Web-Existing

Repositori/Workspace **WK-Web-Existing** digunakan secara eksklusif untuk project web yang sudah memiliki *codebase* atau infrastruktur yang sedang berjalan, namun ingin diadopsi ke dalam sistem **WPWK**.

## Karakteristik Mode Existing
- **Codebase Awal**: Sudah terisi aplikasi (misal `client/` dan `server/` sudah beroperasi).
- **Fokus Utama**: Pemetaan (Mapping), Audit, Pembuatan Inventory Fitur, dan penyelarasan Dokumentasi tanpa mengganggu sistem yang sudah berjalan.
- **Pendekatan AI**: AI (Gemini) diinstruksikan dalam mode **Read-Only** pada tahap awal. AI dilarang keras mengubah, menghapus, atau meng-install dependensi apa pun tanpa *audit summary* yang lengkap.

## Alur Kerja (Workflow)
1. **Adoption Pre-Scan (Level 0)**: AI sekadar membaca struktur project, konfigurasi (*package.json*, env), dan dokumentasi lama yang ada. Tidak ada file yang dibuat atau diubah.
2. **Minimal Control Layer (Level 1)**: Menyiapkan `docs/history/CURRENT_STATUS.md` untuk melacak status adopsi.
3. **Documentation Mapping (Level 2)**: Menilai dokumen yang sudah ada (README lama, wiki) apakah akan dipertahankan, dihapus, atau ditulis ulang.
4. **Feature Inventory (Level 3)**: Mendaftarkan seluruh fitur yang sudah ada ke dalam status *Existing / Needs Review*. Jangan pernah berasumsi sebuah fitur "Completed" sebelum diverifikasi.
5. **Technical Batch (Level 4-5)**: Baru pada tahap ini kode aplikasi (`client` / `server`) boleh disesuaikan atau di-*refactor*.

## Aturan Penting
- **Jangan menimpa paksa!** Jika project lama tidak menggunakan pola folder standar (misalnya memakai `apps/web`), ikuti pola tersebut. Jangan memaksa membuat folder `client/` baru.
- Adopsi adalah proses progresif. Lakukan secara perlahan dari audit hingga kontrol penuh.
