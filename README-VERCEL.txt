VarzXProgramAI - WEB (frontend statis, tanpa build)

1. Buka index.html, cari baris:  const BACKEND_URL="";
   Isi dengan URL HTTPS backend panel, contoh: const BACKEND_URL="https://api.domainanda.com";
   (Tanpa ini, hanya Owner yang bisa mengisi URL lewat tautan "Mode Owner" di halaman login.)
2. Upload SELURUH isi folder ini ke Vercel (index.html, music.mp3, bot-music.mp3, vercel.json harus satu folder).
3. Salin domain Vercel Anda ke CORS_ORIGINS di config.json panel, lalu restart server panel.
4. Tidak ada rahasia di folder ini. Jangan taruh password/API key di index.html.


MULTI-MODEL: Web chat mengambil daftar model gratis dari endpoint backend /v1/models. Pastikan versi panel MULTI terpasang dan CORS_ORIGINS memuat domain Vercel. API key provider hanya disimpan di backend config/environment, tidak di frontend.


MUSIC PLAYLIST
- Musik dikelola melalui music/playlist.json. Tambahkan item {"id":"id-unik","title":"Judul","artist":"VarzXOwn","src":"music/nama-file.mp3"} ke array tracks.
- Upload file audio tersebut ke folder music/ pada repository frontend. File harus boleh diakses publik oleh browser.
- Atur Music menyediakan mode repeat satu lagu atau urutan otomatis, tombol sebelumnya/berikutnya, dan daftar lagu. Chat dapat menjawab perintah daftar musik dan memutar lagu berdasarkan judul yang cocok.
- Sesi login disimpan di localStorage agar tetap masuk setelah halaman dimuat ulang; logout menghapus sesi lokal. Pastikan HTTPS aktif dan lindungi perangkat bersama.
- Prompt AI memiliki gaya bahasa Gaul / santai atau Biasa / profesional dan identitas VarzXProgramCubeAI ciptaan VarzXOwn.
