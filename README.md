# KELONTONG 20/80 — versi 1 (MVP)
Catat utang faktur, piutang+angsuran, retur kedaluwarsa. Offline, data lokal (IndexedDB), tanpa login/server.

## Deploy GitHub Pages
1. Buat repository baru di GitHub, unggah semua file ini ke root (index.html, app.js, sw.js, manifest.json, icon.svg).
2. Settings → Pages → Source: Deploy from a branch → `main` / root → Save.
3. Buka `https://USERNAME.github.io/NAMA-REPO/` di Chrome Android → menu ⋮ → Tambahkan ke layar utama.

## APK
Ikon PNG sudah disertakan. Cara termudah dan gratis: PWABuilder.com (masukkan URL Pages). 

## Penting
Data hanya di HP. Backup JSON rutin. Jika mengubah file, naikkan `C='kelontong-v1'` di sw.js agar cache diperbarui.

## Versi 2
Tab Ide (A–F), reminder nota H-2/H-1 di Utang. Database naik ke versi 2 (data lama aman).

## Versi 3
Ikon nota, sketsa toko di header, titik ribuan di input nominal, tab Ide jadi daftar vertikal + scrollbar geser.

## Versi 4
Kalender arus kas 14 hari (Beranda), alarm harga beli naik (Ide G), radar modal mengendap (Ide H). Database naik ke versi 3.

## Build APK
Workflow: .github/workflows/build-apk.yml (manual, Actions > Build APK > Run workflow). Butuh secret KEYSTORE_BASE64, KS_PASS, KEY_PASS, KEY_ALIAS.

## Versi 5
Pemilih tanggal kalender kustom (panah bulan/tahun), perbaikan janji bayar opsional.

## Versi 6
Ekspor via lembar Bagikan di APK (Filesystem+Share), simulasi Monte Carlo + target 20/80 di tab Ide.

## Versi 7
Efisiensi modal, modal minimum untuk 50/80/100% laba, skema Hemat modal di simulasi.

## Versi 8
Rekomendasi pembagian modal per barang (persentase, Rp, unit) untuk skema terbaik.

## Versi 7
Ekspor JSON/CSV di APK kini membuka dialog simpan Android (pilih Download/penyimpanan internal) lewat plugin native `android-plugin/SaveFilePlugin.java`. Tombol "Bagikan Backup" tetap ada untuk kirim ke WhatsApp/Telegram. Workflow menyalin plugin + MainActivity.java saat build.

## Versi 9
Tab baru "Cari" (di antara Exp dan Ide): daftar manual barang yang perlu dicari/disediakan karena kosong dari sales. Status: Belum dicari / Dalam proses / Sudah ada. Database naik ke versi 5 (data lama aman), ikut Backup/Impor/Hapus Semua.

## Versi 10
Notifikasi lokal Android (plugin @capacitor/local-notifications): reminder nota jam 08.00 di H-2, H-1, dan hari jatuh tempo, tetap jalan saat app ditutup. Tab Backup punya tombol Tes Notifikasi. Badge angka di tab Utang/Cari. Hanya aktif di APK, bukan di browser.

## Versi 11
Fix: notifikasi yang sudah muncul tidak lagi terhapus saat app dibuka/disimpan (sebelumnya jadwal ulang ikut membatalkan notif yang sudah tampil). Notif tidak hilang saat diketuk (autoCancel off); setiap notif membuka app langsung ke tab Utang.

## Versi 12
Reminder di tab Utang dan Beranda kini mencakup nota terlambat (H+1, H+2, dst), H+0, lalu H-1/H-2, urut dari yang paling mendesak; terlambat dan H+0 berwarna merah tebal. Notifikasi jam 08.00: H-2, H-1, H+0, dan tiap hari selama nota belum lunas (sampai 30 hari ke depan sejak app terakhir dibuka). Notif nota yang sudah dibayar ikut dihapus dari bar notifikasi.

## Versi 13
Jam notifikasi reminder nota bisa diatur (default 08.00) dan reminder otomatis bisa dimatikan, lewat kartu Notifikasi di tab Backup. Pengaturan disimpan di HP (bukan bagian file backup JSON).
