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
