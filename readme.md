## 📘 Tentang Riset

* **Tim/Divisi:** KRSTI / NAWASENA
* **Tipe Perangkat:** ESP32
* **Tanggal Mulai - Selesai:** 12/04/2025 – 27/04/2025
* **Status:** ✅ *Selesai*

---

## 📚 Latar Belakang

Proyek ini bertujuan untuk menghubungkan ESP32 dengan stik PS3 KW Super, sebuah stik murah yang tersedia di pasaran. Meskipun harganya terjangkau, stik ini dapat digunakan secara efektif jika dikonfigurasi dengan benar.

---

## 🎯 Tujuan

* Membuat koneksi antara ESP32 dan stik PS3 KW Super melalui Bluetooth.
* Mengembangkan firmware pada ESP32 untuk menerima input dari stik PS3.
* Menguji kestabilan dan responsivitas koneksi antara perangkat.

---

## 📁 Struktur Folder

Struktur direktori proyek untuk memudahkan navigasi:

```
📦 Connect_PS3_KWSuper
├── 📂 images             → Gambar pendukung
├── 📜 LICENSE            → Lisensi MIT
└── 📜 readme.md          → Dokumentasi proyek
```

---

## 🔬 Metodologi

Tabel berikut merinci tools dan teknologi utama yang digunakan dalam riset ini:

| Komponen           | Deskripsi               | Versi  |  
| ------------------ | ----------------------- | ------------- |
| Platform           | ESP32 DevModule         | 3.0.0         |  
| Bahasa Pemrograman | C++                     | -             |  
| IDE                | Arduino IDE             | 2.3.0         | 
| Komunikasi         | Bluetooth               | -             | 
| Dependensi         | Library PS3 untuk ESP32 | -             |  
| Framework          | Arduino Framework       | 3.0.0         |  


* Menggunakan SCP Toolkit untuk pairing stik PS3 dengan ESP32.
* Implementasi kode pada ESP32 untuk menerima dan memproses input dari stik.

---

## ⚙️ Perancangan Sistem

Desain sistem melibatkan:

* ESP32 dengan modul Bluetooth sebagai penerima sinyal dari stik PS3.
* Stik PS3 KW Super yang terhubung melalui Bluetooth ke ESP32.
* Diagram arsitektur dan blok sistem dapat ditambahkan di folder.

---

## 🧪 Eksperimen & Evaluasi

Proses pengujian meliputi:

* Pairing stik PS3 dengan ESP32 menggunakan SCP Toolkit.
* Mengunggah firmware ke ESP32 dan mengamati respons terhadap input dari stik.
* Mencatat kestabilan koneksi dan responsivitas sistem.

---

## 📊 Analisis & Pembahasan

Hasil eksperimen menunjukkan bahwa:

* Stik PS3 KW Super dapat terhubung dengan ESP32 melalui Bluetooth.
* Respons sistem terhadap input cukup stabil, meskipun terdapat beberapa delay yang perlu dioptimalkan.
* Diperlukan penyesuaian lebih lanjut untuk meningkatkan performa dan kompatibilitas.

---

## ✅ Kesimpulan & Rencana Lanjut

* Tujuan utama riset telah tercapai dengan berhasilnya koneksi antara ESP32 dan stik PS3 KW Super.
* Kontribusi utama adalah dokumentasi langkah-langkah koneksi dan implementasi kode pada ESP32.
* Rencana selanjutnya meliputi optimasi kode untuk mengurangi delay dan pengujian dengan berbagai jenis stik PS3 lainnya.

---

## 🕒 Riwayat Revisi

| Versi | Tanggal    | Deskripsi Perubahan | Penulis | Email                |
| ----- | ---------- | ------------------- | ------- | --------------------- |
| 1.0   | 12/04/2025 | Dokumentasi awal    | WenaHarle | madewena0403@gmail.com    |
| 1.1   | 27/04/2025 | Penambahan analisis | WenaHarle | madewena0403@gmail.com  |

