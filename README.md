# 📊 Executive Dashboard PLI BC BOGOR

> Dashboard monitoring terintegrasi untuk Penyuluhan & Layanan Informasi Bea Cukai Bogor

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Made with](https://img.shields.io/badge/Made%20with-HTML%2FCSS%2FJS-orange)]()

## 📋 Gambaran Umum

Dashboard eksekutif yang terintegrasi dengan **Google Sheets** untuk memonitor:

- ✅ Layanan Informasi & Manajemen Risiko
- ✅ Penyuluhan & Edukasi Publik
- ✅ Komunikasi Forensik & Analisis Framing
- ✅ Publikasi & Content Analytics
- ✅ Stakeholder Mapping

## 🚀 Demo

> **Catatan:** Dashboard ini menggunakan Google Sheets sebagai database. Untuk keperluan demo, sistem akan otomatis beralih ke **Mode Demo** jika koneksi ke Google Sheets gagal.

| Mode | Keterangan |
|------|-------------|
| **Online** | Terhubung ke Google Sheets (data real) |
| **Demo** | Menampilkan data contoh (tanpa koneksi) |

## 📁 Struktur Dashboard

```

root/
├── index.html                 # 🏠 Executive Dashboard (Main)
├── stakeholder.html           # 🤝 Stakeholder Mapping
└── sub-dashboard/
├── layanan.html          # 📞 Layanan Informasi
├── penyuluhan.html       # 🎓 Penyuluhan & Edukasi
├── forensik.html         # 📰 Komunikasi Forensik
└── publikasi.html        # 📢 Publikasi & Content Analytics

```

## ✨ Fitur Utama

### 1. Executive Dashboard (`index.html`)
| Fitur | Deskripsi |
|-------|-----------|
| Hero Section | Situasi terkini, kerugian terhindar, hotspot darurat |
| Navigation Cards | 5 sub-dashboard dengan ringkasan KPI |
| SKM Card | Nilai SKM terbaru dengan status deadline |
| Peta Interaktif | Sebaran aduan rokok ilegal (Leaflet) |
| Trigger Aksi | Peringatan dini berdasarkan dampak risiko |
| Generate Laporan | Export PDF / copy ke clipboard |

### 2. Layanan Informasi (`layanan.html`)
- Tren layanan per channel (WhatsApp, Front Desk, Facebook, dll)
- Tren kategori layanan (IMEI, Informasi, Pengaduan)
- Dampak risiko dengan threshold alert
- Insight analisis otomatis

### 3. Penyuluhan (`penyuluhan.html`)
- Total peserta YTD & indeks efektivitas
- Sosialisasi per topik (PMI, DBHCT, Peraturan, UMKM)
- Kegiatan Intimacy & CVC chart
- Linimasa kegiatan

### 4. Komunikasi Forensik (`forensik.html`)
- Matriks mitigasi (Level + Trafik + Tipe Media)
- Analisis framing & sentimen
- Daftar prioritas penanganan
- Insight berbasis teori komunikasi

### 5. Publikasi (`publikasi.html`)
- Total jangkauan YTD: **17.841**
- Efektivitas channel (IG, FB, X)
- Top 5 konten terbaik
- Rekomendasi strategi

### 6. Stakeholder (`stakeholder.html`)
- Matriks Prioritas vs Komunikasi
- Daftar stakeholder dengan rekomendasi

## 🛠️ Teknologi

| Teknologi | Kegunaan |
|-----------|----------|
| HTML5/CSS3 | Struktur & styling |
| JavaScript ES6 | Logika bisnis |
| Chart.js 4.4.0 | Visualisasi data |
| Leaflet 1.9.4 | Peta interaktif |
| Font Awesome 6.0 | Ikon UI |
| html2pdf.js | Export PDF |

## 🔗 Integrasi Google Sheets

Dashboard terintegrasi dengan Google Sheets via **Google Apps Script API**:

```

https://script.google.com/macros/s/AKfycbywHucFlh5aJAPbVMUWGA_REGi9lrax2IjYMbPtHJoMTIYqIriHeRFnjygQMbICNJphhg/exec

```

### Sheet yang Digunakan:

| Sheet Name | Fungsi |
|------------|--------|
| `LAYANAN` | Data layanan informasi |
| `CHANNEL` | Tren layanan per channel |
| `RATA_RATA` | Rata-rata waktu layanan |
| `DAMPAK_RISIKO` | Dampak risiko per kategori |
| `HOTSPOT` | Data hotspot rokok ilegal |
| `ADUAN` | Aduan masyarakat (dengan koordinat) |
| `PENYULUHAN` | Data kegiatan penyuluhan |
| `SKM_DATA` | Survey Kepuasan Masyarakat |
| `CVC_DATA` | Customs Visit Customer |
| `PUBLIKASI` | Data publikasi engagement |
| `FORENSIK` | Pemberitaan media |
| `STAKEHOLDER` | Data stakeholder |
| `KATEGORI_LAYANAN` | Kategori pertanyaan layanan |

## 🚦 Cara Menjalankan

### Prasyarat
- Koneksi internet (untuk akses CDN & API)
- Web browser modern (Chrome, Firefox, Edge)

### Langkah-langkah

```bash
# 1. Clone repository
git clone https://github.com/username/pli-dashboard.git

# 2. Buka folder
cd pli-dashboard

# 3. Jalankan dengan Live Server (disarankan)
# Gunakan VS Code extension "Live Server" atau:
npx live-server

# 4. Atau buka langsung file index.html di browser
```

⚠️ Catatan: Jika membuka langsung (file://), beberapa fitur fetch API mungkin terbatas. Gunakan Live Server untuk hasil optimal.

🔧 Konfigurasi

Mode Demo vs Online

Mode Kondisi Tampilan
Online Koneksi ke Google Sheets berhasil Data real
Demo Koneksi gagal / offline Data contoh

Dashboard akan otomatis menampilkan indikator status di pojok kanan atas.

Private Google Sheets

Dashboard tetap bisa membaca Google Sheet meskipun statusnya PRIVATE, selama:

1. Google Apps Script dideploy dengan Execute as: Me
2. Web App access diatur ke Anyone

📊 Screenshot

Dashboard Preview
Executive Dashboard https://via.placeholder.com/400x200?text=Executive+Dashboard
Layanan Informasi https://via.placeholder.com/400x200?text=Layanan
Komunikasi Forensik https://via.placeholder.com/400x200?text=Forensik

(Tambahkan screenshot asli dari dashboard Anda)

👥 Kontribusi

Kontribusi sangat diterima! Silakan:

1. Fork repository
2. Buat branch fitur (git checkout -b fitur-anda)
3. Commit perubahan (git commit -m 'Menambah fitur X')
4. Push ke branch (git push origin fitur-anda)
5. Buat Pull Request

📝 Lisensi

Distributed under the MIT License. See LICENSE for more information.

📞 Kontak

PLI BC BOGOR
Copyright © 2026 | FOK 1.5

---

⭐️ Show Your Support

Berikan ⭐️ jika proyek ini bermanfaat!

```

---

## 📋 Cara Menggunakan

1. **Copy** semua kode di atas
2. **Paste** ke file `README.md` di repository GitHub Anda
3. **Edit** bagian yang perlu disesuaikan:
   - Ganti `username` di link clone
   - Tambahkan screenshot asli (hapus placeholder)
   - Sesuaikan kontak jika perlu
4. **Save** dan push ke GitHub

## 🖼️ Saran Tambahan Screenshot

Jika ingin menambahkan screenshot asli, gunakan kode ini setelah upload gambar:

```markdown
## 📸 Screenshot

### Executive Dashboard
![Executive Dashboard](screenshots/executive.png)

### Layanan Informasi
![Layanan Informasi](screenshots/layanan.png)

### Komunikasi Forensik
![Forensik](screenshots/forensik.png)
```

Buat folder screenshots/ di repository Anda dan masukkan gambar-gambar tersebut.
