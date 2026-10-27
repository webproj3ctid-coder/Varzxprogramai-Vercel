VarzXProgramAI - WEB (frontend statis, tanpa build)

1. Buka index.html, cari baris:  const BACKEND_URL="";
   Isi dengan URL HTTPS backend panel, contoh: const BACKEND_URL="https://api.domainanda.com";
   (Tanpa ini, hanya Owner yang bisa mengisi URL lewat tautan "Mode Owner" di halaman login.)
2. Upload SELURUH isi folder ini ke Vercel (index.html, music.mp3, bot-music.mp3, vercel.json harus satu folder).
3. Salin domain Vercel Anda ke CORS_ORIGINS di config.json panel, lalu restart server panel.
4. Tidak ada rahasia di folder ini. Jangan taruh password/API key di index.html.


MULTI-MODEL: Web chat mengambil daftar model gratis dari endpoint backend /v1/models. Pastikan versi panel MULTI terpasang dan CORS_ORIGINS memuat domain Vercel. API key provider hanya disimpan di backend config/environment, tidak di frontend.
