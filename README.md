# 🌳 Silsilah Keluarga — Bani Raukhan & Rafi

<p align="center">
  <img src="gunungan.png" alt="Gunungan Wayang Jawa" width="180">
</p>

<p align="center">
  <strong>Pohon silsilah interaktif keluarga besar Bani Raukhan – Rafi</strong><br>
  Dibangun dengan D3.js, bernuansa Jawa Kraton & Sogan, dan dioptimalkan untuk tampilan portrait HP.
</p>

<p align="center">
  <a href="https://cakgup.github.io/bani-raukhan-rafi/">
    <img src="https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen?logo=github" alt="GitHub Pages">
  </a>
  <a href="LICENSE.txt">
    <img src="https://img.shields.io/badge/License-GPL--3.0-blue.svg" alt="License GPL-3.0">
  </a>
  <img src="https://img.shields.io/badge/Made%20with-D3.js-orange" alt="Made with D3.js">
  <img src="https://img.shields.io/badge/Portrait--First-1080x1920-purple" alt="Portrait First">
</p>

---

## ✦ Bismillahirrahmanirrahim

Aplikasi ini dibuat sebagai ikhtiar kecil untuk menjaga ingatan keluarga, merawat nasab, dan mempererat tali persaudaraan lintas generasi.  
Semoga pohon silsilah ini tidak sekadar menjadi tampilan digital, tetapi juga menjadi pengingat bahwa setiap nama memiliki akar, kisah, dan amanah.

> _“Sintèn ingkang boten mangertos asal-usulipun, boten badhé mangertos sintèn sejatinipun piyambak.”_  
> Siapa yang tidak mengenal asal-usulnya, akan sulit memahami siapa dirinya.

---

## 📌 Tentang Aplikasi

**Silsilah Keluarga — Bani Raukhan & Rafi** adalah aplikasi web statis untuk menampilkan pohon keluarga secara interaktif. Aplikasi ini dirancang agar mudah dibuka melalui GitHub Pages, ringan digunakan di perangkat seluler, serta mudah diperbarui melalui file data JSON.

Aplikasi ini cocok digunakan untuk:

- mendokumentasikan silsilah keluarga besar;
- memperkenalkan hubungan kekerabatan kepada generasi muda;
- menyimpan pengetahuan keluarga dalam format digital;
- membuat arsip keluarga yang mudah dibuka dari HP;
- menjadi template awal bagi keluarga lain yang ingin membuat pohon silsilah serupa.

---

## ✨ Fitur Utama

| Fitur | Keterangan |
|---|---|
| 🎭 Halaman Selamat Datang | Tampilan pembuka dengan nuansa Gunungan Wayang dan teks sambutan |
| 🌳 Pohon Silsilah Interaktif | Node keluarga dapat diklik untuk membuka generasi berikutnya |
| 📱 Portrait-First | Dioptimalkan untuk layar HP portrait 1080×1920 |
| 🔍 Pencarian Nama | Cari anggota keluarga, sorot hasil, dan buka cabangnya otomatis |
| 🤏 Zoom & Geser | Mendukung pinch-to-zoom dan drag untuk menjelajah pohon |
| ✿ Status Anggota | Penanda anggota yang telah meninggal dan pasangan yang bercerai |
| 🧭 Tombol Kontrol | Zoom in, zoom out, buka cabang, tutup cabang, dan reset tampilan |
| 🧬 Data Terstruktur | Data silsilah disimpan dalam format JSON agar lebih mudah dirawat |
| 🚀 Tanpa Backend | Cukup HTML, CSS, JavaScript, dan GitHub Pages |

---

## 🖼️ Tampilan Konsep

Aplikasi membawa suasana **Jawa klasik** dengan sentuhan:

- warna emas, sogan, krem, dan cokelat tua;
- elemen visual Gunungan Wayang;
- teks sambutan bernuansa Jawa Krama;
- desain kartu anggota keluarga yang sederhana dan mudah dibaca;
- navigasi yang disesuaikan untuk penggunaan melalui HP.

---

## 🗂️ Struktur Repository

```text
bani-raukhan-rafi/
├── index.html
├── family-data.js
├── bani_raukhan_rafi_tree_d3_visual_reparse.json
├── gunungan.png
├── LICENSE.txt
└── README.md
```

Keterangan:

