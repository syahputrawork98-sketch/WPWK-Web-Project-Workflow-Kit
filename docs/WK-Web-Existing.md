# WK-Web-Existing

WK-Web-Existing adalah template yang dirancang khusus untuk project web yang aplikasinya atau *codebase*-nya sudah ada dan sedang berjalan.

## Karakteristik
- **Sudah Ada Codebase**: Digunakan ketika project sudah memiliki struktur folder sendiri (seperti `client`, `server`, atau struktur kustom lainnya), dan pernah dikerjakan sebelumnya.
- **Fokus pada Kontrol**: Tujuan utama template ini bukanlah menulis fitur baru di awal, melainkan melakukan **audit**, **mapping**, merapikan dokumentasi, dan mendata fitur yang sudah ada (*feature inventory*).
- **Pendekatan Bertahap**: Proses adopsi dilakukan perlahan agar project lama bisa masuk ke sistem kerja WK dengan rapi. Lakukan audit dulu, mapping dulu, baru setelah itu mengeksekusi *controlled batch*.

## Kapan Menggunakannya?
Gunakan template ini ketika Anda ingin mengontrol ulang project lama yang dokumentasi atau *history*-nya belum rapi, tanpa merusak sistem yang sudah berjalan.

## Aturan Penting
- **Jangan merusak struktur lama**: Jangan langsung menimpa `README.md` lama, menghapus folder, atau mengubah letak `client` dan `server` bawaan project pada tahap awal adopsi.
- **Validasi fitur**: Jangan pernah menyebut fitur existing sebagai "Completed" sebelum fitur tersebut benar-benar divalidasi ulang.
- **Bukan untuk project baru**: Jika Anda belum memiliki kode apa pun dan ingin membangun dari nol, gunakanlah `WK-Web-Greenfield`.
