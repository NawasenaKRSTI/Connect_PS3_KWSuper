**Judul Proyek:**
Integrasi Stik PS3 KW Super dengan ESP32 melalui Koneksi Bluetooth untuk Kendali Robotika

**Tim:**
Nawasena – Brawijaya Robotic

**Deskripsi Singkat:**
Proyek ini bertujuan untuk menghubungkan stik PS3 KW Super dengan mikrokontroler ESP32 menggunakan koneksi Bluetooth, memungkinkan kendali nirkabel pada aplikasi robotika.

---

## 1. 📚 Latar Belakang

Penggunaan stik PS3 sebagai perangkat input dalam sistem robotika menawarkan solusi ekonomis dan praktis. Namun, stik PS3 KW Super, yang banyak tersedia di pasaran dengan harga terjangkau, seringkali menghadapi kendala kompatibilitas. Proyek ini bertujuan untuk mengatasi tantangan tersebut dengan mengembangkan metode koneksi yang andal antara stik PS3 KW Super dan ESP32.

---

## 2. 🎯 Tujuan

* Mengembangkan metode koneksi antara stik PS3 KW Super dan ESP32 melalui Bluetooth.
* Mengintegrasikan stik PS3 sebagai perangkat input dalam sistem kendali robotika.
* Menyediakan panduan praktis bagi pengguna lain untuk mereplikasi proses ini.

---

## 3. 🔬 Metodologi

* **Perangkat Keras:**

  * Stik PS3 KW Super
  * ESP32 dengan modul Bluetooth
  * Kabel Mini USB

* **Perangkat Lunak:**

  * Arduino IDE dengan dukungan board ESP32
  * SCP Toolkit untuk pairing stik PS3
  * Library PS3 untuk ESP32

* **Langkah-langkah:**

  1. Menginstal SCP Toolkit dan melakukan pairing stik PS3 dengan ESP32.
  2. Menginstal library PS3 pada Arduino IDE.
  3. Mengunggah kode program ke ESP32 untuk menghubungkan dan membaca input dari stik PS3.

---

## 4. ⚙️ Perancangan Sistem

Sistem terdiri dari stik PS3 KW Super yang terhubung secara nirkabel ke ESP32 melalui Bluetooth. ESP32 menerima input dari stik PS3 dan dapat digunakan untuk mengendalikan aktuator atau sistem robotika lainnya.

---

## 5. 🧪 Eksperimen & Evaluasi

* **Pengujian Koneksi:**

  * Memastikan stik PS3 dapat terhubung ke ESP32 dan mengirimkan data input.
  * Mengamati stabilitas koneksi dan responsivitas input.

* **Evaluasi:**

  * Menilai keandalan koneksi dalam berbagai kondisi.
  * Menguji kompatibilitas dengan berbagai model stik PS3 KW Super.

---

## 6. 📊 Analisis & Pembahasan

Hasil pengujian menunjukkan bahwa stik PS3 KW Super dapat terhubung dengan ESP32 melalui Bluetooth dengan menggunakan SCP Toolkit dan library PS3 yang sesuai. Namun, beberapa model stik mungkin memerlukan penyesuaian tambahan untuk memastikan kompatibilitas penuh.

---

## 7. ✅ Kesimpulan & Rencana Lanjut

* **Kesimpulan:**

  * Metode yang dikembangkan berhasil menghubungkan stik PS3 KW Super dengan ESP32 melalui Bluetooth.
  * Sistem ini dapat digunakan sebagai solusi kendali nirkabel dalam aplikasi robotika.

* **Rencana Lanjut:**

  * Mengembangkan antarmuka pengguna untuk konfigurasi stik.
  * Menguji integrasi dengan berbagai platform robotika.
  * Menyusun dokumentasi lebih lanjut untuk mendukung replikasi oleh pengguna lain.

---

## 8. 🕒 Riwayat Revisi

| Versi | Tanggal    | Deskripsi Perubahan    | Penulis              |
| ----- | ---------- | ---------------------- | -------------------- |
| 1.0   | 2025-05-01 | Draft awal dokumentasi | WenaHarle |

---
