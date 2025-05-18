# Requirements NutriTrack

## Kebutuhan Sistem
- R (versi 4.0.0 atau lebih tinggi)
- Minimal 4GB RAM
- Koneksi internet (untuk instalasi paket dan akses database jika diperlukan)

## Paket R yang Diperlukan
```R
# Paket Utama
install.packages("shiny")         # Framework aplikasi web
install.packages("shinydashboard") # Struktur dashboard
install.packages("ggplot2")       # Visualisasi data
install.packages("dplyr")         # Manipulasi data
install.packages("plotly")        # Grafik interaktif
install.packages("shinyWidgets")  # Widget tambahan untuk UI
install.packages("shinycssloaders") # Loading spinners

# Paket Pendukung (jika diperlukan)
install.packages("DT")            # Tabel interaktif
install.packages("readxl")        # Membaca file Excel
install.packages("writexl")       # Menulis file Excel
install.packages("lubridate")     # Manipulasi tanggal/waktu
install.packages("stringr")       # Manipulasi string
install.packages("readr")         # Membaca file CSV dengan cepat
install.packages("tidyr")         # Pivot dan transformasi data
install.packages("shinyjs")       # JavaScript dalam Shiny
install.packages("shinyBS")       # Komponen Bootstrap untuk Shiny
install.packages("leaflet")       # Peta interaktif
```

## Data yang Tersedia
1. **Data Standar WHO**:
   - Berisi data median tinggi badan dan standar deviasi untuk anak laki-laki dan perempuan
   - Usia dalam rentang 0-60 bulan
   - Variabel: age_months, sex, median_tb, sd_tb

2. **Data Stunting Indonesia**:
   - Data stunting untuk 38 provinsi di Indonesia tahun 2023
   - Variabel: provinsi, jml_balita, jml_stunting, pendek, sangat_pendek, prevalensi, tahun
   
## Dataset yang Perlu Ditambahkan
1. **food_database.csv** - Database makanan dan kandungan nutrisi:
   - food_id: ID unik makanan
   - food_name: Nama makanan
   - calories: Jumlah kalori (kcal)
   - protein: Kandungan protein (g)
   - fat: Kandungan lemak (g)
   - carbs: Kandungan karbohidrat (g)
   - fiber: Kandungan serat (g)
   - calcium: Kandungan kalsium (mg)
   - iron: Kandungan zat besi (mg)
   - vitamin_a: Kandungan vitamin A (mcg)
   - vitamin_c: Kandungan vitamin C (mg)
   - portion: Ukuran porsi standar (g)

## Fitur yang Perlu Diimplementasikan
1. **Visualisasi Data Stunting Indonesia**:
   - Peta sebaran prevalensi stunting per provinsi
   - Grafik perbandingan provinsi dengan prevalensi tertinggi dan terendah
   - Dashboard analisis data stunting

2. **Input Data Anak**:
   - Nama, tanggal lahir, jenis kelamin
   - Berat badan dan tinggi badan saat ini
   - Riwayat pengukuran

3. **Analisis Pertumbuhan**:
   - Perhitungan Z-score berdasarkan standar WHO
   - Penentuan status stunting (normal, pendek, sangat pendek)
   - Grafik tren pertumbuhan individu

4. **Analisis Nutrisi**:
   - Input makanan harian
   - Perhitungan asupan nutrisi
   - Perbandingan dengan kebutuhan harian

5. **Rekomendasi**:
   - Saran menu sesuai kebutuhan nutrisi
   - Intervensi untuk pencegahan stunting
   - Tips pengasuhan dan pemberian makan

6. **Manajemen Data**:
   - Penyimpanan data secara lokal
   - Ekspor data ke format Excel/CSV
   - Backup dan restore data

7. **UI/UX**:
   - Dashboard responsif
   - Tema yang menarik dan ramah pengguna
   - Navigasi intuitif

## Pengujian
1. Unit tests untuk validasi perhitungan nutrisi dan Z-score
2. Pengujian responsivitas aplikasi di berbagai perangkat
3. Validasi input untuk mencegah error
4. Pengujian kegunaan dengan pengguna target (orang tua/petugas kesehatan)

## Rencana Deployment
1. Shinyapps.io untuk versi online
2. Paket standar untuk instalasi lokal
3. Docker container untuk deployment di server sendiri
