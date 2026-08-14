# Sehat Sejahtera - Holistic Therapy Landing Page 🌿

Sebuah purwarupa *Landing Page* modern dan responsif untuk pusat kesehatan dan terapi holistik. Proyek ini dibangun untuk memenuhi kriteria penilaian **Local Business / Health & Wellness** dengan fokus pada hierarki visual, arsitektur komponen, serta pengalaman pengguna (UX) yang mulus.

## ✨ Fitur Utama

- **Desain Responsif 100%**: Tata letak beradaptasi sempurna di layar *Mobile*, *Tablet*, dan *Desktop* menggunakan *Tailwind Grid & Flexbox*.
- **Navigasi Interaktif**: Menu navigasi yang disesuaikan untuk *mobile* (Hamburger menu dengan animasi mulus).
- **Smooth Scrolling**: Transisi antar bagian halaman (Beranda, Tentang Kami, Layanan, Testimoni, Kontak) berjalan secara halus.
- **Formulir Janji Temu**: Formulir yang telah divalidasi dengan HTML5 untuk alur kontak/reservasi yang nyata.
- **Semantic HTML & Aksesibilitas**: Penggunaan struktur tag seperti `<section>`, `<article>`, `<figure>`, dan atribut aria yang tepat untuk performa SEO dan aksesibilitas *Screen Reader*.
- **Modern UI/UX**: Dilengkapi dengan mikro-animasi, *hover states*, efek kaca (*backdrop-blur*), dan tipografi berkualitas (Plus Jakarta Sans).

## 🛠️ Teknologi yang Digunakan

- **Framework**: [Vue 3](https://vuejs.org/) (Composition API & `<script setup>`)
- **Styling**: [Tailwind CSS v4](https://tailwindcss.com/)
- **Build Tool**: [Vite](https://vitejs.dev/)
- **Typography**: [Google Fonts (Plus Jakarta Sans)](https://fonts.google.com/specimen/Plus+Jakarta+Sans)

## 📂 Struktur Proyek

Proyek ini dibangun dengan pendekatan modular (Berbasis Komponen) agar kode lebih mudah dibaca dan dipelihara.

```text
src/
├── components/
│   ├── NavbarComponent.vue      # Navigasi utama (Desktop & Mobile)
│   ├── HeroSection.vue          # Bagian sapaan awal (Hero)
│   ├── AboutSection.vue         # Profil singkat & pencapaian (Trust Badges)
│   ├── ServicesSection.vue      # Menu Layanan (Iterasi Array)
│   ├── ServicesCard.vue         # Komponen Kartu untuk masing-masing Layanan
│   ├── TestimoniSection.vue     # Ulasan Klien
│   ├── ContactSection.vue       # Formulir Reservasi & Janji Temu
│   └── FooterComponent.vue      # Tautan cepat dan kontak penutup
├── App.vue                      # Titik kumpul utama komponen (Main Layout)
└── main.ts                      # Entry point Vue
```

## 🚀 Panduan Menjalankan Secara Lokal (Local Setup)

1. **Pastikan Node.js sudah terpasang** di sistem Anda.
2. **Klon (Clone)** repositori ini:
   ```bash
   git clone <url-repositori-anda>
   cd <nama-folder-repositori>
   ```
3. **Instal dependensi**:
   ```bash
   npm install
   ```
4. **Jalankan server pengembangan (Development Server)**:
   ```bash
   npm run dev
   ```
5. Buka tautan yang muncul di terminal (biasanya `http://localhost:5173`) pada browser Anda.

## 🌐 Panduan Deployment (Vercel / Netlify)

Proyek ini sudah sangat siap untuk di-*deploy* langsung (Ready for Production).

**Menggunakan Vercel:**
1. Login ke [Vercel](https://vercel.com).
2. Buat proyek baru dan impor repositori GitHub Anda.
3. Vercel akan otomatis mendeteksi konfigurasi **Vite/Vue**.
4. Biarkan pengaturan *Build Command* menjadi `npm run build` dan *Output Directory* menjadi `dist`.
5. Klik **Deploy** dan tunggu beberapa detik hingga situs Anda *live*.

---
*Dibuat untuk keperluan penilaian Web Development Assessment.*
