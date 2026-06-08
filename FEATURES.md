# Features

Dokumen ini berisi daftar fitur sistem workflow yang digunakan dalam WPWK.

## Mode Sistem Utama
- **Greenfield Mode**: Panduan dan template struktur (`client/` & `server/`) untuk membangun project dari nol.
- **Existing Project Mode**: Sistem audit, mapping dokumentasi, dan adopsi terstruktur untuk project codebase lama yang sudah berjalan tanpa merusak sistem aslinya (Controlled Adoption).

## Workflow & Safety System
- **Source of Truth System**: GitHub sebagai satu-satunya kebenaran mutlak.
- **Roomchat Role System**: Pemisahan tugas antara Manager (Room 00), Reviewer (Room 01), dan Eksekutor (Gemini Anti-Gravity).
- **Batch Gate System**: Mekanisme validasi sebelum eksekusi dimulai (Pre-Batch Mode vs Batch Execution).
- **Feature Batch Tracker**: Pelacakan fitur menggunakan kode FXX (misal: F00, F01).
- **History Layer Separation**: Pemisahan layer history (`docs/history/`) dari workflow/control layer (`docs/project/`).

## Dokumentasi & Aturan Eksekusi
- **Executor Report System**: Standar pelaporan eksekusi dari Gemini ke User.
- **Review Checklist System**: Standar audit hasil eksekusi oleh Room 01.
- **Documentation Checkpoint System**: Pos pemeriksaan (FXX-CP) untuk memastikan sinkronisasi dokumentasi dan kode.
- **Technical Area Documentation System**: Aturan pencatatan spesifik per area (frontend, backend, database).
- **Template Adaptation Rule**: Panduan menyesuaikan template untuk project nyata.
- **Documentation Debt / Docs Later Rule**: Mekanisme penundaan pembaruan dokumen melalui checkpoint.

## Skenario & Templating Operasional
- **Workflow Scenario Playbook**: Kumpulan skenario penggunaan workflow.
- **Specialist Analysis Room Workflow**: Alur kerja penggunaan AI spesialis eksternal.
- **Project Starter Checklist**: Checklist persiapan saat memulai project nyata.
- **Roomchat 00 Acceptance Template**: Standar validasi hasil eksekusi oleh Manager Room 00.
- **Public / Client-Safe History Mode**: Gaya bahasa netral untuk repository publik atau berhadapan dengan client.
