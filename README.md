# 🌳 Silsilah Keluarga — Bani Raukhan & Rafi

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen?logo=github)](https://cakgup.github.io/bani-raukhan-rafi/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Pohon silsilah interaktif keluarga besar **Bani Raukhan – Rafi** berbasis D3.js, dengan desain estetika Jawa Kraton & Sogan. Dioptimalkan untuk layar portrait 1080×1920 (HP).

---

## ✨ Fitur

| Fitur | Keterangan |
|---|---|
| 🎭 Halaman Selamat Datang | Animasi Gunungan Wayang, teks sambutan Jawa Krama |
| 🌿 Tree Bertahap | Klik node → muncul 1 generasi di bawahnya |
| 📱 Portrait-First | Dioptimalkan untuk HP (1080×1920) |
| 🔍 Pencarian Nama | Sorot anggota yang dicari, cabangnya otomatis terbuka |
| 🔭 Zoom & Geser | Pinch-to-zoom, drag untuk geser |
| ✿ Status Anggota | Meninggal (abu + ✿) dan cerai (border putus-putus) |
| 🎯 Tombol Kontrol | Zoom, reset tampilan, buka/tutup semua cabang |

---

## 🗂️ Struktur File

```
bani-raukhan-rafi/
├── index.html                              ← Aplikasi utama (HTML + CSS + JS)
├── family-data.js                          ← Data silsilah (format JS, auto-generated)
├── bani_raukhan_rafi_tree_d3_visual_reparse.json  ← Sumber data (JSON, edit di sini)
├── gunungan.png                            ← Gambar Gunungan Wayang
└── README.md                               ← Dokumentasi ini
```

> **Penting:** `family-data.js` adalah file *generated* — **jangan edit langsung**.  
> Edit selalu di file `.json`, lalu regenerate `family-data.js` (lihat tutorial di bawah).

---

## 🚀 Menjalankan Secara Lokal

### Cara 1: Python (paling mudah, tidak perlu install)
```bash
python -m http.server 5500 --directory .
```
Buka browser: **http://localhost:5500**

### Cara 2: Node.js / npx
```bash
npx -y serve .
```
Buka browser: **http://localhost:3000**

### Cara 3: VS Code Live Server
Klik kanan `index.html` → **Open with Live Server**

> ⚠️ **Jangan buka `index.html` langsung** (double-click) karena browser memblokir loading `family-data.js` via protokol `file://`.

---

## ✏️ Cara Memperbarui Data Silsilah

### Langkah 1 — Edit file JSON

Buka dan edit file:
```
bani_raukhan_rafi_tree_d3_visual_reparse.json
```

Gunakan teks editor apa saja (VS Code, Notepad++, dll).

---

### Langkah 2 — Struktur Data

Setiap anggota keluarga ditulis sebagai **object JSON** dengan format berikut:

```json
{
  "id": "unik-123",
  "nomor_silsilah": "1.2.3",
  "nama": "NAMA LENGKAP",
  "meninggal": false,
  "generation_from_founder": 2,
  "pasangan": [
    {
      "nama": "NAMA PASANGAN",
      "meninggal": false,
      "cerai": false
    }
  ],
  "children": [
    { ... }
  ]
}
```

**Keterangan field:**

| Field | Tipe | Keterangan |
|---|---|---|
| `id` | string | **Wajib, unik** — tidak boleh sama dengan anggota lain |
| `nomor_silsilah` | string | Nomor urut (misal: `"1"`, `"1.2"`, `"1.2.3"`) |
| `nama` | string | **Nama anggota** — tulis HURUF KAPITAL |
| `meninggal` | boolean | `true` jika sudah meninggal, `false` atau hapus jika masih hidup |
| `generation_from_founder` | number | Generasi ke berapa dari Pendiri (root = 0) |
| `pasangan` | array | Daftar pasangan (bisa lebih dari satu) |
| `pasangan[].nama` | string | Nama pasangan |
| `pasangan[].meninggal` | boolean | Status meninggal pasangan |
| `pasangan[].cerai` | boolean | `true` jika bercerai |
| `children` | array | Daftar anak — isi dengan object yang sama (rekursif) |

---

### Contoh: Menambah Anggota Baru

Cari parent-nya di JSON, lalu tambahkan ke array `children`:

```json
{
  "id": "sunari",
  "nama": "SUNARI",
  "pasangan": [{ "nama": "SUMIATI" }],
  "children": [
    {
      "id": "sunari-anak1",
      "nomor_silsilah": "2.1",
      "nama": "BUDI SANTOSO",
      "meninggal": false,
      "generation_from_founder": 2,
      "pasangan": [{ "nama": "SRI WAHYUNI" }],
      "children": []
    }
  ]
}
```

### Contoh: Menandai Anggota Meninggal

```json
{
  "id": "slamet-01",
  "nama": "SLAMET",
  "meninggal": true,
  "pasangan": [{ "nama": "MARSIAH", "meninggal": true }]
}
```

### Contoh: Pasangan Cerai

```json
"pasangan": [
  { "nama": "SITI", "cerai": true },
  { "nama": "AMINAH" }
]
```

---

### Langkah 3 — Regenerate `family-data.js`

Setelah selesai edit JSON, **wajib** jalankan perintah ini agar perubahan terbaca oleh aplikasi:

**Windows (CMD/PowerShell):**
```powershell
python -c "
import json
with open('bani_raukhan_rafi_tree_d3_visual_reparse.json', 'r', encoding='utf-8') as f:
    raw = f.read()
with open('family-data.js', 'w', encoding='utf-8') as f:
    f.write('const FAMILY_DATA = ' + raw + ';')
print('family-data.js berhasil diperbarui!')
"
```

**Mac/Linux (Terminal):**
```bash
python3 -c "
import json
with open('bani_raukhan_rafi_tree_d3_visual_reparse.json', 'r', encoding='utf-8') as f:
    raw = f.read()
with open('family-data.js', 'w', encoding='utf-8') as f:
    f.write('const FAMILY_DATA = ' + raw + ';')
print('family-data.js berhasil diperbarui!')
"
```

---

### Langkah 4 — Cek di Browser

Buka/refresh `http://localhost:5500` dan periksa:
- Nama baru muncul di tree
- Tidak ada error di Console browser (F12 → Console)

---

### Langkah 5 — Push ke GitHub Pages

```bash
git add bani_raukhan_rafi_tree_d3_visual_reparse.json family-data.js
git commit -m "data: tambah anggota baru [nama]"
git push origin main
```

Tunggu 1–2 menit, lalu buka:
**https://cakgup.github.io/bani-raukhan-rafi**

---

## 🎮 Tombol Kontrol

| Tombol | Fungsi |
|---|---|
| **＋** | Perbesar (zoom in) |
| **－** | Perkecil (zoom out) |
| **🎯** | Sesuaikan tampilan agar semua node terlihat |
| **⊞** | Buka satu generasi berikutnya sekaligus |
| **⊟** | Tutup semua cabang, kembali ke root |
| **🔍** | Cari nama anggota |

---

## 🎨 Mengubah Tampilan

### Warna (CSS Variables)
Edit bagian `:root { ... }` di dalam `index.html`:

```css
:root {
  --gold:    #D4AF37;   /* Warna emas utama */
  --bg:      #0E0905;   /* Latar belakang gelap */
  --cream:   #F5EDD8;   /* Warna kartu */
  --bronze:  #643A11;   /* Coklat tua */
}
```

### Teks Sambutan
Cari dan edit bagian ini di `index.html`:
```html
<p class="w-msg">
  Sugeng rawuh dhumateng sedaya ...
</p>
```

### Gunungan
Ganti file `gunungan.png` dengan gambar lain berformat PNG.  
Gunakan `mix-blend-mode: screen` agar background hitam hilang (sudah aktif secara default).

---

## 🛠️ Teknologi

| Library | Versi | Fungsi |
|---|---|---|
| [D3.js](https://d3js.org/) | v7 | Tree layout, zoom, animasi |
| [Google Fonts](https://fonts.google.com/) | — | Cinzel Decorative, Plus Jakarta Sans |
| HTML + CSS + JS | — | Tidak ada build step, pure static |

---

## 📋 Checklist Update Data

- [ ] Edit `bani_raukhan_rafi_tree_d3_visual_reparse.json`
- [ ] Pastikan setiap `id` **unik**
- [ ] Jalankan script Python untuk regenerate `family-data.js`
- [ ] Test di browser lokal (`localhost:5500`)
- [ ] Commit & push ke GitHub
- [ ] Verifikasi di GitHub Pages

---

## 📄 Lisensi

Data keluarga bersifat **privat**.  
Kode aplikasi dirilis di bawah lisensi **MIT**.

---

*Dikembangkan dengan ❤️ untuk Keluarga Besar Bani Raukhan – Rafi*
