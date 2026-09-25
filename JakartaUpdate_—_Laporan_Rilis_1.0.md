# JakartaUpdate — Laporan Rilis 1.0.0

## Ringkasan

Proyek ini menyediakan source WordPress modular untuk portal berita, dengan satu theme dan dua plugin terpisah. Theme menangani tampilan; Core mengelola modul editorial; plugin Live menangani channel, program, dan pemutar siaran.

## Paket

- `jakartaupdate.zip`: theme.
- `jakartaupdate-core.zip`: plugin editorial.
- `jakartaupdate-live.zip`: plugin Live/TV opsional.
- `jakartaupdate-framework-1.0.0.zip`: source lengkap dan dokumentasi.

## Implementasi pada rilis ini

Theme: template hierarki umum (homepage, artikel, page, archive, category/tag/author, search, 404), responsif mobile/tablet/desktop, menu WordPress, urutan header desktop dan mobile yang diminta, search panel, drawer aksesibel dengan Escape/backdrop/focus trap/body-scroll lock, logo WordPress, kartu berita, artikel, arsip, pencarian, komentar, footer, prefers-reduced-motion, dan mode gelap otomatis bila dipilih.

Core: halaman dashboard/settings; breaking ribbon (manual ID atau post yang ditandai), ticker, CPT berita video dengan halaman pemutaran YouTube/Vimeo/MP4, slot iklan HTML yang disaring, tautan sosial, berbagi/copy link, counter kunjungan ringan, popular/related posts, fallback description dan NewsArticle schema saat plugin SEO umum tidak terdeteksi, ID analytics yang divalidasi, serta ekspor konfigurasi JSON.

Live: CPT channel dan program, status ON AIR/SCHEDULED/OFF AIR, player responsif untuk YouTube Live, YouTube/Vimeo embed tervalidasi, HTTPS HLS dan MP4 native, daftar channel, jadwal program, fallback stream tidak tersedia, dan pemuatan CSS hanya di halaman shortcode.

## Validasi yang dilakukan

Semua berkas PHP diperiksa menggunakan `php -l`; berkas JavaScript diperiksa menggunakan `node --check`. Arsip ZIP diuji struktur dan keterbacaannya. Ini bukan pengujian integrasi pada instalasi WordPress aktif, bukan audit penetrasi, dan bukan pengukuran Lighthouse/Core Web Vitals.

## Batasan penting

Rilis ini belum memiliki setup wizard multi-langkah, homepage builder drag-and-drop/reorder melalui admin, import JSON, ekspor channel/program, filter popular berdasarkan rentang tanggal, penghitung view bersejarah per hari, jadwal status ON AIR otomatis berdasarkan waktu, Gutenberg block khusus, atau menu kustomisasi admin lengkap per modul. Newsletter baru berupa tampilan CTA tanpa koneksi provider. Analytics dan iklan perlu ditinjau sesuai consent/privacy policy situs. Performa final bergantung tema anak, konten, hosting, CDN, stream, dan plugin aktif.

## Kompatibilitas dan go-live

Target minimum WordPress 6.2 dan PHP 8.1. Sebelum situs produksi, instal pada staging; uji tema/plugin lain (khususnya WooCommerce dan plugin SEO), konten Gutenberg/Classic Editor, menu, cache/CDN, seluruh breakpoints dan stream riil; periksa consent analytics serta kebijakan privasi; siapkan backup dan lakukan review keamanan di host sasaran.

## Instalasi ringkas

Aktifkan theme, lalu Core, lalu Live jika dibutuhkan. Buat halaman Live dengan `[ju_live_tv]`, atur URL LIVE melalui Customizer, buat kategori slug `market`, `sport`, `lifestyle`, dan atur logo/menu melalui WordPress. Petunjuk lengkap tersedia di `INSTALL.md` dan `LIVE-TV.md`.

**Status:** source release 1.0.0 siap dipasang dan diuji pada staging; jangan ditafsirkan sebagai hasil validasi menyeluruh pada setiap konfigurasi WordPress atau jaminan siaran produksi.

