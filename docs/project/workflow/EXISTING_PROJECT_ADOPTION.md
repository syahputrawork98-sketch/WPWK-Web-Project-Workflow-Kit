# Existing Project Documentation Adoption — WPWK

## Fungsi Dokumen
Dokumen ini digunakan saat WPWK diterapkan ke project yang sudah memiliki client/server atau codebase berjalan, tetapi dokumentasi, history, dan workflow kontrolnya belum rapi.

- WPWK tidak dipakai untuk menimpa project lama.
- WPWK dipakai sebagai documentation/control layer.
- Fokus awal adalah audit, mapping, dan dokumentasi.
- Client/server tidak boleh disentuh sebelum audit dan batch gate jelas.

## Kapan Digunakan
Gunakan panduan ini jika:
- project sudah memiliki client/
- project sudah memiliki server/
- project sudah memiliki package.json atau framework berjalan
- project sudah pernah deploy
- fitur utama sudah ada
- README/FEATURES/docs belum rapi
- project belum punya feature tracker
- project belum punya batch history
- user ingin mulai mengontrol project lama memakai cara kerja WPWK

## Greenfield vs Existing Project

| Aspek | Greenfield Project | Existing Project |
|---|---|---|
| Codebase | Belum ada / masih kosong | Sudah ada client/server |
| README | Dibuat dari awal | Diaudit dan diadaptasi |
| FEATURES | Dirancang dari awal | Direkonstruksi dari fitur nyata |
| client/server | Bisa dibuat dari template | Tidak boleh disentuh dulu |
| Batch awal | Project starter | Existing project audit |
| Risiko | Lebih rendah | Lebih tinggi karena ada sistem berjalan |

## Prinsip Utama Existing Adoption
- Jangan menyentuh client/server di batch awal.
- Jangan refactor hanya demi menyesuaikan WPWK.
- Jangan menghapus dokumentasi lama tanpa mapping.
- Jangan menimpa README/FEATURES sebelum isi lama dipahami.
- Jangan menganggap fitur existing otomatis Completed.
- Gunakan status Existing / Needs Review jika fitur sudah ada tapi belum divalidasi.
- Tambahkan `docs/project/` sebagai control layer.
- Build up dokumentasi pelan-pelan berdasarkan kondisi nyata project.

## Existing Project Adoption Flow
1. Adoption Pre-Scan
2. Existing Project Audit
3. Documentation Mapping
4. Feature Inventory
5. Risk Classification
6. WPWK Docs Injection
7. Feature Tracker Reconstruction
8. First Controlled Batch

## 1. Adoption Pre-Scan
Tahap ini hanya membaca struktur project.

Yang dicek:
- root files
- README lama
- FEATURES lama jika ada
- docs lama jika ada
- client location
- server location
- package.json
- framework
- env example
- deployment config
- database config
- scripts
- folder penting lain

Output:
Existing Project Pre-Scan Summary

## 2. Existing Project Audit
Audit menilai kondisi project tanpa mengubah file kode.

Existing Project Audit Summary

Project Name:
Repository:
Current Framework:
Frontend Location:
Backend Location:
Database:
Deployment:
Auth:
Existing Docs:
Main Features:
Known Risks:
Unknown Areas:
Recommended Adoption Mode:
Recommended First Batch:

## 3. Documentation Mapping
- README lama dipertahankan jika masih relevan.
- README boleh diadaptasi, bukan ditimpa total tanpa alasan.
- FEATURES lama dipetakan menjadi feature tracker.
- Docs lama bisa dipindahkan, dirangkum, atau direferensikan.
- Jika dokumen lama berantakan, buat mapping dulu sebelum rewrite.

## 4. Feature Inventory
Fitur existing harus didata berdasarkan kondisi nyata.

Existing Feature Inventory

| Feature ID | Feature Name | Area | Current Evidence | Suggested Status | Notes |
|---|---|---|---|---|---|

Contoh status:
- Existing / Stable
- Existing / Needs Review
- Partial
- Unknown
- HOLD
- Deprecated

- Jangan pakai Completed jika belum divalidasi.
- Completed hanya boleh dipakai jika sudah lolos validasi sesuai DoD.

## 5. Risk Classification
Low Risk:
- tambah docs/project/
- membuat CURRENT_STATUS.md
- membuat FEATURE_HISTORY.md
- membuat feature files
- merapikan docs tanpa menyentuh kode

Medium Risk:
- rewrite README
- rewrite FEATURES
- reorganisasi docs lama
- update env example
- mapping script/deployment docs

High Risk:
- mengubah client code
- mengubah server code
- mengubah database schema
- mengubah auth/security
- mengubah deployment/env
- delete/rename file/folder
- refactor besar

Aturan:
- Batch adoption awal harus Low Risk.
- High Risk wajib user confirmation dan review.

## 6. WPWK Docs Injection
Menambahkan struktur kontrol WPWK ke project existing.

Umumnya boleh dibuat:
- docs/project/
- docs/project/workflow/
- docs/project/history/
- docs/project/history/features/
- docs/project/onboarding/

Tetapi:
- Jangan mengubah client/server.
- Jangan install dependency.
- Jangan membuat config baru.
- Jangan menghapus docs lama.
- Jangan membuat fitur aplikasi baru.

## 7. Feature Tracker Reconstruction
Setelah audit, feature tracker dibuat berdasarkan fitur nyata.

Contoh:
| Feature Batch | Feature Name | Area | Status | Reason / HOLD Notes | Next Step | Detail File |
|---|---|---|---|---|---|---|
| F01 | Existing Client System | frontend/client | Existing / Needs Review | Client sudah ada tapi belum diaudit penuh | F01A — Client Structure Audit | features/F01_EXISTING_CLIENT_SYSTEM.md |
| F02 | Existing Server System | backend/server | Existing / Needs Review | Server sudah ada tapi belum diaudit penuh | F02A — Server Structure Audit | features/F02_EXISTING_SERVER_SYSTEM.md |

## 8. First Controlled Batch
Setelah adoption docs masuk, batch berikutnya harus audit terarah, bukan langsung refactor.

Contoh:
- F01A — Client Structure Audit
- F02A — Server Structure Audit
- F03A — Database Presence Audit
- F04A — Deployment Readiness Audit
- FXX-CP — Documentation Checkpoint

## Hal yang Tidak Boleh Dilakukan
- Jangan menimpa project existing dengan struktur WPWK secara paksa.
- Jangan menghapus README lama tanpa backup/mapping.
- Jangan mengubah client/server di batch dokumentasi adoption.
- Jangan install dependency.
- Jangan rename folder besar.
- Jangan mengubah database/auth/deployment tanpa batch khusus.
- Jangan menyebut fitur existing Completed tanpa validasi.
- Jangan menjadikan F00 sebagai fitur aplikasi.

## Existing Adoption Decision Template

Adoption Decision

Project Type:
Existing Project Condition:
Client Status:
Server Status:
Docs Status:
Recommended Adoption Mode:
Risk Level:
Need Roomchat 01 Review:
Need User Confirmation:
First Adoption Batch:
Notes:

## Penutup
Existing project adoption bertujuan membuat project lama lebih mudah dikontrol, bukan mengulang project dari nol.
