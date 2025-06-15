# 🌀 Otakudesu Scraper
Sebuah REST API sederhana untuk mengambil data dari [Otakudesu](https://otakudesu.cloud)

- 🔍 Cari anime
- 📘 Detail anime
- 🎞️ Link streaming & download
- 📺 Daftar ongoing & complete
- ⚡ Caching bawaan (pakai `node-cache`)

---

# 📦 Instalasi

```bash
git clone https://github.com/kamu/otakudesu-api.git
cd otakudesu-api
npm install1```

---

| Method | Endpoint              | Deskripsi                         |
| ------ | --------------------- | --------------------------------- |
| GET    | `/api/health`         | Cek status API dan cache          |
| GET    | `/api/search?q=query` | Cari anime dari keyword           |
| GET    | `/api/anime/:slug`    | Ambil detail lengkap sebuah anime |
| GET    | `/api/episode/:slug`  | Ambil data streaming & mirror     |
| GET    | `/api/ongoing`        | Ambil daftar anime ongoing        |
| GET    | `/api/completed`      | Ambil daftar anime completed      |
| GET    | `/api/cache/stats`    | Statistik cache aktif             |
| DELETE | `/api/cache/clear`    | Bersihkan semua cache             |
