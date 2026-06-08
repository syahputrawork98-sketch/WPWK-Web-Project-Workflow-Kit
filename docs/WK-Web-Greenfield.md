# WK-Web-Greenfield

Repositori/Workspace **WK-Web-Greenfield** digunakan secara eksklusif untuk membangun project web yang benar-benar baru dari nol (tanpa *codebase* sebelumnya).

## Karakteristik Mode Greenfield
- **Codebase Awal**: Kosong atau sekadar template *boilerplate*.
- **Fokus Utama**: Menyiapkan arsitektur dasar, mengonfigurasi *environment*, dan membangun fitur tahap demi tahap (F01, F02, dst).
- **Pendekatan AI**: AI diinstruksikan untuk membuat file baru, struktur folder, dan melakukan *scaffolding* project.

## Alur Kerja (Workflow)
1. **Inisiasi**: Gunakan `npx` atau *starter kit* pilihan di dalam folder `WK-Web-Greenfield`.
2. **Dokumentasi Dasar**: Setup `docs/history/CURRENT_STATUS.md` dan pastikan catatan fitur (FXX) berjalan sejak baris kode pertama ditulis.
3. **Validasi (Batch Gate)**: Sebelum meminta eksekutor (Gemini) menulis kode, pastikan Roomchat 00 dan 01 telah menyepakati langkah-langkah implementasinya.

## Aturan Penting
- Jangan pernah menjalankan *commit* atau *push* dari sisi AI. Hanya **User** yang memiliki hak penuh terhadap kontrol versi.
- Selalu patuhi standar penulisan dokumentasi sesuai area masing-masing (`frontend`, `backend`, `database`, `deployment`).
