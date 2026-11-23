# Keuangan Keluarga: APK lewat GitHub

Repo ini membangun APK Android dari `index.html` memakai GitHub Actions (Capacitor). Tidak perlu Android Studio.

## Langkah
1. Buat repository baru di GitHub (public atau private).
2. **Dari komputer:** ekstrak zip ini, lalu di GitHub pilih Add file > Upload files dan seret SEMUA isi folder, termasuk folder `.github`. Commit ke branch `main`.
3. **Dari HP:** unggah `index.html`, `icon.png`, `package.json`, `capacitor.config.json` lewat Upload files. Lalu Add file > Create new file, ketik nama `.github/workflows/build-apk.yml` dan tempel isi file itu dari zip.
4. Buka tab **Actions**. Workflow "Build APK" jalan otomatis (atau Run workflow). Tunggu sekitar 5 sampai 10 menit sampai ada tanda centang hijau.
5. Buka run yang berhasil, bagian **Artifacts**, unduh `keuangan-keluarga-apk`. Ekstrak, di dalamnya ada `app-debug.apk`.
6. Pasang APK di HP (izinkan "Instal dari sumber tidak dikenal").

## Lisensi dan langganan
- Aplikasi gratis dicoba **7 hari**, lalu terkunci sampai ada langganan aktif.
- Paket: **1 Bulan Rp 25.000** (30 hari) dan **1 Tahun Rp 250.000** (365 hari). Pemesanan lewat WhatsApp admin 0857-5255-7857 (tombol ada di tab Langganan dan di layar kunci).
- Pengguna mengirim **ID Perangkat** ke admin. Admin membuat kode 10 karakter dengan `admin-generator-kode.html` (file terpisah, RAHASIA, jangan diunggah ke GitHub), memilih paket, lalu mengirim kode lewat WhatsApp.
- Kode hanya berlaku untuk satu perangkat, satu kali pakai, dan harus diaktifkan maksimal 30 hari sejak dibuat. Perpanjangan sebelum habis menambah sisa hari.
- Pengaturan ada di baris `const LIC_S=...,TRIAL=7,ADMIN_WA=...` di `index.html`. `LIC_S` (kunci rahasia) harus sama dengan yang ada di file admin.
- Ini pengaman dasar yang berjalan di perangkat. Menghapus data aplikasi memberi trial baru, dan orang yang mahir bisa membongkar kodenya. Perlindungan penuh butuh verifikasi lewat server.

## Catatan
- Ini APK debug, cukup untuk pemakaian pribadi. Play Store perlu APK/AAB release yang ditandatangani.
- Untuk memperbarui aplikasi, ganti `index.html` di repo. APK baru otomatis dibangun.
- Di APK, tombol backup, Excel, dan bagikan membuka menu bagikan Android.
- Jika build gagal, salin pesan error dari langkah yang gagal dan kirim ke Claude.
