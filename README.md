# WK-Workflow-Kit

WK-Workflow-Kit adalah control room utama untuk mengatur penggunaan dua template kerja dalam sistem WK, yaitu WK-Web-Greenfield dan WK-Web-Existing.

Repository ini tidak digunakan untuk menyimpan codebase aplikasi, tidak menyimpan history project tertentu, dan tidak menjadi template kerja langsung untuk project. Fungsi utamanya adalah menjadi peta induk agar user tahu kapan harus memakai template Greenfield dan kapan harus memakai template Existing.

## Struktur WK

WK-Workflow-Kit berada di posisi paling atas.

```text
WK-Workflow-Kit
├── WK-Web-Greenfield
└── WK-Web-Existing
```

## Peran Setiap Repository

### WK-Workflow-Kit
Digunakan sebagai control room atau panduan utama. Repo ini menjelaskan pembagian workflow dan batas penggunaan setiap template.

### WK-Web-Greenfield
Digunakan untuk memulai project web dari nol. Template ini cocok ketika belum ada codebase sebelumnya dan project perlu dibangun dari awal.

### WK-Web-Existing
Digunakan untuk project yang aplikasinya sudah ada. Template ini cocok ketika user ingin mengadopsi, mengaudit, merapikan dokumentasi, membuat history, dan mengontrol project lama tanpa langsung menimpa codebase.

## Cara Memilih Template

Gunakan **WK-Web-Greenfield** jika:
- project benar-benar baru;
- belum ada client/server;
- belum ada struktur aplikasi;
- ingin membangun dari nol;
- ingin memulai feature history sejak awal.

Gunakan **WK-Web-Existing** jika:
- aplikasi/codebase sudah ada;
- sudah ada client/server atau struktur project lama;
- project pernah berjalan/deploy;
- dokumentasi dan history belum rapi;
- user ingin melakukan audit, mapping, dan kontrol project secara bertahap.

## Batasan

WK-Workflow-Kit tidak dipakai untuk:
- menulis kode aplikasi;
- menyimpan fitur project tertentu;
- menyimpan CURRENT_STATUS.md milik project tertentu;
- menyimpan feature history project tertentu;
- menggantikan WK-Web-Greenfield atau WK-Web-Existing.