| File | Fungsi |
|---|---|
| `index.html` | Aplikasi utama yang memuat tampilan, style, dan script |
| `family-data.js` | Data silsilah dalam format JavaScript yang dibaca aplikasi |
| `bani_raukhan_rafi_tree_d3_visual_reparse.json` | Sumber data utama silsilah dalam format JSON |
| `gunungan.png` | Gambar Gunungan Wayang untuk tampilan pembuka |
| `LICENSE.txt` | Lisensi penggunaan kode |
| `README.md` | Dokumentasi repository |

> **Catatan penting:**  
> File `family-data.js` adalah file hasil generate. Untuk mengubah data silsilah, sebaiknya edit file JSON terlebih dahulu, lalu generate ulang `family-data.js`.

---

## 🚀 Cara Menggunakan Aplikasi

### 1. Buka versi online

Aplikasi dapat dibuka melalui GitHub Pages:

```text
https://cakgup.github.io/bani-raukhan-rafi/
```

### 2. Ketuk halaman pembuka

Pada halaman awal, tekan tombol:

```text
✦ Lihat Silsilah ✦
```

### 3. Jelajahi pohon keluarga

Gunakan fitur berikut:

| Kontrol | Fungsi |
|---|---|
| Klik node | Membuka turunan satu generasi di bawahnya |
| `＋` | Memperbesar tampilan |
| `－` | Memperkecil tampilan |
| `⊞` | Membuka cabang/generasi berikutnya |
| `⊟` | Menutup cabang dan kembali ke tampilan awal |
| Kolom pencarian | Mencari nama anggota keluarga |
| Drag layar | Menggeser posisi pohon |
| Pinch layar | Zoom melalui HP |

---

## 💻 Menjalankan Secara Lokal

Jangan membuka `index.html` langsung dengan double click, karena beberapa browser dapat membatasi pembacaan file melalui protokol `file://`.

Gunakan salah satu cara berikut.

### Opsi 1 — Python

```bash
python -m http.server 5500 --directory .
```

Lalu buka:

```text
http://localhost:5500
```

Untuk Mac/Linux yang memakai `python3`:

```bash
python3 -m http.server 5500 --directory .
```

### Opsi 2 — Node.js

```bash
npx -y serve .
```

Lalu buka:

```text
http://localhost:3000
```

### Opsi 3 — VS Code Live Server

1. Buka folder repository di VS Code.
2. Klik kanan file `index.html`.
3. Pilih **Open with Live Server**.
4. Aplikasi akan terbuka di browser.

---

## ✏️ Cara Memperbarui Data Silsilah

### Langkah 1 — Edit file JSON

Buka file berikut:

```text
bani_raukhan_rafi_tree_d3_visual_reparse.json
```

Gunakan editor seperti VS Code, Notepad++, Sublime Text, atau editor lain.

---

### Langkah 2 — Pahami struktur data

