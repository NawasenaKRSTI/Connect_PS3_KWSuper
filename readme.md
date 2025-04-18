# 🎮 ESP32 + PS3 KW Super Controller

[![ESP32](https://img.shields.io/badge/Board-ESP32-blue.svg)](https://www.espressif.com/en/products/socs/esp32)
[![Arduino IDE](https://img.shields.io/badge/IDE-Arduino-orange.svg)](https://www.arduino.cc/en/software)
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

Tutorial ini menunjukkan cara **menghubungkan ESP32 dengan stick PS3 KW Super** — stick 50 ribuan yang kamu temuin di marketplace tapi ternyata bisa dipakai juga kalau tau caranya 😎

> _"Scam Cik, tapi bisa dibikin jalan!"_

---

## 🧭 Table of Contents

- [🧰 Alat dan Bahan](#-alat-dan-bahan)
- [⚙️ Setup ESP32](#️-setup-esp32)
  - [1. Install Library PS3](#1-install-library-ps3-controller-host-by-jeffrey-van-pernis)
  - [2. Cek MAC Address ESP32](#2-cek-mac-address-bluetooth-esp32)
- [🔌 Program Koneksi ke PS3](#-program-koneksi-ke-ps3)
- [🛠️ Setup Kontroller PS3](#️-setup-kontroller-ps3)
  - [1. Install SCP Toolkit](#1-installasi-scp-toolkit)
  - [2. Pairing MAC Stick ke ESP32](#2-setup-mac-bluetooth-kontroller)
- [✅ Cek Koneksi](#-cek-koneksi)
- [🏁 Penutup](#-penutup)

---

## 🧰 Alat dan Bahan

- 🎮 Stick PS3 **KW Super** dari marketplace
- 🔌 Kabel Mini USB
- 💻 **Arduino IDE** (plus Board ESP32 sudah ditambahkan)
- 📟 **ESP32** (pastikan ada Bluetooth-nya)
- 🧰 **SCP Toolkit**  
  ➤ [Download dari GitHub](https://github.com/nefarius/ScpToolkit/releases/tag/v1.7.277.16103-BETA)

---

## ⚙️ Setup ESP32

### 1. Install Library PS3 Controller Host by Jeffrey van Pernis

> Cari dan install melalui Library Manager Arduino IDE:  
> `Ps3Controller by Jeffrey van Pernis`

### 2. Cek MAC Address Bluetooth ESP32

Upload kode berikut ke ESP32 kamu:

```cpp
#include "esp_bt_main.h"
#include "esp_bt_device.h"
 
bool initBluetooth()
{
  if (!btStart()) {
    Serial.println("Failed to initialize controller");
    return false;
  }
 
  if (esp_bluedroid_init() != ESP_OK) {
    Serial.println("Failed to initialize bluedroid");
    return false;
  }
 
  if (esp_bluedroid_enable() != ESP_OK) {
    Serial.println("Failed to enable bluedroid");
    return false;
  }
 
}
 
void printDeviceAddress() {
 
  const uint8_t* point = esp_bt_dev_get_address();
 
  for (int i = 0; i < 6; i++) {
 
    char str[3];
 
    sprintf(str, "%02X", (int)point[i]);
    Serial.print(str);
 
    if (i < 5){
      Serial.print(":");
    }
 
  }
}
 
void setup() {
  Serial.begin(115200);
 
  initBluetooth();
  printDeviceAddress();
}
 
void loop() {}
```

📝 Buka **Serial Monitor** dan **catat MAC address** yang ditampilkan  
📸 ![Cek MAC](images/cek_mac.png)

---

## 🔌 Program Koneksi ke PS3

Upload kode ini ke ESP32 (ganti MAC sesuai MAC address ESP32 kamu):

```cpp
#include <Ps3Controller.h>

void notify()
{
    if( Ps3.data.button.cross ){
        Serial.println("Pressing the cross button");
    }

    if( Ps3.data.button.square ){
        Serial.println("Pressing the square button");
    }

    if( Ps3.data.button.triangle ){
        Serial.println("Pressing the triangle button");
    }

    if( Ps3.data.button.circle ){
        Serial.println("Pressing the circle button");
    }
}

void onConnect(){
  Serial.println("Connected!.");
}

void setup()
{
    Serial.begin(115200);
    Ps3.attach(notify);
    Ps3.attachOnConnect(onConnect);
    Ps3.begin("78:42:1C:6D:77:B6");
    Serial.println("Ready.");
}

void loop()
{
}

```

---

## 🛠️ Setup Kontroller PS3

### 1. Installasi SCP Toolkit

1. Jalankan `ScpToolkit_Setup.exe`
2. Checklist "I agree" dan tekan **Next**  
   ![Install Step 1](images/Install_1.png)
3. Pilih **Bluetooth Pair Utility** (opsional: install semua)  
   ![Install Step 2](images/Install_2.png)

### 2. Setup MAC Bluetooth Kontroller

1. Buka **ScpToolkit Bluetooth Pair Utility (legacy)**  
   ![Pairing Tool](images/tampilan_awal.png)

2. Colok stick ke laptop via kabel mini USB  
   💬 Akan muncul notifikasi  
   ![Notifikasi](images/notif.png)

3. Di jendela Pairing akan muncul:
   - **Local**: MAC stick PS3
   - **Remote**: MAC target (ESP32 kamu)  
   ![MAC muncul](images/mac_muncul.png)

   > Jika belum muncul, tekan **PS + Start** di stick

4. Masukkan MAC ESP32 kamu ke kolom Remote lalu klik **Set**  
   ![Set MAC](images/set_mac.png)

5. Lepas kabel dari stick.

---

## ✅ Cek Koneksi

1. Buka Serial Monitor di Arduino IDE
2. Tekan tombol **RST** di ESP32
3. Tekan tombol **PS** di stick PS3

🎉 Kalau berhasil, kamu akan lihat teks seperti ini:
![Koneksi Berhasil](images/koneksi_berhasil.png)

---

## 🏁 Penutup

> **Selamat!** Kamu berhasil menghubungkan stick PS3 KW Super ke ESP32 dengan Bluetooth.

> _"Tidak ada yang tidak mungkin, selama tidak melanggar hukum alam."_

---

## 🪪 Lisensi

Proyek ini menggunakan lisensi [MIT License](LICENSE)

---

```
