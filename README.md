# Landing Page LHP LKPD TA 2025
**BPK Perwakilan Provinsi Bali**

Landing page untuk Laporan Hasil Pemeriksaan (LHP) Laporan Keuangan Pemerintah Daerah (LKPD) Tahun Anggaran 2025, mencakup 10 Pemerintah Daerah se-Provinsi Bali.

---

## Struktur Proyek

```
├── index.html              # Halaman utama
├── assets/
│   ├── css/
│   │   ├── tailwind.css    # Compiled Tailwind (di-generate, jangan edit manual)
│   │   └── style.css       # Custom styles
│   ├── js/
│   │   └── main.js         # Data entitas, Swiper, hamburger menu, AOS init
│   └── img/                # Gambar kantor 10 entitas (.webp)
├── src/
│   └── input.css           # Sumber direktif Tailwind
├── tailwind.config.js      # Konfigurasi tema Tailwind (spring-green)
├── package.json
└── RENCANA.md              # Log pengembangan bertahap
```

---

## Pengembangan Lokal

### Prasyarat
- Node.js ≥ 18
- npm ≥ 9

### Instalasi
```bash
npm install
```

### Mode Development (watcher)
```bash
npm run dev
```
Tailwind akan otomatis dikompilasi setiap ada perubahan di `index.html` atau `assets/js/`.

### Preview Lokal
```bash
npx serve . --listen 3000
```
Buka: http://localhost:3000

---

## Build Production

```bash
npm run build
```
Menghasilkan `assets/css/tailwind.css` yang sudah diminify.

---

## Deployment

File statis siap deploy — cukup upload seluruh isi folder (kecuali `node_modules/` dan `src/`) ke server:

| Target | Cara |
|--------|------|
| **Server BPK/Pemda** | Upload via FTP/SFTP: `index.html`, `assets/` |
| **GitHub Pages** | Push ke branch `gh-pages` atau folder `docs/` |
| **Netlify / Vercel** | Drag-and-drop folder, atau connect repo Git |

> **Catatan:** Pastikan `npm run build` dijalankan sebelum deploy agar CSS sudah diminify.

---

## Teknologi

| Library | Versi | Keterangan |
|---------|-------|------------|
| Tailwind CSS | 3.x | Utility-first CSS (compiled lokal) |
| Swiper.js | 11.x | Carousel / slider entitas |
| AOS | 2.3.4 | Animasi scroll |
| Font Awesome | 6.5.2 | Ikon |
| Inter | — | Tipografi (Google Fonts) |

---

## Entitas yang Dicakup

1. Pemerintah Provinsi Bali
2. Pemerintah Kota Denpasar
3. Pemerintah Kabupaten Badung
4. Pemerintah Kabupaten Gianyar
5. Pemerintah Kabupaten Buleleng
6. Pemerintah Kabupaten Tabanan
7. Pemerintah Kabupaten Jembrana
8. Pemerintah Kabupaten Klungkung
9. Pemerintah Kabupaten Bangli
10. Pemerintah Kabupaten Karangasem

---

## Tautan Penting

- Portal PPID BPK Bali: https://bali-ppid.bpk.go.id/
