
# 🌀 Otakudesu Scraper

REST API untuk scraping data dari [Otakudesu](https://otakudesu.cloud)

- 🔍 Cari anime 
- 📘 Ambil detail lengkap anime
- 🎞️ Ambil link streaming & download
- 📺 Ambil daftar ongoing & complete
- ⚡ Cache internal (`node-cache`)

---

## ⚙️ Instalasi
```bash
git clone https://github.com/kamu/otakudesu-api.git
cd otakudesu-api
npm install
npm start
````

---

## 📡 Daftar Endpoint

| Method | Endpoint         | Keterangan                          | Parameter       | Contoh                            |
| ------ | ---------------- | ----------------------------------- | --------------- | --------------------------------- |
| GET    | `/health`        | Cek status server & cache           | –               | `/health`                         |
| GET    | `/search`        | Cari anime                          | `q`: kata kunci | `/search?q=naruto`                |
| GET    | `/anime/:slug`   | Ambil detail anime berdasarkan slug | `:slug`         | `/anime/one-piece-sub-indo`       |
| GET    | `/episode/:slug` | Ambil iframe dan mirror episode     | `:slug`         | `/episode/one-piece-episode-1051` |
| GET    | `/ongoing`       | Daftar anime yang masih tayang      | –               | `/ongoing`                        |
| GET    | `/completed`     | Daftar anime yang sudah tamat       | –               | `/completed`                      |
| GET    | `/cache/stats`   | Statistik cache                     | –               | `/cache/stats`                    |
| DELETE | `/cache/clear`   | Bersihkan seluruh cache             | –               | `/cache/clear`                    |

---

## 🔍 Contoh Penggunaan

### Cari Anime

```
GET /api/search?q=kimetsu
```

### Ambil Detail Anime

```
GET /api/anime/kimetsu-no-yaiba-sub-indo
```

### Ambil Link Streaming Episode

```
GET /api/episode/kimetsu-no-yaiba-episode-1-sub-indo
```

---

## 🧠 Struktur Modular

```
.
├── app.js             # Entry point Express
├── routes.js          # Semua routing
├── scraper.js         # Logic scraping HTML
├── utils.js           # Cache & tools
└── README.md
```

---

## 🔧 Kustomisasi

Untuk ganti domain dasar (misalnya mirror otakudesu lain):

```js
app.locals.config = {
  baseUrl: 'https://otakudesu.cloud',
};
```

---

## ⚠️ Catatan

* Tidak menyimpan file video atau konten.
* Hanya menyajikan data publik yang tersedia via HTML Otakudesu.
* Gunakan dengan bijak dan sesuai etika scraping.

---

## 🧾 Lisensi

MIT — bebas digunakan untuk proyek edukasi, pribadi, atau eksperimen.

```

---

Kalau kamu mau versi markdown ini langsung saya simpan jadi `README.md`, tinggal bilang aja: **"buatkan file canvas README"** atau **"simpan ini sebagai readme project gue"** — langsung tancap gas.
```