Setiap anggota keluarga ditulis sebagai object JSON seperti berikut:

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
  "children": []
}
```

Keterangan field:

| Field | Tipe | Keterangan |
|---|---|---|
| `id` | string | ID unik, tidak boleh sama dengan anggota lain |
| `nomor_silsilah` | string | Nomor urut silsilah, misalnya `1`, `1.2`, `1.2.3` |
| `nama` | string | Nama anggota keluarga |
| `meninggal` | boolean | `true` jika telah meninggal, `false` jika masih hidup |
| `generation_from_founder` | number | Nomor generasi dari pendiri/root |
| `pasangan` | array | Daftar pasangan anggota keluarga |
| `pasangan[].nama` | string | Nama pasangan |
| `pasangan[].meninggal` | boolean | Status meninggal pasangan |
| `pasangan[].cerai` | boolean | Status cerai pasangan |
| `children` | array | Daftar anak/turunan |

---

### Langkah 3 — Contoh menambah anggota baru

Cari parent/induknya, lalu tambahkan data anak di dalam array `children`.

```json
{
  "id": "contoh-anak-01",
  "nomor_silsilah": "1.2.1",
  "nama": "NAMA ANGGOTA BARU",
  "meninggal": false,
  "generation_from_founder": 3,
  "pasangan": [
    {
      "nama": "NAMA PASANGAN",
      "meninggal": false,
      "cerai": false
    }
  ],
  "children": []
}
```

---

### Langkah 4 — Contoh menandai anggota telah meninggal

```json
{
  "id": "contoh-anggota-01",
  "nama": "NAMA ANGGOTA",
  "meninggal": true,
  "pasangan": [
    {
      "nama": "NAMA PASANGAN",
      "meninggal": true
    }
  ],
  "children": []
}
```

---

### Langkah 5 — Contoh menandai pasangan cerai

```json
"pasangan": [
  {
    "nama": "NAMA PASANGAN",
    "cerai": true
  }
]
```

---

### Langkah 6 — Generate ulang `family-data.js`

Setelah JSON selesai diedit, jalankan perintah berikut agar aplikasi membaca data terbaru.

#### Windows PowerShell / CMD

```powershell
python -c "import json; raw=open('bani_raukhan_rafi_tree_d3_visual_reparse.json','r',encoding='utf-8').read(); open('family-data.js','w',encoding='utf-8').write('const FAMILY_DATA = ' + raw + ';'); print('family-data.js berhasil diperbarui!')"
```

#### Mac / Linux

```bash
python3 -c "import json; raw=open('bani_raukhan_rafi_tree_d3_visual_reparse.json','r',encoding='utf-8').read(); open('family-data.js','w',encoding='utf-8').write('const FAMILY_DATA = ' + raw + ';'); print('family-data.js berhasil diperbarui!')"
```

---

### Langkah 7 — Cek hasil di browser

Refresh halaman lokal:

```text
http://localhost:5500
```

Periksa:

- nama baru sudah muncul;
- cabang keluarga tampil benar;
- status meninggal/cerai sesuai;
- tidak ada error di Console browser.

Untuk membuka Console:

```text
F12 → Console
```

---

## 🌐 Deploy ke GitHub Pages

Aplikasi ini cocok dipublikasikan melalui GitHub Pages karena tidak membutuhkan backend.

### Cara deploy

1. Masuk ke repository GitHub.
2. Buka menu **Settings**.
3. Pilih **Pages**.
4. Pada bagian **Build and deployment**, pilih:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
5. Klik **Save**.
6. Tunggu beberapa saat sampai GitHub Pages aktif.

URL biasanya berbentuk:

```text
https://username.github.io/nama-repository/
```

Untuk repository ini:

```text
https://cakgup.github.io/bani-raukhan-rafi/
```

---

## 🔁 Cara Duplikasi untuk Keluarga Lain

Repository ini dapat dijadikan template untuk membuat pohon silsilah keluarga lain.

### Opsi 1 — Fork repository

1. Klik tombol **Fork** di GitHub.
2. Ubah nama repository, misalnya:
   ```text
   silsilah-keluarga-[nama-keluarga]
   ```
3. Edit data JSON sesuai keluarga masing-masing.
4. Generate ulang `family-data.js`.
5. Aktifkan GitHub Pages.

### Opsi 2 — Clone manual

```bash
git clone https://github.com/cakgup/bani-raukhan-rafi.git
cd bani-raukhan-rafi
```

Ubah remote ke repository baru:

```bash
git remote remove origin
git remote add origin https://github.com/username/nama-repository-baru.git
git add .
git commit -m "init: duplikasi aplikasi silsilah keluarga"
git push -u origin main
```

---

## 🎨 Mengubah Tampilan

### Mengubah warna

Cari bagian CSS variable di `index.html`, lalu sesuaikan warna:

```css
:root {
  --gold: #D4AF37;
  --bg: #0E0905;
  --cream: #F5EDD8;
  --bronze: #643A11;
}
```

### Mengubah teks sambutan

Cari bagian teks sambutan di `index.html`, misalnya:

```html
Sugeng rawuh dhumateng sedaya Keluarga Ageng Bani Raukhan–Rafi.
```

Ubah sesuai kebutuhan keluarga.

### Mengubah gambar Gunungan

Ganti file:

```text
gunungan.png
```

dengan gambar baru berformat PNG.

Pastikan nama file tetap sama, atau sesuaikan path gambar di `index.html`.

---

## 🧪 Checklist Sebelum Publish

Gunakan daftar berikut setiap kali memperbarui data:

- [ ] Data JSON sudah diedit dengan benar
- [ ] Setiap `id` anggota bersifat unik
- [ ] Struktur `children` tidak rusak
- [ ] Status `meninggal` dan `cerai` sudah sesuai
- [ ] `family-data.js` sudah di-generate ulang
- [ ] Aplikasi sudah dicek di browser lokal
- [ ] Tidak ada error di Console
- [ ] Perubahan sudah di-commit dan di-push
- [ ] GitHub Pages sudah menampilkan data terbaru

---

## 🧩 Troubleshooting

### Data baru tidak muncul

Kemungkinan penyebab:

- lupa generate ulang `family-data.js`;
- browser masih menyimpan cache lama;
- file JSON tidak valid;
- perubahan belum di-push ke GitHub.

Solusi:

```bash
python3 -c "import json; raw=open('bani_raukhan_rafi_tree_d3_visual_reparse.json','r',encoding='utf-8').read(); open('family-data.js','w',encoding='utf-8').write('const FAMILY_DATA = ' + raw + ';')"
```

Lalu refresh browser dengan:

```text
Ctrl + F5
```

---

### Halaman putih atau tidak tampil

Cek Console browser:

```text
F12 → Console
```

Penyebab umum:

- ada koma berlebih di JSON;
- tanda kurung `{}` atau `[]` tidak lengkap;
- nama file salah;
- `family-data.js` tidak terbaca.

---

### Pencarian tidak menemukan nama

Pastikan:

- nama di data sudah benar;
- tidak ada typo;
- data sudah masuk ke `family-data.js`;
- halaman sudah di-refresh setelah update.

---

## 🔐 Catatan Privasi Data Keluarga

Silsilah keluarga sering memuat data pribadi. Karena itu, sebelum dipublikasikan secara terbuka, pertimbangkan hal berikut:

- hindari mencantumkan data sensitif seperti NIK, alamat lengkap, nomor HP, atau tanggal lahir detail;
- gunakan nama seperlunya sesuai kesepakatan keluarga;
- pastikan keluarga memahami bahwa repository publik dapat dilihat orang lain;
- apabila data dianggap privat, gunakan repository private atau hosting terbatas;
- buat pengelolaan data dengan adab, kehati-hatian, dan musyawarah keluarga.

---

## 🛠️ Teknologi yang Digunakan

| Teknologi | Fungsi |
|---|---|
| HTML | Struktur halaman |
| CSS | Tampilan dan desain visual |
| JavaScript | Logika interaksi aplikasi |
| D3.js v7 | Visualisasi tree, zoom, dan node |
| Google Fonts | Tipografi |
| GitHub Pages | Hosting static site gratis |

---

## 🤝 Kontribusi

Kontribusi dapat dilakukan dalam bentuk:

- memperbaiki tampilan;
- merapikan struktur data;
- menambahkan fitur pencarian;
- memperbaiki dokumentasi;
- membuat panduan import/export data;
- menambahkan mode cetak/PDF;
- meningkatkan kenyamanan tampilan di HP.

Alur kontribusi:

```bash
git checkout -b feature/nama-fitur
git add .
git commit -m "feat: tambah nama fitur"
git push origin feature/nama-fitur
```

Lalu buat Pull Request di GitHub.

---

## 📜 Lisensi

Repository ini menggunakan lisensi **GNU General Public License v3.0 (GPL-3.0)** sebagaimana tercantum dalam file `LICENSE.txt`.

Secara ringkas, lisensi ini memberi kebebasan untuk menggunakan, mempelajari, memodifikasi, dan mendistribusikan ulang kode, dengan tetap memperhatikan ketentuan lisensi GPL-3.0.

> Catatan: data keluarga tetap perlu diperlakukan sebagai data privat dan tidak otomatis bebas digunakan di luar izin keluarga.

---

## 🤲 Dedikasi

Aplikasi ini didedikasikan untuk:

- keluarga besar **Bani Raukhan – Rafi**;
- para orang tua, leluhur, dan pendahulu keluarga;
- generasi muda agar tetap mengenal akar keluarganya;
- siapa pun yang ingin menjaga silaturahmi melalui teknologi;
- ummat yang ingin mendokumentasikan nasab, sejarah keluarga, dan ikatan persaudaraan secara baik.

Semoga setiap nama yang tertulis menjadi pengingat untuk mendoakan, menyambung silaturahmi, dan meneruskan kebaikan.

---

<p align="center">
  <strong>Dibuat dengan niat baik, dirawat dengan adab, dan dipersembahkan untuk keluarga serta ummat.</strong>
</p>

<p align="center">
  🌳 Bani Raukhan – Rafi · Silsilah · Silaturahmi · Arsip Keluarga Digital
</p>
