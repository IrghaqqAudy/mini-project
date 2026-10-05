# Mini Project: Automation Fetch Data WeatherAPI

Proyek ini merupakan latihan *mini project* dalam program belajar **AI Automation**. Tujuan utama proyek ini adalah melakukan otomatisasi pengambilan data prakiraan cuaca (*weather forecast*) menggunakan layanan **WeatherAPI** via Python, serta menerapkan manajemen *environment variable* untuk keamanan API Key.

---

## 📌 Fitur Utama

- **Integrasi API**: Mengambil data prakiraan cuaca 3 harian dari WeatherAPI.
- **Keamanan Konfigurasi**: Menggunakan file `.env` dan pustaka `python-dotenv` agar API Key tidak terekspos di dalam kode program (*hardcoded*).
- **Penanganan HTTP Request**: Memanfaatkan pustaka `requests` dengan batas waktu pemanggilan (*timeout*) dan validasi *status code*.

---

## 🛠️ Prasyarat & Instalasi

Pastikan kamu sudah menginstal Python (versi 3.8+) di perangkatmu.

### 1. Kloning Repository / Penyiapan Direktori
Unduh atau tempatkan berkas project di folder kerja kamu.

### 2. Instalasi Pustaka (Dependencies)
Jalankan perintah berikut pada terminal atau sel notebook:

```bash
pip install requests python-dotenv pandas
```

---

## 🔑 Konfigurasi Environment (`.env`)

Buatlah sebuah berkas bernama `.env` pada direktori utama proyek, lalu tambahkan API Key dari WeatherAPI milikmu dengan format berikut:

```env
CUACA_API_KEY=masukkan_api_key_kamu_di_sini
```

> ⚠️ **Catatan**: Pastikan untuk tidak mencantumkan file `.env` ini ke dalam version control (seperti Git/GitHub) demi menjaga kerahasiaan API Key.

---

## 🚀 Cara Menjalankan Kode

1. Buka berkas notebook (`.ipynb`) atau script Python kamu.
2. Jalankan sel pertama untuk memuat library dan memeriksa ketersediaan API Key:
   ```python
   import os
   import requests
   from dotenv import load_dotenv

   load_dotenv()
   API_KEY = os.getenv("CUACA_API_KEY")
   ```
3. Jalankan sel pengambilan data untuk memperoleh prakiraan cuaca wilayah Jakarta selama 3 hari ke depan.

---

## 📊 Contoh Output Program

Jika API Key valid dan koneksi berhasil, luaran (*output*) pada konsol akan menampilkan:

```text
API key berhasil dimuat.
Status Code: 200
Lokasi: Jakarta , Indonesia
Jumlah hari forecast: 3
```

---

*Disusun sebagai bagian dari penugasan Mini Project AI Automation.*
