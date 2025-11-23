TradingIndicator

# 📈 TradingView Custom Indicators Collection

Repository ini adalah koleksi pribadi indikator dan strategi untuk **TradingView** (Pine Script v5). Fokus utama dari koleksi ini adalah menggabungkan **Price Action**, **Smart Money Concepts (SMC)**, dan **Momentum** untuk membantu trader mengambil keputusan yang lebih objektif.

---

## 📋 Daftar Indikator

### 1. Swing Reversal Pro (SMC Edition) - v1.2
Indikator *all-in-one* untuk menangkap momen pembalikan arah (reversal) di pucuk atau lembah, lengkap dengan fitur filter tren dan struktur market institusi.

#### a. Fitur Utama
* **Auto Calculator:** Otomatis menghitung dan menampilkan Entry Price, Stop Loss (di ujung Swing), dan Take Profit (berdasarkan Risk:Reward Ratio).
* **SMC Visuals:** Menampilkan **Order Block (OB)** sebagai area pertahanan dan **Fair Value Gap (FVG)** sebagai magnet target harga.
* **Smart RSI Filter:** Mencegah entry sembarangan dengan filter momentum (Moderate & Sniper Mode).
* **Time-Locked Graphics:** Label dan garis dikunci pada koordinat waktu absolut, sehingga visual tidak bergeser (anti-lag) saat chart di-zoom atau digeser.
* **Anti-Spam Logic:** Menggunakan algoritma *Swing Lookback* yang dapat disesuaikan untuk mengurangi sinyal palsu saat market *choppy*.

#### b. Cara Penggunaan
1.  **Tunggu Konfirmasi Close:** Jangan entry saat candle sinyal masih berjalan. Tunggu hingga candle close dan label entry muncul permanen.
2.  **Cek Konteks SMC:**
    * Lihat ke kiri, apakah sinyal muncul di dekat area Support/Resist kuat?
    * Perhatikan kotak **Order Block** (Hijau/Merah) di belakang sinyal sebagai area aman untuk menaruh Stop Loss.
    * Perhatikan kotak **FVG** (Kuning/Ungu) di depan sebagai target harga (Take Profit).
3.  **Eksekusi:** Pasang order sesuai angka Entry, TP, dan SL yang tertera di label.

#### c. Panduan Setting
* **Swing Lookback Period:**
    * Set ke **3** (Recommended) untuk gaya trading agresif/scalping (Sinyal muncul cepat di ujung).
    * Set ke **5-10** untuk gaya trading swing santai (Sinyal lebih lambat tapi terkonfirmasi).
* **RSI Filter Mode:**
    * `Off`: Menampilkan semua sinyal Price Action murni.
    * `Moderate (<50)`: Buy hanya jika harga masih di area murah/netral.
    * `Sniper (<30)`: Buy hanya jika harga sudah *Oversold* parah (Potensi reward besar).
* **SMC Settings:** Aktifkan/Nonaktifkan *Show Order Block* atau *Show FVG* sesuai kebutuhan kebersihan chart.

---

### 2. Combo: Trend & Volume Engine (TVE) 
Indikator Oscillator (Panel Bawah) yang menggabungkan analisis Tren (MACD) dengan analisis Arus Dana (Volume) dalam satu tampilan visual.

#### a. Fitur Utama
* **4-Color Histogram:** Membedakan tren yang didukung volume besar (Valid) dengan tren volume kecil (Fake).
    * *Hijau Solid:* Bullish + High Volume (Strong Momentum).
    * *Hijau Pudar:* Bullish + Low Volume (Weak Momentum).
    * *Merah Solid:* Bearish + High Volume (Strong Dumping).
    * *Merah Pudar:* Bearish + Low Volume (Weak Dumping).
* **Golden Cross Hunter:** Memberikan label "GC" khusus saat MACD melakukan *crossover* di area negatif (area diskon), sesuai pakem *Buy on Weakness*.
* **Simplified View:** Menghilangkan kebutuhan untuk memasang indikator Volume terpisah yang sering memakan tempat di layar HP.

#### b. Cara Penggunaan (Kombinasi dengan Swing Reversal)
1.  Tunggu sinyal **BUY** dari indikator utama (Chart Atas).
2.  Konfirmasi dengan melihat ke bawah (Combo TVE):
    * Apakah muncul label **GC**? (Nilai Plus).
    * Apakah Histogram berwarna **Hijau Solid**? (Wajib).
3.  Jika sinyal atas BUY tapi Histogram bawah cuma "Hijau Pudar" atau malah merah, sebaiknya kurangi porsi lot atau *wait and see*.

#### c. Panduan Setting
* **Volume Threshold:** (Default: 1.0). Batas toleransi volume. Naikkan ke 1.5 jika ingin filter "High Volume" yang lebih ketat (hanya volume meledak yang dianggap valid).
* **MACD Settings:** Default (12, 26, 9). Bisa disesuaikan dengan preferensi trading masing-masing.
---

## 🛠️ Cara Instalasi (Global)

1.  Buka chart **TradingView**.
2.  Buka panel **Pine Editor** di bagian bawah.
3.  Pilih file script `.pine` dari repository ini, lalu **Copy** semua kodenya.
4.  **Paste** ke dalam Pine Editor.
5.  Klik **Simpan (Save)** dan pilih **Tambahkan ke Chart (Add to Chart)**.

---

## ⚠️ Disclaimer
Script ini dibuat sebagai alat bantu analisis (*Trading Assistant*). Segala keputusan keuntungan dan kerugian adalah tanggung jawab penuh pengguna. Selalu gunakan Money Management yang baik.