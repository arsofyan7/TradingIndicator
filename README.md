# 📈 TradingView Custom Indicators Collection

Repository ini adalah koleksi pribadi indikator dan strategi untuk **TradingView** (Pine Script v5). Fokus utama dari koleksi ini adalah menggabungkan **Price Action**, **Smart Money Concepts (SMC)**, dan **Momentum** untuk membantu trader mengambil keputusan yang lebih objektif.

---

## 📋 Daftar Indikator

### 1. Swing Reversal Pro (SMC Edition) - v1.2
Indikator *all-in-one* chart overlay untuk menangkap momen pembalikan arah (reversal), lengkap dengan filter tren dan struktur market institusi.

#### a. Fitur Utama
* **Auto Calculator:** Menghitung Entry, SL (Swing Low), dan TP (Risk:Reward).
* **SMC Visuals:** Menampilkan **Order Block (OB)** dan **Fair Value Gap (FVG)**.
* **Smart RSI Filter:** Filter Entry berdasarkan momentum (Moderate/Sniper).
* **Time-Locked:** Visual anti-geser/anti-lag.

---

### 2. Combo: Trend & Volume Engine (TVE) - v1.0
Indikator Oscillator (Panel Bawah) yang menggabungkan analisis Tren (MACD) dengan Arus Dana (Volume).

#### a. Fitur Utama
* **4-Color Histogram:** Membedakan tren bervolume besar (Valid) vs kecil (Fake).
* **Golden Cross Hunter:** Label "GC" saat momentum positif di area diskon.
* **Simplified View:** Hemat tempat, 2 indikator dalam 1 panel.

---

### 3. Custom Screener: The Hunter - v1.2 (LQ45 Auto-Sort)
Dashboard monitoring *real-time* untuk memantau 40 saham LQ45 sekaligus dalam satu tabel.

#### a. Fitur Utama
* **Auto-Sorting:** Otomatis mengurutkan saham dengan sinyal **BUY** ke baris paling atas.
* **Smart Logic:** Menggabungkan logika Swing Reversal + RSI + Volume Breakout.
* **Efficiency:** Memantau 40 saham *Blue Chip* tanpa perlu ganti chart.

---

## ⚔️ SOP Trading (Workflow Akun Gratis)

Karena akun TradingView Basic dibatasi maksimal **2 Indikator**, gunakan alur kerja berikut:

### 📡 PHASE 1: Mode Radar (Scanning)

**Setup Indikator:**
1.  **Swing Reversal Pro** (Chart)
2.  **The Hunter Screener** (Overlay)

**Filter Saham "Kotor"**
1.  **Filter seperti File Screenshot**
2.  **Masukkan saham yang Analyst Ratingnya Buy/Strong Buy ke dalam Indikator The Hunter Screener**

**Langkah-langkah:**
1.  Pantau Tabel Screener di pojok kanan atas.
2.  Fokus hanya pada baris paling atas (Ranking 1-5).
3.  Cari yang statusnya **"BUY" (Hijau)**.
4.  Jika ketemu, klik sahamnya. Lihat di chart apakah sinyal *Swing Reversal* (Label Buy & Garis TP/SL) sudah muncul dan bentuk candle-nya bagus.
5.  **Cek Kolom Vol di Screener:** Pastikan bernilai **"H"** (High). Jika "L", waspada sinyal lemah.

### 🎯 PHASE 2: Mode Sniper (Validasi Akhir)
*Lakukan ini hanya jika Anda sudah menemukan kandidat BUY yang potensial dari Fase 1.*

**Setup Indikator:**
1.  **Matikan/Hapus** "The Hunter Screener".
2.  **Tambahkan** "Combo TVE" (Panel Bawah).
*(Posisi Swing Reversal tetap nyala)*

**Langkah-langkah:**
1.  Lihat panel bawah (Combo TVE).
2.  Pastikan Histogram berwarna **Hijau Solid (Terang)**. Ini konfirmasi bahwa kenaikan harga didukung uang besar (Bandar).
3.  Jika Histogram berwarna **Pudar** atau malah Merah, batalkan niat entry (kemungkinan *False Break*).
4.  Jika Valid, pasang order antrian sesuai angka **Entry** dan **SL** yang tertera di label Swing Reversal.

---

## 🛠️ Cara Instalasi

1.  Buka chart **TradingView**.
2.  Buka panel **Pine Editor** di bagian bawah.
3.  Pilih file script `.pine` dari repository ini, Copy semua kodenya.
4.  Paste ke Pine Editor, lalu klik **Simpan** dan **Tambahkan ke Chart**.

---

## 🚀 Quick Links (Akses Cepat)

* **📘 [SOP Trading Mingguan (Full Guide)](SOP_Trading_Mingguan.md)** *(Bisa jadi refeensi sebelum mulai trading - Inget Konsistensi adalah Kunci)*

---
## ⚠️ Disclaimer
Script ini dibuat sebagai alat bantu analisis (*Trading Assistant*). Segala keputusan keuntungan dan kerugian adalah tanggung jawab penuh pengguna. Selalu gunakan Money Management yang baik.