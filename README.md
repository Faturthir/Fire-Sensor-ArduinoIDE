# ESP8266 Fire and Distance Monitoring System

Proyek ini menggunakan ESP8266 untuk mendeteksi keberadaan api dan mengukur jarak menggunakan sensor ultrasonik. Data dikirimkan ke Firebase Realtime Database untuk pemantauan secara real-time.

## 🚀 Fitur
- Mendeteksi keberadaan api menggunakan sensor flame
- Mengukur jarak menggunakan sensor ultrasonik HC-SR04
- Menampilkan status di LCD I2C 16x2
- Menggunakan buzzer sebagai alarm jika jarak berbahaya
- Mengirimkan data ke Firebase Realtime Database

## 🛠️ Perangkat yang Digunakan
- ESP8266 (misalnya, NodeMCU)
- Sensor Flame
- Sensor Ultrasonik HC-SR04
- LCD I2C 16x2
- Buzzer
- Kabel jumper

## 📥 Instalasi Perpustakaan
Sebelum mengunggah kode, pastikan Anda telah menginstal pustaka berikut di Arduino IDE:
- `ESP8266WiFi` (untuk koneksi Wi-Fi)
- `Firebase_ESP_Client` (untuk komunikasi dengan Firebase)
- `LiquidCrystal_I2C` (untuk LCD)

### Cara Menginstal:
1. Buka Arduino IDE.
2. Pergi ke **Sketch** > **Include Library** > **Manage Libraries**.
3. Cari pustaka di atas, lalu klik **Install**.

## 🔌 Wiring
Hubungkan komponen sesuai dengan tabel berikut:

| Komponen | ESP8266 |
|----------|---------|
| Flame Sensor | D5 |
| Trig (Ultrasonik) | D4 |
| Echo (Ultrasonik) | D3 |
| Buzzer | D8 |
| LCD I2C SDA | D2 |
| LCD I2C SCL | D1 |

## 🔧 Konfigurasi Wi-Fi dan Firebase
Ubah SSID dan password Wi-Fi, serta API Key dan Database URL Firebase pada kode berikut:
```cpp
#define WIFI_SSID "Nama_WiFi"
#define WIFI_PASSWORD "Password_WiFi"
#define API_KEY "API_KEY_FIREBASE"
#define DATABASE_URL "URL_FIREBASE"
```

## 📌 Cara Penggunaan
1. Sambungkan ESP8266 ke komputer menggunakan kabel USB.
2. Buka Arduino IDE dan unggah kode.
3. Buka **Serial Monitor** (Baudrate: 9600).
4. Tempelkan api pada sensor flame untuk mendeteksi keberadaannya.
5. Pantau jarak dari objek menggunakan sensor ultrasonik.
6. Lihat data di LCD dan Firebase.

## 🔍 Output Contoh
Saat sistem mendeteksi api dan jarak berbahaya, Serial Monitor akan menampilkan:
```
BAHAYA Jangan mendekat!!!
40 cm JARAK BERBAHAYA
Flame detected!
```
LCD akan menampilkan:
```
BAHAYA!
40 cm JANGAN MENDEKAT
```
Jika tidak ada api, LCD akan menampilkan:
```
SITUASI AMAN
```

## 📜 Lisensi
Proyek ini bersifat open-source dan dapat digunakan untuk keperluan edukasi atau pengembangan lebih lanjut.

---
⭐ Jangan lupa berikan bintang jika proyek ini membantu Anda!

