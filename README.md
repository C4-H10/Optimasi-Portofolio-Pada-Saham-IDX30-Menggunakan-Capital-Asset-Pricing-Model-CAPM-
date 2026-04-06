# Optimasi Portofolio Saham IDX30 Menggunakan Metode CAPM
## Deskripsi Proyek

Program ini dirancang untuk membantu investor dalam melakukan perhitungan teknis guna menentukan alokasi bobot modal yang optimal. Analisis dilakukan dengan memproses data historis harga saham dan membandingkannya dengan pergerakan pasar (IHSG) serta instrumen bebas risiko (BI Rate).

## Tahapan Analisis

Proses pengolahan data dalam repositori ini meliputi beberapa langkah utama:

1. Konfigurasi Parameter: Penentuan periode waktu analisis, daftar ticker saham IDX30, dan input tingkat suku bunga bebas risiko.
2. Akuisisi Data: Pengambilan data harga penutupan harian secara otomatis melalui API Yahoo Finance.
3. Perhitungan Imbal Hasil: Transformasi harga saham menjadi nilai log return harian.
4. Estimasi Variabel CAPM: Perhitungan nilai Beta untuk mengukur risiko sistematis, Alfa untuk mengukur kelebihan imbal hasil, dan Expected Return.
5. Optimasi Portofolio: Penghitungan bobot optimal untuk setiap aset menggunakan pendekatan inversi matriks kovarians.
6. Evaluasi Kinerja: Penilaian efektivitas portofolio menggunakan metode Indeks Sharpe, Indeks Treynor, dan Indeks Jensen.

## Prasyarat dan Pustaka

Untuk menjalankan skrip ini, Anda memerlukan pustaka berikut:

* yfinance (untuk pengambilan data pasar)
* pandas (untuk manipulasi data)
* numpy (untuk perhitungan matematis dan matriks)
* openpyxl (untuk ekspor data ke format Excel)

## Cara Penggunaan

1. Kloning repositori ini ke direktori lokal Anda.
2. Pastikan semua pustaka pendukung telah terinstal melalui manajer paket pip.
3. Buka file notebook (.ipynb) menggunakan Jupyter Notebook atau Google Colab.
4. Sesuaikan variabel tanggal dan daftar saham pada bagian konfigurasi jika diperlukan.
5. Jalankan seluruh sel untuk mendapatkan hasil kalkulasi dan tabel evaluasi.

## Metodologi Pengambilan Keputusan

Penentuan aset yang layak masuk ke dalam portofolio didasarkan pada tiga kriteria:
* Indeks Sharpe: Menilai imbal hasil terhadap risiko total.
* Indeks Treynor: Menilai imbal hasil terhadap risiko sistematis (Beta).
* Indeks Jensen: Mengidentifikasi saham yang berada dalam kondisi undervalued (Alfa positif).
